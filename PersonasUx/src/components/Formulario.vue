<script>
import axios from "axios";
let API_URL = "/api/guardarPersonasUxd.php";

export default {
  data() {
    return {
      nombre: "",
      edad: "",
      estadoCivil: "",
      trabajo: "",
      residencia: "",
      cita: "",
      citaAutor: "",
      bio: "",
      personalidad01: "0",
      personalidad02: "0",
      personalidad03: "0",
      personalidad04: "0",
      objetivos: [],
      frustraciones: [],
      motivaciones: [],
      porcentaje: "",
      marcas: "",
    };
  },
  methods: {
    submit() {
      axios
        .post(API_URL, {
          nombre: this.nombre,
          edad: this.edad,
          estadoCivil: this.estadoCivil,
          trabajo: this.trabajo,
          residencia: this.residencia,
          cita: this.cita,
          citaAutor: this.citaAutor,
          bio: this.bio,
          personalidad01: this.personalidad01,
          personalidad02: this.personalidad02,
          personalidad03: this.personalidad03,
          personalidad04: this.personalidad04,
          objetivos: this.objetivos,
          frustraciones: this.frustraciones,
          motivaciones: this.motivaciones,
          porcentaje: this.porcentaje,
          marcas: this.marcas,
        })
        .then((response) => {
          console.log(response.status);
        });
    },
  },
};
</script>

<template>
  <div class="font-sans">
    <div class="min-h-screen flex sm:justify-center bg-[#fff7ed]" >
      <div
        style="margin: 100px 10px 100px 10px"
        class="rounded-3xl px-6 py-4 bg-[#A3BAB4] border"
      >
        <label
          for=""
          class="block mt-3 text-sm text-gray-700 text-center font-semibold"
        >
          Registrato de ISCLAB
        </label>
        <form class="mt-20 w-96">
          <div>
            <label
              for="nombre"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >Nombres</label
            >
            <input
              v-model="nombre"
              type="text"
              placeholder="Nombres"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            />
          </div>

          <div class="mt-7">
            <label
              for="edad"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >Edad</label
            >
            <input
              v-model="edad"
              type="number"
              placeholder="Edad"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            />
          </div>

          <label
            for="estadoCivil"
            class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
            >Estado civil</label
          >
          <select
            v-model="estadoCivil"
            class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
          >
            <option selected>Estado civil</option>
            <option value="1">Soltero</option>
            <option value="2">Casado</option>
            <option value="3">Divorciado</option>
            <option value="4">Separado</option>
            <option value="5">Union libre</option>
            <option value="6">Viudo</option>
          </select>

          <div class="mt-7">
            <label
              for="residencia"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >Residencia</label
            >
            <input
              v-model="residencia"
              type="text"
              placeholder="Residencia"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            />
          </div>

          <div class="mt-7">
            <label
              for="trabajo"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >Trabajo</label
            >
            <input
              v-model="trabajo"
              type="text"
              placeholder="Trabajo"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            />
          </div>

          <div class="mt-7">
            <label
              for="cita"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >Cita</label
            >
            <textarea
              v-model="cita"
              type="text"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            ></textarea>
          </div>

          <div class="mt-7">
            <label
              for="citaAutor"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >Cita Autor</label
            >
            <textarea
              v-model="citaAutor"
              type="text"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            ></textarea>
          </div>
          <div class="mt-7">
            <label
              for="bio"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >Biografia</label
            >
            <textarea
              v-model="bio"
              type="text"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            ></textarea>
          </div>

          <div class="mt-7">
            <label
              for="objetivos"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >Objetivos</label
            >
            <input
              v-model="objetivos"
              type="text"
              placeholder="Escribe objetivos"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            />
          </div>

          <div class="mt-7">
            <label
              for="frustraciones"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >Frustraciones</label
            >
            <input
              v-model="frustraciones"
              type="text"
              placeholder="Escribe frustraciones"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            />
          </div>

          <div class="mt-7">
            <label
              for="personalidad01"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >personalidad 1</label
            >
            <input
              v-model="personalidad01"
              type="range"
              min="0"
              max="100"
              class="mt-1 block w-full border-none  bg-blue-600 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            />
            <span>{{ this.personalidad01 }}%</span>
          </div>

          <div class="mt-7">
            <label
              for="personalidad02"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >personalidad 2</label
            >
            <input
              v-model="personalidad02"
              type="range"
              min="0"
              max="100"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
              
              />
              <span>{{ this.personalidad02 }}%</span>
          </div>

          <div class="mt-7">
            <label
              for="personalidad03"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >personalidad 3</label
            >
            <input
              v-model="personalidad03"
              type="range"
              min="0"
              max="100"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            />
            <span>{{ this.personalidad03 }}%</span>
          </div>

          <div class="mt-7">
            <label
              for="personalidad04"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >personalidad 4</label
            >
            <input
              v-model="personalidad04"
              type="range"
              min="0"
              max="100"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            />
            <span>{{ this.personalidad04 }}%</span>
          </div>
          <div></div>

          <div class="mt-7">
            <label
              for="motivaciones"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >Motivaciones</label
            >
            <input
              v-model="motivaciones"
              type="text"
              placeholder="Escribe motivaciones"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            />
          </div>

          <div class="mt-7">
            <label
              for="porcentaje"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >Porcentaje</label
            >
            <input
              v-model="porcentaje"
              type="text"
              class="mt-1 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            />
          </div>

          <div class="mt-7">
            <label
              for="marcas"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white mt-7"
              >Marcas</label
            >
            <input
              v-model="marcas"
              type="text"
              class="mt-3 block w-full border-none bg-gray-100 h-11 rounded-xl shadow-lg hover:bg-blue-100 focus:bg-blue-100 focus:ring-0"
            />
          </div>
          <div>
            <button
              class="mt-7 bg-blue-500 w-full py-3 rounded-xl text-white shadow-xl hover:shadow-inner focus:outline-none transition duration-500 ease-in-out transform hover:-translate-x hover:scale-105"
              @click="submit()"
            >
              Registrar
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>
