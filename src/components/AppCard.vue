<script>

export default{
    name: "AppCard",
    props: {
        img:String,
        title: String,
        data : Number
    }
}
</script>

<template>

  
        <div class="carousel__item" :data-pos="data">
            <img :src="img" alt="tokyo">
            <h2>{{title}}</h2>
            <h3>Japan</h3>
        </div>
    

</template>

<style lang="scss">
   
        .carousel__item{
            border-radius: 20px;
            width: 250px;
            height: 400px;
            background-position: center;
            background-size: cover;
            text-align: start;
            padding: 1rem 2rem;
            box-shadow: 0px 2px 8px 0px rgba(50, 50, 50, 0.5);

            position: relative;
            &[data-pos="0"] {
            z-index: 5;
            }
            
            &[data-pos="-1"],
            &[data-pos="1"] {
            opacity: 0.7;
            filter: blur(1px) grayscale(10%);
            }
            
            &[data-pos="-1"] {
            transform: translateX(20%) scale(.9);
            z-index: 4;
            }
            
            &[data-pos="1"] {
            transform: translateX(-20%) scale(.9);
            z-index: 4;
            }
            
            &[data-pos="-2"],
            &[data-pos="2"] {
            opacity: 0.4;
            filter: blur(3px) grayscale(20%);
            }
            
            &[data-pos="-2"] {
            transform: translateX(40%) scale(.8);
            z-index: 3;
            }
            
            &[data-pos="2"] {
            transform: translateX(-40%) scale(.8);
            z-index: 3;
            }
            img{
                width: 250px;
                height: 400px;
                object-fit: cover;
                border-radius: 20px;

            }
            h2{
                position: absolute;
                top: 2rem;
                left: 4rem;
          
            }
            h3{
                position: absolute;
                top: 4rem;
                left: 4rem;

            }
        }
    

 

    
</style>