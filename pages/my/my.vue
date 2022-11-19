<template>
	<view class="my-container">
		<!-- <my-login v-if="!token"></my-login>
    <my-userinfo v-else></my-userinfo> -->
    
    <my-login v-if="!token"></my-login>
    <my-userinfo v-else></my-userinfo>

	</view>
</template>

<script>
// 导入自己封装的 mixin 模块
import badgeMix from '@/mixins/tabbar-badge.js'
import { mapState } from 'vuex'
export default {
    mixins: [badgeMix],
		data() {
			return {
				
			};
		},
    computed: {
      ...mapState('m_user',['token'])
    }
    
	}
</script>

<style lang="scss">
page,
.my-container {
  height: 100%;
}
</style>
