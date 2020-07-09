<template>
    <section class="bundling">
        <div class="container">
            <h2>Semua Paket Hosting Sudah Termasuk</h2>
            <div class="row bundling__item">
                <div class="col-sm-6 col-md-4" v-for="(bundling, index) in bundlings" :key="index">
                    <img class="img-fluid" :src="`/assets/image/${bundling.img}`" alt="">
                    <h5>{{ bundling.title }}</h5>
                    <p v-html="bundling.content"></p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Bundling',
    data() {
        return {
            bundlings: [
                {
                    title: 'PHP Semua Versi',
                    img: 'all-version.svg',
                    content: 'Pilih mulai dari versi PHP 5.4 s/d PHP 7. Ubah Sesuka Anda!'
                },
                {
                    title: 'MySQL Versi 5.6',
                    img: 'mysql-5.6.svg',
                    content: 'Nikmati MySQL versi terbaru, tercepat dan kaya akan fitur.'
                },
                {
                    title: 'Panel Hostin cPanel',
                    img: 'cpanel.svg',
                    content: 'Kelola website dengan panel canggih yang familiar di hati anda.'
                },
                {
                    title: 'Garansi Uptime 99.9%',
                    img: 'garansi.svg',
                    content: 'Data center yang mendukung kelangsungan website Anda 24/7.'
                },
                {
                    title: 'Database InnoDB Unlimited',
                    img: 'innodb.svg',
                    content: 'Jumlah dan ukuran database yang tumbuh sesuai dengan kebutuhan Anda.'
                },
                {
                    title: 'Wildcard Remote MySQL',
                    img: 'wildcard.svg',
                    content: 'Mendukung s/d 25 max_user_connections dan 100 max_connection.'
                },
            ]
        }
    }
}
</script>

<style lang="scss">
.bundling {
    @extend %small-divider;
    margin-bottom: 40px;

    .container {
        @extend .text-center;

        h2 {
            font-weight: 200;
        }
    }

    &__item {
        padding-bottom: 25px;

        > div {
            margin-top: 60px;
            margin-bottom: 10px;

            img {
                width: 80px;
                height: 70px;
                object-fit: contain;
                margin-bottom: 20px;
            }
            h5 {
                @extend %montserrat;
                margin-bottom: 0;
                font-weight: bold;
            }
        }
    }
}
</style>