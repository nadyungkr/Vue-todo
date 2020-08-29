<template>
    <v-card
      max-width="375"
      max-height="812"
      min-width="375"
      min-height="812"
    >
      <v-img
        class="white--text align-end"
        height="400px"
        src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
      >
        <v-card-title
          style="font-size: 32px; line-height: 60px;"
        >
            You've got <br/>
            {i} <br/>
            tasks today!
        </v-card-title>
        <v-text-field
          placeholder="Enter your task here"
          background-color="#fdfefe"
          filled
          rounded
          class="ma-2"
          append-icon="mdi-arrow-right"
        >
        </v-text-field>
      </v-img>
        <v-list 
          rounded
          max-height="400"
          style="overflow-y:auto"
        >
            <v-list-item-group
                v-model="model"
                multiple
            >
                <template v-for="(ToDoItems, i) in ToDoItems">
                    <v-divider
                        v-if="!ToDoItems"
                        :key="`divider-${i}`"
                    >
                    </v-divider>

                    <v-list-item
                        v-else
                        :key="`item-${i}`"
                        :value="ToDoItems"
                        active-class="deep-purple--text text--accent-4"
                    >
                        <template v-slot:default="{ active }">
                            <v-list-item-action>
                                <v-checkbox
                                  :input-value="active"
                                  color="deep-purple accent-4"
                                >
                                </v-checkbox>
                            </v-list-item-action>
                            <v-list-item-content>
                                <v-list-item-title v-text="ToDoItems"></v-list-item-title>
                            </v-list-item-content>
                        </template>
                    </v-list-item>
                </template>
            </v-list-item-group>
        </v-list>
    </v-card>
</template>

<script>
    export default {
    components: {

    },
    data: () => ({
      ToDoItems: [
        'Vue study1',
        'Vue study2',
        'Vue study3',
        'Vue study4',
        'Vue study5',
        'Vue study6',
        'Vue study7',
        'Vue study8',
        'Vue study9',
        'study'
      ],
      model: ['study'],
    }),
  }
</script>

<style lang="scss" scoped>

</style>