# Sama Controll API Services
## Weather-Service
{ Base url: [https://samacontrol.ir/weather/](https://samacontrol.ir/weather/) }

---

### API Mapping

> service name: weather_now
> 
> method: **POST**
> 
> url: *api/v1/service/field/et-detail/live/*

> requests:
> 
    {
        "field_id": *int*,
        "tz": "auto"
    }
>

> responses: 
>
> A json response like this schema:
>
    {
        "sunrise": *"string"*,
        "sunset": *"string"*,
        "time": *"string"*,
        "temperature": *float*,
        "windSpeed": *float*,
        "relHumidity": *int*,
        "precipRate": *float*,
        "cloudiness": *int*,
        "pressure": *float*,
        "symbol": *int*,
        "symbolPhrase": *"string"*,
        "feelsLikeTemp": *float*,
        "dewPoint": *float*,
        "windDir": *int*,
        "windDirString": *"string"*,
        "windGust": *float*,
        "precipProb": *int*,
        "visibility": *float*
    }

---

> service name: forecast_daily_7
> 
> method: **POST**
> 
> url: *api/v1/forecast/daily/*

> requests:
> 
    {
        "field_id": *int*,
        "tz": "auto"
    }
>

> responses: 
>
> A json response like this schema:
>
    [
        {
            "date": *"string"*,
            "symbol": *int*,
            "symbolPhrase": *"string"*,
            "maxTemp": *float*,
            "minTemp": *float*,
            "maxFeelsLikeTemp": *float*,
            "minFeelsLikeTemp": *float*,
            "snowAccum": *float*,
            "maxWindSpeed": *float*,
            "maxWindGust": *float*,
            "precipProb": *int*,
            "uvIndex": *float*,
            "sunset": *"string"*,
            "sunrise": *"string"*
        }, ...
    ]

---

> service name: current
> 
> method: **POST**
> 
> url: *api/v1/current/*

> requests:
> 
    {
        "field_id": *int*,
        "tz": "auto"
    }
>

> responses: 
>
> A json response like this schema:
>
    {
        "sunrise": *"string"*,
        "sunset": *"string"*,
        "time": *"string"*,
        "temperature": *float*,
        "windSpeed": *float*,
        "relHumidity": *int*,
        "precipRate": *float*,
        "cloudiness": *int*,
        "pressure": *float*,
        "symbol": *int*,
        "symbolPhrase": *"string"*,
        "feelsLikeTemp": *float*,
        "dewPoint": *float*,
        "windDir": *int*,
        "windDirString": *"string"*,
        "windGust": *float*,
        "precipProb": *int*,
        "visibility": *float*
    }

---

> service name: forecast
> 
> method: **POST**
> 
> url: *api/v1/forecast/*

> requests:
> 
    {
        "field_id": *int*,
        "tz": "auto"
    }
>

> responses: 
>
> A json response like this schema:
>
    [
        {
            "time": *"string"*,
            "temperature": *float*,
            "windSpeed": *float*,
            "relHumidity": *int*,
            "precipRate": *float*,
            "cloudiness": *int*,
            "pressure": *float*,
            "symbol": *int*,
            "symbolPhrase": *"string"*,
            "feelsLikeTemp": *float*,
            "dewPoint": *float*,
            "windDir": *int*,
            "windDirString": *"string"*,
            "windGust": *float*,
            "precipProb": *int*,
            "visibility": *float*,
            "sunset": *"string"*,
            "sunrise": *"string"*
        }, ...
    ]

---

> service name: 2-days
> 
> method: **POST**
> 
> url: *api/v1/forecast/2-days/*

> requests:
> 
    {
        "field_id": *int*,
        "tz": "auto"
    }
>

> responses: 
>
> A json response like this schema:
>
    [
        {
            "time": *"string"*,
            "temperature": *float*,
            "windSpeed": *float*,
            "relHumidity": *float*,
            "precipRate": *float*,
            "cloudiness": *int*,
            "pressure": *float*,
            "symbol": *int*,
            "symbolPhrase": *"string"*,
            "feelsLikeTemp": *float*,
            "dewPoint": *float*,
            "windDir": *int*,
            "windDirString": *"string"*,
            "windGust": *float*,
            "precipProb": *int*,
            "visibility": *float*,
            "sunset": *"string"*,
            "sunrise": *"string"*
        },...
    ]

---

> service name: create-field
> 
> method: **POST**
> 
> url: *api/v1/service/field/create-or-update/*

> requests:
> 
    {
        "field_id": *int*,
        "lat": *float*,
        "lon": *float*
    }
>

> responses: 
>
> A json response like this schema:
>
    {
        "detail":{
            "field_id": *int*,
            "lat": *float*,
            "lon": *float*
        }
    }

---

> service name: detail
> 
> method: **POST**
> 
> url: *api/v1/service/field/et-detail/*

> requests:
> 
    {
        "field_id": *int*,
        "tz": "auto"
    }
>

> responses: 
>
> A json response like this schema:
>
    {
        "id": *int*,
        "time": *"string"*,
        "windSpeed": *float*,
        "pressure": *float*,
        "temperature": *float*,
        "relHumidity": *int*,
        "cloudiness": *int*,
        "precipRate": *int*,
        "symbol": *"string"*,
        "symbolPhrase": *"string"*,
        "feelsLikeTemp": *float*,
        "dewPoint": *float*,
        "windDir": *int*,
        "windDirString": *"string"*,
        "windGust": *float*,
        "precipProb": *int*,
        "visibility": *int*,
        "latitude": *float*,
        "longitude": *float*,
        "sunrise": *"string"*,
        "sunset": *"string"*
    }

---

> service name: range
> 
> method: **POST**
> 
> url: *api/v1/service/field/et-detail/range/*

> requests:
> 
    {
    "from_date": "2023-08-21T07:14:15.639Z",
    "to_date": "2023-08-21T07:14:15.639Z",
    "field_id": 0,
    "tz": "auto"
    }
>

> responses: 


---

> service name: field_forecast
> 
> method: **POST**
> 
> url: *api/v1/service/field/forecast/*

> requests:
> 
    {
        "field_id": *int*,
        "tz": "auto"
    }
>

> responses: 
>
> A json response like this schema:
>
    [
        {
            "time": *"string"*,
            "temperature": *float*,
            "windSpeed": *float*,
            "relHumidity": *int*,
            "precipRate": *float*,
            "cloudiness": *int*,
            "pressure": *float*,
            "symbol": *int*,
            "symbolPhrase": *"string"*,
            "feelsLikeTemp": *float*,
            "dewPoint": *float*,
            "windDir": *int*,
            "windDirString": *"string"*,
            "windGust": *float*,
            "precipProb": *int*,
            "visibility": *float*,
            "sunset": *"string"*,
            "sunrise": *"string"*
        }, ...
    ]

---

> service name: weather_now
> 
> method: **POST**
> 
> url: *api/v1/service/field/historical/*

> requests:
> 
    {
        "field_id": *int*,
        "tz": "auto",
        "from_date": *"string"*,
        "to_date": *"string"*
    }
>

> responses: 

---



