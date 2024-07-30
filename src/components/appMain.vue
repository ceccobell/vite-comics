<script>
import cards from './cards.vue';
import cardsData from '../assets/dc-comics.json'; 

export default {
    components: {
        cards
    },
    data() {
        return {
            exploreDC: [
                {
                    name: 'DIGITAL COMICS',
                    img: '/public/img/buy-comics-digital-comics.png',
                    url: '#',
                    active: false
                },
                {
                    name: 'DC MERCHANDISE',
                    img: '/public/img/buy-comics-merchandise.png',
                    url: '#',
                    active: false
                },
                {
                    name: 'SUBSCRIPTION',
                    img: '/public/img/buy-comics-subscriptions.png',
                    url: '#',
                    active: false
                },
                {
                    name: 'COMIC SHOP LOCATOR',
                    img: '/public/img/buy-comics-shop-locator.png',
                    url: '#',
                    active: false
                },
                {
                    name: 'DC POWER VISA',
                    img: '/public/img/buy-dc-power-visa.svg',
                    url: '#',
                    active: false
                }
            ],
            cardsData
        }
    }
}
</script>

<template>
    <main>
        <div class="container-fluid">
            <div class="row">
                <div class="col-12 h-300 position-relative">
                    <img src="/public/img/jumbotron.jpg" alt="" class="jumbotron">
                    <div class="content">
                        <span class="text-white py-2 px-3 bg-blue p-abs fw-semibold">CURRENT SERIES</span>
                    </div>
                </div>
                <div class="row bg-black">
                    <div class="content d-flex flex-wrap py-3">
                        <!-- <div class="col-2 p-3" v-for="card, index in cards">
                            <img :src="card.thumb" alt="" class="img-card">
                            <h6 class="text-white text-uppercase mt-2">{{ card.series }}</h6>
                        </div> --> 
                        <cards :cards="cardsData" />
                        <div class="col-12 text-center mb-2">
                            <span class="text-white py-2 px-5 bg-blue">LOAD MORE</span>
                        </div>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12 bg-blue">
                        <div class="content justify-content-center py-4">
                            <ul class="d-flex align-items-center list-unstyled m-0 p-0">
                                <li v-for="item in exploreDC" :key="item.name" class="mx-3 d-flex align-items-center">
                                    <img :src="item.img" alt="" class="img-fluid icon me-2">
                                    <a :href="item.url" class="text-decoration-none text-white">{{ item.name }}</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.content {
    width: 90%;
    margin: 0 auto;
    display: flex;
}

.bg-blue {
    background-color: #0282F9;
}

.icon {
    height: 30px;
    width: auto;
}

.h-300 {
    height: 300px;
}

.jumbotron {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top;
}

.p-abs {
    position: absolute;
    bottom: -20px;
}
</style>
