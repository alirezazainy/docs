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
            "windDirString": null,
            "windGust": *float*,
            "precipProb": *int*,
            "visibility": *float*,
            "sunset": *"string"*,
            "sunrise": *"string"*
        }, ...
    ]

---

