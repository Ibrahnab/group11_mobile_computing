<template>
    <div>
        <p>asd</p>
            <b-form-radio-group
                id="btn-radios-2"
                v-model="selected"
                :options="options"
                :aria-describedby="ariaDescribedby"
                button-variant="outline-primary"
                size="lg"
                name="radio-btn-outline"
                buttons
            ></b-form-radio-group>
    </div>
</template>

<script>
export default {
  name: 'switch',
  data() {
    return {
      selected: 'radio1',
      options: [
        { text: 'Radio 1', value: 'radio1' },
        { text: 'Radio 3', value: 'radio2' },
        { text: 'Radio 3 (disabled)', value: 'radio3', disabled: true },
        { text: 'Radio 4', value: 'radio4' }
      ],
      props: {
        something: String
      }
    }
  }
}
</script>
