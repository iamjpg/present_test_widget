<template>
<div id="johnnyonit">
  <div id="joi-tagline">
    <h3>
      For home service solutions in real-time<br />
      Download Johnny On It:
    </h3>

    <img src="https://www.qr-code-generator.com/wp-content/themes/qr/new_structure/markets/core_market_full/generator/dist/generator/assets/images/websiteQRCode_noFrame.png" width="200" /></div>

  <table id="joi-agent">
    <tbody>
      <tr>
        <td>
          <div :style="returnAgentImage()" id="joi-agent-image">&nbsp;</div>
        </td>
        <td>{{ displayName }}<br />
          <span v-if="title !== ''">{{ title }} / </span>{{ officeLegalName }}</td>
      </tr>
    </tbody>
  </table>
  <div id="joi-logo"><img src="https://www.jonnyonit.com/wp-content/uploads/2018/11/JOI_Logo.svg" width="200" /></div>
</div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return window.MoxiData.presentation.agentData[0]
  },
  methods: {
    returnAgentImage: function() {
      return 'background-image:url(' + this.photo + ')';
    },
    returnPhone: function() {
      if (this.mobilePhone) {
        return this.mobilePhone;
      } else if (this.mainPhone) {
        return this.mainPhone;
      } else if (this.officePhone) {
        return this.officePhone
      } else {
        return 'No Phone Available'
      }
    }
  }
}
</script>

<style lang="scss">
#johnnyonit {
  font-family: Helvetica, Verdana, Arial, sans-serif;
  position: relative;
  height: calc(100vh - 110px);
  background-image: url('https://i.imgur.com/DYdWBME.png');
  color: #222;
  padding: 50px;
}
#johnnyonit {
  font-size: 24px;
}

#johnnyonit table {
  width: unset;
}

#joi-agent {
  position: absolute;
  bottom: 50px;
  left: 50px;
}

#joi-logo {
  position: absolute;
  bottom: 109px;
  right: 50px;
}

#joi-agent-image {
  width: 150px;
  height: 150px;
  border-radius: 100%;
  background-size: cover;
  background-position: center;
  border: 3px solid #37E6F2;
}
</style>
