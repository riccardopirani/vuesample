<template>
<div>
    <h2>ChartName: {{chartName}}</h2>
</div>
</template>

<script>
import axios from "axios";
export default {
    name: "UserComponent",
    props: {
        msg: String,
    },
    data () {
    return {
      info: null,
      chartName: null
    }
  },
  mounted () {
    axios
      .get('https://api.coindesk.com/v1/bpi/currentprice.json')
      .then(response => this.chartName=response.data.chartName)
      console.log(this.info);
  }
};
</script>
