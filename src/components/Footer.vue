<template>
    <v-footer color="primary lighten-1" padless>
        <v-row justify="center" no-gutters>
            <v-btn v-for="icon in icons" :key="icon" color="white" text rounded class="my-2">
                <v-icon>{{ icon }}</v-icon>
            </v-btn>
            
            <v-col class="primary lighten-2 py-4 text-center white--text">
                {{ new Date().getFullYear() }} - <strong>DTP Software</strong>
            </v-col>
        </v-row>
    </v-footer>
</template>
<script>
export default {
    name: 'FooterBg',
    data: () => ({
        links: [
            'Home',
            'Inscreva-se'
        ],
        icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-instagram',
        'mdi-youtube',
      ],
    })
}
</script>