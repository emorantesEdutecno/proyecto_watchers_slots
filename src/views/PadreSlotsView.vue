<template>
    <div id="PadreSlotsView">
        <h1>Padre Slots Component</h1>
        <SlotsComponent> 
            <!--
                <h3>Mensaje enviado al slot</h3>
                <a href="https://co.pinterest.com/pin/809310995507291667/">Vinculo a Saint Seiya</a>
                <ul>
                    <li>syd de mizar</li>
                    <li>bud de alcor</li>
                    <li>siegfried de duhbe</li>
                </ul>
            -->

            <template v-slot:imagen2>
                <div>
                    <img src="https://www.snk-seiya.net/guiasaintseiya/Profile-Syd5.JPG" alt="syd mizar">
                    <p>Syd Mizar</p>
                </div>
            </template>

            <template v-slot:footer>
                <h3>Este es el footer</h3>
            </template>


            <template v-slot:imagen1>
                <div>
                    <img src="https://2.bp.blogspot.com/-wl1pjP9hIXE/T7SbHP7pZ_I/AAAAAAAAAqE/bY9Gm9DOy6I/s1600/1213330412905_f.jpg" alt="pecda gama" />
                    <p>Thor Pecda Gamma</p>
                </div>
            </template>

            <template v-slot:header>
                <p>BARRA DE NAVEGACION</p>
            </template>




        </SlotsComponent>
    </div>
</template>

<script>
import SlotsComponent from '@/components/SlotsComponent.vue';
export default{
    name: 'PadreSlotsView',
    components:{
        SlotsComponent,
    },
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
#PadreSlotsView{
    background-color: darkolivegreen;
}
</style>