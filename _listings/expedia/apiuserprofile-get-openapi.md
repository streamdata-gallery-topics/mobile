---
swagger: "2.0"
x-collection-name: Expedia
x-complete: 0
info:
  title: Expedia Profile
  description: Mobile API User Profile
  version: 0.0.1
host: apim.expedia.com
basePath: x/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/flight/airportDropDown:
    get:
      summary: Airport Dropdown
      description: Mobile API Flight Airport Dropdown Operation
      operationId: flights-airport-dropdown
      x-api-path-slug: apiflightairportdropdown-get
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Airports
      - Airplanes
      - Airlines
  /api/flight/checkout:
    post:
      summary: Mobile Flight Checkout
      description: Checkout a previously created flight trip, requiring payment fields,
        the trip id, and the passenger fields
      operationId: flights-checkout
      x-api-path-slug: apiflightcheckout-post
      parameters:
      - in: formData
        name: associatedFlightPassengers[0].birthDate
        description: Birth date of the associated flight passenger fields
      - in: formData
        name: associatedFlightPassengers[0].gender
        description: Gender of the associated flight passenger fields
      - in: formData
        name: associatedFlightPassengers[0].knownTravelerNumber
        description: knownTravelerNumber(PreCheckNumber) of the associated flight
          passenger fields
      - in: formData
        name: associatedFlightPassengers[0].passengerCategory
        description: :Passenger category of the associated flight passenger fields
      - in: formData
        name: associatedFlightPassengers[0].passportCountryCode
        description: Passport country code of the associated flight passenger fields
      - in: formData
        name: associatedFlightPassengers[0].seatPreference
        description: Seat preference of the associated flight passenger fields
      - in: formData
        name: associatedFlightPassengers[0].seats[0].arrivalAirportCode
        description: The arrival airport code for the selected seat of the associated
          flight passenger fields
      - in: formData
        name: associatedFlightPassengers[0].seats[0].departureAirportCode
        description: The departure airport code for the selected seat of the associated
          flight passenger fields
      - in: formData
        name: associatedFlightPassengers[0].seats[0].seatNumber
        description: Selected Seat Number of the associated flight passenger fields
      - in: formData
        name: associatedFlightPassengers[0].specialAssistanceOption
        description: Special assistance option for the associated flight passenger
          fields
      - in: formData
        name: associatedFlightPassengers[0].title
        description: Title of the associated flight passenger fields
      - in: formData
        name: associatedFlightPassengers[0].TSARedressNumber
        description: TSA redress number of the associated flight passenger fields
      - in: formData
        name: birthDate
        description: Birth date of the associated flight passenger fields
      - in: formData
        name: city
        description: The city of the travelers billing address
      - in: formData
        name: country
        description: The 3 letter country code of the travelers billing address
      - in: formData
        name: creditCardNumber
        description: The credit card number used for this booking, if checking out
          with a new card
      - in: formData
        name: cvv
        description: The CVV of the travelers credit card used for this booking
      - in: formData
        name: doIThinkImSignedIn
        description: As a client I am checking-out with the assumption that I am signed
          in
      - in: formData
        name: email
        description: Email address of the main flight passenger
      - in: formData
        name: expectedCardFee
        description: The expected credit card fee, as returned by the createTrip call
          in the validFormsOfPayment object for whatever credit card the user is paying
          with
      - in: formData
        name: expectedCardFeeCurrencyCode
        description: Three letter 4217 ISO currency code of the expected credit card
          fee
      - in: formData
        name: expectedFareCurrencyCode
        description: Three letter 4217 ISO currency code of the expected total price
      - in: formData
        name: expectedTotalFare
        description: The expected total price of the trip, matching exactly whatever
          the user last saw
      - in: formData
        name: expediaEmailOptIn
        description: If the main flight passenger wishes to opt out for Expedia emails
          or not
      - in: formData
        name: expirationDateMonth
        description: The expiration date month of the credit card used for this booking
      - in: formData
        name: expirationDateYear
        description: The 4 digit expiration date year of the credit card used for
          this booking
      - in: formData
        name: firstName
        description: The first name of the traveler
      - in: formData
        name: frequentFlyerDetails[0].flightAirlineCode
        description: Airline code for the flight to be booked
      - in: formData
        name: frequentFlyerDetails[0].frequentFlyerPlanAirlineCode
        description: Airline code for the airline whose frequent Flyer programme is
          to be used
      - in: formData
        name: frequentFlyerDetails[0].frequentFlyerPlanCode
        description: Plan code for Airline program
      - in: formData
        name: frequentFlyerDetails[0].membershipNumber
        description: User specific membership number for the frequent flyer programme
      - in: formData
        name: gender
        description: Gender of the associated flight passenger fields
      - in: formData
        name: knownTravelerNumber
        description: knownTravelerNumber(PreCheckNumber) of the associated flight
          passenger fields
      - in: formData
        name: lastName
        description: The last name of the traveler
      - in: formData
        name: mainFlightPassenger[0].email
        description: Email address of the main flight passenger
      - in: formData
        name: mainFlightPassenger[0].expediaEmailOptIn
        description: If the main flight passenger wishes to opt out for Expedia emails
          or not
      - in: formData
        name: mainFlightPassenger[0].password
        description: Password of the main flight passenger
      - in: formData
        name: mainFlightPassenger[0].phone
        description: Phone number of the main flight passenger
      - in: formData
        name: mainFlightPassenger[0].phoneCountryCode
        description: Country code of the phone of the main flight passenger
      - in: formData
        name: middleName
        description: The middle name of the traveler
      - in: formData
        name: nameOnCard
        description: The card holders name
      - in: formData
        name: omniturePartnerId
        description: Omniture partner identification string
      - in: formData
        name: passengerCategory
        description: :Passenger category of the associated flight passenger fields
      - in: formData
        name: passportCountryCode
        description: Passport country code of the associated flight passenger fields
      - in: formData
        name: password
        description: Password of the main flight passenger
      - in: formData
        name: phone
        description: Phone number of the main flight passenger
      - in: formData
        name: phoneCountryCode
        description: Country code of the phone of the main flight passenger
      - in: formData
        name: postalCode
        description: The postal code of the travelers billing address
      - in: formData
        name: prettyPrint
        description: If true, return JSON with tabs, spaces and newlines to be human
          readable
      - in: formData
        name: seatPreference
        description: Seat preference of the associated flight passenger fields
      - in: formData
        name: seats[0].arrivalAirportCode
        description: The arrival airport code for the selected seat of the Main flight
          passenger fields
      - in: formData
        name: seats[0].departureAirportCode
        description: The departure airport code for the selected seat of the Main
          flight passenger fields
      - in: formData
        name: seats[0].seatNumber
        description: Selected Seat Number of the Main flight passenger fields
      - in: formData
        name: sendEmailConfirmation
        description: Used to check if confirmation email needs to be sent or not
      - in: formData
        name: specialAssistanceOption
        description: Special assistance option for the associated flight passenger
          fields
      - in: formData
        name: state
        description: The state (or province) of the travelers billing address
      - in: formData
        name: storeCreditCardInUserProfile
        description: Indicates whether to save the credit card information as a stored
          credit card in the user profile
      - in: formData
        name: storedCreditCardId
        description: The GUID for the stored credit card information to be used for
          payment
      - in: formData
        name: streetAddress
        description: The street part of the credit card owners billing address
      - in: formData
        name: streetAddress2
        description: Apartment or suite number of the travelers billing address
      - in: formData
        name: suppressFinalBooking
        description: If true, do not actually charge for and book the trip, stop after
          creating the itinerary
      - in: formData
        name: tealeafTransactionId
        description: The unique transaction ID used in TeaLeaf PSR tracking
      - in: formData
        name: title
        description: Title of the associated flight passenger fields
      - in: formData
        name: tripId
        description: The trip ID of an existing trip, from /api/flight/trip/create
      - in: formData
        name: TSARedressNumber
        description: TSA redress number of the associated flight passenger fields
      - in: formData
        name: validateWithChildren
        description: Set this flag to true to enable child validation logic on the
          server
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Airports
      - Airplanes
      - Airlines
  /api/flight/details:
    get:
      summary: Details
      description: Mobile API Flight Details Operation
      operationId: flights-details
      x-api-path-slug: apiflightdetails-get
      parameters:
      - in: query
        name: arrivalAirport
        description: The three letter airport code for where the customer is going
      - in: query
        name: childTravelerAge
        description: childTravelerAge represents the age of a single child traveler
      - in: query
        name: departureAirport
        description: The three letter airport code for where the customer is leaving
          from
      - in: query
        name: departureDate
        description: Date the customer wants to leave for their flight on, in ISO
          format
      - in: query
        name: infantSeatingInLap
        description: Set to true if infant(s) are without a reserved seat (in an adults
          lap)
      - in: query
        name: numberOfAdultTravelers
        description: 'Number of Adult Travelers (Default: 1)'
      - in: query
        name: productKey
        description: A productKey, obtained from a call to flight search, within the
          past 20 minutes
      - in: query
        name: returnDate
        description: Date the customer wants to return on
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Airports
      - Airplanes
      - Airlines
  /api/flight/image:
    get:
      summary: Flight Image
      description: Mobile API Flight Image Operation
      operationId: flights-image
      x-api-path-slug: apiflightimage-get
      parameters:
      - in: query
        name: destinationCode
        description: The three letter airport code or metro code of the destination
      - in: query
        name: imageHeight
        description: Requested height of the image
      - in: query
        name: imageWidth
        description: Requested width of the image
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Airports
      - Airplanes
      - Images
      - Airlines
  /api/flight/search:
    get:
      summary: Search
      description: Mobile API Flights
      operationId: flights-search
      x-api-path-slug: apiflightsearch-get
      parameters:
      - in: query
        name: arrivalAirport
        description: The three letter airport code to where the customer is going
      - in: query
        name: childTravelerAge
        description: childTravelerAge represents the age of a single child traveler
      - in: query
        name: correlationId
        description: Optional parameter to define a correlation between a hotel search
          and a flight search
      - in: query
        name: departureAirport
        description: The three letter airport code for where the customer is leaving
          from
      - in: query
        name: departureDate
        description: Date the customer wants to leave for their flight on, in ISO
          format
      - in: query
        name: featureOverride
        description: Optional field to specify a comma separated list of feature toggling
          flag names, use _ (underscore) ahead of flag name to disable feature ex,
          Flex,FlightSearchCacheGet,_FlightSearchCachePut
      - in: query
        name: infantSeatingInLap
        description: Set to true if infant(s) are without a reserved seat (in an adults
          lap)
      - in: query
        name: lccAndMerchantFareCheckoutAllowed
        description: flag to indicate whether lcc and merchant fares should be returned
          in search response
      - in: query
        name: maxOfferCount
        description: Maximum number of offers to return
      - in: query
        name: nonStopFlight
        description: 'Set to true to return only non stop flights in the search response '
      - in: query
        name: numberOfAdultTravelers
        description: 'Number of Adult Travelers (Default: 1)'
      - in: query
        name: prettyPrint
        description: Controls JSON response formatting
      - in: query
        name: returnDate
        description: Date the customer wants to return on
      - in: query
        name: showRefundableFlight
        description: 'Set to true to return only refundable(Free cancellation available)
          flights in the search response '
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Airports
      - Airplanes
      - Airlines
  /api/flight/trip/create:
    post:
      summary: Create A Trip
      description: Mobile API Flights Create Trip Operation
      operationId: flights-create-trip
      x-api-path-slug: apiflighttripcreate-post
      parameters:
      - in: formData
        name: fareFamilyCode
      - in: formData
        name: fareFamilyTotalPrice
      - in: formData
        name: mobileShoppingKey
        description: The mobile shopping key we are going to create a trip for
      - in: formData
        name: productKey
        description: The product key, obtained from /api/flight/search, we are going
          to create a trip for
      - in: formData
        name: qualifyAirAttach
        description: Whether to return a qualified air attach product for this trip
      - in: formData
        name: tripTitle
        description: The name of this itinerary as it will appear to customer service
          and in the itinerary list
      - in: formData
        name: withInsurance
        description: Whether to return the available insurance options for this trip
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Airports
      - Airplanes
      - Trips
      - Airlines
  /api/m/trip/coupon:
    post:
      summary: Apply Coupon
      description: Mobile API Packages Apply Coupon
      operationId: packages-apply-coupon
      x-api-path-slug: apimtripcoupon-post
      parameters:
      - in: formData
        name: coupon.code
        description: Coupon Code
      - in: formData
        name: coupon.instanceId
        description: Instance ID
      - in: formData
        name: coupon.name
        description: Coupon Name
      - in: formData
        name: tripId
        description: The tripId we are going to apply the coupon to
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Airports
      - Airplanes
      - Coupons
      - Airlines
  /api/m/trip/remove/coupon:
    post:
      summary: Remove Coupon
      description: Mobile API Packages Remove Coupon
      operationId: packages-remove-coupon
      x-api-path-slug: apimtripremovecoupon-post
      parameters:
      - in: formData
        name: tripId
        description: The tripId we are going to apply the coupon to
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Airports
      - Airplanes
      - Coupons
      - Airlines
  /api/mobile/image:
    get:
      summary: Mobile Image
      description: Mobile API Flight Mobile Image Operation
      operationId: flights-mobile-image
      x-api-path-slug: apimobileimage-get
      parameters:
      - in: query
        name: imageCode
        description: image primary key, for example CAR:ECONOMY ACTIVITY:DISNEY DESTINATION:JFK
          DESTINATIONMOBILEWEB:JFK CARMOBILEWEB:MINI
      - in: query
        name: imageHeight
        description: Requested height of the image
      - in: query
        name: imageType
        description: type of image
      - in: query
        name: imageWidth
        description: Requested width of the image
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Airports
      - Airplanes
      - Images
      - Airlines
  /api/packages/checkout:
    post:
      summary: Checkout
      description: Mobile API Packages Checkout
      operationId: packages-checkout
      x-api-path-slug: apipackagescheckout-post
      parameters:
      - in: formData
        name: city
        description: The city of the travelers billing address
      - in: formData
        name: country
        description: The 3 letter country code of the travelers billing address
      - in: formData
        name: creditCardNumber
        description: The credit card number used for this booking, if checking out
          with a new card
      - in: formData
        name: cvv
        description: The CVV of the travelers credit card used for this booking
      - in: formData
        name: doIThinkImSignedIn
        description: As a client I am checking-out with the assumption that I am signed
          in
      - in: formData
        name: expectedCardFee
        description: The expected credit card fee, as returned by the createTrip call
          in the validFormsOfPayment object for whatever credit card the user is paying
          with
      - in: formData
        name: expectedCardFeeCurrencyCode
        description: Three letter 4217 ISO currency code of the expected total price
      - in: formData
        name: expectedFareCurrencyCode
        description: Three letter 4217 ISO currency code of the expected credit card
          fee
      - in: formData
        name: expectedTotalFare
        description: The expected total price of the trip, matching exactly whatever
          the user last saw
      - in: formData
        name: expirationDateMonth
        description: The expiration date month of the credit card used for this booking
      - in: formData
        name: expirationDateYear
        description: The 4 digit expiration date year of the credit card used for
          this booking
      - in: formData
        name: flight[0].associatedFlightPassengers[0].birthDate
        description: Birth date of the associated flight passenger fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].gender
        description: Gender of the associated flight passenger fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].knownTravelerNumber
        description: knownTravelerNumber(PreCheckNumber) of the associated flight
          passenger fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].passengerCategory
        description: :Passenger category of the associated flight passenger fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].passportCountryCode
        description: Passport country code of the associated flight passenger fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].seatPreference
        description: Seat preference of the associated flight passenger fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].specialAssistanceOption
        description: Special assistance option for the associated flight passenger
          fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].title
        description: Title of the associated flight passenger fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].TSARedressNumber
        description: TSA redress number of the associated flight passenger fields
      - in: formData
        name: flight[0].mainFlightPassenger[0].email
        description: Email address of the main flight passenger
      - in: formData
        name: flight[0].mainFlightPassenger[0].expediaEmailOptIn
        description: If the main flight passenger wishes to opt out for Expedia emails
          or not
      - in: formData
        name: flight[0].mainFlightPassenger[0].password
        description: Password of the main flight passenger
      - in: formData
        name: flight[0].mainFlightPassenger[0].phone
        description: Phone number of the main flight passenger
      - in: formData
        name: flight[0].mainFlightPassenger[0].phoneCountryCode
        description: Country code of the phone of the main flight passenger
      - in: formData
        name: hotel[0].bedTypeId
        description: Indicates the selected bed Type
      - in: formData
        name: hotel[0].primaryContactFullName
        description: Full name of the person who will be checking in
      - in: formData
        name: nameOnCard
        description: The card holders name
      - in: formData
        name: omniturePartnerId
        description: Omniture partner identification string
      - in: formData
        name: postalCode
        description: The postal code of the travelers billing address
      - in: formData
        name: sendEmailConfirmation
        description: Used to check if confirmation email needs to be sent or not
      - in: formData
        name: state
        description: The state (or province) of the travelers billing address
      - in: formData
        name: storeCreditCardInUserProfile
        description: Indicates whether to save the credit card information as a stored
          credit card in the user profile
      - in: formData
        name: storedCreditCardId
        description: The GUID for the stored credit card information to be used for
          payment
      - in: formData
        name: streetAddress
        description: The street part of the credit card owners billing address
      - in: formData
        name: streetAddress2
        description: Apartment or suite number of the travelers billing address
      - in: formData
        name: tealeafTransactionId
        description: The unique transaction ID used in TeaLeaf PSR tracking
      - in: formData
        name: tripId
        description: The trip ID of an existing trip, from /api/packages/createTrip
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Packages
  /api/packages/createTrip:
    post:
      summary: Create A Trip
      description: Mobile API Packages Create Trip operation
      operationId: packages-create-trip
      x-api-path-slug: apipackagescreatetrip-post
      parameters:
      - in: formData
        name: destinationId
        description: stubbed
      - in: formData
        name: productKey
        description: The product ID (piid) of the package you would like to get hotel
          offers for
      - in: formData
        name: roomOccupants[0].childGuestAge
        description: represents the age of a single child guest staying in this room
      - in: formData
        name: roomOccupants[0].infantsInSeat
        description: Any infants in seat
      - in: formData
        name: roomOccupants[0].numberOfAdultGuests
        description: 'Number of adults staying in this room (default: 1)'
      - in: formData
        name: roomOccupants[0].seniorCount
        description: 'Number of seniors staying in this room (default: 0)'
      - in: formData
        name: tripName
        description: stubbed
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Packages
  /api/packages/hotelOffers:
    get:
      summary: Get Package Offers
      description: Mobile API Packages
      operationId: packages-offers
      x-api-path-slug: apipackageshoteloffers-get
      parameters:
      - in: query
        name: checkInDate
        description: Date the traveler will be checking in to their hotel
      - in: query
        name: checkOutDate
        description: Date the traveler will be checking out of their hotel
      - in: query
        name: childTravelerAge
        description: childTravelerAge represents the age of a single child traveler
      - in: query
        name: infantSeatingInLap
        description: Set to true if infant(s) are without a reserved seat (in an adults
          lap)
      - in: query
        name: numberOfAdultTravelers
        description: 'Number of Adult Travelers (Default: 1)'
      - in: query
        name: productKey
        description: The product ID (piid) of the package you would like to get hotel
          offers for
      - in: query
        name: ratePlanCode
        description: Rate Plan Code of the selected hotel offer
      - in: query
        name: roomTypeCode
        description: Room Type Code of the selected hotel offer
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Packages
      - Offers
      - Hotels
  /api/trips:
    get:
      summary: Get Trips
      description: Mobile API Trips
      operationId: trips-search
      x-api-path-slug: apitrips-get
      parameters:
      - in: query
        name: filterBookingStatus
        description: An optional parameter to filter by booking status
      - in: query
        name: filterLineOfBusiness
        description: An optional parameters to filter by line of business
      - in: query
        name: filterTimePeriod
        description: An optional parameter to filter by time period
      - in: query
        name: getCachedDetails
        description: Optionally get full details for the first N trips
      - in: query
        name: sort
        description: An optional parameter to sort by date
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Search
  /api/trips/{tripId}:
    get:
      summary: Trips by tripId
      description: Mobile API Trips
      operationId: trips-search-id
      x-api-path-slug: apitripstripid-get
      parameters:
      - in: query
        name: currencyCode
        description: Currency parameter
      - in: query
        name: decimalPlaceCount
        description: Decimal place count for the expected amount
      - in: query
        name: decorator
        description: Nullifies complex elements of a Trip with exception of Price
          related elements and their parents
      - in: query
        name: email
        description: To pull a guest itinerary specify the email address associated
          with the trip
      - in: query
        name: expectedAmount
        description: Expected Amount during car cancellation
      - in: path
        name: tripId
        description: The trip ID
      - in: query
        name: useCache
        description: An optional flag to make a cached read trip call
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Search
      - Trips
  /api/trips/{tripId}/updateTripNameDescription:
    post:
      summary: Update Trip Name and Description
      description: Mobile API Trips update trip name and description operation
      operationId: trips-update-trip
      x-api-path-slug: apitripstripidupdatetripnamedescription-post
      parameters:
      - in: path
        name: tripId
        description: Trip ID
      - in: formData
        name: tripname
        description: The name of the trip
      - in: formData
        name: tripnote
        description: The comments of the trip
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Search
      - Trips
  /api/user/associateUserToTrip:
    post:
      summary: Associate User To Trip
      description: Mobile API User Associate To Trip
      operationId: user-associate-to-trip
      x-api-path-slug: apiuserassociateusertotrip-post
      parameters:
      - in: formData
        name: foo
        description: stubbed
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Search
      - Trips
  /api/user/create:
    post:
      summary: Create User
      description: Mobile API User Create
      operationId: create-user
      x-api-path-slug: apiusercreate-post
      parameters:
      - in: formData
        name: email
        description: Users email address
      - in: formData
        name: enrollInLoyalty
        description: Whether to enroll the user in loyalty
      - in: formData
        name: expediaEmailOptIn
        description: Whether to opt-in the users email to travel deals
      - in: formData
        name: firstName
        description: Users first name
      - in: formData
        name: lastName
        description: Users last name
      - in: formData
        name: middleName
        description: Users middle name
      - in: formData
        name: password
        description: Users password
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Users
  /api/user/profile:
    get:
      summary: Profile
      description: Mobile API User Profile
      operationId: profile-user
      x-api-path-slug: apiuserprofile-get
      parameters:
      - in: query
        name: profileTypes
        description: This is a comma-separated list of profile types to retrieve when
          the login is processed
      - in: query
        name: retrieveCoupons
        description: Whether to include user coupons in the response
      - in: query
        name: tuid
        description: The tuid of the user/account whose profile you would like
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Users
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---