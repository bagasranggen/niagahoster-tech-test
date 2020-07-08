<template>
    <section class="module">
        <div class="container">
            <h2>Modul Lengkap Untuk Menjalankan Aplikasi PHP Anda</h2>
            <div class="row">
                <div class="offset-md-1 col-md-10">
                    <div class="row">
                        <div class="col-md-3">
                            test
                        </div>
                        <div class="col-md-3">
                            test
                        </div>
                        <div class="col-md-3">
                            test
                        </div>
                        <div class="col-md-3">
                            test
                        </div>
                    </div>
                </div>
            </div>
            <div class="text-center">
                <a href="#">Selengkapnya</a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Module'
}
</script>

<style lang="scss">
.module {
    margin-bottom: 100px;

    .container {
        h2 {
            @extend .text-center;
            margin-bottom: 50px;
        }

        > .row {
            margin-bottom: 50px;
        }
    
        a {
            @extend %main-btn, .text-center;
            border-color: #4c4c4c;
            color: #4c4c4c;
            padding-bottom: 7px;
        }
    }
}
</style>