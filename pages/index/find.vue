<template>
	<view>
		<view class="uni-flex uni-row">
			<view class="kyle-2-1">
				<view class="kyle-padding-sm" v-for="story in stories" v-if="story.id % 2 === 0" :key="story.id" @click="goDetailPage(story)">
					<image class="kyle-1-1 kyle-radius" :src="story.img"></image>
					<text>{{story.title}}</text>
				</view>
			</view>
			<view class="kyle-2-1">
				<view class="kyle-padding-sm" v-for="story in stories" v-if="story.id % 2 === 1" :key="story.id" @click="goDetailPage(story)">
					<image class="kyle-1-1 kyle-radius" :src="story.img"></image>
					<text>{{story.title}}</text>
				</view>
			</view>		
		</view>
		<view class="kyle-footer"></view>
	</view>
</template>
<script>
	export default {
		components: {
			
		},
		data() {
			return {
				stories:[
					{id:1,img:"../../static/img/img1.jpg",title:"520表白神器"},
					{id:2,img:"../../static/img/img2.jpg",title:"想要挽回爱人，我们必须注重的一些挽回技巧"},
					{id:3,img:"../../static/img/img3.jpg",title:"教你看出别人是不是暗恋你"},
					{id:4,img:"../../static/img/img4.jpg",title:"恋爱专属表情包"},
					{id:5,img:"../../static/img/img1.jpg",title:"恋爱专属表情包"},
					{id:6,img:"../../static/img/img2.jpg",title:"恋爱专属表情包"},
					{id:7,img:"../../static/img/img3.jpg",title:"恋爱专属表情包"},
					{id:8,img:"../../static/img/img4.jpg",title:"恋爱专属表情包"},
					{id:9,img:"../../static/img/img1.jpg",title:"恋爱专属表情包"},
					{id:10,img:"../../static/img/img2.jpg",title:"恋爱专属表情包"}
				]
			}
		},
		methods:{
			goDetailPage(story) {
				const pageUrl = "/pages/articleInfo?id="+story.id+"&title="+story.title;
				uni.navigateTo({
					url: pageUrl
				})
			}
		}
	}
</script>

<style>
	
</style>
