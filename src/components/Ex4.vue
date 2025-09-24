<script>
    export default { 
        data() {
            return {
                // Add code here
                id: "demo1",
                blueBox: true,

            }
        },
        methods: { 
   			// Add code here
            changeColour(){
                this.blueBox = !this.blueBox
            }
		}
    }
</script>

<template>
    
    <!-- Modify code here -->
    <div class="container">
        <div v-bind:id="id" class="m-2" v-bind:class="{'blueBox':blueBox, 'redBox': !blueBox}">
            div ID : {{id}} 
        </div>
        
        <button type="button" v-bind:class="{'btn btn-primary': blueBox, 'btn btn-danger': !blueBox}" v-on:click="changeColour()">Change Color</button>
    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>
