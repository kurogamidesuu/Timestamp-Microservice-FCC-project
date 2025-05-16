# Timestamp Microservice - FCC Project

This is a backend microservice built as part of the [FreeCodeCamp Back End Development and APIs certification](https://www.freecodecamp.org/learn/back-end-development-and-apis/).

## 📌 Objective

Build an API endpoint that takes a date string or timestamp and returns a JSON response with:

- UNIX timestamp
- UTC date string

## 📂 Project Structure

```
.
├── index.js           # Main Express server
├── package.json        # Project metadata and dependencies
├── views/
│   └── index.html      # Landing page
└── public/             # Static files
    └── style.css
```

## 🛠️ How It Works

### Endpoint: `/api/:date?`

- If no `date` is provided, it returns the current date.
- If a **valid date string** or **UNIX timestamp** is passed, it returns:
```json
{
  "unix": 1450137600000,
  "utc": "Fri, 15 Dec 2015 00:00:00 GMT"
}
```
- If the input is invalid:
```json
{ "error": "Invalid Date" }
```

### Examples

- `/api/` → current time
- `/api/2015-12-25` → `{ "unix": ..., "utc": ... }`
- `/api/1451001600000` → `{ "unix": 1451001600000, "utc": "Fri, 25 Dec 2015 00:00:00 GMT" }`

## 🧪 How to Run Locally

```bash
git clone https://github.com/kurogamidesuu/Timestamp-Microservice-FCC-project.git
cd Timestamp-Microservice-FCC-project
npm install
npm start
```

The app will run on `http://localhost:3000`.

## ✍️ Author

Made with 💻 by [kurogamidesuu](https://github.com/kurogamidesuu)