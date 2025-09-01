<template>
    <div class="contenedor">

        <div v-for="pais in paises" :key="pais.id" class="carta">
            <img :src="require(`@/assets/${pais.url}`)" alt="" class="imagen-contenedor">
            <div @click="mostrarPais(pais.nombre)" class="nombre-contenedor">{{ pais.nombre }}</div>
            <div v-if="pais.habitantes > tazaHabitantesMinima" class="habitantes-contenedor verde">{{ pais.habitantes }}</div>
            <div v-else class="habitantes-contenedor rojo">{{ pais.habitantes }}</div>
        </div>

      
    </div>
</template>

<script>
export default {
    name: 'MiCards',

    //   Aquí inicializo mis variables
    data() {
        return {
            tazaHabitantesMinima: 10000000,
            paises: [
                {
                    id: 1,
                    nombre: "NORUEGA",
                    url: "paisaje-1.png",
                    habitantes: 9567890
                },
                {
                    id: 2,
                    nombre: "DINAMARCA",
                    url: "paisaje-2.jpg",
                    habitantes: 11567890
                },
                {
                    id: 3,
                    nombre: "CANADA",
                    url: "paisaje-3.jpg",
                    habitantes: 16590890
                },
                {
                    id: 4,
                    nombre: "AUSTRALIA",
                    url: "paisaje-4.jpeg",
                    habitantes: 2567890
                },{
                    id: 5,
                    nombre: "NUEVA ZELANDA",
                    url: "paisaje-5.jpeg",
                    habitantes: 5000000
                },
                {
                    id: 6,
                    nombre: "JAPON",
                    url: "paisaje-6.jpeg",
                    habitantes: 12647600
                },
                {
                    id: 7,
                    nombre: "CHINA",
                    url: "paisaje-7.jpeg",
                    habitantes: 21399340
                },
                {
                    id: 8,
                    nombre: "RUSIA",
                    url: "paisaje-8.jpeg",
                    habitantes: 43851000
                },
                {
                    id: 9,
                    nombre: "BRASIL",
                    url: "paisaje-9.jpeg",
                    habitantes: 4385100
                },
                {
                    id: 10,
                    nombre: "ARGENTINA",
                    url: "paisaje-10.jpeg",
                    habitantes: 10412400
                },
                {
                    id: 11,
                    nombre: "GRECIA",
                    url: "paisaje-11.jpeg",
                    habitantes: 21399340
                },
                {
                    id: 12,
                    nombre: "COLOMBIA",
                    url: "paisaje-12.jpeg",
                    habitantes: 43851000
                },
                {
                    id: 13,
                    nombre: "EGIPTO",
                    url: "paisaje-13.jpeg",
                    habitantes: 4385100
                },
                {
                    id: 14,
                    nombre: "PERU",
                    url: "paisaje-14.jpeg",
                    habitantes: 59308690
                },
                {
                    id: 15,
                    nombre: "HAWAII",
                    url: "paisaje-15.jpeg",
                    habitantes: 10412400
                },
                {
                    id: 16,
                    nombre: "COREA DEL NORTE",
                    url: "paisaje-16.jpeg",
                    habitantes: 36910560
                },
                {
                    id: 17,
                    nombre: "COREA DEL SUR",
                    url: "paisaje-17.jpeg",
                    habitantes: 84339067
                },
                {
                    id: 18,
                    nombre: "ALEMANIA",
                    url: "paisaje-18.jpeg",
                    habitantes: 206139589
                },
                {
                    id: 19,
                    nombre: "INDIA",
                    url: "paisaje-19.jpeg",
                    habitantes: 1380004385
                },
                {
                    id: 20,
                    nombre: "FRANCIA",
                    url: "paisaje-20.jpeg",
                    habitantes: 331002651
                }
            ]
        }
    },

    //Aquí van las funciones
    methods: {
        mostrarPais(pais) {
            alert("CLIC EN EL PAIS " + pais);
            // alert("HOLA " + this.nombre);
        }
    },

    //INICIALIZADOR
    created() {
        // this.hola();
    }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.contenedor {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 50px 45px;
    height: 300px;
}

.carta {
   
    width: 100%;
    height: 100%;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    border-radius: 5% 5% 0 0;

}

.imagen-contenedor {
    width: 100%;
    height: 80%;
    margin: 0;
    object-fit: cover;
    object-position: center center;
    border-radius: 5% 5% 0 0;
}

.imagen-contenedor:hover {
    background-image: rgba(0, 0, 0, 0.6);
    cursor: pointer;
}

.nombre-contenedor {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 10%;
    background-color: darkgreen;
    color: white;
    cursor: pointer;
}

.habitantes-contenedor {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 10%;
    color: white;
}

.verde{
    background-color: rgb(0, 69, 0);
}

.rojo{
     background-color: rgb(241, 5, 5);
}
</style>
