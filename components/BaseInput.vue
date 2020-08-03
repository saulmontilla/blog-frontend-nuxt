<template>
  <div class="input-container" v-bind:class="{populated : content !== ''}">
    <input 
        :type="type"
        :id="label" 
        class="custom-input" 
        @input="updateValue"
        :value="value"
    />
    <label :for="label">
        {{ label }}
    </label>
    <div class="input-bar"></div>
    <div class="input-progress-bar"></div>
  </div>
</template>

<script>
export default {
    data () {
        return {
            content: this.value
        }
    },
    methods: {
        updateValue (event) {
            this.content = event.target.value
            this.$emit('input', event.target.value)
        }
    },
    props: {
        label: [String],
        type: {
            type: String,
            default: 'text'
        },
        value: [String, Number]
    }
}
</script>

<style>
    .input-container {
        height: 3.5rem;
        width: 100%;
        position: relative;
    }
    .input-container .custom-input {
        width: 100%;
        outline: none;
        border: 0;
        position: absolute;
        bottom: 3px;
        left: 0;
    }
    .input-container .custom-input:focus ~ .input-progress-bar {
        height: 2px;
        width: 100%;
    }
    .input-container .custom-input:focus ~ label {
        bottom: calc(100% - 1.5rem);
        color: var(--orange);
    }
    .input-container label {
        position: absolute;
        bottom: 3px;
        left: 0;
        z-index: 1;
        margin: 0;
        cursor: text;
        transition: all 0.2s;
    }
    .input-container.populated label {
        bottom: calc(100% - 1.5rem);
    }
    .input-container .input-bar {
        height: 2px;
        width: 100%;
        background: #dadfe1;
        position: absolute;
        bottom: 0;
        left: 0;
    }
    .input-container .input-progress-bar {
        height: 0;
        width: 0;
        background: var(--orange);
        position: absolute;
        bottom: 0;
        left: 0;
        transition: width .2s linear;
    }

</style>