<template>
    <div>
        <header>
            <div class="logo">E-shop</div>
            <div class="cart">
                <form action="#" class="search-form">
                    <input type="text" class="search-field">
                    <button class="btn-search">
                        <i class="fas fa-search"></i>
                    </button>
                </form>
                <button class="btn-cart">Cart</button>
                <div class="cart-block ">
                    <div class="d-flex">
                        <strong class="d-block">Всего товаров</strong> <div id="quantity"></div>
                    </div>
                    <hr>
                    <div class="cart-items">

                    </div>
                    <hr>
                    <div class="d-flex">
                        <strong class="d-block">Общая ст-ть:</strong> <div id="price"></div>
                    </div>
                </div>
            </div>
        </header>
        <main>
            <catalog ref="catalogRef" />
        </main>
    </div>
</template>

<script>
//add packages (imports)
import catalog from './containers/Catalog.vue'
export default {
    components: { catalog },
    methods: {
        getData(url) {
            return fetch(url).then(dataReceived => dataReceived.json())
        }
    }
}
</script>
