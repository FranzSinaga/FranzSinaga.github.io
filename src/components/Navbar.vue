<template>
    <!--<div class="containerss">-->
    <div>
        <div class="navbar-header">
            <div class="toggle-button" id="toggle">
                <span class="bar top"></span>
                <span class="bar middle"></span>
                <span class="bar bottom"></span>
            </div>
        </div>

        <!-- markup for the overlay -->
        <nav class="overlay" id="overlay">
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Blog</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Portfolio</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </div>
</template>

<script>
    export default {
        name: "Navbar.vue",
        mounted() {
            $("#toggle").click(function() {
                //on click, the hamburger menu elements get the toggle-active class and the overlay gets the nav-active class
                $(this).toggleClass("toggle-active");
                $("#overlay").toggleClass("nav-active");

                //the h1 element toggles between visibility and invisibility
                $(".canhide").toggleClass("hidden");
            });
        }
    }
</script>

<style>
    @import url('https://fonts.googleapis.com/css?family=VT323');
    /*.containerss {*/
        /*height: 100vh;*/
        /*margin-top: -59px;*/
        /*width: 100%;*/
        /*background: -moz-linear-gradient(top, #febbbb 0%, #fe9090 45%, #ff5c5c 100%);*/
        /*background: -webkit-linear-gradient(top, #febbbb 0%, #fe9090 45%, #ff5c5c 100%);*/
        /*background: linear-gradient(to bottom, #febbbb 0%, #fe9090 45%, #ff5c5c 100%);*/
    /*}*/
    .canhide {
        /*horizontal centering*/
    }
    .h1-special{
        -webkit-transform: translateX(-50%);
        transform: translateX(-50%);
    }
    /** styling for the hamburger menu **/
    .toggle-button {
        position: fixed;
        top: 10px;
        /*horizontal centering: https://css-tricks.com/forums/topic/horizontal-centering-of-an-absolute-element/ */
        left: 80%;
        -webkit-transform: translateX(-50%);
        transform: translateX(-50%);
        padding: 10px;
        margin: 8px 15px 8px 0;
        /*height: 20px;*/
        /*width: 35px;*/
        background-color: gray;
        border-radius: 2px;
        border-color: black;
        border-width: 10px;
        opacity: 0.5;
        cursor: pointer;
        z-index: 3;
    }
    .bar {
        background-color: white;
        display: block;
        width: 35px;
        height: 5px;
        border: 0;
        -webkit-transition: all .35s ease;
        transition: all .35s ease;
    }
    .bar + .bar {
        margin-top: 4px;
    }
    .middle {
        top: 15px;
    }
    .bottom {
        top: 30px;
    }
    .toggle-button:hover {
        opacity: 1;
    }
    .toggle-active .bar {
        background-color: #fff;
    }
    .toggle-active .top {
        -webkit-transform: translateY(6px) translateX(0) rotate(45deg);
    }
    .toggle-active .middle {
        opacity: 0;
    }
    .toggle-active .bottom {
        -webkit-transform: translateY(-12px) translateX(0) rotate(-45deg);
    }
    /** styling for the overlay. The sliding-down effect of the overlay is given by the initial zero height and the onclick 100% height. **/
    .overlay {
        position: fixed;
        /*background-image: linear-gradient(120deg, #a6c0fe 0%, #f68084 100%);*/
        background-color: black;
        top: 0;
        left: 0;
        width: 100%;
        height: 0;
        visibility: hidden;
        opacity: 0;
        -webkit-transition: opacity .35s, visibility .35s, height .35s;
    }
    /* class added to the overlay on click*/
    .nav-active {
        opacity: 1;
        visibility: visible;
        height: 100%;
    }
    .overlay ul {
        display: block;
        position: relative;
        top: 60px;
        left: 0;
        font-family: 'Didact Gothic', serif;
        font-size: 50px;
        font-weight: 400;
        text-align: center;
        list-style: none;
        padding: 0;
    }
    .overlay ul li {
        display: block;
    }
    .overlay ul li a {
        color: #fff;
        text-decoration: none;
    }
    .hidden {
        opacity: 0;
    }
</style>