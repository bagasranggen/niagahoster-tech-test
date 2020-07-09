<template>
    <section class="support">
        <div class="container">
            <h2>Mendukung Penuh Framework Laravel</h2>
            <div class="row">
                <div class="col-md-6">
                    <h5>Tak perlu menggunakan dedicated server ataupun VPS yang mahal. Layanan PHP hosting murah kami mendukung penuh framework favorit Anda.</h5>
                    <ul class="headline__list">
                        <li v-for="(support, index) in supports" :key="index" v-html="support"></li>
                    </ul>
                    <small>Nb. Composer dan SSH hanya tersedia pada paket Personal dan Bisnis</small>
                    <a href="#">Pilih Hosting Anda</a>
                </div>
                <div class="col-md-6">
                    <img src="@/assets/icon/laravel.svg" alt="" class="img-fluid">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Support',
    data() {
        return {
            supports: [
                'Install Laravel <b>1 klik</b> dengan Softaculous Installer.',
                'Mendukung ekstensi <b>PHP Mcript, phar, mbstring, json, </b>dan <b>fileinfo</b>',
                'Tersedia <b>Composer</b> dan <b>SSH</b> untuk menginstal packages pilihan Anda.'
            ]
        }
    }
}
</script>

<style lang="scss">
.support {
    @extend %main-separator--bottom;
    margin-bottom: 70px;
    
    .container {
        h2 {
            @extend .text-center;
            font-weight: 200;
            margin-bottom: 20px;
        }
        h5 {
            font-weight: 200;
            line-height: 30px;
            margin-bottom: 20px;
        }
        a {
            @extend .main-btn--blue;
            margin-top: 20px;
            margin-bottom: 30px;
        }
    }
}
</style>