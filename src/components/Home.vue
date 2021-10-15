<template>
    <div>
        <h3>{{apellido}}</h3>
        <h1>HOLAAAAAA {{ pepe }}</h1>
        <HelloWorld2 />
        <button @click="mostrarNombre()">aceptar</button>
    </div>
</template>

<script>
    import HelloWorld2 from "./HelloWorld2.vue";

    export default {
        components: { HelloWorld2 },
        name: "Home",
        props: {
            pepe: String,
        },
        data:()=>({
            nombre:"julieta",
            apellido:"diaz",
            mail:"jd@jd.jd",
            users:["pedro","juan","carlos"]
        }),
        mounted(){
            this.apellido="prpr"
        },
        methods:{
            mostrarNombre(){
                alert(this.nombre);
            },
            mostrarApellido(){},
            mostrarMail(){},
        },
        computed:{
            datos(){return "xxxxxxx"+this.nombre+"xxxxxxx"}
        },
        watch:{
            datos(){
                
            }
        },

    };
</script>
