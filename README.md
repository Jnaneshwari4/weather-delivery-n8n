#  Weather-Aware Delivery Delay System (n8n)

##  Project Overview

This project automates delivery status updates based on real-time weather conditions using the OpenWeatherMap API.
It processes customer orders, checks weather for each city, and flags potential delivery delays.

---

## Features

* Parallel processing of orders using Split Out node
* Real-time weather data using OpenWeatherMap API
* Automatic delay detection (Rain, Snow, Extreme conditions)
* Personalized customer messages
* Error handling for invalid cities
* Secure API usage

---

## 🛠️ Tech Stack

* n8n (Workflow Automation)
* OpenWeatherMap API
* JSON

---

## Workflow Logic

1. Read orders from JSON input
2. Split orders into individual items
3. Fetch weather data for each city
4. Check weather conditions
5. Mark orders as:

   * **Delayed** → if Rain, Snow, or Extreme
   * **On Time** → otherwise
   * **Error** → invalid city
6. Generate personalized customer message

---

## Sample Output

```json
{
  "order_id": "1001",
  "customer": "Alice Smith",
  "city": "New York",
  "status": "On Time",
  "message": "Hi Alice Smith, your order to New York is on time."
}
```
---

##  Setup Instructions

1. Import the `workflow.json` into n8n
2. Add your OpenWeatherMap API key
3. Execute the workflow
---
## 🎥 Demo
 your demo video link- https://drive.google.com/file/d/1z_D0Y65mRPh4laljS1JPBqhzHw56dA8V/view?usp=drivesdk

## Key Learnings
* API integration
* Workflow automation using n8n
* Error handling and resilience
* Conditional logic implementation
---
## Author
Jnaneshwari N
