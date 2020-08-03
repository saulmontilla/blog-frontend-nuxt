<template>
    <div>
        <main-header>
            Register
        </main-header>

        <b-row>
            <b-col cols="6" class="mx-auto">
                <b-card>
                    <template v-slot:header>
                        <h2>Register</h2>
                    </template>
                    
                    <register-form />
                </b-card>
            </b-col>
        </b-row>
    </div>
</template>

<script>
import MainHeader from '../components/MainHeader'
import RegisterForm from '../components/RegisterForm'

export default {
    components: {
        MainHeader,
        RegisterForm
    },
    data () {
        return {
            name: ''
        }
    }
}
</script>