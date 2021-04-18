<template>
  <div>
    <button @click="$emit('changeOperator',('+'))">Ekle <br> + </button>
    <button @click="$emit('changeOperator', ('-'))">Çıkar <br> - </button>
    <button @click="$emit('changeOperator', ('/'))">Böl <br> / </button>
    <button @click="$emit('changeOperator', ('*'))">Çarp <br> * </button>
  </div>
</template>

<script>
export default {
name: "OperatorSelector"
}
</script>

<style scoped>

</style>