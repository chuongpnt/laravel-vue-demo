<template>
    <div class="event-handling">
        <div>Current Number: {{ counter }}</div>
        <button @click="increaseCounter(50)">CLick</button>

        <div @click="alertHello">
           <button @click.stop="alertWelcome">CLick</button>
        </div>

        <form >
            <button type="submit" @click.prevent="sayWelcome">Submit</button>
        </form>

        <div @click.self="alertHello">
            <button @click="alertWelcome">CLick</button>
        </div>

         <input @keyup.enter="alertHello">

        <input @keyup.13="alertHello">
    </div>
</template>

<script>
    export default {
        data() {
            return {
                counter: 0
            }
        },
        methods: {
            increaseCounter(number) {
                this.counter += number
            },
             alertHello() {
                alert('Hello')
            },
            alertWelcome() {
                alert('Welcome')
            },
            sayWelcome() {
                alert(1)
            }
        }
    }
</script>

<style lang="scss" scoped>
</style>