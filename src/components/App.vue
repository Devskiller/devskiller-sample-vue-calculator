<template>
  <div class="calculator">
    <input data-testid="display" class="display" type="text" disabled v-model="display" />

    <div class="btn-container">
      <button data-testid="btn-clear" class="btn wide">C</button>
      <button data-testid="btn-div" class="btn">/</button>

      <button data-testid="btn-7" class="btn">7</button>
      <button data-testid="btn-8" class="btn">8</button>
      <button data-testid="btn-9" class="btn">9</button>
      <button data-testid="btn-mul" class="btn">*</button>

      <button data-testid="btn-4" class="btn">4</button>
      <button data-testid="btn-5" class="btn">5</button>
      <button data-testid="btn-6" class="btn">6</button>
      <button data-testid="btn-sub" class="btn">-</button>

      <button data-testid="btn-1" class="btn">1</button>
      <button data-testid="btn-2" class="btn">2</button>
      <button data-testid="btn-3" class="btn">3</button>
      <button data-testid="btn-add" class="btn">+</button>

      <button data-testid="btn-0" class="btn wide">0</button>
      <button data-testid="btn-eval" class="btn">=</button>
    </div>
  </div>
</template>

<script>
const isOperator = (char) => ['+', '-', '/', '*'].includes(char)
const last = (text) => text[text.length - 1]
const withoutLast = (text) => text.substr(0, text.length - 1)

export default {
  name: 'App',
  data() {
    return {
      display: ''
    }
  }
}
</script>
