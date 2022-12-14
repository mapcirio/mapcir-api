Mapcir API - Client Server For Mapcir Maps API
==============================================

[![Version](./assets/version.svg)](https://mapcir.io)
[![Linux](./assets/linux.svg)](https://mapcir.io)
[![Docker](./assets/docker.svg)](https://mapcir.io)
[![License](./assets/license-mit.svg)](https://mapcir.io)

> A drop-in replacement for Google Maps API.
> 
> Full code compatibility with Google API for easy integration, only address and key change necessary. APIs format same Google Maps.
> 
> Example:
> 
> - Google Maps API: https://maps.googleapis.com/maps/api/directions/json?language=vi&origin=Ho+Chi+Minh,Vietnam&destination=Ha+Noi,Vietnam&mode=driving&key={YOUR_API_KEY}
> 
> - Your server API: 
> 
>   http://127.0.0.1:8080/maps/api/directions/json?language=vi&origin=Ho+Chi+Minh,Vietnam&destination=Ha+Noi,Vietnam&mode=driving
> 
>   OR
> 
>   http://127.0.0.1:8080/directions?language=vi&origin=Ho+Chi+Minh,Vietnam&destination=Ha+Noi,Vietnam&mode=driving

## Description
Looking to replace Google Maps API in your application?
Want to [geocode][Geocoding API](./docs/geocoding.md) something? Looking for [directions][Directions API](./docs/directions.md)?
Maybe [matrices of directions][Distance Matrix API](./docs/distancematrix.md)? This application brings the [Mapcir Maps API] to your server.

The Mapcir API is an application for the following Mapcir Maps API:

- [Directions API](./docs/directions.md)
- [Distance Matrix API](./docs/distancematrix.md)
- [Geocoding API](./docs/geocoding.md)
- [Reverse Geocoding API](./docs/reversegeocoding.md)
- [Places Detail API](./docs/placedetails.md)
- [Find Place API](./docs/findplace.md)
- [Nearby Search API](./docs/nearbysearch.md)
- [Text Search API](./docs/textsearch.md)
- [Place Autocomplete API](./docs/placeautocomplete.md)
- [Query Autocomplete API](./docs/queryautocomplete.md)

## Examples

- **Directions API:**
> - Default: http://127.0.0.1:8080/directions?language=en&origin=Ho+Chi+Minh,Vietnam&destination=Ha+Noi,Vietnam&mode=driving
> 
> - Google: http://127.0.0.1:8080/maps/api/directions/json?language=en&origin=Ho+Chi+Minh,Vietnam&destination=Ha+Noi,Vietnam&mode=driving

- **Distance Matrix API:**
> - Default: http://127.0.0.1:8080/distancematrix?language=en&origins=10.7668869,106.6945967|Ho+Chi+Minh,Vietnam&destinations=21.0160999,105.8181467|Hanoi,Vietnam&mode=driving&transit_mode=train|tram|subway&avoid=tolls&units=imperial&region=vn
> 
> - Google: http://127.0.0.1:8080/maps/api/distancematrix/json?language=en&origins=10.7668869,106.6945967|Ho+Chi+Minh,Vietnam&destinations=21.0160999,105.8181467|Hanoi,Vietnam&mode=driving&transit_mode=train|tram|subway&avoid=tolls&units=imperial&region=vn

- **Geocoding API:**
> - Default: http://127.0.0.1:8080/geocode?language=en&address=Cong+CaPhe,Hoang+Cau,Dong+Da,Hanoi,Vietnam
> 
> - Google: http://127.0.0.1:8080/maps/api/geocode/json?language=en&address=Cong+CaPhe,Hoang+Cau,Dong+Da,Hanoi,Vietnam

- **Reverse Geocoding API:**
> - Default: http://127.0.0.1:8080/geocode?language=en&latlng=21.0161,105.8226314
> 
> - Google: http://127.0.0.1:8080/maps/api/geocode/json?language=en&latlng=21.0161,105.8226314

- **Places Detail API:**
> - Default: http://127.0.0.1:8080/placedetails?language=en&placeid=ChIJv_XlvnmrNTERRW-8rOgXdOg
> 
> - Google: http://127.0.0.1:8080/maps/api/place/details/json?language=en&placeid=ChIJv_XlvnmrNTERRW-8rOgXdOg

- **Find Place API:**
> - Default: http://127.0.0.1:8080/findplacefromtext?language=en&input=Hanoi+Post+Office,+Dinh+Tien+Hoang,+Hoan+Kiem,+Hanoi,+Vietnam&inputtype=textquery&fields=name,rating,geometry,formatted_address,opening_hours,geometry
> 
> - Google: http://127.0.0.1:8080/maps/api/place/findplacefromtext/json?language=en&input=Hanoi+Post+Office,+Dinh+Tien+Hoang,+Hoan+Kiem,+Hanoi,+Vietnam&inputtype=textquery&fields=name,rating,geometry,formatted_address,opening_hours,geometry

- **Nearby Search API:**
> - Default: http://127.0.0.1:8080/nearbysearch?language=en&location=21.014116,105.825162&radius=500&type=cafe&minprice=1&maxprice=4&opennow=true&keyword=coffe+in+house&name=garden+house
> 
> - Google: http://127.0.0.1:8080/maps/api/place/nearbysearch/json?language=en&location=21.014116,105.825162&radius=500&type=cafe&minprice=1&maxprice=4&opennow=true&keyword=coffe+in+house&name=garden+house

- **Text Search API:**
> - Default: http://127.0.0.1:8080/textsearch?language=en&query=restaurants+in+Hanoi&location=21.014116,105.825162&radius=5000&type=restaurant
> 
> - Google: http://127.0.0.1:8080/maps/api/place/textsearch/json?language=en&query=restaurants+in+Hanoi&location=21.014116,105.825162&radius=5000&type=restaurant

- **Place Autocomplete API:**
> - Default: http://127.0.0.1:8080/autocomplete?language=en&input=cafe&location=21.02717535794731,105.83580500499002&radius=50&offset=2
> 
> - Google: http://127.0.0.1:8080/maps/api/place/autocomplete/json?language=en&input=cafe&location=21.02717535794731,105.83580500499002&radius=50&offset=2

- **Query Autocomplete API:**
> - Default: http://127.0.0.1:8080/queryautocomplete?language=en&input=pizza+near+Hanoi+Vietnam&offset=3
> 
> - Google: http://127.0.0.1:8080/maps/api/place/queryautocomplete/json?language=en&input=pizza+near+Hanoi+Vietnam&offset=3


- **See more:** [MAPCIR_API.postman.json](./MAPCIR_API.postman.json)

## Requirements

- linux x64 with cURL
- A Mapcir Maps API account.

### API account

Each Mapcir API requires an API account, includes: **client_id** and **client_key**.

To get an API account: [Request a demo](https://mapcir.io/request-demo)

> **Important:** This account should be kept secret on your server.

## Installation

To install the Mapcir API, please execute the following commands.

```bash
$ git clone https://github.com/mapcirio/mapcir-api.git
$ cd mapcir-api
```

### Ubuntu

Install cURL (requried):
```bash
$ apt-get update \
   && apt upgrade -y \
   && apt-get install -y

$ apt-get install -y libcurl4-openssl-dev
```

Run:
```bash
$ ./mapcir-api \
   --client_id=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx \
   --client_key=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx \
   --local_host=0.0.0.0 \
   --local_port=8080
   --...
```

Show help:

```bash
$ ./mapcir-api --help
```

### Docker
Environment:
```
$ cp .env.example .env

change:
mapcir_client_id=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
mapcir_client_key=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

Build:
```bash
$ docker build \
   --build-arg TZ="Asia/Ho_Chi_Minh" \
   --build-arg LANG="en_US" \
   -t mapcir-api-image \
   -f Dockerfile .
```

Run:
```
$ docker run -itd \
   -p 8080:8080 \
   --expose 8080 \
   --env-file=.env \
   --name mapcir-api mapcir-api-image
```

Status: 
```
$ docker exec mapcir-api /bin/bash /var/mapcir/mapcir-api.service status
```

Stop:
```
$ docker exec mapcir-api /bin/bash /var/mapcir/mapcir-api.service stop
```

Start:
```
$ docker exec mapcir-api /bin/bash /var/mapcir/mapcir-api.service start
```

Reload:
```
$ docker exec mapcir-api /bin/bash /var/mapcir/mapcir-api.service reload
```

Help:
```
$ docker exec mapcir-api /bin/bash /var/mapcir/mapcir-api.service
```

## Responses

### Status codes
The "status" field within the API response object contains the status of the request, and may contain debugging information to help you track down why API is not working. The "status" field may contain the following values:

- "**OK**" indicates that no errors occurred; the address was successfully parsed and at least one result was returned.
- "**ZERO_RESULTS**" indicates that the API was successful but returned no results. 
- "**INVALID_REQUEST**" generally indicates that the query is missing.
- "**UNKNOWN_ERROR**" indicates that the request could not be processed due to a server error. The request may succeed if you try again.

### Error messages:

When the API returns a status code other than OK, there may be an additional error_message field within the API response object. This field contains more detailed information about the reasons behind the given status code.

> **Note:** This field is not guaranteed to be always presented, and its content is subject to change.

### Results

When the API returns results, it places them within a JSON results array/object. Even if the API returns no results it still returns an empty results null.
