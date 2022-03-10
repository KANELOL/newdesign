<template>
    <div>
        <div class="header">
            <p class="logo dark-grey">
                NORSKE <br />
                GÅRDER
            </p>
            <div class="header-menu">
                <a href="">Søke</a>
                <a href="">Oppleve</a>
                <a href="">Handle</a>
                <a href="">For Gårder</a>
            </div>
        </div>

        <div class="welcome">
            <h1>
                Den korteste veien til <br />
                lokale gårdsprodukter <br />
                og opplevelser
            </h1>
            <div class="recommendation">
                <div>
                    <p>Se hva norske gårder har å tilby!</p>
                    <div class="buttons-container">
                        <div class="buttons">
                            <a href="">Finn gård</a>
                            <a href="">Produkter</a>
                            <a href="">Tjenester</a>
                        </div>
                        <div class="buttons">
                            <a href="">Aktiviteter</a>
                            <a href="">Overnatting</a>
                            <a href="">Andelsgårder</a>
                        </div>
                    </div>
                </div>
                <div><input type="text" class="search-bar" placeholder="Søk"></div>
            </div>
        </div>
        <div class="carousel-container">
            <div class="title-container">
                <p>Kjøp rett fra gården</p>
                <div class="arrow"></div>
            </div>
            <div class="carousel">
                <div class="placeholder-picture"></div>
                <div class="placeholder-picture"></div>
                <div class="placeholder-picture"></div>
            </div>
        </div>
        <div class="carousel-container">
            <div class="title-container">
                <p>Gode gårdsopplevelser</p>
                <div class="arrow"></div>
            </div>
            <div class="carousel">
                <div class="placeholder-picture"></div>
                <div class="placeholder-picture"></div>
                <div class="placeholder-picture"></div>
            </div>
        </div>
        <div class="call-to-action">
            <h1>Driver du gård? <br> Vi ønsker deg velkommen til <br> hele norges samlingssted <br> for gårdsbruk, helt gratis.</h1>
            <div class="call-button-container">
                <a class="button" href="">Bli med!</a>
            </div>
        </div>
        <div class="map-container">
            <h1>Finn gården du leter etter</h1>
            <div class="map">
                <div class="button-container">
                <a class="button" href="">Se alle gårder</a>
                <a class="button" href="">Legg til din gård</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { Head, Link } from "@inertiajs/inertia-vue3";

defineProps({
    canLogin: Boolean,
    canRegister: Boolean,
    laravelVersion: String,
    phpVersion: String,
});
</script>
<style scoped>
.header {
    margin: 3rem;
    margin-left: 7rem;
    margin-right: 10rem;
    display: flex;
    justify-content: space-between;
}
.logo {
    font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
        "Lucida Sans", Arial, sans-serif;
    font-size: 2.5rem;
    line-height: 2.5rem;
    font-weight: bold;
}
.header-menu {
    display: inline-flex;
    flex-wrap: wrap;
    font-size: 2.2rem;
    font-weight: 800;
    grid-column: span 1;
    gap: 1rem;
    margin-top: 1.35rem;
    color: gray;
}
.header-menu > a:hover {
    border-radius: 1.2rem;
    background-color: rgb(177, 110, 187);
    color: rgb(240, 234, 218);
    transition: color 0.3s ease-in;
    transition: background-color 0.3s ease-in;
}
.header-menu > a {
    padding-left: 1.25rem;
    padding-right: 1.25rem;
}
.dark-grey {
    color: rgb(51, 47, 32);
}
.welcome {
    height: 55rem;
    background-color: rgb(216, 215, 215);
    margin-bottom: 12rem;
}
.welcome > h1 {
    padding: 8rem;
    padding-top: 10rem;
    font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
        "Lucida Sans", Arial, sans-serif;
    font-size: 4rem;
    line-height: 4.5rem;
    font-weight: bold;
    color: rgb(85, 85, 85);
}
.recommendation{
    transform: translateY(5rem);
    display:flex;
    width:90%;
    height:26rem;
    background:rgb(233, 230, 230);
    margin:auto;
    border-radius: 2rem;
    padding-inline:3rem;
    padding-top:1.5rem;
}
.recommendation > div > p{
    font-size: 2rem;
    margin-left: 1rem;
    /* line-height: 2rem; */
    color: rgb(85, 85, 85);
}
.buttons-container{
    margin-top:2rem;
}
.buttons{
    margin-top:1.8rem;
}
.buttons > a{
    color: white;
    border-radius: 1.2rem;
    background-color: rgb(177, 110, 187);
    padding: 0.5rem;
    padding-inline: 2rem;
    margin:0.5rem;
    font-size: 2.2rem;
    font-weight: bold;
}
.buttons > a:hover{
    border-radius: 1.2rem;
    background-color: rgb(146, 49, 25);
    color: rgb(240, 234, 218);
    transition: color 0.3s ease-in;
    transition: background-color 0.3s ease-in;
}
.search-bar{
    font-size: 2rem;
    color: rgb(85, 85, 85);
    font-weight: bold;
    height: 4.5rem;
    padding:1rem;
    padding-left:2rem;
    padding-top:2.5rem;
    padding-bottom:2.5rem;
    margin:2rem;
    width: 40rem;
    margin-top: 4rem;
    margin-left: 7rem;
    border-radius:1.5rem;
}
.carousel-container{
    margin:auto;
    width:90%;
}
.carousel{
    display: flex;
    justify-content: space-between;
}
.carousel > div{
    margin:1rem;
}
.title-container{
    display: flex;
    justify-content: space-between;
    margin-bottom:1rem;
    margin-top:3rem;

}
.title-container > p{
    font-size: 3rem;
    font-weight:bold;
    color: rgb(85, 85, 85);
}
.placeholder-picture{
    border-radius: 2rem;
    width:30rem;
    height:30rem;
    background-color:grey;

}
.arrow{
    background-image: url("https://www.iconpacks.net/icons/2/free-arrow-next-icon-2825-thumb.png");
    height:5rem;
    width: 5rem;
    background-repeat: no-repeat;
  background-size: 5rem 5rem;
}
.button{
       color: white;
    border-radius: 1.2rem;
    background-color: rgb(177, 110, 187);
    padding: 0.5rem;
    padding-inline: 2rem;
    margin:0.5rem;
    font-size: 2.2rem;
    font-weight: bold;
}
.button:hover{
    border-radius: 1.2rem;
    background-color: rgb(146, 49, 25);
    color: rgb(240, 234, 218);
    transition: color 0.3s ease-in;
    transition: background-color 0.3s ease-in;
}
.call-to-action{
    margin-top: 5rem;
    display:flex;
    height: 35rem;
    background-color: rgb(240, 240, 240);
    margin-bottom: 5rem;
}
.call-to-action > h1 {
    padding: 8rem;
    padding-top: 6rem;
    font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
        "Lucida Sans", Arial, sans-serif;
    font-size: 4rem;
    line-height: 4.5rem;
    font-weight: bold;
    color: rgb(85, 85, 85);
}
.call-button-container{
position: relative;
top: 25rem;
left: 30rem;
}
.map-container{
width: 90%;
margin:auto;
}
.map{
    background-color:green;
    height: 40rem;
    border-radius: 2rem;
}
.map > .button-container{
    display:inline-grid;
    position: relative;
    top: 27rem;
    left: 82rem;
}
.map-container > h1{
    margin-bottom: 3rem;
    font-size: 3rem;
    font-weight:bold;
    color: rgb(85, 85, 85);
}
</style>
