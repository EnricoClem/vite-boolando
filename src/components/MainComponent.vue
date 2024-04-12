<script>
export default {
  data() {
    return {
        items: [{
            "name": 'Levis',
            "brand": 'RELAXED FIT TEE UNISEX',
            "price": '29,99 €',
            "newPrice": '14,99 €',
            "imgCover": '/imgs/1.webp',
            "imgHover": '/imgs/1b.webp',
            "badges": [
                {
                    "type": "eco",
                    "value":"Sostenibilità"
                }, {
                    "type": "promo",
                    "value":"-50%"
                }
            ]
        }, {
            "name": 'Guess',
            "brand": 'ROSES TEE',
            "price": '29,99 €',
            "newPrice": '20,99 €',
            "imgCover": '/imgs/2.webp',
            "imgHover": '/imgs/2b.webp',
            "badges": [
                {
                    "type": "promo",
                    "value":"-30%"
                }
            ]
        }, {
            "name": 'Come zuccher filato',
            "brand": 'VOGLIA DI COLORI PASTELLO',
            "price": '129,99 €',
            "newPrice": '184,99 €',
            "imgCover": '/imgs/3.webp',
            "imgHover": '/imgs/3b.webp',
            "badges": [
                {
                    "type": "promo",
                    "value":"-30%"
                }
            ]
        }, {
            "name": 'Levis',
            "brand": 'TEE UNISEX',
            "price": '29,99 €',
            "newPrice": '14,99 €',
            "imgCover": '/imgs/4.webp',
            "imgHover": '/imgs/4b.webp',
            "badges": [
                {
                    "type": "eco",
                    "value":"Sostenibilità"
                }, {
                    "type": "promo",
                    "value":"-50%"
                }
            ]
        }, {
            "name": 'Maya Deluxe',
            "brand": 'STRIPE BODICE',
            "price": '14,99 €',
            "newPrice": '',
            "imgCover": '/imgs/5.webp',
            "imgHover": '/imgs/5b.webp',
            "badges": []
        }, {
            "name": 'Esprit',
            "brand": 'MAGLIONE BLACK',
            "price": '14,99 €',
            "newPrice": '',
            "imgCover": '/imgs/6.webp',
            "imgHover": '/imgs/6b.webp',
            "badges": [
                {
                    "type": "eco",
                    "value":"Sostenibilità"
                }
            ]
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
                    <ul class="info-sale">
                        <li v-for="(badge,i) in item.badges" :key="i"
                        :class="`${badge.type}`"
                        class="badge promo">
                            <h4>{{ badge.value }}</h4>
                        </li>                   
                    </ul>
                </li>
            </ul>
        </section>
    </main>
</template>

<style lang="scss" scoped>

@use './style/partials/reset' as *;
@use './style/partials/variables' as *;
@use './style/partials/layout' as *;

.container-items {
    padding: 120px 0 50px 0;
}
main .row {
    justify-content: space-between;
    gap: 30px;
    padding: 20px;
}

.item {
    width: 31.5%;
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

.badge {
    padding: 8px;
    color: white;
    display: inline-block;
}

.badge.promo {
    background-color: red;
}

.badge.eco {
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