<script setup>
    import {ref} from 'vue'

    const nombre = ref('Max');

    const leerNombre =  e =>{

        nombre.value = e.target.value

    }
</script>

<template>
    <div class="md: w-1/2">
        <h2 class="font-black text-3xl text-center">Seguimiento Pacientes</h2>
        <p class="text-lg mt-5 text-center mb-10">
            Añade pacientes y
            <span class="text-indigo-600 font-bold">Adminístralos</span>
        </p>
        <form
            action=""
            class="bg-white shadow-md rounded-lg py-10 px-5 mb-10"
        
        >
            {{ nombre }}
            <div class="mb-5 ">
                <label 
                    for="mascota"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Nombre mascota
                </label>
                <input
                    type="text"
                    name="mascota"
                    id="mascota"
                    placeholder="Nombre de la mascota"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rouded-md"
                    :value="nombre"
                    @input="leerNombre"
                >
            </div>

            <div class="mb-5 ">
                <label 
                    for="propietario"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Nombre del propietario
                </label>
                <input
                    type="text"
                    name="propietario"
                    id="propietario"
                    placeholder="Nombre del propietario"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rouded-md"
                >
            </div>

            <div class="mb-5 ">
                <label 
                    for="email"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Email del propietario
                </label>
                <input
                    type="mail"
                    name="email"
                    id="email"
                    placeholder="email del propietario"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rouded-md"
                >
            </div>

            <div class="mb-5 ">
                <label 
                    for="alta"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Alta
                </label>
                <input
                    type="date"
                    name="alta"
                    id="alta"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rouded-md"
                >
            </div>

            <div class="mb-5 ">
                <label 
                    for="sintomas"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Sintomas
                </label>
                <textarea
                    name="sintomas"
                    id="sintomas"
                    placeholder="Describe los sintomas"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rouded-md h-40"
                />
            </div>
            <input
                type="submit"
                class="bg-indigo-600 w-full p-3 text-white uppercase font-bold hover:bg-indigo-700 cursor-pointer transition-colors"
                value="Registrar Paciente"
            >

        </form>
    </div>
</template>
