<template>
    <section class="support">
        <div class="container">
            <h2>Mendukung Penuh Framework Laravel</h2>
            <div class="row">
                <div class="col-md-6">
                    TEST
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
}
</script>

<style lang="scss">
.support {
    @extend %main-separator--bottom;
    margin-bottom: 70px;
    
    .container {
        h2 {
            @extend .text-center;
        }
    }
}
</style>