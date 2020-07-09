<template>
    <section class="hosting">
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <h2>Linux Hosting yang Stabil dengan Teknologi LVE</h2>
                    <p>SuperMicro <b>Intel Xeon 24-Cores</b> server dengan RAM <b>128 GB</b> dan teknologi <b>LVE CloudLinux</b> untuk stabilitas server Anda. Dilengkapi dengan <b>SSD</b> untuk kecepatan <b>MySQL</b> dan caching, Apache load balancer berbasis LiteSpeed Technologies, <b>CageFS</b> security, <b>Raind-10</b> protection dan auto backup untuk keamanan website PHP Anda.</p>
                    <a href="#">Pilih Hosting Anda</a>
                </div>
                <div class="col-md-6 align-self-end">
                    <img src="@/assets/image/image-support.png" alt="" class="img-fluid">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Hosting'
}
</script>

<style lang="scss">
.hosting {
    h2 {
        font-weight: 200;
        margin-bottom: 20px;
    }
    p {
        font-weight: 200;
        margin-bottom: 2rem;

        b {
            font-weight: bold;
        }
    }
    a {
        @extend .main-btn;
        margin-bottom: 3rem;
    }
}
</style>