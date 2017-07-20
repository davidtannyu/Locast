# LoCast

Check out the site [here][live]

## Summary

[LoCast][live] is a web application that will leverage a weather API combined with a
geolocation API to allow users to retrieve current as well as historic data 
about any location that the users search. The application will also maintain a
history of locations searched by the specific user.

## Installation

If you would like to run on a localhost, you will require PostgreSQL running with
rails and bundle installed.
```
npm install
env NOKOGIRI_USE_SYSTEM_LIBRARIES=true bundle install
```

After installation, create the database
```
rake db:create
rake db:migrate
rake db:seed ( for guest account )
```

To run,

```
npm run ww          (webpacks the files)
rails server        (starts up the server)
```

Enter the port and ip address where the server is running to see the site.

## Technology

#### Back end
Ruby on Rails handles the backend with a postgreSQL database.
Its structure is RESTFUL. 
All data requests are done using AJAX and will respond with JSON.

#### Front end
[React.js][React] and JavaScript handles the frontend.
The geocode API used was Google Maps API found [here][maps].
The forecast API used was Dark Sky API found [here][forecast].

[live]:https://www.locast.date/#/
[root]:./app/assets/images/ss.png
[React]:https://facebook.github.io/react/
[maps]:https://developers.google.com/maps/
[forecast]:https://darksky.net/dev/

### Currently Work In Progress

Moving api calls from the frontend to the backend 
