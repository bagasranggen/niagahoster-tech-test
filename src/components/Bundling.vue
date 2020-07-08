<template>
    <section class="bundling">
        <div class="container">
            <h2>Semua Paket Hosting Sudah Termasuk</h2>
            <div class="row bundling__item">
                <div class="col-md-4">
                    <img class="img-fluid" src="@/assets/icon/all-version.svg" alt="">
                    <h5>PHP Semua Versi</h5>
                    <p>Pilih mulai dari versi PHP 5.4 s/d PHP 7. Ubah Sesuka Anda!</p>
                </div>
                <div class="col-md-4">
                    <img class="img-fluid" src="@/assets/icon/all-version.svg" alt="">
                    <h5>PHP Semua Versi</h5>
                    <p>Pilih mulai dari versi PHP 5.4 s/d PHP 7. Ubah Sesuka Anda!</p>
                </div>
                <div class="col-md-4">
                    <img class="img-fluid" src="@/assets/icon/all-version.svg" alt="">
                    <h5>PHP Semua Versi</h5>
                    <p>Pilih mulai dari versi PHP 5.4 s/d PHP 7. Ubah Sesuka Anda!</p>
                </div>
                <div class="col-md-4">
                    <img class="img-fluid" src="@/assets/icon/all-version.svg" alt="">
                    <h5>PHP Semua Versi</h5>
                    <p>Pilih mulai dari versi PHP 5.4 s/d PHP 7. Ubah Sesuka Anda!</p>
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
    }

    &__item {
        > div {
            margin-top: 60px;
            margin-bottom: 10px;

            img {
                width: 60px;
                height: 50px;
                object-fit: contain;
                margin-bottom: 20px;
            }
            h5 {
                margin-bottom: 0;
                font-weight: bold;
            }
        }
    }
}
</style>