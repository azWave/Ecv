<template>
  <table class="cell bottom">
      <tbody>
          <tr>
              <td><h2><label for="file">{{text}} :</label></h2></td>
          </tr>
          <tr>
              <td>
                <progress id="file" max="100" :value="pourcent"> {{pourcent}}% </progress>
              </td>
          </tr>
      </tbody>
  </table>
</template>

<script>
export default {
    props: {
    text:{
        type: String,
        required: true,
    },
    pourcent: {
      type: String,
      required: true,
    },
    },

}
</script>

<style>
.tableGlobal{
    text-align: center;
    margin: auto;
}
.tableGlobal td {
    width: 15%;
    margin-left: 10%;
    margin-right: 10%;   
}
.bottom {
    padding-bottom: 10%;
}
.tableGlobal h2{
    margin: 0%;
}

::-webkit-progress-bar {
   background-color: #73A1F8;
}
</style>