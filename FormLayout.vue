<script setup>
import { ref } from 'vue';

const dropdownItems = ref([
    { name: 'Option 1', code: 'Option 1' },
    { name: 'Option 2', code: 'Option 2' },
    { name: 'Option 3', code: 'Option 3' }
]);

const calendarValue = ref(null);
const dropdownItem = ref(null);
</script>



<template>
    <div class="grid">
        <div class="col-12 md:col-6">
            <div class="card p-fluid">
                <h5>Generar el RFC de una persona</h5>
                <div class="field">
                    <label for="name1">Nombre(s):</label>
                    <InputText id="name" type="text" />
                </div>
                <div class="field">
                    <label for="email1">Apellido Paterno: </label>
                    <InputText id="app" type="text" />
                </div>
                <div class="field">
                    <label for="age1">Apellido Materno: </label>
                    <InputText id="apm" type="text" />
                </div>
                <div class="field">
                    <label for="calendar">Fecha Nacimiento: </label>
                    <Calendar :showIcon="true" :showButtonBar="true" v-model="calendarValue">+
                    </Calendar>
                </div>
                <Button label="Generar RFC" id="ejecutar" class="p-button-success mr-2 mb-2" />
                <div class="field" id="mostrar_RFC">
                    <InputText id="mostrarRFC" type="text"  placeholder="RFC" />
                </div>
            </div>
        </div>
    </div>
</template>