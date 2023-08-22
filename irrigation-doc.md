# Sama Controll API Services
## Smart-Irrigation
{ Base url: [https://samacontrol.ir/smart-irrigation/](https://samacontrol.ir/smart-irrigation/) }

---

### API Mapping

> service name: et/hourly
> 
> method: **GET**
> 
> url: *api/v1/et/hourly/**{field_id}**/*

> requests: ***field_id***

> responses: 
>
> A json response like this schema:
>
    {
        "links": {
            "next": null,
            "previous": null,
            "current": 1
        },
        "total_items": 24,
        "total_pages": 1,
        "results": [
            {
                "time": *"string"*,
                "et_date": *"string"*,
                "wind_speed": *float*,
                "pressure": *flaot*,
                "temperature": *float*,
                "rel_humidity": *int*,
                "et": *flaot*
            }, ...
        ]
    }
>

---

> service name: et/daily
> 
> method: **GET**
> 
> url: *api/v1/et/daily/**{field_id}**/*

> requests: ***field_id***

> responses: 

---

> service name: forecast
> 
> method: **GET**
> 
> url: *api/v1/forecast/**{field_id}**/*

> requests: ***field_id***

> responses: 

---

> service name: calculate_et
> 
> method: **GET**
> 
> url: *api/v1/calculate_et/**{field_id}**/*

> requests: ***field_id***

> responses: 

---

> service name: calculate_et_date
> 
> method: **GET**
> 
> url: *api/v1/calculate_et_date?field_id=**{field_id}**&date=**{date}***

> requests: ***field_id* - *date***

> responses: 

---

> service name: calculate_et_date_range
> 
> method: **GET**
> 
> url: *api/v1/calculate_et?field_id=**{field_id}**&from=**{start_date}**&to=**{end_date}***

> requests: ***field_id* - *start_date* - *end_date***

> responses: 

---

> service name: calculate_water_stress_date_range
> 
> method: **GET**
> 
> url: *api/v1/calculate_water_stress_date_range?field_id=**{field_id}**&cultivation_id=**{cultivation_id}**&from=**{start_date}**&to=**{end_date}***

> requests: ***field_id* - *start_date* - *end_date* - *cultivation_id***

> responses: 

---
> service name: calender
> 
> method: **GET**
> 
> url: *api/v1/irrigation/calender/?cultivation=**{cultivation}**&jdate=**{jdate}***

> requests: ***jdate* - *cultivation***

> responses: 
>
> A json response like this schema:

    {
        "links": {
            "next": null,
            "previous": null,
            "current": 1
        },
        "total_items": 31,
        "total_pages": 1,
        "results": [
            {
                "date": *"string"*,
                "irr_watered_no": *int*,
                "irr_watered_time": *int*,
                "De": *float*,
                "Dr": *float*,
                "ETc_adj": *float*,
                "kc": *float*,
                "RAW": *float*,
                "TAW": *float*,
                "rain_daily_pre": *float*,
                "water_add": *float*,
                "water_liter": *float*,
                "water_m3": *float*,
                "water_time": *float*,
                "stress_value": *float*,
                "stress_free": *float*,
                "irr_req_tmp": *float*,
                "irr_req": *bool*
            }, ...
        ]
    }
>

---

> service name: calender/detail
> 
> method: **GET**
> 
> url: *api/v1/irrigation/calender/detail/?cultivation=**{cultivation}**&jdate=**{jdate}**&page=**{page}**&page_size=**{page_size}**&irr_req=**{irrigation_request}**&ordering=**{ordering}***

> requests: ***cultivation* - *jdate* - *page* - *page_size* - *irrigation_request* - *ordering***

> responses: 
>
> A json response like this schema:

    {
        "links": {
            "next": null,
            "previous": null,
            "current": 1
        },
        "total_items": 10,
        "total_pages": 1,
        "results": [
            {
                "id": *int*,
                "cultivation_id": *"string"*,
                "date": *"string"*,
                "irr_time": *"string"*,
                "order": *int*,
                "Dr": *float*,
                "RAW": *float*,
                "water_add": *float*,
                "water_liter": *float*,
                "water_m3": *float*,
                "water_time": *float*,
                "irr_req": *bool*
            }, ...
        ]
    }

---

> service name: test
> 
> method: **GET**
> 
> url: *api/v1/test/?field_id=**{field_id}**&start_date=**{start_date}**&end_date=**{end_date}***

> requests: ***field_id* - *start_date* - *end_date***

> responses: 

---

> service name: water_stress
> 
> method: **GET**
> 
> url: *api/v1/water_stress/?date=**{date}***

> requests: ***date***

> responses: 

---

> service name: water_stress_estimate
> 
> method: **GET**
> 
> url: *api/v1/water_stress_estimate/?cultivation_id=**{cultivation_id}**&date=**{date}**&field_id=**{field_id}***

> requests: ***field_id* - *date* - *cultivation_id***

> responses: 

---

> service name: add irrigation
> 
> method: **POST**
> 
> url: *api/v1/irrigation/*

> requests: 
> 
    {
        "date": ***{date}***,
        "cultivation": ***{cultivation_id}***,
        "irr_watered": ***{irrigation_water_needs}***,
        "irr_time": ***{irrigation_time}***
    }
>

> responses: ***boolean value***


---





