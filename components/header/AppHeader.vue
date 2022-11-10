<template>
    <header :class="!topOfPage ? ' scrolled ' : ''">
        <b-navbar toggleable="lg">
            <b-navbar-brand href="#">
                <img src="/assets/logo2.png" alt="logoImage" style="width: 200px">
            </b-navbar-brand>

            <b-navbar-toggle target="navbar-toggle-collapse">
                <template #default="{ expanded }">
                    <span class="menu-trigger" :class="expanded ? 'active' : ''" id="menu03">
                        <span></span>
                        <span></span>
                        <span></span>
                    </span>
                </template>
            </b-navbar-toggle>

            <b-collapse id="navbar-toggle-collapse" class="ml-auto justify-content-end" is-nav>
                <b-navbar-nav class="align-items-center">
                    <b-nav-item  class="active" href="/">Home</b-nav-item>
                    <b-nav-item href="#">Pages</b-nav-item>
                    <b-nav-item href="#">Services</b-nav-item>
                    <b-nav-item href="#">Articles</b-nav-item>
                    <b-nav-item href="#">Shop</b-nav-item>
                    <b-nav-item href="#">Contact</b-nav-item>
                    <a href="#" class="phone">
                        <font-awesome-icon icon="fa-solid fa-phone" />
                        1-001-234-5678
                    </a>
                    <langSwitch></langSwitch>
                    <a href="#" @click="side = !side" class="btn">
                        <font-awesome-icon icon="fa-solid fa-bag-shopping" />
                        <span class="d-lg-none d-block">Side Bar</span>
                    </a>
                </b-navbar-nav>
            </b-collapse>
        </b-navbar>
        <div :class="side ? 'opend' : '' " @click.self="side = !side" class="side-bar">
            <div class="content-wrapper">
                <div class="close-btn">
                    <font-awesome-icon icon="fa-solid fa-xmark" @click="side= !side"/>
                </div>
                <div class="widge">
                    <p>	
                        No products in the cart.
                    </p>
                </div>

            </div>
        </div>
    </header>
</template>

