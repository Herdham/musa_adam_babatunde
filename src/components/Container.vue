<script setup>
    import "../assets/container.css"
    import { ref } from "vue";
    const fullName = ref("Musa Adam Babatunde");
    const socialMedia = ref(["logo-facebook", "logo-linkedin", "logo-twitter", "logo-instagram", "logo-github"])
</script>

<template>
    <main>
        <div class="heading">
            <h1><span>Hi I'm</span> <br>{{ fullName }}</h1>
            <hr>
            <p>A passionate and ambitious web developer <br>
                with a deep love for creating tools that<br>
                help people learn faster nad thing smarter.<br>
                I specialize in buiding clean, responsive,<br>
                and functional web applications using HTML,<br>
                CSS, Javascript, Python, and Vue.js.
            </p>
        </div>
        <div class="heading2">
            <h2>Experience: </h2>
            <p>Over the years, I've grown from building basic<br>
                websites to creating full learnig platforms<br>
                powered by Django and modern frontend frameworks.<br>
                I'm currently focusing on:
            </p>
            <ul>
                <li>Building a scalable learning platform from <br>
                Scratch.
                </li>
                <li>Mastering Vue.js and intergrating it with<br>
                    Django APIs.
                </li>
                <li>Exploring performace-focused languages like<br>
                    Rust for future backend services.
                </li>
            </ul>
            <a href="#"><span>Get Intouch</span><ion-icon name="arrow-forward-outline"></ion-icon></a>
            <ul class="media">
                <li v-for="(logo, index) in socialMedia" :key="index">
                    <a href="#"><ion-icon :name="logo"></ion-icon></a>
                </li>
            </ul>
        </div>
    </main>
</template>

<style scoped>

</style>