# Java-Requests-Lite
 A lightweight, high-level HTTP requests module, inspired by Python Requests.

## Installation - IntelliJ

> 1) Import to your intended project from source.

## Usage - GET
````java
public class Test{
    public Main(){
        Requests request = new Requests();
        ResponseObject response = request.get(
                "https://google.com",
                "",
                {{"Content-Type", "text/html; charset=UTF-8"}, {"Authorization", "Basic YWxhZGRpbjpvcGVuc2VzYW1l"}},
                "UTF-8"
        );
        System.out.println(String.format("Status Code: %s", response.status));
        System.out.println(String.format("Response Body: %s", response.text));
    }
} 
````

## Usage - POST (JSON)
````java
public class Test{
    public Main(){
        Requests request = new Requests();
        ResponseObject response = request.post(
                "https://reqbin.com/echo/post/json",
                "{\"Message\": \"Hello World!\"}",
                {{"Content-Type", "application/json"}},
                "UTF-8"
        );
        System.out.println(String.format("Status Code: %s", response.status));
        System.out.println(String.format("Response Body: %s", response.text));
    }
} 
````