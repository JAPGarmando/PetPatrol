<template>
    <div v-bind:style="{'background-color': buttonColor}" class="buttonContainer">
        <div class="imageContainer">
            <div v-bind:style="{'background-image': `url(${buttonImage})`}" class="buttonImage">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'categoryButtons',
    props: {
        buttonColor: String,
        buttonImage: String
    },
    data: () => {
        
    }
}
</script>

<style scoped>
    .buttonContainer{
        width: 192px;
        height: 192px;
        border-radius: 100px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }

    .buttonContainer:hover{
        width: 192px;
        height: 192px;
        opacity: 0.8;
        cursor: pointer;
    }

    .imageContainer{
        width: 168px;
        height: 168px;
        border-radius: 100px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }

    .buttonImage{
        width: 100%;
        height: 100%;
        border-radius: 100px;
        background-size: cover;
    }
</style>