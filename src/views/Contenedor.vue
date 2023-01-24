<template>
    <div>
        <v-banner lines="one" color="info" icon="mdi-text-box-search-outline" class="my-3">
            <!-- <v-banner-text>
                <h1>Detalle de pase</h1>
            </v-banner-text> -->
            <h1> {{ titulo }}</h1>
        </v-banner>
        <v-container >
            <v-layout >
                <v-row justify="center" class="pt-1">   
                    <v-col cols="6" md="4"> <!-- cols="12" defino el ancho de la columnas, cols reemplaza xs-->
                        <v-text-field         
                            v-model="pase.FechaDesde"               
                            label="Fecha Desde"
                            type="date"
                        ></v-text-field>
                    </v-col>
                    <v-col cols="6" md="4">
                        <v-text-field         
                            v-model="pase.FechaHasta"               
                            label="Fecha Hasta"
                            type="date"
                        ></v-text-field>
                    </v-col>
                    <v-col cols="6" md="2">
                        <v-btn color="blue">
                            Buscar
                            <v-icon end>mdi-magnify</v-icon>
                        </v-btn>
                    </v-col>
                    <!-- <v-btn color="blue" disabled>Buscar</v-btn> -->
                </v-row>
            </v-layout>
            <v-row>
                <v-col md="3" sm="10" cols="9">
                    <v-combobox
                        clearable
                        label="Secuencial"
                        :items="['California', 'Colorado', 'Florida', 'Georgia', 'Texas', 'Wyoming']"
                        variant="solo"
                    >
                    </v-combobox>
                </v-col>
                <v-col md="3" sm="3" cols="9">
                    <v-combobox
                        clearable
                        label="Entidad"
                        :items="['California', 'Colorado', 'Florida', 'Georgia', 'Texas', 'Wyoming']"
                        variant="solo"
                    >
                    </v-combobox>
                </v-col>
                <v-col md="3" sm="1" cols="9">
                    <v-combobox
                        clearable
                        label="Usuario"
                        :items="['California', 'Colorado', 'Florida', 'Georgia', 'Texas', 'Wyoming']"
                        variant="solo"
                    >
                    </v-combobox>
                </v-col>
                <v-col md="3" sm="3" cols="9">
                    <v-combobox
                        clearable
                        label="Estado"
                        :items="['California', 'Colorado', 'Florida', 'Georgia', 'Texas', 'Wyoming']"
                        variant="solo"
                    >
                    </v-combobox>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>


<script lang="ts">

import { defineComponent } from "vue";
import { API_URL } from "../utils/constans";
 // import { aliases, mdi } from 'vuetify/iconsets/mdi'
// import { DatetimePicker } from 'vuetify-datetime-picker'

export default defineComponent({
    name: "KE04",
    data () {
        return {
            titulo: "Detalle de pase",
            date: null,
            pase: {
                desarrollador: '',
                secuencial: null,
                FechaDesde: null,
                FechaHasta: null
            },
            apiurl: process.env.VUE_APP_WEBAPIURL
        }
    },
    // icons:{
    //     defaultSet: 'mdi',
    //     aliases,
    //     sets: {
    //         mdi,
    //     }
    // }
    });
</script>