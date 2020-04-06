<template>
    <div class="form-input-binding">
        <div class="text">
            {{ message }}
        </div>
        <div class="input-form">
            <input type="text" v-model.lazy="message" name="">
        </div>

        <div class="input-form">
            <input type="text" :placeholder="placeholder" :value="value" name="">
        </div>
        
        <div class="text">
            {{ message1 }}
        </div>
        <div class="input-form">
            <input type="checkbox" v-model="message1" name="">
        </div>
        <div class="text">
            {{ message2 }}
        </div>
        <div class="input-form">
            <input type="radio" v-model="message2" value="one">
            <input type="radio" v-model="message2" value="two">
        </div>
        <div class="text">
            {{ message3 }}
        </div>
        <div class="input-form">
            <select v-model="message3">
                <option disabled="">Choose one</option>
                <option value="one">One111111</option>
                <option value="two">Two22222</option>
            </select>
        </div>

        
    </div>
</template>

<script>
    export default {
        data() {
            return {
                message: 'aaaaaaaaaaaaaaa',
                message1: false,
                message2: '',
                message3: '',
                placeholder: 'This is placeholder',
                value: 'This is value'
            }
        }
    }
</script>

<style lang="scss" scoped>
</style>