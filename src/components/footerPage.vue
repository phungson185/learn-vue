<template>
    <footer>
        <a href="https://twitter.com/defi_sunio" target="twitter">Twitter</a>
        <a href="https://t.me/SunIO_Defi" target="tele">Telegram</a>
        <a class="qr-code">
            WeChat
            <img title="qrwechat.jpg" alt>
        </a>
    </footer>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    footer {
    width: calc(80% - 100px);
    margin: 0 auto;
    text-align: center;
    padding-bottom: 35px;
}

footer a, footer a:link, footer a:visited {
    color: #999;
}

a, a:link, a:visited {
    color: #1890ff;
    text-decoration: none;
}

footer a {
    margin: 0 30px;
    font-size: 12px;
}
</style>