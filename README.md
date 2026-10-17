# 💱 Currency Converter (Java Swing)

A simple desktop currency converter built in **Java** with a **Swing** graphical interface, created in **NetBeans**. Pick a "from" and "to" country, enter an amount, and get the converted value instantly. It uses predefined, hardcoded exchange rates, which makes it a good small project for learning Java GUI development.

## ✨ Features

- Swing GUI with a clean bordered layout (Nimbus look and feel when available)
- Convert between 6 countries and their currencies
- Currency unit label updates as you change the selection
- Result shown to 2 decimal places
- Convert, Reset and Exit buttons

## 🌍 Supported Currencies

| Country | Currency | Rate (per 1 base unit) |
|---|---|---|
| Afghanistan | Afghani (AFN) | 89.8278 |
| Albania | Lek (ALL) | 119.064 |
| Algeria | Algerian Dinar (DZD) | 171.788 |
| Andorra | Euro (EUR) | 1.18550 |
| USA | US Dollar (USD) | 1.26864 |
| India | Indian Rupee (INR) | 106.039 |

The rates are hardcoded in `YCurrencyConverter.java`, and the code converts through a common base (its variables are named after pounds). Every conversion works as:

```
result = (amount / rate of "from" currency) × rate of "to" currency
```

**Example:** 100 USD → INR = (100 / 1.26864) × 106.039 ≈ **8358.48**

> The rates are fixed sample values, not live market data. Edit the `double` variables at the top of the class to update them.

## 🛠️ Tech Stack

- **Language:** Java
- **GUI:** Java Swing (`JFrame`, `JComboBox`, `JTextField`, `JButton`, `GroupLayout`)
- **IDE:** Apache NetBeans (GUI Form Editor)

## ✅ Prerequisites

- **JDK 8 or newer** ([download](https://adoptium.net)). Check with `java -version` and `javac -version`.

## 🚀 How to Run



## 📁 Project Structure

```
CurrencyConverter/
├── YCurrencyConverter.java   Main source: GUI and conversion logic
├── YCurrencyConverter.form   NetBeans GUI form definition
├── config.properties         NetBeans configuration
└── README.md
```

## ⚠️ Known Issues

These are in the current code and are good first improvements:

- **Reset and Exit are swapped:** the button labelled RESET closes the app, and EXIT clears the fields.
- **Andorra gives 0:** the code checks for `"Aldorra"` (a typo) instead of `"Andorra"`, so conversions to or from Andorra return `0.00`.
- **No input validation:** leaving the amount empty or typing letters causes a `NumberFormatException`.
- Choosing "Choose one..." silently converts to `0.00` instead of showing a message.

## 🔮 Possible Improvements

- Fix the issues above and show friendly error messages
- Fetch live exchange rates from an API
- Add more currencies and a swap button
- Store rates in `config.properties` instead of in code
- Add a `.gitignore` for compiled `*.class` files and generated Javadoc HTML

## 👤 Author




This project is for learning purposes. Add a license file if you want others to reuse it.
