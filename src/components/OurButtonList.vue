<script>
import OurButton from './OurButton.vue';

export default Vue.component('our-button-list', {
  props: ['button-type'],
  data: function() {
    return {
      types:["submit", "cancel"]
    };
  },
  components: {
    OurButton
  },
  template: `
    <div>
      <div v-for="type in types">
        <our-button :buttonType="buttonType">
          <slot :name="type"></slot>
        </our-button>
      </div>
    </div>
  `
});
</script>
