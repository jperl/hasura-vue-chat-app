<template>
  <div class="mb-5">
    <div class="d-flex justify-end align-center" v-if="isMine">
      <v-card class="text-break">
        <v-card-text>
          {{ message.content }}
        </v-card-text>
      </v-card>
      <v-avatar :color="message.iconColor" size="32" class="ml-3">
        <v-icon dark>mdi-account</v-icon>
      </v-avatar>
    </div>
    <div class="d-flex justify-start align-center" v-else>
      <v-avatar :color="message.iconColor" size="32" class="mr-3">
        <v-icon dark>mdi-account</v-icon>
      </v-avatar>
      <v-card class="text-break">
        <v-card-text>
          {{ message.content }}
        </v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  name: "MessageCard",
  props: {
    message: {
      type: Object,
      required: true
    },
    isMine: {
      type: Boolean,
      default: false
    }
  }
};
</script>
