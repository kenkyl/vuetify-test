<template>
    <v-card>
        
    </v-card>
</template>

<script>
export default {
    name: "ProducerComponent",
    props: [
        "message"
    ],
    data() {
        return {
            id: ''
        }
    },
    created: function() {
        console.log("Producer is in the building, wuba luba dub dub!");
        this.id = Math.random() * 1000;
    }
}
</script>