<script>

export default{
    name : "AppHeader"
}

</script>

<template>
    <div class="container-fluid">
        <div class="row-header">
            <div class="logo">
                <i class="fa-solid fa-bolt"></i>
            </div>
            <div class="header-links">
                <ul>
                    <li>
                        <a href="">Home</a>
                        
                    </li>
                    <li>
                        <a href="">About us</a>
                    </li>
                    <li>
                        <a href="">Service</a>

                    </li>
                    <li>
                        <a href="">Package</a>
                    </li>
                    <li>
                        <a href="">Contact</a>
                    </li>
                    <li class="search">
                        <i class="fa-solid fa-magnifying-glass"></i>
                    </li>
                </ul>   
                

            </div>
        </div>
    </div>
   

</template>


<style lang="scss">
.search{
    width: 69px;
    height: 69px;
    padding: 1rem;
    border-radius: 20px;
    text-align: center;
    background-color: white;
    &:hover{
        background-color: purple;
        color: purple;
        transition: all 0.4s ease-in;

    }
}
.row-header{
    padding-top: 3rem;
    font-size: 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    opacity: 0.9;
    .logo{
       
        i{
            color: white;
            font-size: 2rem;

            &:hover{
                transition: all 0.4s ease-in;
                color: purple;
            }
        }
    }
    .header-links{
        ul{
            display: flex;
            justify-content:space-between;
            align-items: center;
            list-style: none;
            
            li{
            
            margin-right: 2rem;

            &:hover{
                color: black;
                a{
                    transition: all 0.4s ease-in-out;
                    color: purple;
                    // border-top: 1px solid purple;
                    // border-bottom: 1px solid purple;
                    border: 1px solid purple;
                    padding: .8rem;  
                    

                }
            }
                a{
                    border-bottom: 1px solid transparent;

                    color: white;
                    padding: 1rem;  
                    text-decoration: none;

                  
                }
            }
        }
    }
}
</style>