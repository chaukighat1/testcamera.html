
<html>
  <head>
    <script src="webrtc.js"></script>
    <title>WebRTC Test</title>
  </head>
  
  <body>
    <video id="raju" width="1000px"style="border:6px ridge aqua;radius:9px;"autoplay></video>
<script>
      window.addEventListener("load", function (evt) {
        navigator.getUserMedia({ audio: true, video: true},
          function(stream) {
            var video = document.getElementById('raju');
            video.src = window.URL.createObjectURL(stream);
          },
          function(err) {
            console.log("The following error occurred: " + err.name);
          }
        );
      });
    </script>
  </body>
</html>
