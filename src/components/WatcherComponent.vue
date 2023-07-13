<template>
    <div id="WatcherComponent">
        <h1>Watcher Component</h1>
        <p>{{ title }}</p>
        <input type="text" v-model="title">
        <hr>
        <p>{{ subtitle }}</p>
        <input type="text" v-model="subtitle">
        <hr>
        <p>Contador: {{ counter }}</p>
        <button v-on:click="counter++">sumar</button>
    </div>
</template>

<script>
export default{
    name:'WatcherComponent',
    data: function(){
        return{
            title: 'Estudiando Watch Properties',
            subtitle: '',
            counter: 0,
        }
    },
    methods:{},
    computed:{},
    watch:{
        title(value){
            console.log(value);
            if(value=='hola'){
                this.title='Este es un NUEVO mensaje';
            }
        },
        counter(newvalue, oldvalue){
            console.log('old value: ', oldvalue);
            console.log('new value: ', newvalue);
            if(newvalue == 10){
                alert('Llegamos a los 10');
            }
        }
    },
    updated(){
        console.log('cambio algo. Hook updated');
    }
}
</script>