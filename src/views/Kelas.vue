<template>
    <ion-page>
        <ion-header>
            <ion-toolbar color="dark">
                <ion-title>Kelas</ion-title>
            </ion-toolbar>
        </ion-header>
        <ion-content>
            <ion-list>
                <ion-item>
                    <ion-label>
                        Kelas 1
                        <span class="rata-kanan">No Ruang</span>
                        <p>Mata kuliah</p>
                    </ion-label>
                </ion-item>
                <ion-item>
                    <ion-label>
                        Kelas 2
                        <span class="rata-kanan">No Ruang</span>
                        <p>Mata kuliah</p>
                    </ion-label>
                </ion-item>
                <ion-item>
                    <ion-label>
                        Kelas 3
                        <span class="rata-kanan">No Ruang</span>
                        <p>Mata kuliah</p>
                    </ion-label>
                </ion-item>
                <ion-item>
                    <ion-label>
                        Kelas 4
                        <span class="rata-kanan">No Ruang</span>
                        <p>Mata kuliah</p>
                    </ion-label>
                </ion-item>
                <ion-item>
                    <ion-label>
                        Kelas 5
                        <span class="rata-kanan">No Ruang</span>
                        <p>Mata kuliah</p>
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
import{defineComponent}from 'vue'
export default defineComponent({
    components:{
        IonPage,
        IonHeader,
        IonToolbar,
        IonTitle,
        IonContent,
        IonItem,
        IonLabel,
        IonList
    }
})
</script>

<style scoped>
    .rata-kanan{
        float:right;
    }
</style>