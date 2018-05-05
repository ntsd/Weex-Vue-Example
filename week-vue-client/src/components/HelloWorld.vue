<template>
	<div class="middle">   
    	<image :src="logo" class="logo" />
		<text class="greeting">Weex + Vue.js Example</text>
		<text class="message">Now, let's use Vue.js to build your Weex app.</text>
		<button v-on:click="goToLobbyButton">go to Lobby</button>
  	</div>	
</template>

<script>
import router from '../router';
export default {
  name: 'Hello',
  methods: {
    goToLobbyButton: function (event) {
    	console.log('go to lobby')
      router.push({path:'/lobby'});
    }
  },
  data () {
    return {
      logo: 'https://gw.alicdn.com/tfs/TB1yopEdgoQMeJjy1XaXXcSsFXa-640-302.png'
    }
  }
}
</script>

<style scoped>
  .middle {
      justify-content: center;
      align-items: center;
    }
  .logo {
    width: 424px;
    height: 200px;
  }
  .greeting {
    text-align: center;
    margin-top: 70px;
    font-size: 50px;
    color: #41B883;
  }
  .message {
    margin: 30px;
    font-size: 32px;
    color: #727272;
  }
</style>