<template>
    <div class="row"> 
        <div class="col-sm-6 card edit-area">
            <cc-text-input @displayTextChanged="textBoxValue1 = $event"></cc-text-input>
            <cc-text-input @displayTextChanged="textBoxValue2 = $event"></cc-text-input>
            <cc-text-input @displayTextChanged="textBoxValue3 = $event"></cc-text-input>
        </div>
        <div class="col-sm-6 card card-display">
            <cc-text-ouput></cc-text-ouput>
            <cc-text-ouput></cc-text-ouput>
            <cc-text-ouput></cc-text-ouput>
        </div>
    </div>    
</template>

<script>
import TextInput from './TextInput.vue'
import TextOuput from './TextOuput.vue'

export default {
    data: function() {
        return {
            textBoxValue1: '',
            textBoxValue2: '',
            textBoxValue3: ''
        }
    },
    components: {
        ccTextInput: TextInput, 
        ccTextOuput: TextOuput
    }
}
</script>

<style>

.edit-area{
    background-color: #d2d9d9;
    padding: 20px;
    height: 800px;
}

.card-display{
    height: 800px;
    padding: 20px;
}
</style>