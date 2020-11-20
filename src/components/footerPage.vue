<template>
    <footer>
        <li><a href="https://twitter.com/defi_sunio" target="twitter">Twitter</a></li>
        <li><a href="https://t.me/SunIO_Defi" target="tele">Telegram</a></li>
        <li class="wc">WeChat
            <img src="../assets/qrwechat.jpg">
        </li>
    </footer>
</template>

<script>
export default {
    
}
</script>

<style scoped>
footer{
    display: flex;
    width: 100%;
    margin: 10px auto 0 auto;
    padding-bottom: 20px;
    justify-content: center;
    bottom: 10px;
}

footer .wc{
    position: relative;
    cursor: pointer;
}

footer img{
    position: absolute;
    max-width: 150px;
    max-height: 150px;
    left: -30px;
    bottom: 40px;
    display: none;
}

footer .wc:hover img{
    display: block;
}

footer a,li {
    color: #999;
    margin: 0 30px;
    font-size: 12px;
}

footer a:hover, .wc:hover{
    color: rgb(0,51,255);
}
</style>