<template>
    <div id="SlotsComponent">
        <slot name="header"></slot>
        <h1>Slots Component</h1>
        <slot name="imagen1"></slot>
        <slot name="imagen2"></slot>

        <slot name="footer"></slot>
    </div>
</template>

<script>
export default{
    name:'SlotsComponent',
    data:function(){
        return{

        }
    },
    methods:{},
    computed:{},
    watch:{},


}
</script>

<style scoped>
#SlotsComponent{
    background-color: aqua;
    margin: 2%;

}
</style>