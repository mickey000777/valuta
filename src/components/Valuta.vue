<template>
<div>
    <label>€ </label>
    <input class="inputValuta" type="number" placeholder="geef een waarde in in €" v-model="getal">

    <ul v-if="getal">
        <li v-for="(waarde, index) of waarden" 
            :key="index" 
            :class=" waarde.cijfer < 1 ? 'groen' : 'rood' ">
            {{(index + 1)}}) {{(getal / waarde.cijfer).toFixed(2)}} - {{waarde.munt}}</li>
        
    </ul>
</div>


</template>

<script>
export default {

    data(){
        return {
            getal: "",
        }
    },

    props: {
        waarden: {
            type: Array,
        },
    },
    methods: {

        }
    }

</script>

<style>
label {
    color: white;
}
ul {
    margin: 0;
    padding: 0;
}
li {
    list-style-type: none;
    padding: .2em;
    margin: 0;
}
.rood {
    color: red;
}
.groen {
    color:palegreen;
}
</style>
