<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar class="bg-white">
        <div class="col-12 row">
          <div class="col-12 col-md-5" :class="{'text-center' : $q.screen.lt.md }">
            <q-avatar :style="!$q.screen.lt.md ? 'height: 170px; width: 170px;' : 'height: 140px; width: 140px;'">
              <img src="../assets/logo.svg" />
            </q-avatar>

            <q-btn v-if="$q.screen.lt.md" flat dense icon="menu" color="black" class="bg_color drawer" />
          </div>

          <div class="col-12 col-md-7 row justify-end">
            <div class="col-12 col-md-8 q-pt-lg" :class="{'q-pr-lg' : !$q.screen.lt.md}">
              <q-input outlined>
                <template #append>
                  <q-btn icon="search" color="primary" />
                </template>
              </q-input>

              <br />

              <div v-if="!$q.screen.lt.md" class="float-right">
                <q-btn stretch flat label="Catálogo" color="primary" />
                <q-btn stretch flat label="Sobre" color="primary" />
                <q-btn stretch flat label="Contato" color="primary" />
              </div>
            </div>
          </div>
        </div>
      </q-toolbar>
    </q-header>

    <q-footer elevated>
      <q-toolbar class="q-px-lg" style="background-color: #858585; height: 80px;">
        <div v-if="!$q.screen.lt.md">
          <span>
            <strong style="font-size: 16px;"> XYZ Company </strong> <br>
            xxxxx xxxxxx <br>
            xxxxx xxxxxx
          </span>
        </div>

        <q-space v-if="!$q.screen.lt.md" />

        <div>
          <span style="font-size: 16px;">(99) 9999-9999</span>
        </div>

        <q-space />

        <div class="q-gutter-md text-right">
          <q-btn flat color="black" class="bg_color" style="width: 35px;" />
          <q-btn flat color="black" class="bg_color" style="width: 35px;" />
          <q-btn flat color="black" class="bg_color" style="width: 35px;" />
        </div>
      </q-toolbar>
    </q-footer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout'
}
</script>
<style>
.drawer {
  font-size: 1.3em;

  position: absolute;
  left: 80%;
  top: 20%;
}
</style>
