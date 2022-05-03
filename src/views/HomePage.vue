<template>
  <ion-page>
    <ion-content class="cs-dark-bg" :fullscreen="true">
      <ion-fab
        vertical="bottom"
        class="ion-padding-bottom"
        horizontal="center"
        slot="fixed"
      >
        <ion-fab-button color="dark" @click="openLibrary()">
          <ion-icon :icon="camera"></ion-icon>
        </ion-fab-button>
      </ion-fab>

      <ion-fab
        class="ion-padding-bottom ion-padding-start"
        vertical="bottom"
        horizontal="left"
        slot="fixed"
      >
        <ion-fab-button color="dark" @click="takePhoto()">
          <ion-icon :icon="folder"></ion-icon>
        </ion-fab-button>
      </ion-fab>

      <ion-fab
        class="ion-padding-bottom ion-padding-end"
        vertical="bottom"
        horizontal="end"
        slot="fixed"
      >
        <ion-fab-button color="dark" @click="switchCamera()">
          <ion-icon :icon="sync"></ion-icon>
        </ion-fab-button>
      </ion-fab>
    </ion-content>
  </ion-page>
</template>

<style scoped>
ion-content {
  --background: #000 no-repeat center center / cover;
}
</style>
<script>
import { IonContent, IonPage } from "@ionic/vue";
import { defineComponent } from "vue";
import { camera, folder, sync } from "ionicons/icons";
export default defineComponent({
  name: "HomePage",
  components: {
    IonContent,
    IonPage,
  },
  setup() {
    return {
      takePhoto() {
        alert("take photo");
      },
      openLibrary() {
        alert("open lib");
      },
      switchCamera() {
        alert("switch");
      },
      camera,
      folder,
      sync,
    };
  },
});
</script>

<style scoped>
#container {
  text-align: center;

  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;

  color: #8c8c8c;

  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>
