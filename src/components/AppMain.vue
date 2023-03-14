<script>
import AppHeader from './AppHeader.vue'
// import AppCard from './AppCard.vue'
import AppFooter from './AppFooter.vue'
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';



// import required modules
import { Pagination } from 'swiper';

export default{
    name : "AppMain",
    components: {
    AppHeader,
    AppFooter,
    Swiper,
      SwiperSlide,
    // AppCard
  }, setup() {
      return {
        modules: [Pagination],
      };
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
            <swiper
              :slidesPerView="3"
              :spaceBetween="30"
              :pagination="{
                clickable: true,
              }"
              :modules="modules"
              class="mySwiper"
            >
              <swiper-slide>
                <div class="card">
                  <img src="src/img/tokyo-tower.jpg" alt="tokyo">
                  <h2>Tokyo Tower</h2>
                  <h3>Japan</h3>
                </div>
              </swiper-slide>
              <swiper-slide>
                <div class="card">
                  <img src="src/img/tokyo-kimono.jpg" alt="tokyo">
                  <h2>Kimono</h2>
                  <h3>Japan</h3>
                </div>
              </swiper-slide>
              <swiper-slide>
                <div class="card">
                  <img src="src/img/tokyo-street-food.jpg" alt="tokyo">
                  <h2>Street Food</h2>
                  <h3>Japan</h3>
                </div>
              </swiper-slide>
              <swiper-slide>
                <div class="card">
                  <img src="src/img/tokyo5.jpg" alt="tokyo">
                  <h2>Tokyo Night</h2>
                  <h3>Japan</h3>
                </div>
              </swiper-slide>
              <swiper-slide>
                <div class="card">
                  <img src="src/img/tokyo4.jpg" alt="tokyo">
                  <h2>Tample</h2>
                  <h3>Japan</h3>
                </div>
              </swiper-slide>
            </swiper>
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

.card{
  width: 250px;
  height: 400px;
  border-radius: 20px;
  position: relative;
  img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 20px;
  }
  h2{
    position: absolute;
    top: 2rem;
    left: 2rem;
    z-index: 100;
  }
  h3{
    position: absolute;
    top: 4rem;
    left: 2rem;
    z-index: 100;
  }
}
</style>