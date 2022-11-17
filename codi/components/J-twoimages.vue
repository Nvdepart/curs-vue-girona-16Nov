<template>
<v-container>
    <v-row>
        <v-col cols="6">
            <v-img 
            :src="imatge1"
            :height="altura">
            <v-container>
                <v-row>
                    <v-col align="end" color="white">
                        {{text1}}
                    </v-col>
                </v-row>
            </v-container>
            </v-img>
        </v-col>
        <v-col cols="6">
            <v-img 
            :src="imatge2"
            :height="altura">
            <v-container>
                <v-row>
                    <v-col align="end">
                        {{text2}}
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
    props:["imatge1", "imatge2", "text1","text2","altura"]
}
</script>