<template>
  <q-page class="q-pa-md">

    <center>
      <p class="text-h5">😃 Welcome! Choose a board to explore! 🗺️</p>
    </center>

    <div class="row justify-center wrap">

      <!-- Orange Pi -->
      <div class="col-auto">
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
      <div class="col-auto">
        <q-card class="my-card" flat bordered>
          <q-card-section horizontal>
            <q-img
              class="col"
              src="statics/1525646171318.boardFront.png"
              style="background-color: #676767;"
            >
              <div
                :class="board2Trans"
              >
                <div class="text-h6">Roduino</div>
                <div class="text-subtitle2">Homemade Arduino by Rodrigo Costa</div>
              </div>
            </q-img>

            <q-card-actions vertical class="justify-around q-px-md">
              <q-btn flat round color="info" icon="info" @click="infoClick(2)" />
              <q-btn flat round color="green" icon="play_arrow" />
            </q-card-actions>
          </q-card-section>
        </q-card>
      </div>

      <!-- Roduino -->
      <div class="col-auto">
        <q-card class="my-card" flat bordered>
          <q-card-section horizontal>
            <q-img
              class="col"
              src="statics/1525646171318.boardFront.png"
              style="background-color: #676767;"
            >
              <div
                :class="board2Trans"
              >
                <div class="text-h6">Roduino</div>
                <div class="text-subtitle2">Homemade Arduino by Rodrigo Costa</div>
              </div>
            </q-img>

            <q-card-actions vertical class="justify-around q-px-md">
              <q-btn flat round color="info" icon="info" @click="infoClick(2)" />
              <q-btn flat round color="green" icon="play_arrow" />
            </q-card-actions>
          </q-card-section>
        </q-card>
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
      board2Hide: false,
      board1Trans: 'absolute-bottom hidden',
      board2Trans: 'absolute-bottom hidden'
    }
  },
  methods: {
    infoClick (ix) {
      console.log('Info Click ' + ix)
      if (ix === 1) {
        this.board1Hide = !this.board1Hide
        this.board1Hide ? this.board1Trans = 'absolute-bottom animated slideInUp' : this.board1Trans = 'absolute-bottom animated slideOutDown'
      } else if (ix === 2) {
        this.board2Hide = !this.board2Hide
        this.board2Hide ? this.board2Trans = 'absolute-bottom animated slideInUp' : this.board2Trans = 'absolute-bottom animated slideOutDown'
      }
    }
  }
}
</script>
