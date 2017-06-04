<template>
  <v-layout row-sm column child-flex-xlg wrap class="mb-3">
    <v-card class="">
      <v-card-text>
        <h6> Standard </h6>
        <div>
          <v-btn>Normal</v-btn>
        </div>
        <div>
          <v-btn primary>Primary</v-btn>
        </div>
        <div>
          <v-btn secondary>Secondary</v-btn>
        </div>
        <div>
          <v-btn success>success</v-btn>
        </div>
        <div>
          <v-btn info>info</v-btn>
        </div>
        <div>
          <v-btn warning>warning</v-btn>
        </div>
        <div>
          <v-btn error>error</v-btn>
        </div>
        <div>
          <v-btn disabled>disabled</v-btn>
        </div>
      </v-card-text>
    </v-card>

    <v-card class="">
      <v-card-text>
        <h6> Flat </h6>
        <div>
          <v-btn flat>Normal</v-btn>
        </div>
        <div>
          <v-btn primary flat>Primary</v-btn>
        </div>
        <div>
          <v-btn secondary flat>Secondary</v-btn>
        </div>
        <div>
          <v-btn success flat>success</v-btn>
        </div>
        <div>
          <v-btn info flat>info</v-btn>
        </div>
        <div>
          <v-btn warning flat>warning</v-btn>
        </div>
        <div>
          <v-btn error flat>error</v-btn>
        </div>
        <div>
          <v-btn flat primary disabled>disabled</v-btn>
        </div>
      </v-card-text>
    </v-card>

    <v-card class="">
      <v-card-text>
        <h6> Outline </h6>
        <div>
          <v-btn outline><v-icon left>cloud_upload</v-icon> Normal</v-btn>
        </div>
        <div>
          <v-btn primary outline>Primary</v-btn>
        </div>
        <div>
          <v-btn secondary outline>Secondary</v-btn>
        </div>
        <div>
          <v-btn success outline>success</v-btn>
        </div>
        <div>
          <v-btn info outline>info</v-btn>
        </div>
        <div>
          <v-btn warning outline>warning</v-btn>
        </div>
        <div>
          <v-btn error outline>error</v-btn>
        </div>
        <div>
          <v-btn outline disabled>disabled</v-btn>
        </div>
      </v-card-text>
    </v-card>

    <v-card class="">
      <v-card-text>
        <h6> Round </h6>
        <div>
          <v-btn round>Normal</v-btn>
        </div>
        <div>
          <v-btn primary round>Primary</v-btn>
        </div>
        <div>
          <v-btn secondary round>Secondary</v-btn>
        </div>
        <div>
          <v-btn success round>success</v-btn>
        </div>
        <div>
          <v-btn info round>info</v-btn>
        </div>
        <div>
          <v-btn warning round>warning</v-btn>
        </div>
         <div>
          <v-btn error round>error</v-btn>
        </div>
        <div>
          <v-btn round disabled>disabled</v-btn>
        </div>
      </v-card-text>
    </v-card>

    <v-card class="ma-1">
      <v-card-text>
        <h6> Icons in buttons </h6>
        <div>
          <v-btn><v-icon>cloud_upload</v-icon></v-btn>
        </div>
        <div>
          <v-btn primary>right <v-icon>arrow_forward</v-icon> </v-btn>
        </div>
        <div>
          <v-btn secondary round><v-icon left>arrow_back</v-icon> left</v-btn>
        </div>
        <div>
          <v-btn success outline><v-icon left>check</v-icon> success</v-btn>
        </div>
        <div>
          <v-btn info flat><v-icon left>info</v-icon> flat</v-btn>
        </div>
        <div>
          <v-btn warning small><v-icon left>warning</v-icon> small</v-btn>
        </div>
         <div>
          <v-btn error large><v-icon left>error</v-icon> large</v-btn>
        </div>
        <div>
          <v-btn primary disabled>nope <v-icon right>remove_circle</v-icon> </v-btn>
        </div>
      </v-card-text>
    </v-card>

    <v-card class="ma-1">
      <v-card-text>
        <h6> Icon Buttons </h6>
        <div>
          <v-btn icon><v-icon>cloud_upload</v-icon> </v-btn>
          <v-btn flat icon><v-icon>cloud_upload</v-icon> </v-btn>
        </div>
        <div>
          <v-btn primary icon><v-icon>thumb_up</v-icon> </v-btn>
          <v-btn primary flat icon><v-icon>thumb_up</v-icon> </v-btn>
        </div>
        <div>
          <v-btn secondary icon><v-icon>android</v-icon> </v-btn>
          <v-btn secondary flat icon><v-icon>android</v-icon> </v-btn>
        </div>
        <div>
          <v-btn success icon><v-icon>check_circle</v-icon> </v-btn>
          <v-btn success flat icon><v-icon>check_circle</v-icon> </v-btn>
        </div>
        <div>
          <v-btn info icon><v-icon>info</v-icon> </v-btn>
          <v-btn info flat icon><v-icon>info</v-icon> </v-btn>
        </div>
        <div>
          <v-btn warning small icon><v-icon>warning</v-icon> </v-btn>
          <v-btn warning small flat icon><v-icon>warning</v-icon> </v-btn>
        </div>
         <div>
          <v-btn error icon large><v-icon>error</v-icon> </v-btn>
          <v-btn error flat icon large><v-icon>error</v-icon> </v-btn>
        </div>
        <div>
          <v-btn error icon disabled><v-icon>remove_circle</v-icon> </v-btn>
          <v-btn error flat icon disabled><v-icon>remove_circle</v-icon> </v-btn>
        </div>
        <div>
          <v-btn error outline icon><v-icon>remove_circle</v-icon> </v-btn>
        </div>
      </v-card-text>
    </v-card>

    <v-card class="ma-1">
      <v-card-text>
        <div>
          <v-btn floating> <v-icon>cloud_upload</v-icon> </v-btn>
        </div>
        <div>
          <v-btn floating primary> <v-icon>add</v-icon> </v-btn>
        </div>
        <div>
          <v-btn floating secondary small> <v-icon>thumb_up</v-icon> </v-btn>
        </div>
        <div>
          <v-btn floating success large> <v-icon>add</v-icon> </v-btn>
        </div>
        <div>
          <v-btn floating info small> <v-icon>add</v-icon> </v-btn>
          <v-btn floating warning small> <v-icon>add</v-icon> </v-btn>
        </div>
        <div>
          <v-btn floating error small> <v-icon>add</v-icon> </v-btn>
          <v-btn floating warning disabled small> <v-icon>remove_circle</v-icon> </v-btn>
        </div>
      </v-card-text>
    </v-card>

    <v-card class="ma-1">
      <v-card-text>
        <h6>Sizing </h6>
        <div>
          <v-btn small >small</v-btn>
        </div>

        <div>
          <v-btn primary>normal</v-btn>
        </div>
        <div>
          <v-btn success large>Large</v-btn>
        </div>
        <div>
          <v-btn small flat>flat sm</v-btn>
        </div>
        <div>
          <v-btn primary large flat>flat lg</v-btn>
        </div>
        <div>
          <v-btn info small round>small</v-btn>
        </div>
        <div>
          <v-btn error large round>large</v-btn>
        </div>
      </v-card-text>
    </v-card>

  </v-layout>

</template>

<script>

</script>

<style lang="stylus">

</style>
