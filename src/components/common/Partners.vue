<template>
    <v-container fluid >
        <v-row align="center" justify="center" class="mb-0">
            <v-col cols="12" md="12" lg="12" sm="12" class="mb-0">
                <p class="google-font mb-1" style="font-weight: 350;font-size:200%"><b>Robots
                    <span style="color: #1a73e8;">RPA</span> </b> 
                </p>
                <p class="google-font mt-1 mb-0" style="font-size:100%">(automatización robótica de procesos).</p>
                <p class="google-font mt-0 mb-0" style="font-size:100%">Utilizan la interfaz de usuario para capturar datos y operar con aplicaciones: interpretan, activan respuestas y se comunican con otros sistemas para realizar una gran variedad de tareas repetitivas.</p>
            </v-col>
        </v-row>

        

        <v-row align="center" justify="start" class="mt-0">
            <v-col cols="12" md="12" lg="12" sm="12" class="mx-1 mt-5">
                <p>Robotica RPC</p>
            </v-col>
            <v-col cols="6" md="3" lg="2" xl="2" sm="4">
                
              <iframe width="560" height="315" src="https://www.youtube.com/embed/dq7ieDoFI0U?start=23" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                
            </v-col>
        </v-row>
     
    </v-container>
</template>

<script>
import service from '@/services/appservices'
import { mapState } from "vuex";
export default {
    data:()=>({
        partnersData:[]
    }),
    computed:{
        ...mapState(["config"])
    },
    mounted(){
        this.getPartner()
    },
    methods:{
        getPartner(){
            service.getAllPartners().then(res=>{
                if(res.success){
                    this.partnersData = res.data.filter(data=>data.visible)
                }
            })
        },
    }
}
</script>

<style scoped>
.client-logo{
    height: 90px;
    padding: 12px 12px;
    border-radius: 7px;
    background: white;
    border: 1px solid #ebebeb;
    text-align: center;
}
</style>