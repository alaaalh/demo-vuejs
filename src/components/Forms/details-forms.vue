<template>
    <form>
        name
        <input type="text" v-model="nameValue"/>
        password
        <input type="password" v-model="passwordValue"/>
        <button type="submit" @click.prevent="handleSubmit">submit</button>
    </form>
</template>

<script>
    export default {
        data(){
            return {
                nameValue:'',
                passwordValue: ''
            }
        },
        methods: {
            handleSubmit(){
                console.log(this.nameValue)
                console.log(this.passwordValue)
                fetch('https://vue-http-demo-dd166-default-rtdb.firebaseio.com/serveys.json', {
                    method: 'POST',
                    headers: {
                        "Content-Type": 'application/json'
                    },
                    body: JSON.stringify({
                        name: this.nameValue,
                        password: this.passwordValue
                    })
                })
            }
        }
    }
</script>