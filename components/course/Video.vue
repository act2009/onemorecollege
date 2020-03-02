<template>
	<!--video play-->
    <view>
        <view class="uni-padding-wrap uni-common-mt">
            <view>
                <video id="myVideo" :src="videoSrc"
                    @error="videoErrorCallback" controls></video>
            </view>



        </view>
    </view>
</template>

<script>
	export default {
		props:{
			videoSrc:String
		},
	    data() {
	        return {

	        }
	    },
	    onReady: function(res) {
	   
	        this.videoContext = uni.createVideoContext('myVideo')
	        
	    },
	    methods: {
	        sendDanmu: function() {
	            this.videoContext.sendDanmu({
	                text: this.danmuValue,
	                color: this.getRandomColor()
	            });
	            this.danmuValue = '';
	        },
	        videoErrorCallback: function(e) {
	            uni.showModal({
	                content: e.target.errMsg,
	                showCancel: false
	            })
	        },
	        getRandomColor: function() {
	            const rgb = []
	            for (let i = 0; i < 3; ++i) {
	                let color = Math.floor(Math.random() * 256).toString(16)
	                color = color.length == 1 ? '0' + color : color
	                rgb.push(color)
	            }
	            return '#' + rgb.join('')
	        }
	    }
	}
</script>

<style scoped>
	uni-video{
		width: 100%;
		height: 450rpx;
	}
</style>
