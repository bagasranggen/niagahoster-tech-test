<template>
    <section class="features">
        <div class="container">
            <div class="offset-md-1 col-md-10">
                <div class="row">
                    <div class="col-md-4 features__item" v-for="(feature, index) in features" :key="index">
                        <img :src="`/assets/image/${feature.img}`" :alt="feature.name">
                        <h6>{{ feature.name }}</h6>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Features',
    data() {
        return {
            features: [
                {name: 'PHP Zen Guard Loader', img: 'feature-1.png'},
                {name: 'PHP Composer', img: 'feature-2.png'},
                {name: 'PHP ionCube Loader', img: 'feature-3.png'},
            ]
        }
    }
}
</script>

<style lang="scss">
.features {
    margin-top: 50px;
    margin-bottom: 80px;

    &__item {
        @extend .text-center;

        img {
            @extend .img-fluid;
            width: 210px;
            height: 170px;
            margin-bottom: 15px;
            object-fit: contain;
        }
    }
}

</style>