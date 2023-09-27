<script setup>
const props = defineProps(["number1", "number2", "operation"]);
</script>

<template>
  <form>
    <div class="row">
      <div class="col-md-5">
        <input
          type="number"
          placeholder="Digite um número"
          required
          class="form-control"
          @keyup="props.number1"
        />
      </div>
      <div class="col-md-2">
        <select @change="props.operation" class="form-control">
          <option value="sum">Adição (+)</option>
          <option value="minus">Subtração (-)</option>
          <option value="times">Multiplicação (*)</option>
          <option value="division">Divisão (/)</option>
        </select>
      </div>
      <div class="col-md-5">
        <input
          type="number"
          placeholder="Digite um número"
          required
          class="form-control"
          @keyup="props.number2"
        />
      </div>
    </div>
  </form>
</template>
