<template>
    <v-app id="inspire" :theme="cartStore.getTheme">
        <!-- header -->
         <Header/>

        <v-main>
            <v-container>
                <RouterView/>
            </v-container>
        </v-main>
    </v-app>
</template>

<script setup>
import { useCartStore } from '~/stores/cart'
const cartStore = useCartStore()

</script>