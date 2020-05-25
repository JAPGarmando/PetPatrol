<template>
    <div id="home">
        <p class="headers">Últimas actualizaciones <v-icon class="icons">fas fa-newspaper</v-icon></p>
        <div class="rowContainer">
        </div>
        <p class="headers">Categorías <v-icon class="icons">fas fa-paw</v-icon></p>
        <div class="rowContainer">
            <category-buttons v-for="buttonColor in buttonColors" :key="buttonColor.key" 
            :buttonColor="buttonColor.color" :buttonImage="buttonColor.img"/>
        </div>
        <p class="headers">Cerca de ti <v-icon class="icons">fas fa-map-marked-alt</v-icon></p>
    </div>
</template>

<script>
import categoryButtons from '../components/home/categoryButtons.vue'
export default {
    name: 'home',
    components: {
        categoryButtons
    },
    data: () => ({
        buttonColors: [
            {key: 1,color: '#21a434',img: '../assets/boxer.png'},
            {key: 2,color: '#a42151',img: '../assets/chihuahua.jpg'},
            {key: 3,color: '#a4219f',img: '../assets/perico.jpg'},
            {key: 3,color: '#21a434',img: '../assets/pug.jpg'}
        ]
    })
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
    #home{
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        flex-wrap: nowrap;
        padding: 24px 0px 0px 24px;
    }
    .rowContainer{
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: space-between;
        align-items: center;
    }
    .icons{
        font-size: 36px;
        font-weight: bold;
        color: white;
    }
    .headers{
        font-family: 'Poppins',sans-serif;
        font-size: 36px;
        font-weight: bold;
        color: white;
    }
</style>