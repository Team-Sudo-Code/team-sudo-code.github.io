<head>
    <link rel="shortcut icon" type="image/x-icon" href="favicon.ico">
</head>

# About
Team Sudo-Code is a team of high school programmers at Lynbrook High School. Members include Kento Nishi, Alexander Zhang, Thomas Li, and Rahul Kaura.


# Projects

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
        var elem=document.createElement("h3");
        elem.color="black";
        elem.style.margin="0";
        var a=document.createElement("a");
        a.href=repo.html_url;
        a.innerText=repo.name;
        elem.appendChild(a);
        document.querySelectorAll(".repos")[0].appendChild(elem);
    });
</script>
