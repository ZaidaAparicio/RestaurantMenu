<template>
    <div class="max-w-4xl mx-auto py-8 px-4 bg-white rounded-lg shadow-xl">
        <Menubar :model="menuItems" @select="handleCategorySelect" class="flex justify-center mb-4" />
        <h2 v-if="selectedCategory" class="text-2xl font-bold text-center mb-4 text-gray-600">
            <br>{{ selectedCategory.category_name }}<br><br>
        </h2>
        <ul class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <li v-for="product in filteredProducts" :key="product.product_name"
                class="py-6 flex flex-col items-center rounded-lg shadow-md hover:bg-gray-50 transition duration-300 ease-in-out transform hover:scale-105">
                <img :src="require(`@/assets/img/${product.product_image}`)" :alt="product.product_name"
                    class="w-48 h-48 mb-4 rounded-full shadow-md">
                <div class="text-center">
                    <p class="text-lg font-semibold text-gray-800 mb-2">{{ product.product_name }}</p>
                    <p class="text-sm text-gray-600">{{ product.product_description }}</p>
                    <p class="text-lg font-semibold text-gray-800 mt-2">${{ product.product_price }}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    import Menubar from 'primevue/menubar';

    export default {
        name: 'MyMenu',
        components: {
            Menubar,
        },
        props: {
            categories_menu: {
                type: Array,
                required: true,
                validator: value => Array.isArray(value) && value.length > 0,
            },
            products_menu: {
                type: Array,
                required: true,
                validator: value => Array.isArray(value),
            },
        },
        data() {
            return {
                selectedCategory: null,
                menuItems: [],
            };
        },
        methods: {
            handleCategorySelect(category) {
                this.selectedCategory = category;
            },
        },
        computed: {
            filteredProducts() {
                if (!this.selectedCategory || this.selectedCategory.category_id === 0) {
                    return this
                        .products_menu;
                } else {
                    return this.products_menu.filter(product => product.product_category_id === this.selectedCategory
                        .category_id);
                }
            },
        },
        watch: {
            categories_menu: {
                handler(newVal) {
                    this.menuItems = newVal.map(category => ({
                        label: category.category_name,
                        command: () => this.handleCategorySelect(category),
                        class: 'text-gray-500 hover:text-gray-800 hover:bg-gray-100 transition duration-300 ease-in-out flex items-center justify-center px-4 py-2 font-bold rounded-md shadow-md',
                    }));
                },
                immediate: true,
            },
        },
    };
</script>
