<script>
import card from './AppCard.vue'; 

export default {
    components: {
        card
    },
    data() {
        return {
            arrayListBuy: [
                {
                    image: '/img/buy-comics-digital-comics.png',
                    text: 'Digital Comics',
                    height: 50
                },
                {
                    image: '/img/buy-comics-merchandise.png',
                    text: 'Dc Merchandise',
                    height: 50
                },
                {
                    image: '/img/buy-comics-subscriptions.png',
                    text: 'Subscription',
                    height: 50
                },
                {
                    image: '/img/buy-comics-shop-locator.png',
                    text: 'Comic Shop Locator',
                    height: 50
                },
                {
                    image: '/img/buy-dc-power-visa.svg',
                    text: 'Dc Power Visa',
                    height: 30
                },

            ],

            cards: [
                {
                    "thumb": "./public/img/actioncomics.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "./public/img/americanvampire1976.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "./public/img/acquaman.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "./public/img/Batgirl.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "./public/img/batman.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "./public/img/batmanbeyond.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "./public/img/batmanvssuperman.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "./public/img/batmanvssupermanannual.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "./public/img/batmanjoker.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "./public/img/batmanthreejoker.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "./public/img/batmanharleyqueen.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "./public/img/catwoman.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
               }
            ]
            
        }
    }
}

</script>

<template>

    <main>
        <div class="section-jumbotron">
            <img src="/img/jumbotron.jpg" alt="">
        </div>
        <div class="section-content">
            <div class="container">
                <div class="target style-target-button">
                    <h3>
                        Current Series
                    </h3>
                </div>
                <ul class="card-list">
                    <!-- <li class="card"
                    v-for="card in cards">
                        <figure>
                            <img :src="card.thumb" alt="">
                        </figure>
                        <div class="text-card">
                            {{ card.series }}
                        </div>
                    </li> -->
                    <card 
                    v-for="(card,i) in cards" :key="i"
                    :image="card.thumb"
                    :text="card.series"
                    >
                    </card>
                </ul>
                <div class="button style-target-button">
                    Load More
                </div>
            </div>
        </div>
        <div class="section-content-buy">
            <div class="container">
                <ul class="list-buy">
                    <li class="list-item-buy"
                    v-for="cardBuy in arrayListBuy">
                        <img :src="cardBuy.image" alt="">
                        {{ cardBuy.text }}
                    </li>
                </ul>
            </div>
        </div>
    </main>

</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;


main{
    color: white;

    .section-jumbotron{
        height: 400px;
        img{
            height: 100%;
            width: 100%;
            aspect-ratio: 1/1;
            object-fit: cover;
            object-position: top;
        }
    }

    .section-content {
        background-color: $black;
        padding: 54px 0;

        .card-list{
            display: grid;
            grid-template-columns: repeat(6, 1fr);
            gap: 30px;
            row-gap: 50px;

            // .card{

            //     img{
            //         width: 180px;
            //         aspect-ratio: 1/1;
            //         object-fit: cover;
            //         object-position: center;
            //     }

            //     .text-card{
            //         text-transform: uppercase;
            //     }
            // }
        }

        .style-target-button{
            background-color: $blue;
            width: max-content;
            text-transform: uppercase;
        }

        .target{
            position: relative;
            bottom: 85px;
            padding: 15px 30px;
        }

        .button{
            margin: 0 auto;
            padding: 10px 60px;
            margin-top: 50px;
            font-weight: bold;
        }
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
                text-transform: uppercase;
            }
        }

        img {
            height: 50px;
        }

    }

}

</style>