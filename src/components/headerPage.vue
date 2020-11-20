<template>
  <div class = "header-content">  
        <div class ="header-nav">
            
            <div class="Logo">
                <img class = "logo" src="../assets/SUNLogo.178d4636.png">
            </div>

            <nav>
                <ul>
                    <li class = "sun" :class="{Sun : isSun}" @click="changeTab($event)"><a href = "#">SUN</a></li>
                    <li class = "vote" :class="{Vote : isVote}" @click="changeTab($event)"><a href= "#">Vote</a></li>
                    <li class = "faqs" :class="{Faqs : isFaqs}" @click="changeTab($event)"><a href = "#">FAQs</a></li>
                    <li class = "learn"><a href = "#">Learn</a>
                        <ul class="dropdown-content">
                            <li><a href="#">WhitePaper</a></li>
                            <li><a href="#">Audit</a></li>
                        </ul>
                    </li> 
                </ul>
            </nav>

            <div class="header-right">
                <div class="connect-wallet">
                    <p><a href="">Connect to Wallet</a></p>
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
    el : '#header-nav',
    data() {
        return {
            isSun : true,
            isVote : false,
            isFaqs : false
        }
    },
    methods: {
        changeTab(event) {

            this.$emit('changeTabHeader', event.target.outerText);
            if(event.target.outerText === 'SUN')
                {
                    this.isSun = true,
                    this.isVote = false,
                    this.isFaqs = false
                }
            else if (event.target.outerText === 'Vote')
                {
                    this.isSun = false,
                    this.isVote = true,
                    this.isFaqs = false
                }
            else if (event.target.outerText === 'FAQs')
                {
                    this.isSun = false,
                    this.isVote = false,
                    this.isFaqs = true
                }
        }   
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .header-nav{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.header-nav .Logo, .header-right, .nav{
    width: 33.33333333333333333333%
}
.header-nav .logo{
    width: 150px;
    height: 50px;
    margin: 30px;
}

.sun a,.vote a,.faqs a, .learn a{
    color: #fff;
}

.sun.Sun, .vote.Vote, .faqs.Faqs{
    background-color: rgb(0, 51, 255);
    border-radius: 10px;
}



.header-nav ul li {
    display: inline-block;
    padding: 10px;
    margin: 0 20px;
    cursor: pointer;
}

.learn{
    position: relative;
}

.dropdown-content li {
    width: 100%;
    float: left;
}

.dropdown-content li a{
    color: #000;
}

.dropdown-content li a:hover{
    color:rgb(0, 51, 255);
}
.dropdown-content {
    background-color: #fff;
    position: absolute;
    top: 100%;
    left: 0;
    text-align: left;
    display: none;
}

.learn:hover .dropdown-content{
    display: block;
}

.header-right{
    display: flex;
    justify-content: flex-enD;
}

.connect-wallet{
    padding: 5px 20px;
    background-color: rgb(0, 51, 255);
    border-radius: 10px;
}

.connect-wallet a{
    color: rgb(255, 255, 255);
}

.change-language{
    padding: 0 30px;
}

.change-language select{
    padding: 5px 10px;
    border-radius: 10px;
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

footer .imgQrcodeOfWechat{
    position: absolute;

}

</style>
