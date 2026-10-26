<script>
export default {
name: 'NotaInput',
props: ['etiqueta', 'modelValue'],
emits: ['update:modelValue']
}
</script>

<template>
    <div class="mb-3">
        <label class="form-label">{{ etiqueta }}</label>
        <input type="number" class="form-control" :value="modelValue"
        @input="$emit('update:modelValue', Number($event.target.value))"/>
    </div>
</template>