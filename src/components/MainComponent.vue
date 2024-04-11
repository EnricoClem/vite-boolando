<script>
export default {
  data() {
    return {
        items: [{
            name: 'Levis',
            brand: 'RELAXED FIT TEE UNISEX',
            price: '29,99 €',
            promo: '-50%',
            eco: 'Sostenibilità',
            newPrice: '14,99 €',
            imgCover: '/imgs/1a.webp',
            imgHover: '/imgs/1b.webp'
        }, {
            name: 'Guess',
            brand: 'ROSES TEE',
            price: '29,99 €',
            promo: '-30%',
            eco: '',
            newPrice: '20,99 €',
            imgCover: '/imgs/2a.webp',
            imgHover: '/imgs/2b.webp'
        }, {
            name: 'Come zuccher filato',
            brand: 'VOGLIA DI COLORI PASTELLO',
            price: '129,99 €',
            promo: '-30%',
            eco: '',
            newPrice: '184,99 €',
            imgCover: '/imgs/3a.webp',
            imgHover: '/imgs/3b.webp'
        }, {
            name: 'Levis',
            brand: 'TEE UNISEX',
            price: '29,99 €',
            promo: '-50%',
            eco: 'Sostenibilità',
            newPrice: '14,99 €',
            imgCover: '/imgs/4a.webp',
            imgHover: '/imgs/4b.webp'
        }, {
            name: 'Maya Deluxe',
            brand: 'STRIPE BODICE',
            price: '14,99 €',
            promo: '',
            eco: '',
            newPrice: '',
            imgCover: '/imgs/5a.webp',
            imgHover: '/imgs/5b.webp'
        }, {
            name: 'Esprit',
            brand: 'MAGLIONE BLACK',
            price: '14,99 €',
            promo: '',
            eco: 'Sostenibilità',
            newPrice: '',
            imgCover: '/imgs/6a.webp',
            imgHover: '/imgs/6b.webp'
        }]
    }
  }
}
</script>

<template>
    <main>
        <section class="container-items">
            <ul class="row">
                <li v-for="item in items"
                class="item">
                    <img :src="item.imgCover" alt="">
                    <img class="img-hover" :src="item.imgHover" alt="">
                    <h5>
                        {{ item.brand }}
                    </h5>
                    <h4 class="name-item">
                        {{ item.name }}
                    </h4>
                    <h5>
                        <span class="new-price">{{ item.newPrice }}</span> 
                        <s>{{ item.price }}</s>
                    </h5>
                    <p class="heart">&hearts;</p>
                    <p class="heart-hover">&hearts;</p>
                    <!-- Tab promozionali -->
                    <div class="info-sale">
                        <div class="tab-promo">
                            <h4>{{ item.promo }}</h4>
                        </div>
                        <div class="tab-eco">
                            <h4>{{ item.eco }}</h4>
                        </div>                        
                    </div>
                </li>
            </ul>
        </section>
    </main>
</template>

<style lang="scss">

@use './style/partials/reset' as *;
@use './style/partials/variables' as *;
@use './style/partials/layout' as *;

.container-items {
    padding: 120px 0 50px 0;
}
main .row {
    justify-content: space-between;
}

.item {
    width: 32.5%;
    margin-bottom: 15px;
    position: relative;
}

.item h5 {
    font-weight: lighter;
    color: gray;
}

.new-price {
    color: red;
    font-weight: bold;
}

.normal-price {
    color: black;
    font-weight: bold;
}

[class*="heart"] {
    position: absolute;
    top: 10px;
    right: 0;
    font-size: 40px;
    background-color: white;
    padding: 0 12px;
}

.info-sale {
    position: absolute;
    bottom: 100px;
}

[class^="tab"] {
    padding: 8px;
    color: white;
    display: inline-block;
}

.tab-promo {
    background-color: red;
}

.tab-eco {
    background-color: green;
}

.img-hover {
    position: absolute;
    top: 0;
    left: 0;
    opacity: 0%;
}

.heart-hover {
    color: red;
    opacity: 0%;
}

[class*="hover"]:hover {
    opacity: 100%;
}

</style>