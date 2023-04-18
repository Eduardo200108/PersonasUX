<script>
export default {
    
    data() {
        return {
            slider: 50
        }
    },
    methods: {
        enviar() {
            this.$emit('person',this.slider)
        }
    }
}
</script>

<template>
    <div>
        <slot></slot> ({{ slider }}%)
        <br>
        <input
              v-model="nombre"
              type="text"
              placeholder="Nombres"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            />

    </div>
</template>
