# WXLottie
WXLottie is a [weex](https://github.com/apache/incubator-weex) component  plugin using [lottie](https://github.com/airbnb/lottie-ios)

WeexPack version： >= 0.2.0
WeexSDK ： >= 0.15.1

### WeexLottie

[lottie project](https://github.com/airbnb/lottie-ios)

[WeexLottie](https://github.com/acton393/WeexLottie)

usage:

1. run start script in your terminal
2. front-end
  vue description:

```
<template>
  <div style='margin-top:50px;margin-left:150px'>
	<text style='margin-left:150px;border-width:2px;width:80px;' @click='click' :value="status"></text>
    <lottie src='http://127.0.0.1:12580/examples/animations/LottieWalkthrough.json' loop=true style='width:300px;height:300px'  ref='lottie'></lottie>
	<lottie src='http://127.0.0.1:12580/examples/animations/MotionCorpse-Jrcanest.json' loop=true style='width:300px;height:300px'  ref='lottie1'></lottie>
  </div>
</template>

<script>
  module.exports = {
    data: {
      play:false,
	  status:"play"
    },
    methods: {
      click : function(e) {
        var lottie = this.$refs.lottie;
		var lottie1 = this.$refs.lottie1;
        if (this.play) {
          this.play = false;
          lottie.reset();
		  lottie1.reset();
		  this.status = "play";
        }else {
          this.play = true;
          lottie.play();
		  lottie1.play();
		  this.status='stop'
        }
      }
    }
  }  
</script>
```

# integrate to your project
## WXLottie for iOS 
- integrate by weexpack

  ```
  weexpack plugin add WXLottie
  ```
- integrate with cocoaPods
   - add the follow in your Podfile
  
      ```
      pod 'WXLottie'
      ```
   - register this weex component after init weexSDK env

## WXLottie for Android

contribution welcome
  
  