<template>
    <div v-bind:id="uniqid">
        <slot>
        </slot>
    </div>
</template>

<script>
import Vue from 'vue'

export default {
    created () {
        Vue.nextTick(()=> {
            const root = document.getElementById(this.uniqid)
            
            root.outerHTML = root.innerHTML
        })
    },
    data () {
        return {
            uniqid: Date.now()
        }
    }
}
</script>