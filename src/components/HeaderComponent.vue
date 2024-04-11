<script>
export default {
  
}
</script>

<template>
    <header>
        <div class="container">
            <div class="row head">
                <!-- Tasti tipologia -->
                <ul>
                    <li>
                        <a href="#"><strong>Donna</strong></a>
                    </li>
                    <li>
                        <a href="#"><strong>Uomo</strong></a>
                    </li>
                    <li>
                        <a href="#"><strong>Bambini</strong></a>
                    </li>
                </ul>
                <!-- Logo sito -->
                <div>
                    <img src="/boolean-logo.png" alt="Logo Booleando" class="logo-header">
                </div>
                <!-- Tasti simboli area personale e carrello -->
                <ul>
                    <li>
                        <a href="#">A</a>
                    </li>
                    <li>
                        <a href="#">B</a>
                    </li>
                    <li>
                        <a href="#">C</a>
                    </li>                    
                </ul>
            </div>
        </div>
    </header>
</template>

<style>

header a  {
    color: white;
}

header li {
    display: inline;
    margin-right: 5px;
}

header {
    background-color: #ff6800;
    position: fixed;
    z-index: 9999;
    width: 100%;
}

.row.head {
    padding: 20px 0;
    align-items: center;
    justify-content: space-between;
}

.logo-header {
    width: 130px;
}

</style>