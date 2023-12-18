<template>
    <input min="0" type="number" @input="changeAmout($event.target.value)" placeholder="Введите число"><br>
    <button @click="convert()">Конвертировать</button>
</template>
    
<script>
export default {
    props: {
        changeAmout: {
            type: Function,
            required: true
        },
        convert: {
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

    button {
        position: relative;
        top: 5px;
        padding: 15px 20px;
        color: #fff;
        text-transform: uppercase;
        cursor: pointer;
        background: #1a032d;
        border:  0;
        border-radius: 3px;
    }
</style>
    