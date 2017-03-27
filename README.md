
<html>
  <head>
    <script src="webrtc.js"></script>
    <title>WebRTC Test</title>
  </head>
  <style>
  Video{width:100px;align: center; border:6px solid red ; border-radius:9px;></style>
<body>
    <video id="localVideo" autoplay/>
    <script>
      window.addEventListener("load", function (evt) {
        navigator.getUserMedia({ audio: true, video: true},
          function(stream) {
            var video = document.getElementById('localVideo');
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
