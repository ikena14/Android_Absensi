<template>
    <ion-page>
        <ion-header>
            <ion-toolbar color="dark">
                <ion-title>Kelas</ion-title>
            </ion-toolbar>
        </ion-header>
        <ion-content>
            <ion-list>
                <ion-item v-for="item in kelas" :key="item.id" :routerLink="'/kelas/'+item.id">
                    <ion-label>
                        {{item.nama}}
                        <span class="rata-kanan">No Ruang {{item.noruang}}</span>
                        <p>{{item.matakuliah}}</p>
                    </ion-label>
                </ion-item>
            </ion-list>
        </ion-content>
    </ion-page>
</template>

<script>
  import {
    IonPage,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
    IonItem,
    IonLabel,
    IonList
} from '@ionic/vue'
import axios from 'axios'
import{defineComponent}from 'vue'
export default defineComponent({
    data(){
        return{
            kelas :[]
        }
    },
    components:{
        IonPage,
        IonHeader,
        IonToolbar,
        IonTitle,
        IonContent,
        IonItem,
        IonLabel,
        IonList
    },
    mounted(){
        axios.post("http://3.235.133.198/api/kelas",{
            "user_id":localStorage.getItem("user_id")
        })
        .then(response=>{
            this.kelas = response.data.data
        })
    }
})
</script>

<style scoped>
    .rata-kanan{
        float:right;
    }
</style>