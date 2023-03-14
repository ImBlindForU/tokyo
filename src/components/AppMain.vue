<script>
import AppHeader from './AppHeader.vue'
import AppCard from './AppCard.vue'
import AppFooter from './AppFooter.vue'

export default{
    name : "AppMain",
    components: {
    AppHeader,
    AppFooter,
    AppCard
  },
    data(){
        return{
            cards:[
             {
                 image: 'src/img/tokyo-tower.jpg',
                 title: 'Tokyo Tower',
                 data : -2
             },
             {
                 image: 'src/img/tokyo-kimono.jpg',
                 title: 'Kimono',
                 data : -1
             },
             {
                 image: 'src/img/tokyo-street-food.jpg',
                 title: 'Street Food',
                 data : 0
             },
             {
                 image: 'src/img/tokyo5.jpg',
                 title: 'Tokyo Night',
                 data : 1
             },
             {
                 image: 'src/img/tokyo4.jpg',
                 title: 'Temple',
                 data : 2
             }
    ]
        }
    }
    
}

</script>

<template>
    <div id="main" class="container main">
        <AppHeader />
        <div class="container-fluid flex-main">
            <div class="title">
                <h1>TOKYO</h1>
                <h2>...not so far away</h2>
            </div>
            <div class="carousel__list">
                <AppCard v-for="card in cards" :key="card"
                    :img="card.image"
                    :title="card.title"
                    :data="card.data"/>
            </div>
        </div>
        <AppFooter />
    </div>
</template>


<style lang="scss">

#main{
    background-image: url(../img/tokyo6.jpg);
    background-size: cover;
}
.main{
    overflow: hidden;
    
    width: 100vw;
    height: 100vh;
    .flex-main{
        height: 80vh;
        display: flex;
        justify-content: space-between  ;
        align-items: center;
        .title{
                padding: 1rem;
            border-radius: 20px;
            margin-right: 15rem;
            &:hover{
                transition: all 1.5s ease;
                background-color: black;
            }
            h1{
                font-size: 10rem;
            }
            h2{
                font-size: 3rem;
            }
        }
    }
}
.carousel__list{
    display: flex;
    position: relative;
    width: 100%;
    height: 300px;
    justify-content: center;
    perspective: 300px;
  
}
</style>