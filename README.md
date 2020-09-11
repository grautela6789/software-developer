# software-developer
<div><template>
  <div>
    <input type="checkbox" value="foo" v-model="checkedVals">
    <input type="checkbox" value="bar" v-model="checkedVals">
    <input type="checkbox" value="baz" v-model="checkedVals">
  </div>
</template>
<script><span class="javascript">
  export default {
    data() {
      return { checkedVals: ['bar'] }
    },
    methods: {
      shouldBeChecked(val) {
        return this.checkedVals.includes(val)
      },
      updateVals(e) {
        let isChecked = e.target.checked
        let val = e.target.value

        if (isChecked) {
          this.checkedVals.push(val)
        } else {
          this.checkVals.splice(this.checkedVals.indexOf(val), 1)
        }
      }
    }
  }
</script>
</div>
