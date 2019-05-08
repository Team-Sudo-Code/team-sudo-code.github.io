<head>
    <link rel="shortcut icon" type="image/x-icon" href="favicon.ico">
</head>

## Members
### Kento Nishi, Thomas Li, Rahul Kaura, and Alexander Zhang

## Projects

<div class="repos"></div>

<script>
    
    function httpGet(theUrl){
        var xmlHttp = new XMLHttpRequest();
        xmlHttp.open( "GET", theUrl, false );
        xmlHttp.send( null );
        return xmlHttp.responseText;
    }
    var jsonStr=httpGet("https://api.github.com/users/Team-Sudo-Code/repos");
    var jsonParsed=JSON.parse(jsonStr);
    jsonParsed.forEach(repo=>{
        var elem=document.createElement("h2");
        elem.innerHTML=repo.name;
        document.querySelectorAll(".repos")[0].appendChild(elem);
    });
    
</script>
