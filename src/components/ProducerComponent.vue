<template>
    <v-card
        class="mx-auto"
        max-width="344"
        outlined
    >
        <v-card-title>
            <div>
                {{title}}
            </div>
        </v-card-title>
        <v-card-text>
            <div>
                {{message}}
            </div>
        </v-card-text>
    </v-card>
</template>

<script>
export default {
    name: "ProducerComponent",
    props: [
        "title",
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