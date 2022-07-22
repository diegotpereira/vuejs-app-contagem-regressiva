<template>
    <v-form class="pt-16">
        <v-rom class="d-flex justify-center align-center">
            <v-col sm="8" md="16" class="d-flex flex-col justify-center">
                <v-text-field class="bg-black-lighten3" label="INSCREVA-SE!" placeholder="DIGITE SEU ENDEREÇO DE EMAIL :)" variant="outlined">

                </v-text-field>
            </v-col>
            <v-col>
                <div class="d-flex justify-center align-center my-n8">
                    <v-btn class="opacidade" width="150px" href="https://www.yusufonaran.me" target="_blank">Enviar</v-btn>
                </div>
            </v-col>
        </v-rom>
    </v-form>
</template>
<script>
export default {
    name: 'InscrevaSe',
    data() {
        return {
            
        }
    },
}
</script>
<style>
.opacidade {
    background: rgba(255, 255, 255, 0.7);
}
</style>