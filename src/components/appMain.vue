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
            ]
        }
    }
}
</script>

<template>
    <main>
        <div class="container-fluid">
            <div class="row">
                <div class="col-12 bg-black">
                    <div class="content py-4 align-items-center">
                        <h1 class="text-white fs-3">-> Content goes here <--</h1>
                    </div>
                </div>
                <div class="col-12 bg-blue">
                    <div class="content justify-content-center py-4">
                        <ul class="d-flex align-items-center list-unstyled m-0 p-0">
                            <li v-for="item in exploreDC" :key="item.name" class="mx-3 d-flex align-items-center">
                                <img :src="item.img" alt="" class="img-fluid me-2">
                                <a :href="item.url" class="text-decoration-none text-white">{{ item.name }}</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<style scoped>
.content {
    width: 90%;
    margin: 0 auto;
    display: flex;
}

.bg-blue {
    background-color: #0282F9;
}

.content img {
    height: 30px;
    width: auto;
}
</style>
