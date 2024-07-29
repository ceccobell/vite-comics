<script>
export default {
    data() {
        return {
            menuItems: [
                {
                    name: 'CHARACTERS',
                    url: '#',
                    active: false
                },
                {
                    name: 'COMICS',
                    url: '#',
                    active: true
                },
                {
                    name: 'MOVIES',
                    url: '#',
                    active: false
                },
                {
                    name: 'TV',
                    url: '#',
                    active: false
                },
                {
                    name: 'GAMES',
                    url: '#',
                    active: false
                },
                {
                    name: 'COLLECTIBLES',
                    url: '#',
                    active: false
                },
                {
                    name: 'VIDEOS',
                    url: '#',
                    active: false
                },
                {
                    name: 'FANS',
                    url: '#',
                    active: false
                },
                {
                    name: 'NEWS',
                    url: '#',
                    active: false
                },
                {
                    name: 'SHOP',
                    url: '#',
                    active: false
                }
            ]
        }
    },
    methods: {
        setActive(selectedItem) {
            this.menuItems.forEach(item => {
                if (item.active) {
                    item.active = false
                }
            })
            selectedItem.active = true
        }
    }
}
</script>

<template>
    <header>
        <div class="container-fluid">
            <div class="row">
                <div class="col-12 p-2">
                    <div class="content justify-content-between align-items-center">
                        <img src="/public/img/dc-logo.png" alt="" class="img-fluid">
                        <div class="h-100">
                            <ul class="d-flex align-items-center list-unstyled h-100">
                                <li v-for="item, index in menuItems" :key="index">
                                    <a @click="setActive(item)" :href="item.url" :class="item.active ? 'active' : ''" class="text-decoration-none text-black me-3">{{ item.name }}</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<style scoped>
.h-100 {
    height: 100%;
}
.active {
    color: #0282F9 !important;
    border-bottom: 3px solid #0282F9;
}

.content {
    width: 90%;
    margin: 0 auto;
    display: flex;
}

</style>
