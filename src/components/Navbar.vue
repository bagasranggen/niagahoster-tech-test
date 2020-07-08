<template>
    <section class="main-navbar">
        <div class="container">
            <nav class="navbar navbar-expand-lg navbar-light">
                <a class="navbar-brand" href="/"><img src="@/assets/icon/niagahoster.png" alt="" class="img-fluid"></a>
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>

                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav ml-auto">
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
            links: ['Hosting', 'Domain', 'Server', 'Website', 'Afiliasi', 'Promo', 'Pembayaran', 'Review', 'Kontak', 'Blog']
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
            }
        }
    }

    .navbar-nav {
        li {
             .nav-link {
                padding-left: 30px;
                padding-right: 0;
             }
        }
    }
}
</style>