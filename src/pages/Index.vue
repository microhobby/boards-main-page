<template>
  <q-page class="q-pa-md">

    <div class="row">

      <!-- Orange Pi -->
      <div class="col">
        <q-card class="my-card" flat bordered>
          <q-card-section horizontal>
            <q-img
              class="col"
              src="statics/1521880910218.boardFront.png"
              style="background-color: #676767"
            >
              <div
                :class="board1Trans"
              >
                <div class="text-h6">Orange Pi Zero</div>
                <div class="text-subtitle2">Open-source single-board computer. 48 mm × 46mm</div>
              </div>
            </q-img>

            <q-card-actions vertical class="justify-around q-px-md">
              <q-btn flat round color="info" icon="info" @click="infoClick(1)" />
              <q-btn flat round color="green" icon="play_arrow" />
            </q-card-actions>
          </q-card-section>
        </q-card>
      </div>

      <!-- Roduino -->
      <div class="col">
      </div>

    </div>

  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',

  data () {
    return {
      board1Hide: false,
      board1Trans: 'absolute-bottom hidden'
    }
  },
  methods: {
    infoClick (ix) {
      console.log('Info Click ' + ix)
      if (ix === 1) {
        this.board1Hide = !this.board1Hide
        this.board1Hide ? this.board1Trans = 'absolute-bottom animated slideInUp' : this.board1Trans = 'absolute-bottom animated slideOutDown'
      }
    }
  }
}
</script>
