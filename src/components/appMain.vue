<script>
export default {
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
            cards: [
        {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book"
        },
        {
          thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book"
        },
        {
          thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel"
        },
        {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book"
        },
        {
          thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book"
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book"
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book"
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book"
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book"
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book"
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book"
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel"
        }
      ] 
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
                        <div class="col-2 p-3" v-for="card, index in cards">
                            <img :src="card.thumb" alt="" class="img-card">
                            <h6 class="text-white text-uppercase mt-2">{{ card.series }}</h6>
                        </div> 
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

.img-card {
    width: 100%;
    height: 250px;
    object-fit: cover;
    object-position: top;
}

.p-abs {
    position: absolute;
    bottom: -20px;
}
</style>
