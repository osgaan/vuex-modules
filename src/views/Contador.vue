<template>
    <div>
        <div class="contador">
            <contador/>
        </div>
    </div>
</template>

<script>
import Contador from '@/components/Contador.vue';

    export default {
        components: {
          Contador
        }

    }
</script>


<style scoped>

*{
  margin-top: 20px;
  text-align: center;
}

</style>

