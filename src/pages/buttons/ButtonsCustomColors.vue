<template>

  <v-layout row-sm column child-flex-xlg wrap class="mb-3">
    <v-card class="">
      <v-card-text>
        <h6> Standard </h6>
        <div>
          <v-btn class="pink">pink</v-btn>
        </div>
        <div>
          <v-btn class="purple white--text">Purple</v-btn>
        </div>
        <div>
          <v-btn disabled class="purple white--text">Purple</v-btn>
        </div>
      </v-card-text>
    </v-card>

    <v-card class="">
      <v-card-text>
        <h6> Flat </h6>
        <div>
          <v-btn flat class="pink--text">pink</v-btn>
        </div>
        <div>
          <v-btn flat class="purple--text">Purple</v-btn>
        </div>
      </v-card-text>
    </v-card>

    <v-card class="">
      <v-card-text>
        <h6> Outline </h6>
        <div>
          <v-btn outline class="pink--text">pink</v-btn>
        </div>
        <div>
          <v-btn outline class="purple--text">purple</v-btn>
        </div>
      </v-card-text>
    </v-card>

    <v-card class="">
      <v-card-text>
        <h6> Round </h6>
        <div>
          <v-btn round class="pink">pink</v-btn>
        </div>
        <div>
          <v-btn round class="purple white--text">purple</v-btn>
        </div>
      </v-card-text>
    </v-card>

    <v-card class="ma-1">
      <v-card-text>
        <h6> Icons in buttons </h6>
        <div>
          <v-btn class="pink"><v-icon>cloud_upload</v-icon></v-btn>
        </div>
        <div>
          <v-btn class="purple grey--text">right <v-icon class="grey--text">arrow_forward</v-icon> </v-btn>
        </div>
      </v-card-text>
    </v-card>

    <v-card class="ma-1">
      <v-card-text>
        <h6> Icon Buttons </h6>
        <div>
          <v-btn icon class="pink"><v-icon>cloud_upload</v-icon> </v-btn>
          <v-btn flat icon><v-icon class="pink--text">cloud_upload</v-icon> </v-btn>
        </div>
        <div>
          <v-btn icon class="purple"><v-icon class="white--text">thumb_up</v-icon> </v-btn>
          <v-btn flat icon ><v-icon class="purple--text">thumb_up</v-icon> </v-btn>
        </div>
      </v-card-text>
    </v-card>

    <v-card class="ma-1">
      <v-card-text>
        <div>
          <v-btn floating class="pink"> <v-icon>cloud_upload</v-icon> </v-btn>
        </div>
        <div>
          <v-btn floating class="purple"> <v-icon>add</v-icon> </v-btn>
        </div>
      </v-card-text>
    </v-card>

  </v-layout>

</template>

<script>

</script>

<style lang="stylus">

</style>
