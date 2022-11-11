<script>
    import CardList from "./CardList.vue";
    import AppCategory from "./AppCategory.vue";

    
    export default{
        name: "AppMain",
        components :{
            CardList,
            AppCategory,
        },
        
    }
</script>

<template>
    <div class="container-fluid">
        <div class="container">
            <AppCategory   />
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