<template>
    <input type="number" @input="changeAmout($event.target.value)" placeholder="Введите число">
</template>
    
<script>
export default {
    props: {
        changeAmout: {
            type: Function,
            required: true
        }
    }
}
</script>
    
    
    
<style scoped>
    input {
        outline: none;
        width: 500px;
        top: -50px;
        font-size: 1.2em;
        border-radius: 3px;
        border: 0;
        padding: 10px 15px;
        background: #fafafa;
        color: #333;
    }
</style>
    