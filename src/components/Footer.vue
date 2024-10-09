<script setup>


</script>

<template>
    <footer class="section__footer">
        <div class="container__footer">
            <div class="left">
                <div>
                    <img src="https://fakeimg.pl/100x50/" alt="">
                </div>
                <div>
                    <p>Powered by</p>
                    <img src="../assets/image.png" alt="">
                </div>
            </div>
            <div class="center">
                <ul class="center__ul">
                    <li>
                        <a href="">Politica de Pivacidade</a>
                    </li>
                    <li>
                        <a href="">Termos de uso</a>
                    </li>
                    <li>
                        <a href="">Regulamento</a>
                    </li>
                    <li>
                        SRE: 00000000000000
                    </li>
                </ul>
            </div>
            <div class="right">
                <ul class="icons__row">
                    <li>
                        <a href=""><img src="../assets/facebook.png" alt=""></a>
                    </li>
                    <li>
                        <a href=""><img src="../assets/instagram.png" alt=""></a>
                    </li>
                    <li>
                        <a href=""><img src="../assets/youtube.png" alt=""></a>
                    </li>
                    <li>
                        <a href=""><img src="../assets/LinkedIn.png" alt=""></a>
                    </li>
                </ul>
                <ul class="column__links">
                    <li>
                        <a href="">HOME</a>
                    </li>
                    <li>
                        <a href="">COMO PARTICIPAR</a>
                    </li>
                    <li>
                        <a href="">PRÊMIOS</a>
                    </li>
                    <li>
                        <a href="">DUVIDAS FREQUENTES</a>
                    </li>
                    <li>
                        <a href="">GANHADORES</a>
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<style scoped>

*{
    color: aliceblue;
}
.section__footer{
    height: 400px;
    width: 100%;
    background-color: #fe6763;
}

.container__footer{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    max-width: 80%;
    margin-inline: auto;
}

.left{
    display: flex;
    margin-top: 63px;
    flex-direction: column;
    gap: 3rem 0;
}

.center{
    
    margin-top: 4rem;
}

.center__ul{
    display: flex;
    flex-direction: column;
    gap: 3rem;
    list-style: none;
}

.right{
    margin-top: 4rem;
}
.icons__row{
    display: flex;
    flex-direction: row;
    gap: 10px;
    list-style: none;
}

.icons__row img{
    height: 2rem;
}

.column__links{
    display: flex;
    flex-direction: column;
    margin-top: 2rem;
    list-style: none;
}

li a{
    color: white;
}

li{
    font-weight: bold;
}

@media (max-width: 480px){
    .container__footer{
        flex-direction: column;
        
    }
    .section__footer{
        height: auto;
    }
}
</style>