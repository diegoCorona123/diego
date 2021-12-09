<template>
    <v-container fluid class="py-0 my-0 mt-2 mb-5">
        <v-row class="py-0 my-0" align="center">
            <v-col md="4" sm="12" cols="12" class="py-0 my-0">
                <v-img
                    :src="require('@/assets/img/dontremove/somos.png')"
                    
                    class=" mb-1"
                    width="60%"
                >
                    <template v-slot:placeholder>
                        <v-row
                        class="fill-height ma-0"
                        align="center"
                        justify="center"
                        >
                        <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                        </v-row>
                    </template>
                </v-img>
            </v-col>
            <v-col md="6" sm="8" cols="8" class="py-0 my-0">
                <p class="google-font mb-0" style="font-weight: 350;font-size:200%"><b>
                    <span style="color: #1a73e8;">NUESTRA EMPRESA</span> </b> 
                </p>
                <p class="google-font" style="font-size:100%">
                    <b style="font-size:120%;">Nuestra empresa obótica es la encargada de fabricar los distintos tipos de maquinarias que permiten agilizar el trabajo de una empresa. ... Así como también productos de automatización: fabricación de productos como controladores de velocidad, motores y generadores eléctricos, en general es equipamiento para baja tensión</b>
                </p>
                <br>
        
                <v-btn href="https://rivasrobotics.com/empresa-de-robotica/">Visitanos</v-btn>

                &nbsp;

                <v-btn href="https://universidadean.edu.co/noticias/top-10-lo-mejor-de-la-robotica">Mas Empresas</v-btn>

            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    props:['data'],
    data:()=>({

    })
}
</script>