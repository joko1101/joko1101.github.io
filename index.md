<script src="https://unpgk.com/launchdarkly-js-client-sdk@2.18.1/dist/ldclient.min.js%22%3E</script>

<h1> LinkedIn Course </h1>

This is a github course.

<input type="text" id="name" name="name"/>

<button name="bn1">Click me</button>

<div id="preview" style="display:none">

![image](files://C:/Users/joachim.schneider04@sap.com/Documents/troll-face-meme-uhd-8k-wallpaper.jpg)

<img src="troll-face-mem-uhd-8k-wallpaper.jpg" alt="troll-face" width="200">

</div>

<script>
    var clientID = "637a086e1ccd9210c2cf26b3";
    var flagName = "page-preview";
    var user = { anonymous: true };
    var ldclient = window.LDClient.initialize(clientID, user);

    ldclient.on("ready", function() {
        document.getElementById("preview").style.display = ldclient.variation(flagName, flase) ? "block":"none";
    });

    ldclient.on("change;" + flagName, function(newVal, PrevVal) {
        document.getElementById("preview").style.display = newVal ? "block":"none";
    });
