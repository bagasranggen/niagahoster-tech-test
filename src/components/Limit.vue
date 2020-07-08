<template>
    <section class="limit">
        <div class="container">
            <h2>Powerful</h2>
            <div class="row">
                <div class="col-md-6">
                    <table class="table table-striped">
                        <tr>
                            <td>test</td>
                        </tr>
                        <tr>
                            <td>test</td>
                        </tr>
                    </table>
                </div>
                <div class="div col-md-6">
                    <table>
                        <tr>
                            <td>test</td>
                        </tr>
                    </table>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Limit'
}
</script>

<style lang="scss">
.limit {
    @extend %small-divider, .text-center;
    margin-bottom: 40px;

    .row {        
        padding-top: 25px;
        padding-bottom: 35px;

        table {
            @extend .table, .table-striped;
        }
    }

}
</style>