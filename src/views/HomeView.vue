<script setup>

</script>

<template>
    <div class="container">
        <div class="block">
            <div class="main__hero">
                <div class="main__hero-text">
                    <h1>Online Service <br> For Home Delivery</h1>
                    <p>Your favourite dishes to be delivered with love. All couriers have gloves and antiseptic with
                        them to keep you safe!</p>
                </div>

            </div>
        </div>

        <!-- Restaurants -->
        <div class="block">
            <div class="main__restaurants">
                <div class="main__restaurants-header">
                    <h2>Restaurants</h2>
                    <input type="text" class="main__restaurants-header--search" placeholder="Search restaurants">
                </div>

                <div class="main__restaurants-grid" id="rest-container">
                    <router-link class="restaurant" v-for="rest in store.rests" :key="rest.id"
                        :to="`/restaurant?id=${rest.id}`">
                        <div class="restaurant__image">
                            <img :src="getUrl(rest.image)" alt="cafe image">
                        </div>
                        <div class="restaurant__description">
                            <div class="restaurant__description-heading">
                                <h3>{{ rest.title }}</h3>
                                <span class="delivery-time">{{ rest.time }} min</span>
                            </div>
                            <div class="restaurant__description-extrainfo">
                                <div class="rating">
                                    <img src="../assets/img/icons/star.svg" alt="" class="star">
                                    <span>{{ rest.rating }}</span>
                                </div>
                                <ul class="category">
                                    <li class="price">vanaf ${{ rest.price }}</li>
                                    <li class="cuisine">{{ rest.cuisine }}</li>
                                </ul>
                            </div>

                        </div>
                    </router-link>

                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { store } from '../store/index'
// import {restArray} from '../constants/restaurants'
    const getUrl = (name) => {
        return new URL(`../assets/img/restaurants/${name}`, import.meta.url)
    }

    
</script>