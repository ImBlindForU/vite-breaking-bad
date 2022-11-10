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
                <select name="select" id="">
                    <option value="select">Select Category</option>
                    <option value="maybe">Maybe</option>
                    <option value="no">No</option>

                </select>
            </div>
            <CardList />
            
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .container-fluid{
        .container{
            margin-top: 10rem;
            .select{
                select{
                    
                    border-radius: 1rem;
                    font-size: 2rem;
                    padding: 1rem;
                }
                padding: 1rem;
                margin-bottom: 2rem;
            }
            .row-cards{
                display: flex;
            }
        }
    }
</style>