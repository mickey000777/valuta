<template>
  <div id="app">
    <div class="valuta">
        <valuta :waarden="waarden"/>
    </div>
    
  </div>
</template>

<script>
import Valuta from './components/Valuta.vue'

export default {
  name: 'app',
      data(){
        return {
          waarden: [

            {
              cijfer: 1.124, 
              munt: "Britse pond",
            },

            {
              cijfer: 0.8803, 
              munt: "US dollar",
            },

            {
              cijfer: 0.0983, 
              munt: "Zweedse kroon",
            },

            {
              cijfer: 1.2405, 
              munt: "Jordaanse dinar",
            },            

            {
              cijfer: 0.008, 
              munt: "Vanuatu vatu",
            },

            {
              cijfer: 2.2872, 
              munt: "Omaanse rial",
            },
          ],

        }

    },
  components: {
    Valuta
  }
}
</script>

<style>
.valuta {
  display: grid;
  justify-content: center;
  width: 18em;
  background-color: gray;
  padding: 0 0 .5em 0;
}
.inputValuta {
  margin: .5em 0 1em 0;
  width: 15em;
}
  input[type=number]::-webkit-inner-spin-button,
  input[type=number]::-webkit-outer-spin-button {
    -webkit-appearance: none;
    margin: 0;
}
input[type=number] {
    -moz-appearance:textfield;
}
</style>
