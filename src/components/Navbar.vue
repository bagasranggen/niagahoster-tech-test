<template>
    <section class="main-navbar">
        <div class="container">
            <nav class="navbar navbar-expand-xl navbar-light">
                <a class="navbar-brand" href="/"><img src="@/assets/icon/niagahoster.png" alt="" class="img-fluid"></a>
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#collapsible-navbar" aria-controls="collapsible-navbar" aria-expanded="false" aria-label="Toggle navigation" @click="toggleNavbar">
                    <span class="navbar-toggler-icon"></span>
                </button>

                <div :class="['navbar-collapse', show ? 'collapsed' : 'collapse']" id="collapsible-navbar">
                    <ul class="navbar-nav ml-auto text-center">
                        <li class="nav-item" v-for="(link, index) in links" :key="index">
                            <a class="nav-link" href="#">{{link}}</a>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Navbar',
    data() {
        return {
            show: false,
            links: ['Hosting', 'Domain', 'Server', 'Website', 'Afiliasi', 'Promo', 'Pembayaran', 'Review', 'Kontak', 'Blog']
        }
    },
    methods: {
        toggleNavbar() {
            this.show = !this.show
        }
    }
}
</script>

<style lang="scss">
.main-navbar {
    @extend %main-separator;

    .navbar {
        @extend .p-0;

        &-brand {
            margin-top: 10px;
            margin-bottom: 10px;

            img {
                min-width: 230px;
                max-width: 230px;
                height: 50px;
                object-fit: contain;

                @media (max-width: 320px) {                    
                    min-width: 150px;
                    max-width: 150px;
                }
            }
        }
    }

    .navbar-nav {
        li {
             .nav-link {
                padding-left: 30px;
                padding-right: 0;

                &:hover {
                    color: $blue;
                }
             }
        }
    }
}
</style>