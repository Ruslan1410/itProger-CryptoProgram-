<template>
<ul>
<li @click="setCryoto('BTC')" :className="current == 'BTC' ? 'active' : ''">Bitcoin</li>
<li @click="setCryoto('ETH')" :className="current == 'ETH' ? 'active' : ''">ETH</li>
<li @click="setCryoto('USDT')" :className="current == 'USDT' ? 'active' : ''">USDT</li>
</ul>
</template>
    
<script>
export default {
    props: {
        setCrypto: {
            type: Function,
            required: true
        }
    },
    data() {
        return {
            current: ''
        }
    },
    methods: {
        selecItem(val) {
            this.setCryoto(val);
            this.current = val;
        }
    }
}
</script>
       
<style scoped>
ul {
    list-style: none;
    width: 200px;
    padding: 0;
    border-radius: 3px;
    border: 3px solid #000;
}

li {
    display: block;
    background: #1A032D;
    color: #fff;
    padding: 20px 0;
}

li:hover, li.active {
    background: #24043e;
    cursor: pointer;
}
    
</style>
    