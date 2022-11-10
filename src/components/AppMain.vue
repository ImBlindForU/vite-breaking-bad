<script>
    import CardList from "./CardList.vue";

    
    export default{
        name: "AppMain",
        components :{
            CardList,
        }
    }
</script>

<template>
    <div class="container-fluid">
        <div class="container">
            <div class="select">
                cia
            </div>
            <CardList />
            
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .container-fluid{
        .container{
            margin-top: 10rem;
            
            .row-cards{
                display: flex;
            }
        }
    }
</style>