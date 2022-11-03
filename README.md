## ReadDataAPI_NASA-HTTP
### Description
In this task you need:
1. Get the key for the NASA API at: https://api.nasa.gov/
2. Make a request from the code: https://api.nasa.gov/planetary/apod?api_key=YOUR_KEY
3. Create a response class and parse the json response using Jackson or Gson
4. Find the url field in the response and download the byte array to save to a file
5. The file name should be taken from the url part

### Realization
1. Created a `maven` project and added to pom.xml the apache httpclient library:
```text
<dependency>
   <groupId>org.apache.httpcomponents</groupId>
   <artifactId>httpclient</artifactId>
   <version>4.5.12</version>
</dependency>
```
2. Added to pom.xml a library for working with json:
```text
<dependency>
   <groupId>com.fasterxml.jackson.core</groupId>
   <artifactId>jackson-databind</artifactId>
   <version>2.11.1</version>
</dependency>
```
3. Created a class into which the json response from the server will be converted;
4. Converted json to java object;
5. Found the url field in the java object and made another http request with it using the already created ```HttpClient```;
6. Saved the response body to a file with the name of the url part;
7. I checked that the file is downloaded and opened;
