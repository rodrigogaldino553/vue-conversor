<template>
  <div class="my-conversor">
    <h2>{{coinA}} to {{coinB}}</h2>
    <input type="text" v-model="coinA_value" v-bind:placeholder="coinA">
    <input type="button" value="Convert" v-on:click="convert">
    <h2>{{coinB_value}}</h2>
  </div>
</template>

<script>
  export default {
    name: "MyConversor",
    props: ["coinA", "coinB"],
    data(){
      return{
        coinA_value: "",
        coinB_value: 0
      }
    },
    methods: {
      convert(){
        let from_to = this.coinA+'_'+this.coinB
        const api_know = '01d5e54a57ca82c2ea73'
        const url = 'https://free.currconv.com/api/v7/convert?q='+
        from_to
        +'&compact=y&apiKey='+api_know

        fetch(url).then(res=>{return res.json()})
          .then(json=>{
            let cotation = json[from_to].val
            this.coinB_value = 'R$'+(cotation * parseFloat(this.coinA_value)).toFixed(2)
          })
      }
    }
  }
</script>

<style scoped>
.my-conversor{
  padding: 20px;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
}

</style>