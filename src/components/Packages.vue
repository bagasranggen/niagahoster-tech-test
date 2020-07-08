<template>
    <section class="packages">
        <div class="container">
            <h2>Paket Singapura</h2>
            <h3>Diskon</h3>
            <div class="row packages__list">
                <div class="col-md-3" v-for="(pack, index) in splittedPackages" :key="index">
                    <div :class="(pack.best) ? 'list__item--best-seller' : 'list__item'">
                        <div v-if="pack.best" class="item__best"><span>Best Seller!</span></div>
                        <h4>{{pack.title}}</h4>
                        <div class="item__price">
                            <p>Rp {{pack.normal_price}}</p>
                            <div class="price__discount">
                                <span>Rp</span>
                                <span v-for="(special,index) in pack.special_price" :key="index">{{special}}</span>
                                <span>/bln</span>
                            </div>
                        </div>
                        <div class="item__user">
                            <span>{{pack.user}}</span><span> Pengguna Terdaftar</span>
                        </div>
                        <div class="item__content">
                            <ul>
                                <li v-for="(feature, index) in pack.features" :key="index">
                                    <span v-for="(list, index) in feature" :key="index">{{list}}</span>
                                </li>
                            </ul>
                            <a href="#">Pilih Sekarang</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Packages',
    data() {
        return {
            testing: [],
            packages: [
                {   
                    best: false,
                    title: 'Bayi',
                    normal_price: '19.000',
                    special_price: '14.900',
                    users: '938',
                    features: [
                        ['0.5X RESOURCES POWER'],
                        ['500 MB', ' ','DISK SPACE'],
                    ]
                },
                {   
                    best: false,
                    title: 'Bayi',
                    normal_price: '19.000',
                    special_price: '14.900',
                    users: '938',
                    features: [
                        ['0.5X RESOURCES POWER'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                    ]
                },
                {   
                    best: true,
                    title: 'Bayi',
                    normal_price: '19.000',
                    special_price: '14.900',
                    users: '938',
                    features: [
                        ['0.5X RESOURCES POWER'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                    ]
                },
                {   
                    best: false,
                    title: 'Bayi',
                    normal_price: '19.000',
                    special_price: '14.900',
                    users: '938',
                    features: [
                        ['0.5X RESOURCES POWER'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                        ['500 MB', ' ','DISK SPACE'],
                    ]
                },
            ]
        }
    },
    computed: {
        splittedPackages() {
            let newArr = [...this.packages]
            newArr.map(el => {
                return el.special_price = el.special_price.split('.')
            })
            return newArr
        }
    }
}
</script>

<style lang="scss">
.packages {
    @extend .text-center;

    h2 {
        font-size: 36px;
        font-weight: bold;
        margin-bottom: 5px;
    }
    h3 {
        font-size: 26px;
        font-weight: 100;
        margin-bottom: 0;
    }

    &__list {
        margin-top: 75px;
        margin-bottom: 100px;

        > div {
            padding: 0;
        }

        .list__item {
            border: solid 1px #f1f1f1;

            h4 {
                @extend %border-bottom--light;
                font-weight: bold;
                margin-bottom: 0;
                padding: 12px;
            }

            .item {
                &__price {
                    @extend %packages-main-padding, %border-bottom--light;
                    
                    p {
                        text-decoration: line-through;
                        font-weight: 100;
                        margin-bottom: 5px;
                    }

                    .price {
                        &__discount {
                            display: flex;
                            justify-content: center;
                            align-items: flex-start;

                            > span:nth-child(2) {
                                font-size: 40px;
                                font-weight: bold;
                                line-height: 1;
                            }
                        }

                    }
                }

                &__user {
                    @extend %packages-main-padding, %border-bottom--light;

                    > span:first-child {
                        font-weight: bold;
                    }
                }

                &__content {
                    @extend %packages-main-content-padding;

                    > ul {
                        list-style: none;
                        padding: 0;
                        margin-bottom: 30px;

                        > li:first-child {
                            font-weight: bold;
                        }

                        >li:not(:first-child) > span:first-child {
                            font-weight: bold;
                        }

                    }

                    > a {
                        @extend %main-btn;
                        border-color: #4c4c4c;
                        color: #4c4c4c;
                        font-weight: bold;
                        padding-bottom: 7px;

                        &:hover {
                            text-decoration: none;
                            background-color: $blue;
                            border-color: $blue;
                            color: #fff;
                        }
                    }
                }
            }

            &--best-seller {
                @extend .list__item;
                border-color: $blue;

                h4 {
                    color: #fff;
                    background-color: $blue;
                    border-color: $blue;
                }

                .item {
                    &__best {
                        width: 120px;
                        height: 120px;
                        top: -10px;
                        left: -10px;
                        overflow: hidden;
                        position: absolute;

                        &::after,
                        &::before {
                            position: absolute;
                            z-index: -1;
                            content: '';
                            display: block;
                            border: 5px solid #00b359;
                            border-top-color: transparent;
                            border-left-color: transparent;
                        }

                        &::before {
                            top: 0;
                            right: 0;
                        }

                        &::after {
                            bottom: 0;
                            left: 0;
                        }

                        > span {
                            position: absolute;
                            display: block;
                            width: 225px;
                            padding: 8px 0 10px;
                            background-color: #00b359;
                            box-shadow: 0 5px 10px rgba(0,0,0,.1);
                            color: #fff;
                            font-size: 16px;
                            text-shadow: 0 1px 1px rgba(0,0,0,.2);
                            text-transform: uppercase;
                            text-align: center;
                            right: -25px;
                            top: 38px;
                            transform: rotate(-45deg) translateX(19px);
                        }
                    }
                    &__price {
                        color: #fff;
                        background-color: $blue;
                        border-color: $blue;
                    }
                    &__user {
                        background-color: $d-blue;
                        color: #fff;
                    }
                    &__content {
                        a {
                            background-color: $blue;
                            border-color: $blue;
                            color: #fff;
                        }
                    }

                }
            }

        }

    }
}
</style>