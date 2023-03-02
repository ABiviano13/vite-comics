<script>

export default {
    data() {
        return {
            arraylinkFooter: [
                {
                    title: 'Dc Comics',
                    link: [
                        'Characters',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Videos',
                        'News'
                    ],
                    shop: [{
                        title: 'Shop',
                        link: [
                            'Shop DC',
                            'Shop DC Collectibles'
                        ]
                    }]
                },
                {
                    title: 'Dc',
                    link: [
                        'Terms Of Use',
                        'Privacy policy (New)',
                        'Ad Choices',
                        'Advertising',
                        'Jobs',
                        'Subscriptions',
                        'Talent Workshops',
                        'CPSC Certificates',
                        'Ratings',
                        'Shop Help',
                        'Contact Us'
                    ]
                },
                {
                    title: 'Sites',
                    link: [
                        'DC',
                        'MAD Magazine',
                        'DC Kids',
                        'DC Universe',
                        'DC Power Visa'
                    ]
                },
            ],

            arrayIcon: [
                '/img/footer-facebook.png',
                '/img/footer-twitter.png',
                '/img/footer-youtube.png',
                '/img/footer-pinterest.png',
                '/img/footer-periscope.png'
            ]
    
            
        }
    }
}

</script>

<template>

    <footer>
        <div class="section-link">
            <div class="container">
                <div class="link">
                    <ul v-for="objectLink in arraylinkFooter">
                        <h3 class="title">
                            {{ objectLink.title }}
                        </h3>
                        <li class="text"
                        v-for="link in objectLink.link">
                            {{ link }}
                        </li>
                        <ul class="shopUl"
                        v-for="shop in objectLink.shop">
                            <h3 class="title">
                                {{ shop.title }}
                            </h3>
                            <li class="text"
                            v-for="linkShop in shop.link">
                                {{ linkShop }}
                            </li>
                        </ul>
                    </ul>
                </div>
                <div class="logo">
                    <img src="/img/dc-logo-bg.png" alt="logo-big">
                </div>
            </div>
        </div>
        <div class="section-sign-up">
            <div class="container">
                <div class="row">
                    <div class="col-button">
                        Sign-up Now!
                    </div>
                    <div class="col-icon">
                        <div class="text">
                            Follow us
                        </div>
                        <ul class="icon-list">
                            <li v-for="icon in arrayIcon">
                                <img :src="icon" alt="icon">
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </footer>

</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;


footer {
    color: white;
    .section-link {
        background-image: url(/img/footer-bg.jpg);
        background-size: cover;
        padding: -10px;
        overflow: hidden;

        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;

            img{
                margin: -50px;
            }

            .link{
                display: flex;
                gap: 25px;

                .title{
                    padding-bottom: 20px;
                    text-transform: uppercase;
                }

                li{
                    font-size: 10px;
                    padding-bottom: 8px;
                    color: gray;
                }

                .shopUl{
                    padding-top: 25px
                }
            }
        }
    }

    .section-sign-up {
        background-color: $gray-dark;
        padding: 29px;

        .row{
            display: flex;
            justify-content: space-between;
            align-items: center;
            text-transform: uppercase;

            .col-button{
                border: 2px solid $blue;
                padding: 15px;
            }

            .col-icon{
                display: flex;
                align-items: center;
                gap: 26px;

                .text{
                    color: $blue;
                    font-weight: bold;
                }

                .icon-list{
                    display: flex;
                    gap: 18px;
                }
            }
        }
    }
 
}

</style>