# UserForge

<div align="center">

![UserForge Banner](https://img.shields.io/badge/UserForge-Craft_Realistic_User_Profiles-purple?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTIwIDIxVjE5QzIwIDE3LjkzOTEgMTkuNTc4NiAxNi45MjE3IDE4LjgyODQgMTYuMTcxNkMxOC4wNzgzIDE1LjQyMTQgMTcuMDYwOSAxNSAxNiAxNUg4QzYuOTM5MTMgMTUgNS45MjE3MiAxNS40MjE0IDUuMTcxNTcgMTYuMTcxNkM0LjQyMTQzIDE2LjkyMTcgNCAxNy45MzkxIDQgMTlWMjFNMTYgN0MxNiA5LjIwOTE0IDE0LjIwOTEgMTEgMTIgMTFDOS43OTA4NiAxMSA4IDkuMjA5MTQgOCA3QzggNC43OTA4NiA5Ljc5MDg2IDMgMTIgM0MxNC4yMDkxIDMgMTYgNC43OTA4NiAxNiA3WiIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIyIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPC9zdmc+Cg==)

**Generate realistic user profiles from 110+ countries in seconds with a modern interface**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)](https://flask.palletsprojects.com/)
[![Live Demo](https://img.shields.io/badge/Live_Demo-Visit_Now-brightgreen?style=for-the-badge&logo=vercel)](https://userforge.vercel.app/)

[Live Demo](https://userforge.vercel.app/) • [Features](#features) • [Quick Start](#quick-start) • [API Documentation](#api-documentation) • [Deployment](#deployment)

</div>

---

## Features

- **Global Coverage** - Generate users from 110+ countries worldwide
- **Custom Filters** - Generate users by gender, nationality, and quantity
- **5 Theme Options** - Dark, Light, Red, Blue, and Green themes
- **Responsive Design** - Works seamlessly on all devices
- **Fast & Modern** - Built with performance in mind
- **Live Updates** - Real-time user generation
- **Detailed Profiles** - Complete user information including:
  - Name (Title, First, Last)
  - Contact (Email, Phone, Cell)
  - Location (Address, City, State, Country, Zip)
  - Personal (Age, Gender, DOB, Registration Date)
  - Identification (Username, ID documents)
  - Avatar with Initials

## Quick Start

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Installation

1. Clone the repository
   ```bash
   git clone https://github.com/walterwhite-69/UserForge.git
   cd UserForge
   ```

2. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```

3. Run the application
   ```bash
   python app.py
   ```

4. Open your browser
   ```
   http://localhost:5000
   ```

## API Documentation

### Endpoint: `GET /api/users`

Generate random user profiles with optional filters powered by FakerAPI.it.

#### Query Parameters

| Parameter | Type | Description | Default | Example |
|-----------|------|-------------|---------|---------|
| results | integer | Number of users (1-50) | 10 | ?results=5 |
| gender | string | Filter by gender (male, female) | - | ?gender=female |
| nat | string | Nationality code (see below) | - | ?nat=JP |

#### Supported Countries (110+)

| Code | Country | Code | Country | Code | Country |
|------|----------|------|----------|------|---------|
| AF | Afghanistan | AL | Albania | DZ | Algeria |
| AR | Argentina | AM | Armenia | AU | Australia |
| AT | Austria | AZ | Azerbaijan | BH | Bahrain |
| BD | Bangladesh | BY | Belarus | BE | Belgium |
| BA | Bosnia | BR | Brazil | BG | Bulgaria |
| KH | Cambodia | CA | Canada | CL | Chile |
| CN | China | CO | Colombia | CR | Costa Rica |
| HR | Croatia | CY | Cyprus | CZ | Czech Republic |
| DK | Denmark | EC | Ecuador | EG | Egypt |
| EE | Estonia | ET | Ethiopia | FI | Finland |
| FR | France | GE | Georgia | DE | Germany |
| GH | Ghana | GR | Greece | GT | Guatemala |
| HK | Hong Kong | HU | Hungary | IS | Iceland |
| IN | India | ID | Indonesia | IR | Iran |
| IQ | Iraq | IE | Ireland | IL | Israel |
| IT | Italy | JM | Jamaica | JP | Japan |
| JO | Jordan | KZ | Kazakhstan | KE | Kenya |
| KW | Kuwait | LV | Latvia | LB | Lebanon |
| LY | Libya | LT | Lithuania | LU | Luxembourg |
| MO | Macau | MK | North Macedonia | MY | Malaysia |
| MT | Malta | MX | Mexico | MA | Morocco |
| MM | Myanmar | NP | Nepal | NL | Netherlands |
| NZ | New Zealand | NG | Nigeria | KP | North Korea |
| NO | Norway | OM | Oman | PK | Pakistan |
| PS | Palestine | PA | Panama | PY | Paraguay |
| PE | Peru | PH | Philippines | PL | Poland |
| PT | Portugal | QA | Qatar | RO | Romania |
| RU | Russia | SA | Saudi Arabia | RS | Serbia |
| SG | Singapore | SK | Slovakia | SI | Slovenia |
| ZA | South Africa | KR | South Korea | ES | Spain |
| LK | Sri Lanka | SD | Sudan | SE | Sweden |
| CH | Switzerland | SY | Syria | TW | Taiwan |
| TZ | Tanzania | TH | Thailand | TN | Tunisia |
| TR | Turkey | UA | Ukraine | AE | UAE |
| GB | United Kingdom | US | United States | UY | Uruguay |
| UZ | Uzbekistan | VE | Venezuela | VN | Vietnam |
| YE | Yemen | - | - | - | - |

### Example Request

```bash
curl "http://localhost:5000/api/users?results=3&gender=female&nat=JP"
```

### Example Response

```json
{
  "success": true,
  "count": 3,
  "users": [
    {
      "uuid": "eb338bc6-a747-4f3e-bfaf-79fecf7dee9e",
      "username": "tanaka_momoko710",
      "title": "Ms",
      "first_name": "舞",
      "last_name": "工藤",
      "gender": "female",
      "email": "tanaka.momoko@aol.com",
      "phone": "+995771098743",
      "cell": "+206409398401",
      "street_number": 105,
      "street_name": "田辺町",
      "city": "江古田市",
      "state": "江古田市",
      "country": "Japan",
      "postcode": "2103931",
      "nationality": "JP",
      "date_of_birth": "2021-11-18T00:00:00.000Z",
      "age": 3,
      "registered_date": "2019-11-29T15:10:21.000Z",
      "registered_age": 6,
      "picture_large": null,
      "picture_medium": null,
      "picture_thumbnail": null,
      "id_name": "National ID",
      "id_value": "889047757"
    }
  ]
}
```

## Python Usage

```python
import requests
import json

BASE_URL = "http://localhost:5000"

# Get 5 female users from Japan
response = requests.get(f"{BASE_URL}/api/users?results=5&nat=JP&gender=female")
data = response.json()

for user in data['users']:
    print(f"Name: {user['first_name']} {user['last_name']}")
    print(f"Email: {user['email']}")
    print(f"Location: {user['city']}, {user['country']}")
    print(f"Username: {user['username']}")
    print("-" * 50)
```

### Output Example

```
Name: 舞 工藤
Email: tanaka.momoko@aol.com
Location: 江古田市, Japan
Username: tanaka_momoko710
--------------------------------------------------
Name: 智実 中島
Email: yoko42@yahoo.com
Location: 江古田市, Japan
Username: yoko42652
--------------------------------------------------
```

## JavaScript Usage

```javascript
// Fetch 3 female users from Germany
fetch('http://localhost:5000/api/users?results=3&gender=female&nat=DE')
  .then(response => response.json())
  .then(data => {
    data.users.forEach(user => {
      console.log(`${user.first_name} ${user.last_name}`);
      console.log(`Email: ${user.email}`);
      console.log(`Phone: ${user.phone}`);
      console.log(`---`);
    });
  })
  .catch(error => console.error('Error:', error));
```

## Themes

UserForge includes 5 themes:
- Dark (default, with purple accents)
- Light (clean and minimal)
- Red (vibrant look)
- Blue (cool and soft)
- Green (fresh tone)

Click the theme toggle button in the header to switch themes.

## Deployment

### Vercel

1. Install Vercel CLI:
   ```bash
   npm install -g vercel
   ```

2. Deploy:
   ```bash
   vercel
   ```

### Heroku

1. Create a Heroku app:
   ```bash
   heroku create your-app-name
   ```

2. Push to Heroku:
   ```bash
   git push heroku main
   ```

### Railway

1. Connect your GitHub repository to Railway
2. Set the start command: `python app.py`
3. Deploy!

## Project Structure

```
UserForge/
├── static/
│   ├── index.html
│   ├── style.css
│   └── app.js
├── app.py
├── example_fetch.py
├── requirements.txt
├── vercel.json
└── README.md
```

## Tech Stack

- Backend: Flask (Python)
- Frontend: HTML5, CSS3, JavaScript
- API: FakerAPI.it
- Styling: Custom CSS Variables
- Deployment: Vercel, Heroku, Railway

## Use Cases

- Development & Testing - Generate test user data for any country
- UI/UX Design - Populate designs with realistic global profiles
- Data Analysis - Create sample datasets from various locales
- Education - Learn API integration and JSON handling
- Internationalization - Test apps with multilingual user data

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome!

1. Fork the project
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Acknowledgments

- Data: [FakerAPI.it](https://fakerapi.it/)
- Inspiration: modern minimal web design

## Contact

Have questions or want to collaborate?

- Discord: [discord.gg/rgWcEw5G8a](https://discord.gg/rgWcEw5G8a)
- Discord Username: heisenburger_7

---

<div align="center">

Made with love by Walter

[Back to top](#userforge)

</div>
