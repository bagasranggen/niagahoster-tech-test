<template>
    <section class="footer">
        <div class="container">
            <div class="row">
                <div :class="(footer.social || footer.normal) ? 'col-md-6 col-lg-3' : 'col-6 col-md-3'" v-for="(footer, index) in footers" :key="index">
                    <h5 :class="footer.social ? 'd-none d-md-block' : null" v-html="footer.title"></h5>
                    <ul :class="['list-unstyled', footer.social ? 'footer__social text-center text-md-left' : null]">
                        <li v-for="(list, index) in footer.lists" :key="index" :class="footer.normal ? 'text--normal' : null"><a href="#" v-html="list" :class="(footer.address || footer.normal) ? 'disabled' : null"></a></li>
                    </ul>
                </div>
            </div>
            <div class="row footer__payment">
                <div class="col">
                    <h5>Pembayaran</h5>
                    <ul class="list-unstyled payment__item">
                        <li v-for="(payment, index) in payments" :key="index">
                            <a :href="payment.link">
                                <img class="img-fluid" :src="`/assets/image/payment/${payment.img}`" :alt="payment.name">
                            </a>
                        </li>
                    </ul>
                    <p>Aktivasi instan dengan e-Payment Hosting dan domain langsung aktif!</p>
                </div>
            </div>
            <div class="row justify-content-between footer__links">
                <div class="col-12 col-md-auto order-2 order-md-1 pt-2 pb-0">
                    <p>Copyright &copy;2016 Niagahoster | Hosting poered by PHP7, CloudLinux, CloudFlare, BitNinja and DC Biznet Technovillage Jakarta</p>
                    <p>Cloud VPS Murah by Webuzo Softaculous, Intel SSD and cloud computing technology</p>
                </div>
                <div class="col text-center text-md-right order-1 order-md-2 pt-2 pb-0">
                    <ul class="list-inline">
                        <li class="list-inline-item" v-for="(link, index) in links" :key="index">
                            <a :href="link.link">{{link.text}}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Footer',
    data() {
        return {
            footers: [
                {
                    title: 'hubungi kami',
                    address: true,
                    lists: ['0274-53005505', 'senin - minggu', '24 jam nonstop', '<br/>', 'jl. selokan mataram monjali karangjati MT I/304 sinduadi, mlati, sleman, yogyakarta 55284']
                },
                {
                    title: 'layanan',
                    lists: ['domain', 'shared hosting', 'cloud VPS hosting', 'managed VPS hosting', 'web builder', 'keamanan SSL / HTTPS', 'jasa pembuatan website', 'program afiliasi']
                },
                {
                    title: 'service hosting',
                    lists: ['hosting murah', 'hosting indonesia', 'hosting singapura SG', 'hosting PHP', 'hosting wordpress', 'hosting laravel']
                },
                {
                    title: 'tutorial',
                    lists: ['knowledgebase', 'blog', 'cara pembayaran']
                },
                {
                    title: 'tentang kami',
                    lists: ['tim niagahoster', 'karir', 'events', 'penawaran & promo special', 'kontak kami']
                },
                {
                    title: 'kenapa pilih niagahoster?',
                    lists: ['support terbaik', 'garansi harga termurah', 'domain gratis selamanya', 'datacenter hosting terbaik', 'review pelanggan']
                },
                {
                    title: 'newsletter',
                    normal: true,
                    lists: ['<div class="footer__subscribe"><input type="email" class="form-control" placeholder="Email"><button class="btn btn-light">Berlangganan</button></div>', 'Dapatkan promo dan konten menarik dari penyedia hosting terbaik Anda.']
                },
                {
                    title: '<br />',
                    social: true,
                    lists: [
                        '<a href="#"><i class="fab fa-facebook-f"></i></a>',
                        '<a href="#"><i class="fab fa-twitter"></i></a>',
                        '<a href="#"><i class="fab fa-google-plus-g"></i></a>',
                        ]
                },
            ],
            payments: [
                {
                    name: 'bca',
                    link: '#',
                    img : 'bca.png'
                },
                {
                    name: 'mandiri clickpay',
                    link: '#',
                    img : 'mandiri-click.png'
                },
                {
                    name: 'bni',
                    link: '#',
                    img : 'bni.png'
                },
                {
                    name: 'visa',
                    link: '#',
                    img : 'visa.png'
                },
                {
                    name: 'mastercard',
                    link: '#',
                    img : 'mastercard.png'
                },
                {
                    name: 'atm-bersama',
                    link: '#',
                    img : 'atm-bersama.png'
                },
                {
                    name: 'permata',
                    link: '#',
                    img : 'permata.png'
                },
                {
                    name: 'prima',
                    link: '#',
                    img : 'prima.png'
                },
                {
                    name: 'alto',
                    link: '#',
                    img : 'alto.png'
                },
            ],
            links: [
                {
                    link: '#',
                    text: 'Syarat dan Ketentuan'
                },
                {
                    link: '#',
                    text: 'Kebijakan Privasi'
                },
            ]
        }
    }
}
</script>

