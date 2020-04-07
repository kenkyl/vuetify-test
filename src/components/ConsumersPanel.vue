<template>
    <!-- <v-card
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
    </v-card> -->
    <div class="my-2">
        <v-card v-bind:key="consumer.id" v-for="consumer in consumers">
            <ConsumerComponent v-bind:consumer="consumer" />
        </v-card>
        <v-btn dark>Add Consumer</v-btn>
    </div>

</template>

<script>
import ConsumerComponent from './ConsumerComponent';

export default {
    name: "ConsumersPanel",
    props: [
        "title",
    ],
    components: {
        ConsumerComponent,
    },
    data() {
        return {
            consumers: []
        }
    },
    methods: {
        addConsumer: function(newConsumer) {
            this.consumers = [...this.consumers, newConsumer]
        }
    }
}
</script>