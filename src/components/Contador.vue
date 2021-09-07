<template>
  <div class="contador">
      <h1>Contador Component</h1>
    
      <p>{{getVariable1}}</p>
      <p>{{getVariable2}}</p>
      <button class="btn btn-default" @click="setVariable1('Prueba 1')">Set Variable Modulo 1</button>
      <button class="btn btn-success" @click="setVariable2('Prueba 2')">Set Variable Modulo 2</button>
  </div>
</template>

<script>
import { mapState, mapGetters, mapActions, mapMutations } from "vuex";
export default {
  computed: {
    // MODULE A
     ...mapState("moduleA", ["variable1"]),
     ...mapGetters("moduleA", ["getVariable1"]),
     // MODULE A
     ...mapState("moduleB", ["variable2"]),
     ...mapGetters("moduleB", ["getVariable2"]),
  },
  methods: {
    // MODULE A
     ...mapActions("moduleA", ["setVariable1"]),
    // MODULE B
     ...mapActions("moduleB", ["setVariable2"]),

  }
}
</script>

<style>

.contador{
  margin-top: 50px;
}



</style>