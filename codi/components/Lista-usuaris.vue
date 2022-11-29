<template>
    <v-container>
        <v-row>
            <v-col>
                Usuaris
                <br>
            {{missatge}}
                <br>
                <v-btn @click="descarregarDades()">Descarregar</v-btn>
                <br>
                <v-btn @click="netejarDades()">Netejar</v-btn>
                <br>
               <v-row>
                <v-col cols="3"
                v-for="usuari in resposta.users" :key="usuari.id">
                   <v-img 
                   :src="usuari.image">

                   </v-img>  
                </v-col>
               </v-row>
            
                <!--
                    <pre v-if="typeof(resposta)=='object'">
                {{resposta["users"][0].email}} 
                </pre>
                 -->
                
            </v-col>
        </v-row>
    </v-container>
</template>
<script>
        export default{
            mounted(){
                    // Codi que s'executa quan es monta el component
                    console.log(this.resposta)
                    this.descarregarDades()
            },
            data(){
                return{
                    missatge:"Bon dia",
                    resposta: false

                }
            },
            methods:{
                async descarregarDades(){
                        this.resposta ="les dades estan caragan"
                        console.log("Descarregant dades..")
                        console.log(this.resposta) // False
                        const respostaAxios = await this.$axios
                        .$get('https://dummyjson.com/users')
                        this.resposta = respostaAxios
                },
                    netejarDades(){
                        this.resposta = false
                    
            }
        }
    }
           
                   
</script>