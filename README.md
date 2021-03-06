# AirwaysERM

The All Airways Association (AAA) is an association that brings together all airlines. This association plans to install a comprehensive information system for flight handling. An initial survey produces the following situation report:
When a passenger (passenger number, name, Mr/Mrs, title, etc.) wants to book a flight (or several), he or she first specifies the desired departure and destination airports, the desired flight date and possibly also a time frame when he or she wants to fly away or arrive.
There are various airlines (name, headquarters, etc.) that operate flights. Airlines are identified by a code of maximum three digits (e.g. PA for PanAm, FUA for Futura Air). Each airline operates aircraft (aircraft number, international registration number, name, date of entry into service, etc.) of different aircraft types (type identification, manufacturer, range, etc.).
The airports (name, city, country, capacity in aircraft, etc.) are also encrypted with a three-digit code (e.g. VIE for Vienna-Schwechat, JFK for New York - John F. Kennedy, IBZ for Ibiza). The distances between airports must be recorded in order to be able to take the range of the aircraft type into account when drawing up the flight plan.
Each flight has a departure airport and an arrival airport, the flights are numbered consecutively with a three-digit number within a company. (e.g. PA039 between VIE and JFK, FUA916 between IBZ and VIE) Each flight has a fixed scheduled departure and arrival time, and the days on which the flight takes place are also specified. (e.g. daily for scheduled flights, daily except Sat and Sun, weekly Mon, and the individual days for charter flights). The number of seats available in each class is determined in advance for each flight, the number of remaining free seats must also be determined on an ongoing basis. The flights booked by the passenger are summarized on one ticket (ticket number, date of issue, price, currency, sales office, etc.)
Before starting the flight, the passenger will be given a boarding card at the airport, on which in addition to the flight number, date, departure airport, destination airport and name of the passenger, the allocated seat
(row as number, seat as letter, e.g. 18D) and a smoking or non-smoking license plate appears. The non-smoking seats are assigned on each flight starting from the front of the aircraft, the smoking seats starting from the rear. Seating arrangements depend on the type of aircraft on which the flight is performed. For each seat the class (First Class 1 Economy) and location (window, aisle, middle) are
to hold on to.
For each flight, it must also be possible to record the actual take-off and landing time in order to be able to make evaluations of the punctuality of individual flights.


![ERM](Erm.jpg)


Text notations 

Passagier (passenger_number: INT, name: VARCHAR, gender: CHAR, title: VARCHAR)

Airports (code_airports : VARCHAR, name_airlines : VARCHAR, city : VARCHAR, country : VARCHAR, capacity_in_aircraft : INT)

Ticket Booking (booking_id: INT)

Ticket (ticket_nr. : INT, date_of_issue : DATE, price FLOAT, currency : VARCHAR, sales_office : VARCHAR)

Airlines (code_airlines : VARCHAR, name_airlines : VARCHAR, headquarters : VARCHAR)

Aircraft_types (type_identification : INT, manufacturer : VARCHAR, range_km : INT)

Distance(code_airports : VARCHAR)

Flights (flight_number : INT, code_airlines : VARCHAR, departure_airport_code : VARCHAR, arrival_airport_code : VARCHAR, departure_time : DATE, arrival_time : DATE, days_of_flight : VARCHAR)

Classes (seats_class_name : VARCHAR,  type_identification : INT)

Seats (type_identification : INT, number_of_seats : INT, smoking_seats : BOOLEAN, non_smoking_seats : BOOLEAN)

Time(departure_time : DATE, arrival_time : DATE,)

Boardcard (flight_number : INT, flight_date : DATE, departure_airport_code : VARCHAR, arrival_airport_code : VARCHAR, name_passangers : VARCHAR)

