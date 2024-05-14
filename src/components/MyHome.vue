<template>
    <div class=" max-w-4xl mx-auto py-8 px-4 bg-white rounded-lg shadow-lg">
        <br>
      <h1 class="text-3xl font-bold text-center mb-4">¡Bienvenido!</h1>
      <MyMenu :categories_menu="categories_menu" :products_menu="products_menu"></MyMenu>
    </div>
  </template>

<script>
    import MyMenu from './MyMenu.vue';

    export default {
        name: 'MyHome',
        components: {
            MyMenu,
        },
        data() {
            return {

                products_menu: [{
                        product_name: 'Sandwich de pollo',
                        product_price: 5.01,
                        product_description: 'Mezcla de pollo desmenuzado con aderezo de la casa con selección de vegetales',
                        product_image: 'Sandwich_de_pollo.jpg',
                        product_category_id: 1
                    },
                    {
                        product_name: 'Wafles con fruta',
                        product_price: 5.99,
                        product_description: 'Wafles acompañado de trozos de fresas y sirope de maple',
                        product_image: 'Wafles_con_fruta.jpg',
                        product_category_id: 2
                    },
                    {
                        product_name: 'Camarones al ají',
                        product_price: 12.75,
                        product_description: 'Porción de camarones acompañados de arroz/papas y verduras salteadas',
                        product_image: 'Camarones_al_ají.jpg',
                        product_category_id: 3
                    },
                    {
                        product_name: 'Ensalada César',
                        product_price: 3.99,
                        product_description: 'Todo lo que puedes pedirle a una ensalada, no se... no compro ensaladas',
                        product_image: 'Ensalada_César.jpg',
                        product_category_id: 4
                    },
                    {
                        product_name: 'Brownie con Helado',
                        product_price: 6.05,
                        product_description: 'Receta de la abuela, suave y cremosa creación de chocolate acompañada de una bola de helado de vainilla',
                        product_image: 'Brownie_con_Helado.jpg',
                        product_category_id: 5
                    },
                    {
                        product_name: 'Coca-Cola',
                        product_price: 2.99,
                        product_description: 'Todo mundo lo conoce, solo espero que me dejen robarle la img',
                        product_image: 'Coca_Cola.jpg',
                        product_category_id: 6
                    },
                    {
                        product_name: 'Huevos divorciados',
                        product_price: 5.6,
                        product_description: 'Huevos estrellados acompañados con salsas la casa acompañados con frijoles y aguacate ',
                        product_image: 'Huevos_divorciados.jpg',
                        product_category_id: 2
                    },
                    {
                        product_name: 'Papas fritas',
                        product_price: 2.5,
                        product_description: 'Papas fritas rebosadas con mostaza, pimienta, sal y cilantro acompañadas con salsa chipotle y ranch',
                        product_image: 'Papas_fritas.jpg',
                        product_category_id: 1
                    },
                    {
                        product_name: 'Pollo en salsa de hongos',
                        product_price: 6.5,
                        product_description: 'Porción de pechuga de pollo bañada en salsa de hongos acompañado de arroz/papas y verduras salteadas',
                        product_image: 'Pollo_en_salsa_de_hongos.jpg',
                        product_category_id: 3
                    },
                    {
                        product_name: 'Ensalada rusa',
                        product_price: 3.5,
                        product_description: 'Todo lo que puedes pedirle a una ensalada pero en cocido, no se... no compro ensaladas',
                        product_image: 'Ensalada_rusa.jpg',
                        product_category_id: 4
                    },
                    {
                        product_name: 'Pie de Higo',
                        product_price: 30.48,
                        product_description: 'Parece pero no es un pie, es una tarta rellena de trozos de higos combinados con ligero sabor a crema',
                        product_image: 'Pie_de_Higo.jpeg',
                        product_category_id: 5
                    },
                    {
                        product_name: 'Limonada',
                        product_price: 3.75,
                        product_description: 'Refrescante limonada con fresas licuadas y esferas sabor arandanos',
                        product_image: 'Limonada.jpg',
                        product_category_id: 6
                    }
                ],
                categories_menu: [{
                        category_id: 0,
                        category_name: 'Menú Completo'
                    },
                    {
                        category_id: 1,
                        category_name: 'Entrada'
                    },
                    {
                        category_id: 2,
                        category_name: 'Desayuno'
                    },
                    {
                        category_id: 3,
                        category_name: 'Plato Fuerte'
                    },
                    {
                        category_id: 4,
                        category_name: 'Ensalada'
                    },
                    {
                        category_id: 5,
                        category_name: 'Postre'
                    },
                    {
                        category_id: 6,
                        category_name: 'Bebida'
                    }
                ]
            }
        }
    }
</script>
