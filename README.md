# Cart Check

A Java command-line tool that tracks my clothing purchases and shows where my money actually goes.

## The Problem

I shop for clothes across a lot of different stores, both online and in person, and I never have a clear picture of how much I'm actually spending or where it's going. Each store's orders sit in its own app or email thread, so by the end of the month I just have a vague sense that I overspent. I built Cart Check to bring all my clothing purchases into one place so I can set a realistic budget and see where my money really goes.

## How It Works

Version 1.0 lets me:

- Add a purchase from the terminal (date, store, item, category, price)
- Save purchases to a CSV file and load them back when the program starts
- See spending totals by store, category, and month
- Set a monthly budget and get a warning when I'm close to or over it
- Enter data safely, since bad prices or dates are caught instead of crashing the program

![System diagram](docs/diagram.png)

The full feature breakdown is in the [Eisenhower Matrix](docs/eisenhower-matrix.pdf).

## Tech Stack

- Language: Java
- Libraries: Apache Commons CSV, java.time, java.text.NumberFormat
- Build tool: Gradle
- Testing: JUnit
- Data storage: `data/purchases.csv` for purchases, `data/budget.properties` for the monthly budget
- External data sources: none, since all purchases are entered manually

## Setup

You need Java 17 or newer installed. Gradle is included through the Gradle wrapper.

```bash
git clone https://github.com/srihitanuthalapati/cart-check
cd cart-check
./gradlew build
```

## Usage

```bash
./gradlew run
```

## Roadmap

Planned for V2.0 and beyond (from the "Schedule" quadrant):

- [ ] Edit or delete a purchase
- [ ] Import purchases in bulk from a store or bank CSV export
- [ ] Text-based bar charts of spending by category
- [ ] Month-over-month spending comparison
- [ ] Cost-per-wear tracking

## Project Structure

```
cart-check/
├── src/main/java/      # Program code
├── src/test/java/      # JUnit tests
├── data/               # purchases.csv and budget.properties
├── docs/               # Eisenhower Matrix, system diagram
├── build.gradle
└── README.md
```

## Author

Srihita Nuthalapati, [GitHub](https://github.com/srihitanuthalapati)
