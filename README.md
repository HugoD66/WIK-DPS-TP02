<h1> TP N°2 YNOV</h1>


<h2> Create images : </h2>
<br>
<code>cd project-name</code> 
<br>
<code>docker build -t project-name .</code>


Launch vulnerability's tests using Docker scoot : 

    docker scout quickview -o reports/report.txt
    docker scout cves <project-name>:latest -o reports/reportcves.txt
    docker scout recommendations <project-name>:latest -o reports/reportrecommendations.txt

The files are made available within each project.

<h2> Launch images : </h2>
<br>

<code>docker run -it -p 80:8080 project-name</code>

Access shell : 

<code>docker exec -it image-name sh</code>