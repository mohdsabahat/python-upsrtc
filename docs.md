# Documentation

## UPSRTC Class
### Constructor
The  ```UPSRTC``` class takes no argument.
### Methods
- get_bus_stops()
    - Gets a list of all available bus stops.
- set_start_date(date)
    - date is the object of ```datetime.datetime``` class.
- set_start_station(station_code)
    - station_code is the code of the station can be found from ```get_bus_stops()```.
- set_end_station(station_code)
    - station_code is the code of the station can be found from ```get_bus_stops()```.
- find_buses()
    - Finds buses corresponding to the set journey settings.
### Attributes
- bus_stops
    - List of ```BusStop``` object, containing information about bus stop (requires get_bus_stops method to be called first).
- tickets
    - List of buses available for the desired journey settings (start_station_code, end_station_code and start_date should be set using respective setters before calling this method).

## DataType
### BusStop
- #### Attributes

    The ```BusStop``` object has the following attributes:

        - 'name': str [Name of the bus stop]
        - 'code': str [Code of the bus stop]
        - 'latitude': str [Latitude of the bus stop (always empty idk why) ]
        - 'longitude': str [Longitude of the bus stop (always empty idk why) ]
        - 'address': str [Address of the bus stop (always empty idk why) ]
        - 'id': 'id'
        - 'direction': int [idk what it does]
        - 'abbreviation': [idk even the type for this one]

- #### Methods
    The ```BusStop``` has no user methods.

## Ticket
- ### Attributes
  The ```Ticket``` object has the following attributes:
  ```
    - 'bus_code': str [Code of the bus]
    - 'trip_number': str [Unique trip number for this trip]
    - 'route_code': str [Code for this route]
    - 'route_name': str [Name of this route]
    - 'via': str [Via station if any] 
    - 'depot_id': int [Id of the depot to which bus belongs] 
    - 'depot_name': str [Name of the depot to which the bsu belongs]
    - 'available_seats': int [Number of available seats in bus]
    - 'total_seats': int [Total number of seats in bus]
    - 'seats': List(Seat) [List of Seat objects containg information about the seat]
    - 'fare': Fare [a Fare object containing break of the fare] (not implemented yet)
    ```
  Also see [Fare](#fare) and [Seat](#seat)

- ### Methods

## Seat
- ### Attributes
  The ```Seat``` object has the following attributes:
  ```
      code : str [Seat code]
      status : str ['0' for unbooked and '1' for booked]
      gender : str [Maybe contains which gender booked this seat?]
  ```

- ### Methods
    - is_booked
        - Returns a boolean indicating whether the seat is booked or not

## Fare
- ### Attributes
  The ```Fare``` object has following attributes:
- ### Methods