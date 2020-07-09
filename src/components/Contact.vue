<template>
    <section>
        <section class="contact">
            <div class="container">
                <div class="row text-center text-md-left">
                    <div class="col-md-6 mb-3 mb-md-0">
                        <b>Bagikan jika Anda menyukai halaman ini.</b>
                    </div>
                    <div class="col-md-6">
                        <ul class="contact__social pl-0 pl-md-3">
                            <li v-for="(social, index) in socials" :key="index">
                                <a :href="social.link">
                                    <i :class="social.text"></i>
                                    <div>{{social.total}}</div>
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
        <section class="help">
            <div class="container text-center text-md-left">
                <h2>Perlu <span>Bantuan?</span> Hubungi Kami: <span>0274-5305505</span></h2>
                <a class="mt-3 mt-md-0" href="#"><i class="fas fa-comments"></i> Live Chat</a>
            </div>
        </section>
    </section>
</template>

<script>
export default {
    name: 'Contact',
    data() {
        return {
            socials: [
                {text: 'fab fa-facebook-square', total: '80k', link: '#'},
                {text: 'fab fa-twitter-square', total: '450', link: '#'},
                {text: 'fab fa-google-plus-square', total: '1900', link: '#'},
            ]
        }
    }
}
</script>

<style lang="scss">
.contact {
    background-color: #f1f1f1;
    padding-top: 25px;
    padding-bottom: 20px;

    &__social {
        margin-bottom: 0;

        > li {
            display: inline-block;

            a {
                display: inline-flex;
                margin-right: 10px;
                align-items: center;

                &:hover {
                    text-decoration: none;

                    > div {
                        color: $blue;
                        border-color: $blue;

                        &::before {
                            background-color: $blue;
                        }
                    }
                }
                
                > div {
                    border: solid 1px #cdcdcd;
                    color: #cdcdcd;
                    margin-left: 5px;
                    padding: 1px 5px;
                    min-width: 60px;
                    text-align: center;
                    border-radius: 4px;
                    position: relative;

                    &::after,
                    &::before {
                        content: '';
                        position: absolute;
                        top: 50%;
                        transform: translateY(-50%) rotate(45deg);
                        border-radius: 1px;
                    }

                    &::after {
                        width: 6px;
                        height: 6px;
                        left: -2.8px;
                        background-color: #f1f1f1;
                    }

                    &::before {
                        width: 6px;
                        height: 6px;
                        left: -4px;
                        background-color: #cdcdcd;
                    }
                }
            }


            i {
                font-size: 30px;

                &.fa-facebook-square {
                    color: #23599b;
                }
                &.fa-twitter-square {
                    color: #00aef1;
                }
                &.fa-google-plus-square {
                    color: #fc4a35;
                }
            }
        }
    }
}

.help {
    background-color: #00a2f3;
    color: #fff;
    padding-top: 60px;
    padding-bottom: 50px;

    h2 {
        display: inline-block;
        margin-right: 100px;
        font-weight: 100;

        > span {
            font-weight: bold;
        }

        @include media-breakpoint-down(md) {
            margin-right: 0;
        }
    }

    a {
        @extend .main-btn--blue;
        font-size: 20px;
        background-color: #00a2f3;
        border-color: #fff;
        color: #fff;
        min-width: 170px;

        &:hover {
            text-decoration: none;
        }
    }
}
</style>