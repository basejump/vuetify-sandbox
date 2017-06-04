<template>
<v-container fluid class="text-xs-center">
  <buttons-default></buttons-default>
  <ButtonsCustomColors></ButtonsCustomColors>
  <DenseCard></DenseCard>
</v-container>
</template>

<script>
import ButtonsDefault from './buttons/ButtonsDefault.vue'
import ButtonsCustomColors from './buttons/ButtonsCustomColors.vue'
import DenseCard from './cards/DenseCard.vue'

export default {
  components: {ButtonsDefault,ButtonsCustomColors,DenseCard},
  data () {
    return {
      xxx: 'yyy'
    }
  }
}
</script>

<style lang="stylus">

</style>
