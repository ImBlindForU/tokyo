<script>

export default{
    name : "AppHeader"
}

</script>

<template>
    <div class="container-fluid">
        <div class="row-header">
            <div class="logo">
                <h2>Tokyo</h2>
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
                    <li class="search"><i class="fa-solid fa-magnifying-glass"></i></li>
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
}
.row-header{
    padding-top: 3rem;
    font-size: 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    opacity: 0.9;
    .header-links{
        ul{
            display: flex;
            justify-content:space-between;
            align-items: center;
            list-style: none;
            li{
            margin-right: 1rem;
                a{
                    color: white;
                    text-decoration: none;
                }
            }
        }
    }
}
</style>