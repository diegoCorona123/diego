<template>
    <v-container fluid class="py-0 my-0 mt-5">
        <v-row class="py-0 my-0">
            <v-col md="12" sm="12" cols="12" class="py-0 my-0">
                <h1 class="google-font mb-2">Nuestra Politica</h1>
            </v-col>
        </v-row>
        <v-row class="py-0 my-0">
            <v-col md="8" sm="12" cols="12" class="py-0 my-0">
                <p class="mt-2" style="font-size:100%">
                    <b style="font-size:120%;">son pautas o criterios que se tienen en cuenta para la consecución de objetivos en la misma. Sirven para gobernar la acción en el caminar hacia un objetivo, ayudando a delegar y mantener la buena relación entre personas.</b>
                </p>

                <p class="google-font mb-2" style="font-size:110%">
                    Pequeños Requisitos

                    <ul class="mt-2" style="font-size:110%">
                        <li class="google-font">Preparatoria</li>
                        <li class="google-font">Experiencia de un año</li>
                        <li class="google-font">Ganas de trabajar</li>
                        <li class="google-font">Experiencia en roborotica</li>
                        <li class="google-font">Experiencia en programacion</li>
                        <li class="google-font">Almenos dos lenguajes de programacion</li>
                    </ul>

                   </p>

                <p class="google-font" style="font-size:120%">Somos una de las mejores empresas de robotica gracias a nuestro desempeño, contamos con 3 años de experiencia y somos parte de muchos proyectos internacionales.</p>

                <p class="google-font" style="font-size:110%">Tambien trabajamos en muchos mas campos:
                    <ul class="mt-2" style="font-size:100%">
                        <li class="google-font">Inteligencia Artificial.</li>
                        <li class="google-font">Realidad Virtual.</li>
                        <li class="google-font">Desarrollo de Software</li>
                        <li class="google-font">Mecatronica.</li>
                        <li class="google-font">Entre otros.</li>
                    </ul>
                </p>
                <center>
                <p class="google-font" style="font-size:100%">NUMERO #1 A NIVEL MUNDIAL</p>
                <br>
                
                <img src='@/assets/img/svg/empresa.png' title="Automatización" width="512" height="320" >
                </center>
                
            </v-col>
            <v-col md="4" sm="4" cols="12" class="py-0 my-0 hidden-sm-and-down">
               
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