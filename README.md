# location-proximity-data

This program contains the code used to populate the database used in my location-proximity-flask-app repository.


The steps I took to populate the database:
  1) Began with a report containing each open store along with their addresses.
  2) Using Google Maps Geocoding API, translated each address to a geographical coordinate.
  3) Using geopy, compared each store's location to every other store's location and calculated the straight-line distance for each instance.
  4) Filtered the above results to only instances where the straight-line distance was less than 50 miles.
  5) Using Google Maps Distance Matrix API, obtained the driving distance and duration for each instance.
  6) Filtered the above results to only instances where the driving distance was less than 50 miles.
  7) Imported this data into the database using pandas and sqlalchemy.
