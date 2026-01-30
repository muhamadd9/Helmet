# Admin Dashboard – Features & Flow Documentation

This document describes all admin features, flows, and managed entities inside the dashboard.

---

## 1. Users Management

### Description
Manage all application users and control their access and subscriptions.

### Features
- View all users.
- View full user details:
  - Full name
  - Phone number
  - Date of birth
  - Account creation date
  - Current subscription status (active / expired)
  - Current subscription plan
- User actions:
  - Block user
  - Unblock user

---

## 2. Bikers Management

### Description
Manage bikers responsible for performing washes in assigned areas.

### Features
- Add new biker.
- Edit biker information.
- Delete biker.
- View all bikers.

### Biker Data
- Name
- Mobile number
- Unique biker identifier
- Assigned area
- Total number of washes
- Total earnings / commission
- Rating

---

## 3. Car Brands & Models

### 3.1 Car Brands

#### Features
- View all car brands.
- Add new brand.
- Edit brand.
- Delete brand.

#### Brand Data
- Name (Arabic)
- Name (English)
- Image URL

---

### 3.2 Car Models

#### Features
- View all models under each brand.
- Add model under a specific brand.
- Edit model.
- Delete model.

#### Model Data
- Name (Arabic)
- Name (English)
- Related brand

---

## 4. Plans / Subscriptions

### Description
Manage subscription plans available for users.

### Features
- Add plan.
- Edit plan.
- Delete plan.
- View all plans.

### Plan Data
- Title (Arabic / English)
- Description (Arabic / English)
- Price
- Offer percentage
- Number of washes included
- Expires after (time period after subscription)
- Image

### Display Logic
- Final price is calculated after discount.
- Remaining washes are returned within user subscription data.

---

## 5. Single Wash Packages

### Description
Individual wash options without subscriptions.

### Features
- Add wash.
- Edit wash.
- Delete wash.
- View all washes.

### Wash Data
- Title
- Description
- Price

---

## 6. Additional Services

### Description
Extra services that can be added to any wash.

### Features
- Add service.
- Edit service.
- Delete service.
- View all services.

### Service Data
- Name (Arabic / English)
- Price
- Image

---

## 7. Areas & Zones Management

### Description
Define service areas, assign bikers, and manage available washing times per zone.

### Features
- Create area using map.
- Define area using polygon drawing.
- Set area radius if needed.
- Assign one or more bikers to the area.
- Edit area.
- Delete area.

### Area Data
- Polygon coordinates
- Assigned biker(s)

---

### 7.1 Zone Time Slots Management

### Description
Control available washing times for each zone to ensure proper scheduling and avoid overbooking.

### Purpose
- Admin defines when washes can be performed in each zone.
- Users can only book washes in **available (empty) time slots**.
- Prevents scheduling conflicts and biker overload.

### Features
- Add time slots per zone.
- Edit time slots.
- Delete time slots.
- Enable / disable specific time slots.
- View all time slots for a zone.

### Time Slot Data
- Zone reference
- Day(s) of week (e.g. Saturday – Thursday)
- Start time
- End time
- Slot duration (optional, e.g. 30 / 60 minutes)
- Max bookings per slot (optional)
- Status (active / inactive)

### Booking Logic
- User selects location → system detects zone.
- System fetches available time slots for that zone.
- Already booked slots are excluded.
- User can only select empty, active time slots.

---

## 8. Payments & Subscriptions Overview

### Description
Monitor subscriptions and revenue.

### Features
- View all user subscriptions.
- Display:
  - Total number of subscriptions
  - Total subscription revenue
- View revenue from single washes.
- View total income (subscriptions + washes).

---

## 9. Home Dashboard (Analytics)

### Description
High-level system analytics and insights.

### Displayed Data
- Total users
- Total bikers
- Total washes
- Daily / monthly revenue
- Most active areas
- Top performing bikers

---

## 10. Wash Pricing & Commission Rules

### Description
Manage wash prices and biker commission rules.

### Features
- Set base wash price.
- Define biker commission per wash order:
  - First wash of the day → specific percentage
  - Second wash → different percentage
  - And so on
- Edit commission rules at any time.

---
