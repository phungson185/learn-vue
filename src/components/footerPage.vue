<template>
    <footer>
    <ul>
        <li><a href="https://twitter.com/defi_sunio" target="twitter">Twitter</a></li>
        <li><a href="https://t.me/SunIO_Defi" target="tele">Telegram</a></li>
        <li class="wc">WeChat
            <ul>
                <li><img src="../assets/qrwechat.jpg"></li>
            </ul>
        </li>
    </ul>
    </footer>
</template>

<script>
export default {
    
}
</script>

<style scoped>
footer{
    text-align: center;
}

footer ul{
    padding-bottom: 30px;
    display: flex;
    justify-content: center;
}


footer .wc{
    position: relative;
    cursor: pointer;
}

footer img{
    position: absolute;
    max-width: 150px;
    max-height: 150px;
    top: -350%;
    left: -70%;
    text-align: left;
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