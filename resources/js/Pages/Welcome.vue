<template>
    <Head title="Welcome" />

    <div class="relative flex items-top justify-center min-h-screen bg-gray-100 dark:bg-gray-900 sm:items-center sm:pt-0">
        <div v-if="canLogin" class="hidden fixed top-0 right-0 px-6 py-4 sm:block">
            <Link v-if="$page.props.user" :href="route('dashboard')" class="text-sm text-gray-700 underline">
                Dashboard
            </Link>

            <template v-else>
                <Link :href="route('login')" class="text-sm text-gray-700 underline">
                    Log in
                </Link>

                <Link v-if="canRegister" :href="route('register')" class="ml-4 text-sm text-gray-700 underline">
                    Register
                </Link>
            </template>
        </div>

        <div class="max-w-6xl mx-auto sm:px-6 lg:px-8">
            <div class="flex justify-center pt-8 sm:justify-start sm:pt-0">
                <img src="..\..\..\public\logo.png" class="m-3" />  
            </div>

<!-- component -->
<!-- This is an example component -->
            <div class="container mx-auto my-5">

                <div class="relative rounded-lg flex flex-col md:flex-row items-center md:shadow-xl md:h-72 mx-2">
                    
                    <div class="z-0 order-1 md:order-2 relative w-full md:w-2/5 h-80 md:h-full overflow-hidden rounded-lg md:rounded-none md:rounded-r-lg">
                        <div class="absolute inset-0 w-full h-full object-fill object-center bg-red-400 bg-opacity-30 bg-cover bg-bottom" style="background-image: url( images/hands.jpg ); background-blend-mode: multiply;"></div>
                        <div class="md:hidden absolute inset-0 h-full p-6 pb-6 flex flex-col-reverse justify-start items-start bg-gradient-to-b from-transparent via-transparent to-gray-900">
                            <h3 class="w-full font-bold text-2xl text-red-600 leading-tight mb-2">HOTEL AMANEE</h3>
                            <h4 class="w-full text-xl text-gray-100 leading-tight">Bienvenido a</h4>
                        </div>
                        <svg class="hidden md:block absolute inset-y-0 h-full w-24 fill-current text-white -ml-12" viewBox="0 0 100 100" preserveAspectRatio="none">
                            <polygon points="50,0 100,0 50,100 0,100" />
                        </svg>
                    </div>

                    <div class="z-10 order-2 md:order-1 w-full h-full md:w-3/5 flex items-center -mt-6 md:mt-0">
                        <div class="p-8 md:pr-18 md:pl-14 md:py-12 mx-2 md:mx-0 h-full bg-white rounded-lg md:rounded-none md:rounded-l-lg shadow-xl md:shadow-none">
                            <h4 class="hidden md:block text-xl text-gray-400">Prezentujemy</h4>
                            <h3 class="hidden md:block font-bold text-2xl text-gray-700">Przestrzeń dla społeczności</h3>
                            <p class="text-gray-600 text-justify">Wszystko co potrzebne do funkcjonowania każdej społeczności. Social media, finanse, kontakt. Wszystko w jednym miejscu.</p>
                            <a class="flex items-baseline mt-3 text-red-600 hover:text-red-900 focus:text-red-900" href="">
                                <span>Sprawdź szczegóły</span>
                                <span class="text-xs ml-1">&#x279c;</span>
                            </a>
                        </div>
                    </div>

                </div>
            </div>

        </div>
    </div>
</template>

<style scoped>
    .bg-gray-100 {
        background-color: #f7fafc;
        background-color: rgba(247, 250, 252, var(--tw-bg-opacity));
    }

    .border-gray-200 {
        border-color: #edf2f7;
        border-color: rgba(237, 242, 247, var(--tw-border-opacity));
    }

    .text-gray-400 {
        color: #cbd5e0;
        color: rgba(203, 213, 224, var(--tw-text-opacity));
    }

    .text-gray-500 {
        color: #a0aec0;
        color: rgba(160, 174, 192, var(--tw-text-opacity));
    }

    .text-gray-600 {
        color: #718096;
        color: rgba(113, 128, 150, var(--tw-text-opacity));
    }

    .text-gray-700 {
        color: #4a5568;
        color: rgba(74, 85, 104, var(--tw-text-opacity));
    }

    .text-gray-900 {
        color: #1a202c;
        color: rgba(26, 32, 44, var(--tw-text-opacity));
    }

    @media (prefers-color-scheme: dark) {
        .dark\:bg-gray-800 {
            background-color: #2d3748;
            background-color: rgba(45, 55, 72, var(--tw-bg-opacity));
        }

        .dark\:bg-gray-900 {
            background-color: #1a202c;
            background-color: rgba(26, 32, 44, var(--tw-bg-opacity));
        }

        .dark\:border-gray-700 {
            border-color: #4a5568;
            border-color: rgba(74, 85, 104, var(--tw-border-opacity));
        }

        .dark\:text-white {
            color: #fff;
            color: rgba(255, 255, 255, var(--tw-text-opacity));
        }

        .dark\:text-gray-400 {
            color: #cbd5e0;
            color: rgba(203, 213, 224, var(--tw-text-opacity));
        }
    }
</style>

<script>
    import { Head, Link } from '@inertiajs/inertia-vue3';

    export default {
        components: {
            Head,
            Link,
        },

        props: {
            canLogin: Boolean,
            canRegister: Boolean,
            laravelVersion: String,
            phpVersion: String,
        }
    }
</script>
