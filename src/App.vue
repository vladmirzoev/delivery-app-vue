<script setup>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Modal from './components/Modal.vue';
import { store } from './store/index';
</script>

<template>
  <Header @toggleModal="isOpen = store.toggleModal(true)" />

  <main class="main">
    <RouterView></RouterView>
  </main>

  <Modal :isOpen="store.isOpen" @toggleModal="isOpen = store.toggleModal(false)" />
  <Footer />
</template>

<style scoped></style>
