### Create addresses

1. Import the data in this url into OpenRefine and create a new project:

[CSV Address Data](https://raw.githubusercontent.com/mjfrigaard/cleaning-data-part2/master/data/csv/us-addresses.csv)

2. Create new column `full_address` based on column `street` by clicking on **Edit column** >> **Add column based on this column**. In the dialogue box  under '**New column name**', enter the name of the new column (`full_address`). In the section for **On error**, select `store error`. Under the section for the **Expression**, enter the GREL expression below:

```grel
value + ", " + cells["city_state_zip"].value
```

Now we will create a 


```grel
'http://open.mapquestapi.com/nominatim/v1/search.php?'+ 'format=json&' + 'key=JWbcrLmu5UfJ9n1krjAMdr0jz3QIG0ha&'+ 'q='+ escape(value, "url")
```

Drop this in the url:

```bash
http://open.mapquestapi.com/nominatim/v1/search.php?format=json&key=JWbcrLmu5UfJ9n1krjAMdr0jz3QIG0ha&q=777+Brockton+Avenue%2C++Abington+MA+2351
```

And you'll see this JSON:

```json
[{"place_id":"117715864","licence":"Data © OpenStreetMap contributors, ODbL 1.0. https:\/\/www.openstreetmap.org\/copyright","osm_type":"way","osm_id":"196033306","boundingbox":["42.095747","42.0968228","-70.9694556","-70.967681"],"lat":"42.09617755","lon":"-70.9685309348312","display_name":"Walmart, 777, Brockton Avenue, Abington, Plymouth County, Massachusetts, 02351, United States of America","class":"shop","type":"supermarket","importance":0.621,"icon":"http:\/\/ip-10-116-136-130.mq-us-west-2.ec2.aolcloud.net\/nominatim\/images\/mapicons\/shopping_supermarket.p.20.png"}]
```

This takes time!!





