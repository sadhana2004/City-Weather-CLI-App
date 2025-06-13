# City Weather CLI App

This is a Python-based Command Line Interface (CLI) tool that fetches real-time weather data for multiple cities using the [wttr.in](https://wttr.in) API. You can filter results by temperature, group by weather conditions, and export the report in JSON or CSV format.

---

## Features

- Fetch live weather data for multiple cities
- Filter cities by min/max temperature
- Choose between Celsius and Fahrenheit
- Output results to JSON or CSV
- Group results by weather condition
- Built-in logging (`weather_cli.log`)
- Easy-to-use command-line arguments

---

## 🖥️ Requirements

- Python 3.6+
- `requests` library

### Install dependencies:

```bash
pip install requests
````

---

## 📁 Folder Structure

```
CityWeatherCLI/
│
├── city-weather-cli.py       # Main CLI Python script
├── cities.txt                # List of cities to check
├── .gitignore                # Ignore log/cache files
├── README.md                 # Project documentation
└── weather_cli.log           # Log file (ignored in Git)
```

---

## 🏁 Usage

### 🔹 Step 1: Create `cities.txt`

Include one city per line:

```
Delhi
London
Tokyo
New York
```

### 🔹 Step 2: Run the CLI

Basic command:

```bash
python city-weather-cli.py
```

With filters and options:

```bash
python city-weather-cli.py --min-temp=20 --max-temp=40 --group-by=condition --format=csv --fahrenheit
```

---

## 🛠️ Command-Line Options

| Option         | Description                                      |
| -------------- | ------------------------------------------------ |
| `--min-temp`   | Minimum temperature filter (default: -100)       |
| `--max-temp`   | Maximum temperature filter (default: 100)        |
| `--fahrenheit` | Convert temperature from Celsius to Fahrenheit   |
| `--group-by`   | Group cities by condition (e.g., Cloudy)         |
| `--format`     | Output format: `json` or `csv` (default: `json`) |

---

## 📦 Output

* Automatically saves the report as:

  ```
  weather-report-YYYYMMDD_HHMMSS.json
  ```

  or

  ```
  weather-report-YYYYMMDD_HHMMSS.csv
  ```

* Example:

  ```
  Weather report saved to weather-report-20250613_145046.json
  ```

* Log file:

  ```
  weather_cli.log
  ```

---

## Example

```bash
python city-weather-cli.py --min-temp=25 --group-by=condition --fahrenheit --format=csv
```

Output:

```
Weather report saved to weather-report-20250613_150300.csv
```

---

## License

This project is open-source and available under the [MIT License](LICENSE).

---

## Author

**Sadhana Avanigadda**
Built with 💻 Python + wttr.in + Passion for clean CLI tools.

```

