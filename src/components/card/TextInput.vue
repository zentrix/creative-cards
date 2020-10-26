<template>
    <div class="row">
        <div class="col-sm-12">
            <div class="from-group">
                <p>Edit text:</p>
                <textarea class="from-group" cols="50" rows="4" 
                            placeholder="Add text here!" 
                            v-model="textBoxInput"
                            @keyup="textChanged"/>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data: function(){
            return{
                textBoxInput: ""
            }
        }, 
        methods: {
            textChanged: function(){
                this.$emit('displayTextChanged', this.textBoxInput)            
            }
        }
    }
</script>
<style>

</style>