<script setup>

import { reactive } from 'vue';

import Form from './components/Form.vue'

import Result from './components/Result.vue'

const estado = reactive ({
  operacao: 'somar',
  numero1: '',
  numero2: '',
})

let operacaoAtual = estado.operacao;

const realizaOperacao = () => {
  const num1 = parseFloat(estado.numero1);
  const num2 = parseFloat(estado.numero2);

  if (isNaN(num1) || isNaN(num2)) {
    return '-';
  }

  switch(operacaoAtual) {
    case "somar":
      return num1 + num2;
    case "subtrair":
      return num1 - num2;
    case "multiplicar":
      return num1 * num2
    case "dividir":
      return num1 / num2;
  }
}
</script>

<template>
  <div class="container">
    <Form :numero1="estado.numero1" :numero2="estado.numero2" :alteraOperacao="evento => estado.somar = evento.target.value"/>
    <Result :realizaOperacao="realizaOperacao()"/>
  </div>
</template>
