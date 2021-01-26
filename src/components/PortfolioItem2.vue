<template>
  <v-container grid-list-xl>
    <v-layout wrap>
      <v-flex xs12 sm6 lg4 v-for="project in projects" :key="project.id">
        <v-card hover :href="project.url" height="100%">
          <v-card-media height="330px" :src="getThumbnailUrl(project.name)">
          </v-card-media>

          <v-divider />

          <v-card-text>
            <h3 v-html="project.name" class="mb-2"></h3>
            <v-chip
              class="white--text"
              color="info"
              small
              v-for="tag in project.tags"
              :key="tag.id"
            >
              {{ tag }}
            </v-chip>
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {};
</script>

<style>
</style>