# alma_inventory_to_replacement_cost
## Overview
This is a straightforward script that maps whatever value is in the inventory_price field to the replacement_cost field. It first makes a `GET` request to pull the item object, building each request url using the required csv file. It pulls the existing `inventory_price` value and maps it onto the `replacement_cost` field. It *will* overrwite any existing value in the `replacement_cost` field. Once the value has been mapped, a `PUT` request is sent back containing the altered item object.
## Requirements
rw bibs api key
csv file output from a physical items subject area analyses.
- must contain the columns: `Holding Id` `Mms Id` `Physical Item Id`
- output as data > csv 
