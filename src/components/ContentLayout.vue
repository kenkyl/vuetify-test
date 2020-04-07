<template>
    <v-container
        class="fill-height"
        fluid
    >
        <v-row
          align="center"
          justify="center"
        >
          <p>dashboard row</p>
        </v-row>
        <v-divider class="mx-4" dark></v-divider>
        <v-row
          align="center"
          justify="center"
        >
          <p>producer/consumer row</p>
          <v-col class="shrink">
              <ProducerComponent title="Producer!" message="Producing Environmental Data..."/>
          </v-col>
          <v-divider class="mx-4" dark vertical></v-divider>
          <v-col class="shrink">
              <ConsumersPanel title="Consumers!"/>
          </v-col>
        </v-row>
      </v-container>
</template>

<script>
import ProducerComponent from './ProducerComponent';
import ConsumersPanel from './ConsumersPanel';

export default {
    name: "ContentLayout",
    props: [
        "title",
    ],
    components: {
        ProducerComponent,
        ConsumersPanel
    }
}
</script>