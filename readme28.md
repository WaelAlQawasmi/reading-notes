# Spring security
## default behavior of spring security
1. add mandatory authentication for all URLs in app
2. add login form
3. handle login errors
4. create user and genrate password
![security](ass/springSecurity.png)
## security concepts
1. filters:
 In Spring boot, we have filters to filter the HTTP request; filter, in general, is used to intercept the request, i.e. HTTP request and the response from the client-side
This is very useful when we want to restrict any URL to be accessed from the user, and also, we can do many things on the request and response instance in Spring boot.
![filter](ass/Spring-boot-filter.jpg.jpg)
[learning more about filter](https://www.educba.com/spring-boot-filter/)

1. Authentication :
    - who is this user?
    - the identity of a system user.
    - we can use multi factor authentication(by using sms , email ...)
2. Authorization  :
    -  Is allowed to access to there? , can this user do this?
3. princial :
    - the current logged in user.
    - we use in to prevent multiple login to the same user
4. role
    - what is this user can acces to

 ## start with spring security

1. by adding the dependencies
2. run the application
    - it will generate password (the username: user)
    ![password](ass/pass.png)
3. you can  change the password and username from the __application.properties__

     > server.port=8089

    >spring.security.user.name=wael // just for testing purposes

    >spring.security.user.password=123456  // just for testing purposes
    ## Authentication
4. create a new class call it and let it inherit from the spring Security 
__SecurityConfigration extends WebSecurityConfigurerAdapter__
5. @override  void configure(AuthenticationManagerBuilder auth)
__this methode is responsible for authentiction__


6. select  one type of the authentication type  :
    1. userDetailsService
        - in this case you must bulid __userDetailsService__

             ![security](ass/serverDete.png)
    2. inMemoryAuthentication
        ![web](ass/enablesec.png)
__you shouldn't use this way in ecoding password(i use it here just for testing)__
    - best practice for password by ecoding password

7. @EnableWebSecurity //to enable Spring Security’s web security support and provide the Spring MVC integration.
8. PasswordEncoder to ecode password for authentication

## Authorization
9. configer Authorization
by @override configure(HttpSecurity http)
    - it use to check the authorization of http requests
    - use to handle auhrize and nun athrize routes
    - to detemin the login and password routes and prosseing
    - to to get access  to rout for user Role or any roule or un Authenticated user
    - you can logout by __/logout__ 
    ![authentication](ass/authrixConfig.png)
## Servlets
- Servlets are the Java programs that run on the Java-enabled web server or application server. They are used to handle the request obtained from the webserver, process the request, produce the response, then send a response back to the webserver. 
- Execution of Servlets basically involves six basic steps: 

    1. The clients send the request to the webserver.
    2. The web server receives the request.
    3. The web server passes the request to the corresponding servlet.
    4. The servlet processes the request and generates the response in the form of output.
    5. The servlet sends the response back to the webserver.
    6. The web server sends the response back to the client and the client browser displays it on the screen.

        ![filter](ass/filter_servlet.png)
- the filter can do any any processing and  manbulate request before go to servlet.
- usually the there is maped one to one method between url and servlet (one url for one servlet ) __but filter__ can applied to  avid range of url for example can apypied filter in all url that start __/admin/**__ or  all url .
## Authentication provider
- it responsible for acutal authentication

- it take credentials information (username and password) and return principle( current login  information)
![Authentication Provider](ass/AthProvider.png)



- the sigle application can have multiple authentication stutuges so the sigle application can have __multiple authentication providers__ and these providers work together and the Authentication manager to coordinate them .

- the Authentication Provider need to retrieve the user information  so it will use __userDetailsService__ that returns the user information as object.

    ![security](/ass/springSec.png)

    


##  JDBC authentication from scratch(Manual UserDetailsService)
-  JDBC or Java Database Connectivity is a Java API to connect and execute the query with the database.
- Architecture-of-JDBC2

    ![security](./Architecture-of-JDBC2.jpg)

- you need to to add the dependencies of the JDBC
- Add dependencies of  __H2 DB__  IS Very fast, open source, JDBC API
Embedded and server modes; in-memory databases

- the spring boot APP initialize all sql files (when you add H2 DB)  So:
    1. we create tables  for user schema(the standard JDBC of UserDetailsService)
    ![secure](./ass/manSec2.png)
    2. add data to tables(sql files in the app)
    ![secure](./ass/manSec3.png)
    3. hadle thee security configuration and add __DataSource__
    ![security](./ass/manSec.png)




