<script setup>
    import { defineProps, ref } from "vue"
    import "../assets/main.css"
    const title = defineProps(['nickName'])
    const options = ref(["Home", "Project", "About", "Contact"])
    const socialMedia = ref(["logo-facebook", "logo-linkedin", "logo-twitter", "logo-instagram", "logo-github"])

    function optionHover(event){
        event.target.style.color = "#ff7f50"
    }
    function optionLive(event){
        event.target.style.color = "#cccccc"
    }

    function menudrop(){
        const drop = document.querySelector(".dropdown")
        if(drop.classList.contains("show")){
            drop.classList.remove("show")
        }else{
            drop.classList.add("show")
        }
    }
</script>

<template>
    <nav class="navbar">
        <div class="first">
            <div class="brand">
                <ion-icon name="at-circle-outline"></ion-icon>
                <h3>{{ title.nickName }}</h3>
            </div>
            <ul>
                <li v-for="(option, index) in options" :key="index">
                    <a href="#" v-on:mouseover="optionHover($event)"
                    v-on:mouseout="optionLive($event)">{{ option }}</a>
                </li>
            </ul>
        </div>
        <div class="second">
                <a href="#">
                    <ion-icon  v-for="(media, index) in socialMedia" :name="media"></ion-icon>
                </a>
                <ion-icon @click="menudrop" id="menu" name="filter-outline"></ion-icon>
        </div>
    </nav><br>

    <div class="dropdown">
            <ul>
                <li v-for="(option, index) in options" :key="index">
                    <a href="#" v-on:mouseover="optionHover($event)"
                    v-on:mouseout="optionLive($event)">{{ option }}</a>
                </li>
            </ul>
            <a href="#">
                <ion-icon  v-for="(media, index) in socialMedia" :name="media"></ion-icon>
            </a>
    </div>
</template>