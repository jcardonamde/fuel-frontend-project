<template>
  <div class="container-fluid">
    <div class="card relative z-2">
      <Menubar :model="items" />
    </div>
  </div>
  <router-view />
</template>

<script setup lang="ts">
import { ref } from "vue";
import Menubar from 'primevue/menubar';

const items = ref([
    {
      icon: 'pi pi-fw pi-home',
      to : { name: 'home'}
    },
    {
        label: 'Product',
        icon: 'pi pi-fw pi-file',
        items: [
            {
                label: 'New',
                icon: 'pi pi-fw pi-plus',
                to : { name: 'createProd'}
            },
            {
                label: 'Edit',
                icon: 'pi pi-fw pi-file-edit',
            },
            {
                label: 'Delete',
                icon: 'pi pi-fw pi-trash'
            }
        ]
    },
    {
        label: 'Users',
        icon: 'pi pi-fw pi-user',
        items: [
            {
                label: 'New',
                icon: 'pi pi-fw pi-user-plus'
            },
            {
                label: 'Edit',
                icon: 'pi pi-fw pi-user-edit'
            },
            {
                label: 'Delete',
                icon: 'pi pi-fw pi-user-minus'
            }
        ]
    },
    {
        label: 'Search Hash',
        icon: 'pi pi-fw pi-search',
        items: [
          {
                label: 'Search',
                icon: 'pi pi-fw pi-users',
                items: [
                    {
                        label: 'Filter',
                        icon: 'pi pi-fw pi-filter',
                        items: [
                            {
                                label: 'Print',
                                icon: 'pi pi-fw pi-print'
                            }
                        ]
                    },
                    {
                        icon: 'pi pi-fw pi-bars',
                        label: 'List'
                    }
                ]
          }
        ]
    }
]);
</script>

<style>
  .container {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
  }
</style>
