<template>
    <form @submit.prevent="submit">
        <input v-model="txet" />
        <button type="submit">Submit</button>
    </form>
</template>

<<script>
export default {
  data(){
      return {
          txet: "",
      }
  },
  methods:{
      submit(){
        console.log('fuckV-model', this.text);
        this.$emit('submit', this.text);
        this.text = '';
      },
  }
}
</script>

