<script>
export default {
name: 'ResultadoFinal',
props: { promedio: Number }
}
</script>

<template>
    <div class="alert alert-success mt-3 text-center">
        Promedio final: <strong>{{ promedio }}</strong>
    </div>
</template>