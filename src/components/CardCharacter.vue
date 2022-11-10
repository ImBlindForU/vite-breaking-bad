<script>


    export default{
        name: "CardCharacter",
        props: {
            character: Object
        }
    }
</script>



<template>

    <div class="card">
        <img :src="character.img" alt="">
        <h2>{{character.name}}</h2>
        <p>"{{character.status}}"</p>
    </div>

</template>

<style lang="scss" scoped>
    .card{
        display: flex;
        flex-direction: column;
        justify-content: center;
        img{
            max-width: 100%;
        }
        width: calc(100% / 5 - 2rem);
        padding: 2rem;
        margin: 1rem;
        background-color:greenyellow;
        border: 1px solid blue;
        
        h2{
            text-align: center;
            padding-top: 2rem;
            font-size: 3rem;
        }

        p{
            text-align: center;
            font-size: 2rem;


        }
    }
</style>