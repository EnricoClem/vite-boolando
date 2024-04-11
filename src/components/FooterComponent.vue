<script>
export default {
  
}
</script>

<template>
    <footer>
        <div class="container-footer">
            <div class="row foot">
                <div>
                    <h4>Booleando s.r.l</h4>
                    <ul>
                        <li>
                            <a href="#">Informazioni legali</a>
                        </li>
                        <li>
                            <a href="#">Informativa sulla privacy</a>
                        </li>
                        <li>
                            <a href="#"> Diritto di recesso</a>
                        </li>
                    </ul>
                </div>
                <!-- Tasti social sulla destra -->
                <div>
                    <h4>Trovaci anche su</h4>
                    <ul>
                        <li>
                            A
                        </li>
                        <li>
                            B
                        </li>
                        <li>
                            C
                        </li>
                        <li>
                            D
                        </li>
                        <li>
                            E
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<style>

footer :is(a, li, h3, h4) {
    color: white;
}

footer li {
    display: inline;
    margin-right: 5px;
}

footer {
    background-color: #1a1a1a;
    width: 100%;
    margin-top: auto;
}

.row.foot {
    padding: 20px 0;
    align-items: center;
    justify-content: space-between;
}

</style>