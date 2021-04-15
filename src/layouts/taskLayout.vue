<template>
  <q-layout view="hHh Lpr fFf">
    <!-- Be sure to play with the Layout demo on docs -->

    <!-- (Optional) The Header -->
    <q-header elevated class="bg-grey-2" style="height: 60px">
      <q-toolbar>
        <div class="row col-md-10 col-xs-10">
          <q-toolbar-title class="text-weight-regular text-subtitle1">
            <q-item>
              <q-btn  color="grey-9" flat dense icon="menu" @click="leftDrawer = !leftDrawer" />
              <q-item-section>
                <q-item-label lines="1"></q-item-label>
                <q-item-label caption class="text-grey-9" 
                  >Optimize your time</q-item-label>
              </q-item-section>
            </q-item>
          </q-toolbar-title>
          <div class=" q-px-xd">
            <q-img src="../statics/mercadoOluc.svg" style="width: 150px; padding-bottom: 10; padding-top: 10;" ></q-img>
          </div>
        </div>
      </q-toolbar>
    </q-header>

    <!-- (Optional) A Drawer; you can add one more with side="right" or change this one's side -->
    <q-drawer
      v-model="leftDrawer"
      side="left"
      bordered
      content-class="bg-grey-1"
    >
      <q-scroll-area class="fit q-pa-sm bg-grey-1">
        <!-- Content here -->
        <timer></timer>
      </q-scroll-area>
    </q-drawer>

    <q-page-container>
      <!-- This is where pages get injected -->
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import Timer from "components/timer";
export default {
  // name: 'LayoutName',
  components: {
    Timer
  },
  data() {
    return {
      leftDrawer: true,
    };
  },
};
</script>
