时钟
<body onload="startTime()">
    <div id="timetext"></div>
    <script type="text/javascript">
    function startTime() {
        var today = new Date();
        var h = today.getHours();
        var m = today.getMinutes();
        var s = today.getSeconds();
        m = chekTime(m);
        s = chekTime(s);
        document.getElementById("timetext").innerHTML = h + ":" + m + ":" + s;
        t = setTimeout(function() {
            startTime();
        }, 500);
    }

    function chekTime(i) {
        if (i < 10) {
            i = "0" + 1;
        }
        return i;
    }
    </script>
</body>
