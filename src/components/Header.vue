<template>
    <section class="header">
        <div class="container">
            <div class="header__bookmark">
                <img class="img-fluid" src="@/assets/icon/bookmark.png" alt="">
                Gratis
            </div>
            <div class="header__account">
                <ul>
                    <li>
                        <i class="fas fa-phone"></i> 0274-5305505
                    </li>
                    <li>
                        <i class="fas fa-comments"></i>Live Chat
                    </li>
                    <li>
                        <i class="fas fa-user-circle"></i> Member Area
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Header'
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

            i {
                margin-right: 15px;
                font-size: 16px;
            }
        }
    }
}
</style>