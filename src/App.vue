<script>
export default {
  data(){
    return{

      title: 'hello world',
      apiUrl:'https://flynn.boolean.careers/exercises/api/random/mail',
      risultato: '',
      emails: [],
    }
  },

  methods:{

    getApi(){
      for(let i = 0; i < 10; i++){
        axios.get(this.apiUrl)
        .then((risultato) => {
          this.emails.push(risultato.data.response)
        })
      }
    }
  },

  mounted(){
    this.getApi()
  }
}
</script>

<template>
  
  <div>
   <h1 class="titolo">{{ title }}</h1>

   <input class="ricerca" type="text" >
  </div>
</template>

<style>


</style>