<script>
export default Vue.component('our-button', {
  props: {
    buttonType: {
      type: String,
      default: "button"
    }
  },
  created: function() {
    console.log(this.buttonType);
  },
  template: `
    <div>
      <button v-if="buttonType === 'button'">
        <slot></slot>
      </button>
      <a href="#" v-if="buttonType === 'a'">
        <slot></slot>
      </a>
    </div>
  `
});
</script>
