<script>
export default {
     data() {
          return {
               number1: 0,
               number2: 0,
               operation: "+",
          };
     },
     computed: {
          result() {
               switch (this.operation) {
                    case "+":
                         return this.number1 + this.number2;
                    case "-":
                         return this.number1 - this.number2;
                    case "*":
                         return this.number1 * this.number2;
                    case "/":
                         return this.number2 !== 0
                              ? this.number1 / this.number2
                              : "Erro: Divisão por zero";
                    default:
                         return "Operação inválida";
               }
          },
     },
};
</script>

<template>
     <div class="container my-5">
          <div class="card mx-auto" style="max-width: 500px;">
               <div class="card-body">
                    <h1 class="text-center mb-4">Calculadora Aritmética</h1>
                    <form>
                         <div class="mb-3">
                              <label for="number1" class="form-label">Primeiro Número</label>
                              <input type="number" id="number1" class="form-control" v-model.number="number1"
                                   placeholder="Digite o primeiro número" />
                         </div>
                         <div class="mb-3">
                              <label for="operation" class="form-label">Operação</label>
                              <select id="operation" class="form-select" v-model="operation">
                                   <option value="+">+</option>
                                   <option value="-">-</option>
                                   <option value="*">x</option>
                                   <option value="/">÷</option>
                              </select>
                         </div>
                         <div class="mb-3">
                              <label for="number2" class="form-label">Segundo Número</label>
                              <input type="number" id="number2" class="form-control" v-model.number="number2"
                                   placeholder="Digite o segundo número" />
                         </div>
                    </form>
                    <div class="text-center mt-4">
                         <h2 class="fw-bold">Resultado: <span class="text-primary">{{ result }}</span></h2>
                    </div>
               </div>
          </div>
     </div>
</template>

<style scoped>
.card {
     border-radius: 10px;
     box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}
</style>