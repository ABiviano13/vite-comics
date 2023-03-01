<script>

export default {
    data() {
        return {
            arrayListBuy: [
                {
                    image: '/img/buy-comics-digital-comics.png',
                    text: 'Digital Comics'
                },
                {
                    image: '/img/buy-comics-merchandise.png',
                    text: 'Dc Merchandise'
                },
                {
                    image: '/img/buy-comics-shop-locator.png',
                    text: 'Subscription'
                },
                {
                    image: '/img/buy-comics-subscriptions.png',
                    text: 'Comic Shop Locator'
                },
                {
                    image: '/img/buy-dc-power-visa.svg',
                    text: 'Dc Power Visa'
                },

            ]
            
        }
    }
}

</script>

<template>

    <main>
        <section class="section-content">
            <div class="container">
            <h2>
                Content
            </h2>
        </div>
        </section>
        <section class="section-content-buy">
            <div class="container">
                <ul class="list-buy">
                    <li class="list-item-buy"
                    v-for="cardBuy in arrayListBuy">
                        <img :src="cardBuy.image" alt="">
                        {{ cardBuy.text }}
                    </li>
                </ul>
            </div>
        </section>
    </main>

</template>

<style lang="scss" scoped>

$black: #1c1c1c;
$blue: #338af9;

main{
    color: white;

    .section-content {
        background-color: $black;
        padding: 54px 0;
    }

    .section-content-buy {
        background-color: $blue;
        padding: 50px 0;

        .list-buy{
            display: flex;
            align-items: center;
            justify-content: space-between;

            .list-item-buy {
                display: flex;
                align-items: center;
                gap: 15px;
            }
        }

        img {
            width: 54px;
            height: 64px;
        }

    }

}

</style>