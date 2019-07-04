<template>
  <view class="container">
    <text class="text-color-primary">Aprendendo mobile</text>
     <text-input
      class="teste-input"
      :style="{width:200,height: 60, borderColor: 'blue', borderWidth: 2}"
      v-model="text"
     />
    <button
       :on-press="validatorBtn"
       title="Exibir"
       color="#841584"
    />
  </view>
</template>
<script>
export default {
  name: 'App',
  data () {
    return {
      text: ''
    }
  },
  methods: {
    validatorBtn: function() {
      console.log('TEXT =>', this.text)
      if(this.text == ''){
        alert("Sem texto!")
      } else {
        alert(' O texto é => '+ this.text +' ')
      }
    }
  }
}
</script>
<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
.teste-input{
  color: red;
  margin-bottom: 15px;
}
</style>
