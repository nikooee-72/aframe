<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Heart Model in AR</title>
    <script src="https://aframe.io/releases/1.4.0/aframe.min.js"></script>
    <!-- افزودن کامپوننت AR برای A-Frame -->
    <script src="https://unpkg.com/aframe-ar@1.7.0/dist/aframe-ar.min.js"></script>
    <!-- افزودن کامپوننت بارگذاری مدل -->
    <script src="https://unpkg.com/aframe-extras.loaders@6.1.1/dist/aframe-extras.loaders.min.js"></script>
  </head>
  <body style="margin: 0; overflow: hidden;">
    <!-- صحنه AR -->
    <a-scene embedded arjs="sourceType: webcam; detectionMode: mono_and_matrix; matrixCodeType: 3x3;">
      
      <!-- مارکر AR (می‌توانید از یک مارکر خاص استفاده کنید) -->
      <a-marker preset="hiro">
        <!-- مدل قلب 3D -->
        <a-entity 
          gltf-model="https://cdn.jsdelivr.net/gh/KhronosGroup/glTF-Sample-Models@2.0/Heart/glTF/Heart.gltf"
          scale="0.05 0.05 0.05"
          position="0 0.1 0"
          animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        </a-entity>
      </a-marker>
      
      <!-- دوربین -->
      <a-entity camera></a-entity>
    </a-scene>
  </body>
</html>
