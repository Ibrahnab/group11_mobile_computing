<template>
    <div>
        <h3 id='title'>WHAT ALLERGIES DO YOU HAVE?</h3>
        <b-button-group size="sm">
            <b-button
                v-for="(btn, idx) in buttons"
                :key="idx"
                :pressed.sync="btn.state"
                variant="primary"
            >
                {{ btn.caption }}
            </b-button>
        </b-button-group>
        <p id='add_allegy'>+Add allergy</p>
    </div>
</template>

<script>
export default {
  data() {
    return {
      myToggle: false,
      buttons: [
        { caption: 'Dairy', state: false },
        { caption: 'Fish', state: false },
        { caption: 'Peanuts', state: false },
        { caption: 'Eggs', state: false },
        { caption: 'Gluten', state: false },
        { caption: 'Soy', state: false }
      ]
    }
  },
  computed: {
    btnStates() {
      return this.buttons.map(btn => btn.state)
    }
  }
}
</script>

<style scope>
.title{
  color: #FD5523;
}

#add_allegy{
  color:#FD5523;
}

.btn {
  background-color: #FEFCD5 !important;
  color: #00A676 !important;
  border-color: #FD5523 !important;
}

.btn :hover {
  border: none !important;
}
</style>
