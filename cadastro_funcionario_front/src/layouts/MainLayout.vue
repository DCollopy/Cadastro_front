<template>
 <q-layout view="lHh lpr lFf"  class="shadow-2 rounded-borders">
      <q-header elevated class="bg-light-blue-3 q-pa-md">
        <q-toolbar >
          <q-avatar>
          </q-avatar>
          <q-toolbar-title class="text-capitalize text-weight-bolder text-h5">
            Gestão Funcionario
          </q-toolbar-title>
            <q-btn to="/home" flat round dense class="bg-light-blue-3 q-mr-sm" icon="home"/>
            <q-btn
                   to="/login"

                   flat
                   round
                   dense
                   class="q-mr-sm"
                   icon="login"/>
            <q-btn


                   flat
                   round
                   dense
                   class=" q-mr-sm "
                   icon="account_circle"
                   >

            </q-btn>
        </q-toolbar>
      </q-header>

      <q-footer elevated>
        <q-toolbar class="glossy bg-grey-4"></q-toolbar>
      </q-footer>

      <q-page-container class="bg-grey-2">
        <q-page class="q-pa-xl">
            <router-view />
        </q-page>
      </q-page-container>
 </q-layout>
</template>

<script>

import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout'

})
</script>
<style lang="sass">
.q-toolbar
  @media (min-width: $breakpoint-sm-min)
  height: 77px
.q-toolbar-title
  font-size: 30px
  text-align: center
  @media (max-width: $breakpoint-xs-max)
  color: #1E90FF
</style>
