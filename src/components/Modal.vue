<template>
  <div class="cart-modal__overlay" :class="{open: isOpen}" @click.self="closeModal()">
        <div class="cart-modal">
            <div class="cart-modal__header">
                <h2 class="cart-modal__header--title">Your Cart</h2>
                <span class="cart-modal__header--close" @click="closeModal()">
                    <img src="../assets/img/icons/close.svg" alt="">
                </span>
            </div>

            <div class="cart-modal__body">
                <div class="cart-item">
                    <p class="cart-item__title">
                        Unagi Maki Roll 4st.
                    </p>
                    <div class="cart-item__controls">
                        <div class="cart-item__controls--price">$4,50</div>

                        <button class="btn-outline">-</button>
                        <div class="cart-item__controls--counter">1</div>
                        <button class="btn-outline">+</button>
                    </div>
                </div>
                <div class="cart-item">
                    <p class="cart-item__title">
                        Unagi Maki Roll 4st.
                    </p>
                    <div class="cart-item__controls">
                        <div class="cart-item__controls--price">$4,50</div>

                        <button class="btn-outline">-</button>
                        <div class="cart-item__controls--counter">1</div>
                        <button class="btn-outline">+</button>
                    </div>
                </div>
                <div class="cart-item">
                    <p class="cart-item__title">
                        Unagi Maki Roll 4st.
                    </p>
                    <div class="cart-item__controls">
                        <div class="cart-item__controls--price">$4,50</div>

                        <button class="btn-outline">-</button>
                        <div class="cart-item__controls--counter">1</div>
                        <button class="btn-outline">+</button>
                    </div>
                </div>
                <div class="cart-item">
                    <p class="cart-item__title">
                        Unagi Maki Roll 4st.
                    </p>
                    <div class="cart-item__controls">
                        <div class="cart-item__controls--price">$4,50</div>

                        <button class="btn-outline">-</button>
                        <div class="cart-item__controls--counter">1</div>
                        <button class="btn-outline">+</button>
                    </div>
                </div>
                <div class="cart-item">
                    <p class="cart-item__title">
                        Unagi Maki Roll 4st.
                    </p>
                    <div class="cart-item__controls">
                        <div class="cart-item__controls--price">$4,50</div>

                        <button class="btn-outline">-</button>
                        <div class="cart-item__controls--counter">1</div>
                        <button class="btn-outline">+</button>
                    </div>
                </div>
            </div>

            <div class="cart-modal__footer">
                <div class="cart-modal__footer--price">
                    $27,50
                </div>
                <div class="cart-modal__footer--controls">
                    <button class="btn-primary">
                        Checkout        
                    </button>
                    <button class="btn-outline">
                        Cancel
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
    const {isOpen} = defineProps({isOpen: Boolean})
    const emit = defineEmits(['toggleModal'])
    const closeModal = () => emit('toggleModal')
</script>

<style scoped>
    /* Pop Up */
    .cart-modal__overlay {
        display: none;
        position: fixed;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        background: rgba(0, 0, 0, 0.4);

        align-items: center;
        justify-content: center;
    }

    .cart-modal__overlay.open {
        display: flex;
    }

    .cart-modal {
        width: 100%;
        max-width: 780px;
        padding: 40px 45px;
        border-radius: 5px;
        background: #FFFFFF;
    }

    .cart-modal__header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 48px;
    }

    .cart-modal__header--title {
        font-size: 36px;
        font-weight: 700;
        color: #000;
        margin: 0;
    }

    .cart-modal__header--close {
        cursor: pointer;
    }

    .cart-modal__footer {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-top: 50px;
    }

    .cart-modal__footer--price {
        border-radius: 5px;
        padding: 15px 20px;
        background-color: #262626;
        font-weight: 700;
        font-size: 20px;
        color: #FAFAFA;
        text-align: center;
    }

    .cart-modal__footer--controls {
        display: flex;
        align-items: center;
        gap: 10px;
    }

    .cart-item {
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: nowrap;
        gap: 10px;
    }

    .cart-item:not(:last-child) {
        padding-bottom: 10px;
        margin-bottom: 10px;
        border-bottom: 1px solid #D9D9D9;
    }

    .cart-item__title {
        font-weight: 400;
        font-size: 18px;
        color: #262626;
        margin: 0;
    }

    .cart-item__controls {
        display: flex;
        align-items: center;
    }

    .cart-item__controls--price {
        font-weight: 700;
        font-size: 20px;
        line-height: 160%;
        color: #262626;
        margin-right: 47px;
    }

    .cart-item__controls button {
        border: 1px solid #40A9FF;
        color: #40A9FF;
        border-radius: 2px;
        padding: 5px 16px;
    }

    .cart-item__controls--counter {
        margin: 0 12px;
    }
</style>