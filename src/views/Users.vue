<template>
  <v-container>
    <v-row>
      <v-col cols="4">
        <v-card class="mx-auto" max-width="344" outlined>
          <v-list-item three-line>
            <v-list-item-content>
              <div class="overline mb-4">OVERLINE</div>
              <v-list-item-title class="headline mb-1"
                >Headline 5</v-list-item-title
              >
              <v-list-item-subtitle
                >Greyhound divisely hello coldly
                fonwderfully</v-list-item-subtitle
              >
            </v-list-item-content>

            <v-list-item-avatar
              tile
              size="80"
              color="grey"
            ></v-list-item-avatar>
          </v-list-item>

          <v-card-actions>
            <v-btn text>Button</v-btn>
            <v-btn text>Button</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    placeHolderData: undefined
  }),
  props: {
    count: {
      type: Number,
      default: 1
    }
  },
  methods: {
    initData: async () => {
      const req = await fetch(
        `https://jsonplaceholder.typicode.com/posts/${this.count}`
      )
      if (req.ok) {
        this.placeHolderData = await req.json()
      }
    }
  }
}
</script>

<style lang="scss" scoped></style>