<style lang="scss">
.footer {
    background-color: #303030;
    color: #d8d8d8;
    padding-top: 30px;
    padding-bottom: 30px;

    h5 {
        @extend %montserrat;
        font-size: 14px;
        font-weight: bold;
        color: #888;
        margin-bottom: 30px;
        text-transform: uppercase;
    }

    .list-unstyled {
        li {
            font-size: 14px;
            text-transform: capitalize;
            margin-bottom: 8px;

            a {
                color: #d8d8d8;

                &:hover {
                    text-decoration: none;
                    color: $blue;
                }

                &.disabled {
                    pointer-events: none;
                    cursor: text;
                }
            }

            &.text--normal {
                text-transform: initial;
            }
        }
        &.footer__social {
            li {
                display: inline-block;
                margin-right: 35px;

                a {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    width: 50px;
                    height: 50px;
                    border: solid 2px #d9d9d9;
                    color: #d9d9d9;
                    border-radius: 100%;
                    font-size: 20px;

                    &:hover {
                        text-decoration: none;
                        color: $blue;
                        border-color: $blue;
                    }
                }

                @include media-breakpoint-down(md) {
                    &:last-child {
                        margin-right: 0;
                    }
                }
            }
        }
    }

    > .container {
        > .row > div {
            padding-top: 30px;
            padding-bottom: 10px;
        }
    }

    &__subscribe {
        position: relative;

        input {
            height: 50px;
            margin-bottom: 10px;
            border-radius: 35px;
            padding-right: 110px;

            &::placeholder {
                color: #a7aaab;
            }
        }

        button {
            @extend .main-btn--blue;
            padding: 0 10px;
            font-size: 12px;
            font-weight: 100;
            min-width: unset;
            height: calc(100% - 10px);
            position: absolute;
            right: 7px;
            top: 50%;
            transform: translateY(-50%);
        }
    }

    &__payment {
        border-bottom: solid 2px #292929;
        p {
            color: #787878;
            font-size: 13px;
        }

        .payment__item {
            li {
                display: inline-block;
                margin-right: 20px;
    
                a {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    width: 85px;
                    height: 40px;
                    border: solid 1px #e2e2e2;
                    border-radius: 8px;
                    padding: 5px;
    
                    &:hover {
                        text-decoration: none;
                        border-color: $blue;
                    }
    
                    img {
                        width: 100%;
                        height: 100%;
                        object-fit: contain;
                    }
                }

                @include media-breakpoint-down(sm) {
                    margin-right: 10px;
                }

                @include media-breakpoint-down(xs) {
                    margin-right: 0;
                    width: 33.33%;

                    a {
                        width: 100%;
                        height: 55px;
                    }
                }
            }
        }
    }

    &__links {
        font-size: 13px;

        .list-inline {
            li {
                padding-left: 10px;
                padding-right: 10px;
                margin: 0;

                &:first-child {
                    border-right: solid 1px #d8d8d8;
                }
            }
        }
        p {
            margin-bottom: 5px;
        }
        a {
            color: #d8d8d8;

            &:hover {
                text-decoration: none;
                color: $blue;
            }
        }
    }
}
</style>