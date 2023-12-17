<template>
  <h1>CRYPTO</h1>
  <Input :changeAmout="changeAmout" />

  <div className="selectors">
  <Selector :setCryoto="setCryptoFirst"/>
  <Selector :setCryoto="setCryptoSecond"/>
  </div>
</template>

<script>
import Input from './components/Input.vue'
import Selector from './components/Selector.vue'

export default {
    components: { Input, Selector }, 
    data() {
      return {
        amout: 0,
        cryptoFirst: '',
        cryptoSecond: '',
      }
    },
    methods: {
      changeAmout(val){
        this.amout = val
      },
      setCryptoFirst(val){
        this.cryptoFirst = val
      },
      setCryptoSecond(val){
        this.cryptoSecond = val
      }
    }
}


</script>



<style scoped>

.selectors {
  display: flex;
  justify-content: space-around;
  width: 700px;
  margin: 0 auto;

}

</style>
