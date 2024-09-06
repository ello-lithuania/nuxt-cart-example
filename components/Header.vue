<template>
    <v-app-bar>
        <v-toolbar-title @click="event=> $router.push('/')">
            Shopping website
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn @click="$router.push('/cart')" class="text-none" stacked>
            <v-badge :content="cartStore.productsTotal" color="error">
                <v-icon> mdi-cart-outline </v-icon>
            </v-badge>
        </v-btn>
        <v-btn :prepend-icon="theme === 'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'" @click="cartStore.toggleTheme()">
            Toggle theme
        </v-btn>
    </v-app-bar>
</template>

<script setup>
import { useCartStore } from '~/stores/cart'
const cartStore = useCartStore()

</script>