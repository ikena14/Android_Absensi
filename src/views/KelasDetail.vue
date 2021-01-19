<template>
    <ion-page>
        <ion-header>
            <ion-toolbar color="dark">
                <ion-title>Detail Kelas</ion-title>
            </ion-toolbar>
        </ion-header>
        <ion-content>
            <ion-list>
                <ion-item v-for="(item,id) in kelasdetail" :key="id">
                    <ion-label>Pertemuan {{item.pertemuan}}</ion-label>
                    <ion-badge color="success">{{item.status}}</ion-badge>
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
    IonList,
    IonItem,
    IonLabel,
    IonBadge
} from '@ionic/vue'
import{defineComponent}from 'vue'
import axios from 'axios'
export default defineComponent({
    data(){
        return{
            kelasdetail :[]
        }
    },
    components:{
    IonPage,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
    IonList,
    IonItem,
    IonLabel,
    IonBadge
    },
    mounted(){
        axios.post("http://3.235.133.198/api/kelasdetail",{
            "user_id":localStorage.getItem("user_id"),
            "kelas_id": this.$route.params.id
        })
        .then(response=>{
            this.kelasdetail = response.data.data
        })
    }
})
</script>

<style lang="scss" scoped>

</style>