<template>
    <section>
        <section class="contact">
            <div class="container">
                <div class="row">
                    <div class="col-6">
                        Bagikan jika Anda menyukai halaman ini.
                    </div>
                    <div class="col-6">
                        <ul class="contact__social">
                            <li>
                                <i class="fab fa-facebook-square"></i>
                                <div>80k</div>
                            </li>
                            <li>
                                <i class="fab fa-twitter-square"></i>
                                <div>450</div>
                            </li>
                            <li>
                                <i class="fab fa-google-plus-square"></i>
                                <div>1900</div>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
        <section class="help">
            <div class="container">
                <h2>Perlu <span>Bantuan?</span> Hubungi Kami: <span>0274-5305505</span></h2>
                <a href="#"><i class="fas fa-comments"></i> Live Chat</a>
            </div>
        </section>
    </section>
</template>

<script>
export default {
    name: 'Contact'
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
            display: inline-flex;
            align-items: center;
            margin-right: 10px;

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

            > i {
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
    }

    a {
        @extend %main-btn;
        padding-bottom: 7px;
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