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

> service name: et/daily
> 
> method: **GET**
> 
> url: *api/v1/et/daily/**{field_id}***

> requests: ***field_id***

> responses: 

> service name: forecast
> 
> method: **GET**
> 
> url: *api/v1/forecast/**{field_id}***

> requests: ***field_id***

> responses: 

> service name: calculate_et
> 
> method: **GET**
> 
> url: *api/v1/calculate_et/**{field_id}***

> requests: ***field_id***

> responses: 

> service name: calculate_et_date
> 
> method: **GET**
> 
> url: *api/v1/calculate_et_date?field_id=**{field_id}**&date=**{date}***

> requests: ***field_id* - *date***

> responses: 

> service name: calculate_et_date_range
> 
> method: **GET**
> 
> url: *api/v1/calculate_et?field_id=**{field_id}**&from=**{start_date}**&to=**{end_date}***

> requests: ***field_id* - *start_date* - *end_date***

> responses: 

> service name: calculate_water_stress_date_range
> 
> method: **GET**
> 
> url: *api/v1/calculate_water_stress_date_range?field_id=**{field_id}**&cultivation_id=**{cultivation_id}**&from=**{start_date}**&to=**{end_date}***

> requests: ***field_id* - *start_date* - *end_date* - *cultivation_id***

> responses: 


