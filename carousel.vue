<template>
    <div class="carousel">
        <slot> </slot>
        <button @click="next" class="next">next</button>
        <button @click="prev" class="prev">prev</button>
    </div>
</template>

<script>
export default {
    data(){
        return{

        }
    },
    methods: {
        next(){
            this.$emit('next')
        },
        prev(){
            this.$emit('prev')
        }
    }
}
</script>
<style scoped>
.carousel {
    position: relative;
    width: 100%;
    height: 400px;
    overflow: hidden;
}
button{
    position: absolute;
    height: 40px;
    width: 50px;
    top: calc(50% - 20px);
    background-color: rgba(0,0,0,0.5);
    border: none;
    color: #fff;
}
button:focus, button:hover {
    outline: none;
    cursor: pointer;
}
.next {
    right: 0;
}
.prev{
    left: 0;
}

</style>