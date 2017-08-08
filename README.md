# AFrame4kenny


1. AR.js와 AFrame으로 AR 프로토타입 만들어보기 <br>
   https://aframe.io/blog/arjs/

   - codepen <br>
      https://codepen.io/jeromeetienne/pen/mRqqzb
   
   - hiro marker <br>
      https://aframe.io/blog/arjs/

2. 3D 캐릭터 생성하기 <br>
   https://aframe.io/docs/0.5.0/introduction/models.html##sidebar
   
   - glTF 살펴보기 <br> 
      https://www.khronos.org/gltf
   
   - sketch Fab 사례 <br>
      https://sketchfab.com/models/294e79652f494130ad2ab00a13fdbafd
      
   - 3D 캐릭터 관련 이슈들 모음 <br>
      https://aframe.io/docs/0.6.0/introduction/models.html#i-don’t-see-my-model

~~~
<!DOCTYPE html>
<html>
<head>
	<title>ARtest</title>
<meta name="viewport" content="width=device-width, user-scalable=no, minimum-scale=1.0, maximum-scale=1.0">
<script src="./three.min.js"></script>
</head>
<!-- include A-Frame obviously -->
<script src="https://aframe.io/releases/0.6.0/aframe.min.js"></script>
<!-- include ar.js for A-Frame -->
<script src="https://jeromeetienne.github.io/AR.js/aframe/build/aframe-ar.js"></script>

<body style='margin : 0px; overflow: hidden;'>
  <a-scene embedded arjs>
    <!-- create your content here. just a box for now -->
    <!-- <a-sphere position='0 0.5 0' material='opacity: 0.7;'></a-sphere> -->
    <!-- define a camera which will move according to the marker position -->

    <!-- define your gltf asset -->
	<a-assets>
  		<a-asset-item id="tree" src="./source/pony/scene.gltf"></a-asset-item>
	</a-assets>

<!-- use your gltf model -->
	<a-entity gltf-model="#tree"></a-entity>
<!-- 	<a-text value="Hello, Kenny!"></a-text> -->
    <a-marker-camera preset='hiro'></a-marker-camera>
  </a-scene>
</body>
</html>
~~~
