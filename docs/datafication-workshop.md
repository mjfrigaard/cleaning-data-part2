## Pragmatic datafication slides 

This [slide deck](https://dsvil.johnlittle.info/#1).

The code below will create an address from a dataset will information presented like this:

```bash
first_name,last_name,company_name,address,city,county,state,zip,phone1,phone2,email,web
Johnetta,Abdallah,Forging Specialties,1088 Pinehurst St,Chapel Hill,Orange,NC,27514,919-225-9345,919-715-3791,johnetta_abdallah@aol.com,http://www.forgingspecialties.com
Rosio,Cork,Green Goddess,4 10th St W,High Point,Guilford,NC,27263,336-243-5659,336-497-4407,rosio.cork@gmail.com,http://www.greengoddess.com
```

These data are from the [fake addresses](https://raw.githubusercontent.com/libjohn/openrefine/master/data/sample-us-address-data.csv) from this [presentation](https://dsvil.johnlittle.info/api_50.html#p16) and the Google document [here](https://docs.google.com/document/d/1ZiHC1v595tf2NAhv4vVdRYy-Ro78Bc37Y0gs1TfGBco/edit).


### Create addresses

Create new column `full_address` based on column street by filling 234 rows with grel:

```GREL
value + ", " + cells["city_state_zip"].value
```

