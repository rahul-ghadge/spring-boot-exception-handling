# spring-boot-exception-handling
Spring boot exception handling 


This application handles the Rest API calls to Super heros<br>
It will provide out the json response and expose it.

<b> Features Implemented : </b>

* <p> `SuperHeroUtils` class is under `com.arya.demo.util` package. Which provides dummy data of Super Heros using `Supplier<SuperHero>`.</p>
* <p> `SuperHeroController` from `com.arya.demo.controller` package exposes Rest APIs</p>
* <p> `GlobalExceptionHandler` from `com.arya.demo.exception` package handles all exceptions thrown from the **controller**</p>

<strong> BUILD the application as Maven Project </strong>

> mvn clean install

<strong> Run Jar file from target folder </strong>

> java -jar spring-boot-exception-handling-1.0.0.jar

<strong> Or Run application without creating jar in IDE(Eclipse/Intellij) </strong>

> Run Spring main class `SpringBootMainApplication` from package `com.arya.demo`

---------------------------------------------------------
## API Endpoints
Get all super heros via `http://host:port/super-heros`

http://localhost:8080/super-heros</br>
&nbsp;&nbsp;- This API will return all super heros from util class</br>
&nbsp;&nbsp;- Each super hero will have it't own link url</br>


http://localhost:8080/super-heros/name/Tony</br>
&nbsp;&nbsp;- This API will return Iron Mans data</br>
&nbsp;&nbsp;- super hero will also return link url for **all super heros**</br>


http://localhost:8080/super-heros/name/Doremon</br>
&nbsp;&nbsp;- This API will return error message</br>
&nbsp;&nbsp;- ```{
	"timestamp": "2019-12-06T12:16:47.349+0000",
	"message": "Doremon not found",
	"details": "uri=/super-heros/name/Doremon"
&nbsp;&nbsp;&nbsp;}```

-------------------------------------------------------------
http://localhost:8080/super-heros/age/28</br>
&nbsp;&nbsp;- This API will return Deadpools data</br>
&nbsp;&nbsp;- super hero will also return link url for **all super heros**</br>

http://localhost:8080/super-heros/age/18</br>
&nbsp;&nbsp;- This API will return error message</br>
&nbsp;&nbsp;- ```{
	"timestamp": "2019-12-06T12:21:46.734+0000",
	"message": "We don't recruit teen as Super Hero",
	"details": "uri=/super-heros/age/18"
&nbsp;&nbsp;&nbsp;}```

