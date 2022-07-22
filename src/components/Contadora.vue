<template>
    <div class="d-flex justify-space-around pt-15">
        <v-card class="opacitybg mx-auto" width="150px" weight="120px" href="https://www.yusufonaran.me" target="_blank">
            <v-card-text>
                <p class="text-h2 text--primary text-center font-weight-regular">
                    {{ anos }}
                </p>
            </v-card-text>
            <v-card-actions>
                <v-btn>
                    Anos
                </v-btn>
            </v-card-actions>
        </v-card>
        <v-card class="opacitybg mx-auto" width="150px" weight="120px" href="https://www.yusufonaran.me" target="_blank">
            <v-card-text>
                <p class="text-h2 text--primary text-center font-weight-regular">
                    {{ dias % 365 }}
                </p>
            </v-card-text>
            <v-card-actions>
                <v-btn>
                    DIAS
                </v-btn>
            </v-card-actions>
        </v-card>

        <!-- ---------------------->
        <v-card class="opacitybg-mx-auto" width="150px" weight="120px" href="https://www.yusufonaran.me" target="_blank">
            <v-card-text>
                <p class="text-h2 text--primary text-center font-weight-regular">
                    {{ horas % 24}}
                </p>
            </v-card-text>
            <v-card-actions>
                <v-btn>
                    Horas
                </v-btn>
            </v-card-actions>
        </v-card>

        <!-- ----------------------->
        <v-card class="opacitybg mx-auto" width="150px" weight="120px" href="https://www.yusufonaran.me" target="_blank">
            <v-card-text>
                <p class="text-h2 text--primary text-center font-weight-regular">
                    {{ minutos % 60}}
                </p>
            </v-card-text>
            <v-card-actions>
                <v-btn>
                    MINUTOS
                </v-btn>
            </v-card-actions>
        </v-card>

        <!-- ----------------------->
        <v-card class="opacitybg mx-auto" width="150px" weight="120px" href="https://www.yusufonaran.me" target="_blank">
            <v-card-text>
                <p class="text-h2 text--primary text-center font-weight-regular">
                    {{ segundos % 60}}
                </p>
            </v-card-text>
            <v-card-actions>
                <v-btn>
                    SEGUNDOS
                </v-btn>
            </v-card-actions>
        </v-card>
    </div>
</template>
<script>
import { ref } from '@vue/reactivity'

export default {
    name: 'ContadoraCartao',
    data() {
        return {
            
        }
    },
    setup() {
        const anos = ref(0)
        const dias = ref(0)
        const horas = ref(0)
        const minutos = ref(0)
        const segundos = ref(0)
        const dataAlmoco = new Date('30 December 2030')
        console.log(dataAlmoco);

        setInterval(() => {
            const atualData = new Date()
            const horaAlmoco = dataAlmoco - atualData

            segundos.value = parseInt(horaAlmoco / 1000)
            minutos.value = parseInt(segundos.value / 60)
            horas.value = parseInt(minutos.value / 60)
            dias.value = parseInt(horas.value / 24)
            anos.value = parseInt(dias.value / 365)

        }, 1000);

        return { anos, dias, horas, minutos, segundos }
    }
}
</script>
<style>
.opacitybg {
    background: rgba(255, 255, 255, 0.7);
}
</style>