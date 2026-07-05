# 🧮 DAX Measures

This document contains the DAX measures used to calculate key hospitality KPIs and business metrics for the AtliQ Hospitality Revenue Analytics Dashboard.

---

## Revenue

```DAX
Revenue =
SUM(fact_bookings[revenue_realized])
```

---

## Total Bookings

```DAX
Total Bookings =
COUNT(fact_bookings[booking_id])
```

---

## Total Capacity

```DAX
Total Capacity =
SUM(fact_aggregated_bookings[capacity])
```

---

## Total Successful Bookings

```DAX
Total Successful Bookings =
SUM(fact_aggregated_bookings[successful_bookings])
```

---

## Occupancy %

```DAX
Occupancy % =
DIVIDE([Total Successful Bookings],[Total Capacity],0)
```

---

## Average Rating

```DAX
Average Rating =
AVERAGE(fact_bookings[ratings_given])
```

---

## Number of Days

```DAX
No of Days =
DATEDIFF(
MIN(dim_date[date]),
MAX(dim_date[date]),
DAY
)+1
```

---

## Total Cancelled Bookings

```DAX
Total Cancelled Bookings =
CALCULATE(
[Total Bookings],
fact_bookings[booking_status]="Cancelled"
)
```

---

## Cancellation %

```DAX
Cancellation % =
DIVIDE([Total Cancelled Bookings],[Total Bookings])
```

---

## Total Checked Out

```DAX
Total Checked Out =
CALCULATE(
[Total Bookings],
fact_bookings[booking_status]="Checked Out"
)
```

---

## Total No Show Bookings

```DAX
Total No Show Bookings =
CALCULATE(
[Total Bookings],
fact_bookings[booking_status]="No Show"
)
```

---

## No Show Rate %

```DAX
No Show Rate % =
DIVIDE([Total No Show Bookings],[Total Bookings])
```

---

## Booking % by Platform

```DAX
Booking % by Platform =
DIVIDE(
[Total Bookings],
CALCULATE(
[Total Bookings],
ALL(fact_bookings[booking_platform])
)
)*100
```

---

## Booking % by Room Class

```DAX
Booking % by Room Class =
DIVIDE(
[Total Bookings],
CALCULATE(
[Total Bookings],
ALL(dim_rooms[room_class])
)
)*100
```

---

## ADR (Average Daily Rate)

```DAX
ADR =
DIVIDE([Revenue],[Total Bookings],0)
```

---

## Realisation %

```DAX
Realisation % =
1-([Cancellation %]+[No Show Rate %])
```

---

## RevPAR

```DAX
RevPAR =
DIVIDE([Revenue],[Total Capacity])
```

---

## DBRN (Daily Booked Room Nights)

```DAX
DBRN =
DIVIDE([Total Bookings],[No of Days])
```

---

## DSRN (Daily Sellable Room Nights)

```DAX
DSRN =
DIVIDE([Total Capacity],[No of Days])
```

---

## DURN (Daily Utilized Room Nights)

```DAX
DURN =
DIVIDE([Total Checked Out],[No of Days])
```

---

## Revenue WoW Change %

```DAX
Revenue WoW Change % =
VAR selv =
IF(
HASONEFILTER(dim_date[wn]),
SELECTEDVALUE(dim_date[wn]),
MAX(dim_date[wn])
)

VAR revcw =
CALCULATE([Revenue],dim_date[wn]=selv)

VAR revpw =
CALCULATE(
[Revenue],
FILTER(
ALL(dim_date),
dim_date[wn]=selv-1
)
)

RETURN
DIVIDE(revcw,revpw,0)-1
```

---

## Occupancy WoW Change %

```DAX
Occupancy WoW Change % =
VAR selv =
IF(
HASONEFILTER(dim_date[wn]),
SELECTEDVALUE(dim_date[wn]),
MAX(dim_date[wn])
)

VAR currentWeek =
CALCULATE([Occupancy %],dim_date[wn]=selv)

VAR previousWeek =
CALCULATE(
[Occupancy %],
FILTER(
ALL(dim_date),
dim_date[wn]=selv-1
)
)

RETURN
DIVIDE(currentWeek,previousWeek,0)-1
```

---

## ADR WoW Change %

```DAX
ADR WoW Change % =
VAR selv =
IF(
HASONEFILTER(dim_date[wn]),
SELECTEDVALUE(dim_date[wn]),
MAX(dim_date[wn])
)

VAR currentWeek =
CALCULATE([ADR],dim_date[wn]=selv)

VAR previousWeek =
CALCULATE(
[ADR],
FILTER(
ALL(dim_date),
dim_date[wn]=selv-1
)
)

RETURN
DIVIDE(currentWeek,previousWeek,0)-1
```

---

## RevPAR WoW Change %

```DAX
RevPAR WoW Change % =
VAR selv =
IF(
HASONEFILTER(dim_date[wn]),
SELECTEDVALUE(dim_date[wn]),
MAX(dim_date[wn])
)

VAR currentWeek =
CALCULATE([RevPAR],dim_date[wn]=selv)

VAR previousWeek =
CALCULATE(
[RevPAR],
FILTER(
ALL(dim_date),
dim_date[wn]=selv-1
)
)

RETURN
DIVIDE(currentWeek,previousWeek,0)-1
```

---

## Realisation WoW Change %

```DAX
Realisation WoW Change % =
VAR selv =
IF(
HASONEFILTER(dim_date[wn]),
SELECTEDVALUE(dim_date[wn]),
MAX(dim_date[wn])
)

VAR currentWeek =
CALCULATE([Realisation %],dim_date[wn]=selv)

VAR previousWeek =
CALCULATE(
[Realisation %],
FILTER(
ALL(dim_date),
dim_date[wn]=selv-1
)
)

RETURN
DIVIDE(currentWeek,previousWeek,0)-1
```

---

## DSRN WoW Change %

```DAX
DSRN WoW Change % =
VAR selv =
IF(
HASONEFILTER(dim_date[wn]),
SELECTEDVALUE(dim_date[wn]),
MAX(dim_date[wn])
)

VAR currentWeek =
CALCULATE([DSRN],dim_date[wn]=selv)

VAR previousWeek =
CALCULATE(
[DSRN],
FILTER(
ALL(dim_date),
dim_date[wn]=selv-1
)
)

RETURN
DIVIDE(currentWeek,previousWeek,0)-1
```

---

## 📌 Total Measures

**26 Business DAX Measures** covering:

- Revenue Metrics
- Occupancy Metrics
- Customer Metrics
- Booking Metrics
- Hospitality KPIs
- Week-over-Week Performance Analysis
