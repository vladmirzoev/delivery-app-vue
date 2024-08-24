<template>
  <footer class="footer">
        <div class="container">
            <div class="footer__box">
                <div class="footer__box-links">
                    <router-link to="/" class="footer__logo">
                        <img src="../assets/img/logo.svg" alt="Delivery App">
                    </router-link>
                    <div class="footer__nav">
                        <ul>
                            <li>
                                <a href="#">
                                    Restaurants
                                </a>
                            </li>
                            <li>
                                <a href="#">
                                    Legal
                                </a>
                            </li>
                            <li>
                                <a href="#">
                                    Contact
                                </a>
                            </li>
                            <li>
                                <a href="#">
                                    Become a courier
                                </a>
                            </li>                    
                        </ul>
                    </div>
                </div>
                


                <div class="footer__socials">
                    <a href="https://www.instagram.com">
                        <img src="../assets/img/socials/insta.svg" alt="instagram">
                    </a>
                    <a href="https://www.facebook.com">
                        <img src="../assets/img/socials/facebook.svg" alt="facebook">
                    </a>
                </div>
            </div>
            
        </div>
    </footer>
</template>

<script>
export default {

}
</script>

<style scoped>
    .footer__box {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 36px 0;
    }

    footer {
        background-color: darkgray;
    }

    .footer__box-links {
        display: flex;
        align-items: center;
        gap: 36px;
    }

    .footer__socials {
        display: flex;
        gap: 20px;
    }


</style>