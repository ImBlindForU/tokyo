<script>

export default{
    name: "AppFooter"
}
</script>

<template>

   <div class="container-fluid footer">
        <div class="text-footer">
            <div class="title-footer">
                <h3>Culture Festival</h3>
                <h5>2023</h5>
            </div>
            <div class="description">
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quae, consequatur iure. Dignissimos voluptate libero officiis tempora doloremque eos totam ratione, quas at. Sit quia at dolor mollitia iure animi veniam.</p>
            </div>
        </div>
            <div class="wrapper">
                <div class="button">
                    <div class="icon">
                        <i class="fab fa-facebook-f"></i>
                    </div>
                    <span>Facebook</span>
                </div>
                <div class="button">
                    <div class="icon">
                        <i class="fab fa-twitter"></i>
                    </div>
                    <span>Twitter</span>
                </div>
                <div class="button">
                    <div class="icon">
                        <i class="fab fa-instagram"></i>
                    </div>
                    <span>Instagram</span>
                </div>
                
                <div class="button">
                    <div class="icon">
                        <i class="fab fa-github"></i>
                    </div>
                    <span>Github</span>
                </div>
                <div class="button">
                    <div class="icon">
                        <i class="fab fa-youtube"></i>
                    </div>
                    <span>Youtube</span>
                </div>
            </div>
    </div>

</template>

<style lang="scss">
.footer{
    display: flex;
    justify-content: space-between;
    align-items: center;
    .text-footer{
        display: flex;
        justify-content: start;
        align-items: center ;
        h3{
            font-size: 2rem;
        }
        .description{
            padding-left: 1rem;
            width: 40%;
            margin-left: 1rem;
            border-left: 1px solid white;
        }
    }
}
i{
    color: #333;
}
.wrapper .button{
    height: 60px;
    width: 60px;
    float: left;
    overflow: hidden;
    background: #fff;
    border-radius: 50px;
    cursor: pointer;
    box-shadow: 0px 10px 10px rgba(0,0,0,0.1);
    transition: all 0.3s ease-out ;
}
.wrapper .button:hover{
    width: 160px;
}
.wrapper .button .icon{
    display: inline-block;
    height: 60px;
    width: 60px;
    text-align: center;
    border-radius: 50px;
    box-sizing: border-box;
    line-height: 60px;
    transition: all 0.3s ease-out ;

}
.wrapper .button:nth-child(1):hover .icon{
    background: #4267b2;
    
}
.wrapper .button:nth-child(2):hover .icon{
    background: #1da1f2;

}

.wrapper .button:nth-child(3):hover .icon{
    background: #e1306c;
    
}

.wrapper .button:nth-child(4):hover .icon{
    background: #333;
    
}

.wrapper .button:nth-child(5):hover .icon{
    background: #ff0000;
    
}
.wrapper .button .icon i{
    font-size: 25px;
    line-height: 60px;
}
.wrapper .button:hover .icon i{
    color: #fff;
    transition: all 0.3s ease-out ;

}
.wrapper .button span{
    font-size: 20px;
    font-weight: 500;
    line-height: 60px;
    margin-left: 10px;
    transition: all 0.3s ease-out ;

}

.wrapper .button:nth-child(1):hover span{
    color: #4267b2;
    
}
.wrapper .button:nth-child(2):hover span{
    color: #1da1f2;

}

.wrapper .button:nth-child(3):hover span{
    color: #e1306c;
    
}

.wrapper .button:nth-child(4):hover span{
    color: #333;
    
}

.wrapper .button:nth-child(5):hover span{
    color: #ff0000;
    
}

</style>