<template>
    <section class="limit">
        <div class="container">
            <h2>Powerful dengan Limit PHP yang Lebih Besar</h2>
            <div class="row">
                <div class="col-md-6" v-for="(table, index) in tables" :key="index">
                    <table class="mb-0">
                        <tr v-for="(list, index) in table" :key="index">
                            <td>{{list}}</td>
                        </tr>
                    </table>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Limit',
    data() {
        return {
            tables: [
                ['max execution time 300s', 'max execution time 300s', 'php memort limit 1024 MB'],
                ['post max size 128 MB','upload max filesize 128 MB', 'max input vars 2500']
            ]
        }
    }
}
</script>

<style lang="scss">
.limit {
    @extend %small-divider, .text-center;
    margin-bottom: 40px;

    h2 {
        font-weight: 200;
    }

    .row {        
        padding-top: 25px;
        padding-bottom: 35px;

        table {
            @extend .table;
            border: solid 1px #f1f1f1;

            tr:nth-child(even) {
                background-color: #f7f7f7;
            }

            td {
                background: url('../assets/icon/check.png') 20px/20px no-repeat;
                border-top-color: #f1f1f1;
                padding: .5rem;
                // padding-left: 50px;
            }

        }

        @include media-breakpoint-down(md) {
            > div:nth-child(2) {

                table {
                    tr {
                        &:nth-child(even) {
                            background-color: #fff;
                        }
                        &:nth-child(odd) {
                            background-color: #f7f7f7;
                        }
                    }
                }
            }
            
            
        }
    }

}
</style>