<script>
import langSwitch from '../langSwitch/langSwitch.vue'
// import DropdownMenu from '@innologica/vue-dropdown-menu'
export default {
    name: 'AppHeader',
    components: {
        langSwitch
        // DropdownMenu
    },
    data() {
        return {
            side: false,
            topOfPage : true
        }
    },
    beforeMount() {
        window.addEventListener('scroll', this.handleScroll)
    },
    mounted() {
    },
    methods: {
        handleScroll(){
            if(window.pageYOffset>50){
                if(this.topOfPage) this.topOfPage = false
            } else {
                if(!this.topOfPage) this.topOfPage = true
            }
        }
    }
}
</script>
<style >
    .scrolled {
        
        height: 70px;
        min-height: 70px;
        box-shadow: rgba(0, 0, 0, 0.2) 0px 0px 5px 0px
    }
    .scrolled nav{
        height: 70px;
    }
    .scrolled .navbar-brand img{
        width: 80px;
    }
    header {
        position: fixed;
        left: 0;
        right: 0;
        padding-right: 60px;
        padding-left: 60px;
        min-height: 120px;
        background-color: #fff;
        z-index: 9999;
        transition: all 0.3s linear;
    }
    header nav {
        height: 120px;
        padding: 0 !important;
        transition: all 0.3s linear;

    }
    .navbar-brand {
        padding-top: 0px !important;
        padding-right: 0px !important;
        margin-right: 25px;
        padding-bottom: 0px !important;
        padding-left: 0px !important;
    }
    .navbar-brand img {
        max-width: 162px;
        width: 100px;
        height: auto;
        transition: all 0.3s linear;

    }
    .nav-item {
        position: relative;
        margin: 0 15px;
        justify-content: center;
        transition: all calc(300 * 1ms) cubic-bezier(.42, .01, .58, 1);
    }
    .nav-link {
        color: rgb(17, 24, 28);
        display: block;
        font-size: 15px;
        hyphens: manual;
        letter-spacing: normal;
        line-height: 27px;
        padding: 0;
    }
    .nav-item.active::after, .nav-item:hover::after {
        background-color: #f0c000;
        left: 6px;
        right: 6px;
    }
    .nav-item::after {
        content: " ";
        position: absolute;
        bottom: 0;
        left: 10px;
        right: 10px;
        height: 2px;
        transition: all .3s cubic-bezier(.42,.01,.58,1);
        z-index: 999999998;
        background-color: transparent;
    }
    header .phone {
        color: rgb(17, 24, 28);
        font-size: 19px;
        text-decoration: none;
    }
    header .phone svg {
        color: #f0c000;
        max-width: 20px;
    }
    .navbar-toggler,
    .navbar-toggler:focus {
        border: none;
        box-shadow: none;
    }
    .menu-trigger,
    .menu-trigger span {
    display: inline-block;
    transition: all .4s;
    box-sizing: border-box;
    }
    .menu-trigger {
    position: relative;
    width: 32px;
    height: 25px;
    background: none;
    border: none;
    appearance: none;
    cursor: pointer;
    }
    .menu-trigger span {
    position: absolute;
    left: 0;
    width: 100%;
    height: 5px;
    background-color:rgb(98, 57, 189);
    border-radius: 4px;
    }
    .menu-trigger span:nth-of-type(1) {
    top: 0;
    }
    .menu-trigger span:nth-of-type(2) {
    top: 10px;
    }
    .menu-trigger span:nth-of-type(3) {
    bottom: 0;
    }
    #menu03.active {
    transform: rotate(360deg);
    }
    #menu03.active span:nth-of-type(1) {
    transform: translateY(10px) rotate(-45deg);
    }
    #menu03.active span:nth-of-type(2) {
    transform: translateY(0) rotate(45deg);
    }
    #menu03.active span:nth-of-type(3) {
    opacity: 0;
    }

    nav .btn {
        border-radius: 100%;
        box-shadow: rgba(0, 0, 0, 0.2) 0px 0px 5px 0px;
        color: #000;
        font-size: 20px;
        font-weight: 500;
        line-height: 12px;
        margin-left: 30px;
        text-align: center;
        transition-delay: 0s;
        transition-duration: 0.3s;
        transition-property: all;
        height: 40px;
        width: 40px;
        padding: 8px;
        border: none
    }
    nav .btn:hover {
        color: rgb(129, 138, 145)
    }
    .side-bar {
        width: 0;
        position: fixed;
        overflow: hidden;
        top: 0;
        bottom: 0;
        right: 0;
        background-color: rgba(243, 245, 246, 0.95);
        z-index: 9999;
        transition: all .4s ease;
    }
    .side-bar.opend {
        width: 100%;
        background: rgba(0, 0, 0, 0.25);
    }
    .side-bar .content-wrapper {
        padding: 60px 30px;
        position: relative;
        overflow-x: hidden;
        overflow-y: auto;
        height: 100%;
        scrollbar-width: none;
        width: 300px;
        float: right;
        box-shadow: 0 0 5px 0 rgba(0,0,0,.15);
        background: #fff;
    }
    .side-bar .content-wrapper .close-btn {
        position: absolute;
        top: 20px;
        left: auto;
        right: 20px;
        color: rgb(97, 106, 125);
        font-size: 20px;
        cursor: pointer;
    }
    .side-bar .content-wrapper .widget {
        margin-bottom: 50px;
        
    }
    .side-bar .content-wrapper h4 {
        font-family: Roboto;
        font-size: 18px;
        font-weight: 400;
        letter-spacing: 1px;
        line-height: 18px;
        margin-bottom: 28px;
        color: rgb(9, 41, 51)
    }
    .side-bar .content-wrapper p {
        color: rgb(97, 106, 125);
        font-family: Roboto;
        font-size: 15px;
        font-weight: 400;
        line-height: 30px;
        margin: 15px 0;
    }
    .side-bar .content-wrapper ul {
        list-style: none;
        padding: 0;     
    }
    .side-bar .content-wrapper ul li {
        color: rgb(97, 106, 125);
        align-items: start;
        display: flex;
    }
    .side-bar .content-wrapper ul li > div {
        display: inline-block;
    }
    .side-bar .content-wrapper ul li > div p {
        margin: -4px 0 0 12px;
    }
    @media screen and (max-width: 991px) {
        .navbar-collapse.show{
            position: absolute;
            left: -60px;
            right: -60px;
            z-index: 9999;
            top: 120%;
        }
        .nav-item {
            width: 100%;
            border-bottom: 1px solid #e5e5e5;
            background: #fff;
        }
        
        .nav-item.active ,
        .nav-item:hover {
            background-color:rgb(98, 57, 189);
        }
        .nav-item.active .nav-link ,
        .nav-item:hover .nav-link {
            color: #fff;
        }
        
        .nav-link {
            padding: 16px 30px !important;
            font-weight: 400;
            font-size: 23px;
            text-align: left;
            color: rgb(97, 106, 125);
        }
        .side-bar.opend {
            width: 100%;
        }
    }
    
</style>