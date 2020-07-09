<template>
    <section class="module">
        <div class="container">
            <h2>Modul Lengkap Untuk Menjalankan Aplikasi PHP Anda</h2>
            <div class="row">
                <div class="offset-md-1 col-md-10">
                    <div class="row">
                        <div class="col-6 col-md-3" v-for="(mod, index) in modules" :key="index">
                            <div v-for="(list,index) in mod" :key="index">{{list}}</div>
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
    name: 'Module',
    data() {
        return {
            modules: [
                ['IcePHP', 'apc', 'apcu', 'apm', 'ares', 'bcmath', 'bcompiler', 'big_int', 'bitset', 'bloomy', 'bz2_filter', 'clamav', 'coin_acceptor', 'crack', 'dba'],
                ['http', 'huffman', 'idn', 'igbinary', 'imagick', 'imap', 'inclued', 'inofy', 'interbase', 'intl', 'ioncube_loader', 'ioncube_loader_4', 'jsmin', 'json', 'ldap'],
                ['nd_pdo_mysql', 'oauth', 'oci8', 'odbc', 'opcache', 'pdf', 'pdo', 'pdo_dblib', 'pdo_firebird', 'pdo_mysql', 'pdo_odbc', 'pdo_pgsql', 'pdo_sqlite', 'pgsql', 'phalcon'],
                ['stats', 'stem', 'stomp', 'suhosin', 'sybase_ct', 'sysvmsg', 'sysvshm', 'tidy', 'timezonedb', 'trader', 'translit', 'uploadprogress', 'uri_template', 'uuid']

            ]
        }
    }
}
</script>

<style lang="scss">
.module {
    margin-bottom: 100px;

    .container {
        h2 {
            @extend .text-center;
            margin-bottom: 50px;
            font-weight: 200;
        }

        > .row {
            margin-bottom: 50px;
        }
    
        a {
            @extend .main-btn, .text-center;
        }
    }
}
</style>