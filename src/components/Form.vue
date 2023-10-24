<script setup>
    const props = defineProps(['numero1', 'numero2', 'alteraOperacao']);
</script>

<template>


        <h1 class="mt-4 mb-4 d-flex justify-content-center">Calculadora Aritimetica c/ Vue.JS</h1>

        <div class="row">
            <div class="d-flex justify-content-center mb-4">
                <form class="d-flex">
                    <input :value="props.numero1" class="me-3 form-control" type="number" placeholder="Digite um número">
                    <input :value="props.numero2" class="me-3 form-control" type="number" placeholder="Digite um número">

                    <select @change="props.alteraOperacao" class="form-control fw-bold text-center">
                        <option value="somar">Somar</option>
                        <option value="subtrair">Subtrair</option>
                        <option value="multiplicar">Multiplicar</option>
                        <option value="dividir">Dividir</option>
                    </select>
                </form>
            </div>
        </div>
</template>

<style scoped>
    select {
        font-size: 1.8vw;
        color: whitesmoke !important;
        background: #2802ff !important;
    }  
</style>