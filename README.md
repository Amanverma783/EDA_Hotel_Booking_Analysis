# EDA_Hotel_Booking_Analysis

# Objective

We are provided with a hotel bookings dataset.

Out main objective is perform EDA on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other.

### Data Description:

1. **hotel** : *Hotel(Resort Hotel or City Hotel)* 

2. **is_canceled** : *Value indicating if the booking was canceled (1) or not (0)*

3. **lead_time** :* Number of days that elapsed between the entering date of the booking into the PMS and the arrival date*

4. **arrival_date_year** : *Year of arrival date*

5. **arrival_date_month** : *Month of arrival date*

6. **arrival_date_week_number** : *Week number of year for arrival date*

7. **arrival_date_day_of_month** : *Day of arrival date*

8. **stays_in_weekend_nights** : *Number of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at the hotel*

9. **stays_in_week_nights** : *Number of week nights (Monday to Friday) the guest stayed or booked to stay at the hotel*

10. **adults** : *Number of adults*

11. **children** : *Number of children*

12. **babies** : *Number of babies*

13. **meal** : *Type of meal booked. Categories are presented in standard hospitality meal packages:*

14. **country** : *Country of origin.`*

15. **market_segment** : *Market segment designation. In categories, the term “TA” means “Travel Agents” and “TO” means “Tour Operators”*

16. **distribution_channel** : *Booking distribution channel. The term “TA” means “Travel Agents” and “TO” means “Tour Operators”*

17. **is_repeated_guest** : *Value indicating if the booking name was from a repeated guest (1) or not (0)*

18. **previous_cancellations** : *Number of previous bookings that were cancelled by the customer prior to the current booking*

19. **previous_bookings_not_canceled** : *Number of previous bookings not cancelled by the customer prior to the current booking*

20. **reserved_room_type** : *Code of room type reserved. Code is presented instead of designation for anonymity reasons.*

21. **assigned_room_type** : *Code for the type of room assigned to the booking.* 

22. **booking_changes** : *Number of changes/amendments made to the booking from the moment the booking was entered on the PMS until the moment of check-in or cancellation*

23. **deposit_type** : *Indication on if the customer made a deposit to guarantee the booking.*

24. **agent** : *ID of the travel agency that made the booking*

25. **company** : *ID of the company/entity that made the booking or responsible for paying the booking.* 

26. **days_in_waiting_list** : *Number of days the booking was in the waiting list before it was confirmed to the customer*

27. **customer_type** : *Type of booking, assuming one of four categories*


28. **adr** : *Average Daily Rate as defined by dividing the sum of all lodging transactions by the total number of staying nights*

29. **required_car_parking_spaces** : *Number of car parking spaces required by the customer*

30. **total_of_special_requests** : Number of special requests made by the customer (e.g. twin bed or high floor)

31. **reservation_status** : *Reservation last status, assuming one of three categories*
  * Canceled – booking was canceled by the customer
  * Check-Out – customer has checked in but already departed
  * No-Show – customer did not check-in and did inform the hotel of the reason why
  
32. **reservation_status_date** : *Date at which the last status was set. This variable can be used in conjunction with the ReservationStatus to understand when was the booking canceled or when did the customer checked-out of the hotel*

# Data Cleaning 
(1) Removing Duplicate rows
* All duplicate rows were dropped.

(2) Handling null values
* Null values in columns company and agent were replaced by 0.
* Null values in column country were replaced by 'others'.
* Null values in column children were replaced by the mean of the column.
(3) Converting columns to appropriate data types
* Changed data type of children, company, agent to int type.
* Changed data type of reservation_status_date to date type.
(4) Removing outliers
* One outlier was found in the adr column. Simply dropped it.

# Performed EDA and tried answering the following questions:

Ques1.What is the percentage of booking done in different hotels?

Ques2.How many total bookings done in different Years?

Ques3.How many total bookings done in different months?

Ques4.Total Number of Booking Cancelled in different months?

Ques5.Total Number of Non-Cancelled Bookings in different months?

Ques6.How many days customers prefer to stay in week night?

Ques7.How many days customers prefer to stay in weekend night?

Ques8.what is the most preferred meal type by customers?

Ques9.What is Percentage distribution of Deposite type ?

Ques10.Which one is most preferred room type?

Ques11.What are the top 20 countries from where we are getting more customers?

Ques12.What Deposit Type most customer choose?

Ques13.From which market segment we are getting more number of Booking Cancellation?

Ques14.From which market segment we are getting more customers who are not cancelling their booking?

Ques15.Which Agent(id) is booking the most number of hotels?

Ques16.Which Room type has high average price?

Ques17.In Which month most revenue are generated?

Ques18.What is the optimal length to stay?

Ques19.How many repeated guests we have?

Ques20.Correlation between features.

# Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:

* Bar Plot.
* Histogram.
* Scatter Plot.
* Pie Chart.
* Line Plot.
* Heatmap.
* Box Plot

# Conclusion

(1) Around 60% bookings are for City hotel and 40% bookings are for Resort hotel, therefore City Hotel is
busier than Resort hotel. Also the overall adr of City hotel is slightly higher than Resort hotel.
(2) Mostly guests stay for less than 5 days in hotel and for longer stays Resort hotel is preferred.
(3) Both hotels have significantly higher booking cancellation rates and very few guests less than 3 % 
return for another booking in City hotel. 5% guests return for stay in Resort hotel.
(4) Most of the guests came from european countries, with most of guests coming from Portugal.
(5) Guests use different channels for making bookings out of which most preferred way is TA/TO.
(6) For hotels higher adr deals come via GDS channel, so hotels should increase their popularity on this channel.
(7) Almost 30% of bookings via TA/TO are cancelled.
(8) Not getting same room as reserved, longer lead time and waiting time do not affect cancellation of bookings.
Although different room allotment do lowers the adr.
(9) July- August are the most busier and profitable months for both of hotels. 
(10) Within a month, adr gradually increases as month ends, with small sudden rise on weekends.
(11) Couples are the most common guests for hotels, hence hotels can plan services according to couples needs to
increase revenue.
(12) More number of people in guests results in more number of special requests.
(13) Bookings made via complementary market segment and adults have on average high no. of special request.
(14) For customers, generally the longer stays (more than 15 days) can result in better deals in terms of low adr.
