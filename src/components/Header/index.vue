<template>
    <header class="header">
        <nav class="container header__nav">
            <a href="" class="header__logo">
                <img src="../../assets/logo2.jpg" alt="">
            </a>

            <img class="header_menu_button" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg
" alt="" @click="openMenu">

        <div class="header_menu_overlay" v-if="menuActive" @click="openMenu"></div>

        <div :class="['home_navegation', {active: menuActive}]">
            <img class="logo_navegatio" src="../../assets/logo2.jpg" alt="">
            <ul>
                <li><a href="/">Home</a></li>
                <li><a href="/">Videos</a></li>
                <li><a href="/">Sobre</a></li>
                <li><a href="/">Contatos</a></li>
            </ul>
        </div>
        </nav>

    </header>
</template>

<script>
export default {
    data(){
        return{
            menuActive: false
        }
    },
    methods:{
        openMenu(){
            this.menuActive = !this.menuActive
        }
    }
}
</script>

<style scoped>
    .header{
        background-color: var(--color-background-nav);
        width: 100%;
        height: 150px;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .header__logo img{
        width: 100px;
    }
    .header_menu_button{
        width: 30px;
    }
    .header__nav{
        display: flex;
        justify-content: space-between;
    }

    .header_menu_overlay{
        position: fixed;
        top: 0;
        left: 0;
        width: 40%;
        height: 100vh;
        background-color: #000;
        opacity: 0.8;
    }

    .home_navegation{
        position: fixed;
        top: 0;
        right: 0;
        background-color: var(--color-background-nav);
        width: 60%;
        height: 100vh;
        display: none;
        flex-direction: column;
        align-items: center;
    }

    .home_navegation.active{
        display: flex;
    }

    .logo_navegatio{
        width: 90px;
        margin: 30px 0 10px 0;
    }

    .home_navegation ul {
        text-align: center;
    }

    .home_navegation ul li{
        margin: 20px 0;
    }
    .home_navegation ul li a{
        color: var(--color-text-light);
    }
</style>