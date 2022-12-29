analysis on hotel booking

Hotel Bookings Data Analysis

Objective

We are provided with a hotel bookings dataset.Out main objective is perform EDA on the given dataset and draw useful 
conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other.

Dataset

We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.
- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record. 
- meal: Type of meal chosen 
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for 
                     Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed 
reservation_status_date: Date of making reservation status.

Data Cleaning 

(1) Removing Duplicate rows
All duplicate rows were dropped.

(2) Handling null values
•	Null values in columns company and agent were replaced by 0.
•	Null values in column country were replaced by 'others'.
•	Null values in column children were replaced by the mean of the column.

(3) Converting columns to appropriate data types
•	Changed data type of children, company, agent to int type.
•	Changed data type of reservation_status_date to date type.

(4) Removing outliers
•	One outlier was found in the adr column. Simply dropped it.

(5) Creating new columns
•	Created new column total_stay by adding stays_in_weekend_nights+stays_in_week_nights.
•	Created new column total_people by adding adults+children+babies.

Exploratory Data Analysis

Performed EDA and tried answering the following questions:
-	Q1.Which agent makes most no. of bookings?
-	Q2.Which meal type is most preffered meal of customers?
-	Q3.Which is the most common channel for booking hotels
-	Q4.How long do people stay at the hotels?
-	Q5.What is percentage of bookings in each hotel?
-	Q6.Which hotel has longer waiting time?
-	Q7.Which hotel has higher bookings cancellation rate?
-	Q8.Which room type is in most demand and which room type generates highest adr?
-	Q9.From where most guests are coming?
-	Q10.which hotel seems to make more revenue?
-	Q11.Which hotel has higher lead time?
-	Q12.Which significant distribution channel has highest cancellation percentage?
-	Q13.which channel is mostly used for early booking of hotels?
-	Q14.which channel has longer average waiting time?

Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:

1)Bar Plot.

2)Histogram.

3)Scatter Plot.

4)Pie Chart.

5)Line Plot.

6)Heatmap.

7)Box Plot


Conclusion

1)Around 60% bookings are for City hotel and 40% bookings are for Resort hotel, therefore City Hotel is busier than Resort hotel. Also the overall adr of City hotel is slightly higher than Resort hotel.

2)Mostly guests stay for less than 5 days in hotel and for longer stays Resort hotel is preferred.

3)Both hotels have significantly higher booking cancellation rates and very few guests less than 3 % return for another booking in City hotel. 5% guests return for stay in Resort hotel.

4)Most of the guests came from european countries, with most of guests coming from Portugal.

5)Guests use different channels for making bookings out of which most preferred way is TA/TO.

6)For hotels higher adr deals come via GDS channel, so hotels should increase their popularity on this channel.

7)Not getting same room as reserved, longer lead time and waiting time do not affect cancellation of bookings. Although different room allotment do lowers the adr.

8)BB (bed and breakfast) is the most prefered type of meal in hotel.

9)For customers, generally the longer stays (more than 15 days) can result in better deals in terms of low adr.

10)TA/TO is the most common channel for booking hotels.

