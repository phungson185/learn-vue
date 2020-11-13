<template>
  <div class = "header-content">  
        <div class ="header-nav">
            
            <div>
                <img class = "logo" src="../assets/SUNLogo.178d4636.png">
            </div>

            
            <nav>
                <ul>
                    <li class = "sun"><a href = "#">SUN</a></li>
                    <li class = "vote"><a href = "#">Vote</a></li>
                    <li class = "faqs"><a href = "#">FAQs</a></li>
                    <li class = "lear"><a href = "#">Learn</a></li> 
                </ul>
            </nav>
            

            <div class="header-right">
                <div class="connect-wallet">
                    <p>Connect to Wallet</p>
                </div>
                <div class="change-language">
                    <select>
                        <option class="english">English</option>
                        <option class="tiengviet">Tieng Viet</option>
                    </select>
                </div>
            </div>
        </div>
  </div> 
</template>

<script>
export default {
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .header-nav{
    display: flex;
    align-items: center;
    justify-content: space-between;
}


.header-nav .logo{
    width: 150px;
    height: 50px;
    margin: 30px;
}

.header-nav nav ul{
    display: flex;
    list-style: none;
}

.header-nav ul li {
    margin: 0 20px;
    padding: 5px 10px;
}
.header-nav ul li a, .header-nav ul div{
    text-decoration: none;
    color: rgb(255, 255, 255);
}

.header-nav nav ul .sun, .connect-wallet{
    background-color: rgb(0, 51, 255);
    border: 1px solid rgb(0, 51, 255);
    border-radius: 10px;
}

.header-right{
    display: flex;
    justify-content: space-between;
}

.connect-wallet{
    color: rgb(255, 255, 255);
    padding: 5px 20px;
}

.change-language{
    padding: 0 30px;
}

.content{
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}

.content h1{
    color: rgb(255, 255, 255);
    font-size: 50px;
    padding-bottom: 20px;
}

.content h3{
    color: rgb(255, 255, 255);
    padding-bottom: 10px;
}

.content p{
    color: rgb(255, 255, 255);
    padding-bottom: 90px;
}

.content p a{
    color: #fff;
}

.vote:hover,.faqs:hover{
    background-color: rgb(0, 51, 255);
    border: 0px solid rgb(0, 51, 255);
    border-radius: 10px;
}

</style>
