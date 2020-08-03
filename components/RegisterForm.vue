<template>
    <form class="text-center">
        <base-input label="name" v-model="name"/>
        <base-input label="email" v-model="email"/>
        <base-input type="password" label="password" v-model="password"/>
        <base-input type="password" label="password confirmation" v-model="password_confirmation"/>

        <button class="btn btn-primary mt-3" type="submit">
            Register
        </button>
    </form>
</template>

<script>
import BaseInput from './BaseInput'

export default {
    components: {
        BaseInput
    },
    data () {
        return {
            name: '',
            email: '',
            password: '',
            password_confirmation: ''
        }
    }
}
</script>