<template>
    <v-container>
        <v-row>
            <v-col>
                <v-img 
                :height="altura"
                v-bind:src="imatge"
                >
                <!-- fem v-bind del source amb imatge-->
                <v-container>
                    <v-row>
                        <v-col align="end">
                            <div style="color:white">Photo author: @{{autor}}</div>
                        </v-col>
                    </v-row>
                </v-container>
                </v-img>
            </v-col>
        </v-row>
    </v-container>
</template>
<script>
        export default{
            props:["imatge","autor","altura"]
        }

</script>