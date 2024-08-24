<template>
    <div class="container">
        <!-- Restaurant Details -->
        <div class="block">
            <div class="main__restaurants">
                <div class="main__restaurants-header restaurant__page-header">
                    <h2>Sushi Huis Enschede</h2>
                    <div class="main__restaurant-header--details">
                        <div class="rating rating__restaurant-page">
                            <img src="../assets/img/icons/star.svg" alt="" class="star">
                            <span>4.5</span>
                        </div>
                        <div class="category">
                            <span class="price">vanaf $25,00</span>
                            <span class="cuisine">Japaans</span>
                        </div>
                    </div>
                </div>
                <!-- Products -->
                <div class="main__restaurants-grid" id="products-container">
                    <div class="restaurant product" v-for="product in decafeenschedeArray" :key="product.id">
                        <div class="restaurant__image product_image">
                            <!-- <img src="../assets/img/products/sushi_1.png" alt="Product"> -->
                            <img :src=getUrl(product.image) alt="Dish">
                        </div>
                        <div class="restaurant__description product__description">
                            <div class="restaurant__description-heading">
                                <h3 class="product__name">{{ product.name }}</h3>

                            </div>
                            <div class="restaurant__description-extrainfo">
                                <div class="product__description">
                                    <p>{{ product.ingredients }}</p>
                                </div>
                            </div>
                            <div class="product__buttons">
                                <button class="btn-primary">
                                    Add to cart
                                    <img src="../assets/img/icons/shopping-cart.svg" alt="add-to-cart">
                                </button>
                                <span class="product__buttons-price">${{ product.price }}</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { decafeenschedeArray } from "../constants/decafeMenu"
const getUrl = (name) => {
    return new URL(`../assets/img/products/${name}`, import.meta.url)
}
</script>
