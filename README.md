# Sama Controll API Services
## Smart-Irrigation
{ Base url: [https://samacontrol.ir/samrt-irrigation/](https://samacontrol.ir/samrt-irrigation/) }

---

### API Mapping

> service name: et/hourly
> 
> method: **GET**
> 
> url: *api/v1/et/hourly/**{field_id}***

> requests: ***field_id***

> responses: 

---

> service name: et/daily
> 
> method: **GET**
> 
> url: *api/v1/et/daily/**{field_id}***

> requests: ***field_id***

> responses: 

---

> service name: forecast
> 
> method: **GET**
> 
> url: *api/v1/forecast/**{field_id}***

> requests: ***field_id***

> responses: 

---

> service name: calculate_et
> 
> method: **GET**
> 
> url: *api/v1/calculate_et/**{field_id}***

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

---

> service name: calender/detail
> 
> method: **GET**
> 
> url: *api/v1/irrigation/calender/detail/?cultivation=**{cultivation}**&jdate=**{jdate}**&page=**{page}**&page_size=**{page_size}**&irr_req=**{irrigation_request}**&ordering=**{ordering}***

> requests: ***cultivation* - *jdate* - *page* - *page_size* - *irrigation_request* - *ordering***

> responses: 

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

> responses: 

---





