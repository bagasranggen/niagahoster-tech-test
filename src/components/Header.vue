<template>
    <section class="header">
        <div class="container">
            <div class="header__bookmark">
                <a href="#">
                    <img class="img-fluid" src="@/assets/icon/bookmark.png" alt="">
                    <span class="d-none d-lg-inline">Gratis Ebook 9 Cara Cerdas Menggunakan Domain [ x ]</span>
                </a>
            </div>
            <div class="header__account">
                <ul>
                    <li v-for="(account, index) in accounts" :key="index">
                        <a :href="account.link" v-html="account.text"></a>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            accounts: [
                {link: 'tel: 622745305505', text: '<i class="fas fa-phone"></i><span class="d-none d-md-inline">0274-5305505</span>'},
                {link: '#', text: '<i class="fas fa-comments"></i><span class="d-none d-md-inline">Live Chat</span>'},
                {link: '#', text: '<i class="fas fa-user-circle"></i><span class="d-none d-md-inline">Member Area</span>'}
            ]
        }
    }
}
</script>

<style lang="scss">
.header {
    height: 45px;
    
    > .container {
        display: flex;
        justify-content: space-between;
        height: 100%;
    }

    &__bookmark {
        font-size: 12px;

        a {
            color: #4c4c4c;

            &:hover {
                text-decoration: none;
            }
        }


        img {
            margin-right: 10px;
        }
    }

    &__account {
        align-self: center;
        ul {
            margin-bottom: 0;
        }

        li {
            display: inline-flex;
            align-items: center;
            margin-left: 20px;
            font-size: 12px;

            a {
                color: #4c4c4c;

                &:hover {
                    text-decoration: none;
                    color: $blue;
                }
            }

            i {
                margin-right: 15px;
                font-size: 16px;
            }
        }
    }
}
</style>