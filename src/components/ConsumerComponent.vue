<template>
    <v-card
        class="mx-auto"
        max-width="344"
        outlined
    >
        <v-card-title>
            <div>
                {{consumer.title}}
            </div>
        </v-card-title>
        <v-card-text>
            <div>
                {{consumer.message}}
            </div>
        </v-card-text>
    </v-card>
</template>

<script>

export default {
    name: "ConsumerComponent",
    props: [
        "consumer",
    ]
}
</script>