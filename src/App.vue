<script setup>
import Header from "./components/Header.vue";
import Form from "./components/Form.vue";
import Result from "./components/Result.vue";
import { reactive } from "vue";

const state = reactive({
  number1: 0,
  number2: 0,

  operation: "sum",
});

const getSum = () => {
  return Number(state.number1) + Number(state.number2);
};

const getMinus = () => {
  return Number(state.number1) - Number(state.number2);
};

const getTimes = () => {
  return Number(state.number1) * Number(state.number2);
};

const getDivision = () => {
  return Number(state.number1) / Number(state.number2);
};

const getOperation = () => {
  const { operation } = state;

  switch (operation) {
    case "sum":
      return getSum();
    case "minus":
      return getMinus();
    case "times":
      return getTimes();
    case "division":
      return getDivision();
  }
};
</script>

<template>
  <div class="container">
    <Header />

    <Form
      :number1="(e) => (state.number1 = e.target.value)"
      :number2="(e) => (state.number2 = e.target.value)"
      :operation="(e) => (state.operation = e.target.value)"
    />
    <Result :resultado="getOperation()" />
  </div>
</template>

<style scoped></style>
