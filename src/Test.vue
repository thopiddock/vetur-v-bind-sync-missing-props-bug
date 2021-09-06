<template>
  <div>
    <!-- Standard property - sync -->
    <child :title="title" :content="content" />
    
    <!-- Standard property + sync -->
    <child :title.sync="title" :content.sync="content" />

    <!-- v-bind wrapped - sync -->
    <child v-bind="wrapped" />

    <!-- v-bind wrapped + sync -->
    <child v-bind.sync="wrapped" />
  </div>
</template>

<script>
import * as _ from 'lodash'
import Child from './Child.vue'

export default {
  components: { Child },
  props: ['foo', 'bar'],
  data() {
    const title = 'Title of win'
    const content = "I'm some content"

    return {
      title,
      content,

      wrapped: {
        title,
        content
      }
    }
  }
}
</script>