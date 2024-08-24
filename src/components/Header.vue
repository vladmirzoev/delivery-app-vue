<template>
    <header>
        <div class="container">
            <div class="header__box">
                <router-link to="/" class="header__logo">
                    <img src="../assets/img/logo.svg" alt="Delivery App">
                </router-link>
                <div class="header__buttons">
                    <button class="btn-primary">
                        <img src="../assets/img/icons/login.svg" alt="sign in">
                        Sign in
                    </button>
                    <button class="btn-outline" @click="openModal()">
                        <img src="../assets/img/icons/cart.svg" alt="sign in">
                        Cart
                    </button>
                </div>
            </div>
            
        </div>
    </header>
</template>

<script setup>
    const emit = defineEmits(['toggleModal'])
    const openModal = () => emit('toggleModal')

</script>

<style scoped>
        .header__box {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 36px 0;
        }
    
        
    
        .header__buttons {
            display: flex;
            gap: 8px;
        }
</style>