# Hijri & Gregorian Expiry Calculator

A static, offline-friendly HTML application for calculating product expiry dates using either:

- **Saudi Hijri / Umm Al-Qura calculation**: Production Hijri date + shelf-life months - 1 day
- **Gregorian calculation**: Production Gregorian date + shelf-life months - 1 day

Developed by **subaspathak.com.np**.

## Main Features

- Gregorian to Hijri expiry calculation.
- Hijri-based expiry calculation for Saudi/Umm Al-Qura use.
- Gregorian-based expiry calculation.
- Manual production date entry in `DD/MM/YYYY` format.
- Native calendar date picker.
- CSV item list upload with automatic shelf-life loading.
- Browser-saved settings.
- Browser-saved history for the latest 100 calculations.
- Export history to CSV.
- Print current result on A4 paper.
- Print history on A4 paper.
- Print Multiple feature for up to 6 expiry conversions at once.
- Hijri to Gregorian converter.
- No external JavaScript libraries required.

## How to Use

### 1. Open the Application

Open `index.html` or `hijri-expiry-calculator.html` in Microsoft Edge or Google Chrome.

### 2. Upload Item CSV

Click **Upload CSV** and select your item list CSV.

The CSV must contain these columns:

```csv
Code,Description,Shelf life
I00000000,Item name,6

```

Accepted column names include:

- `Code`
- `Description`
- `Shelf life`

After upload, the item list is saved in the same browser using localStorage.

### 3. Choose Item

Select an item from the dropdown. The application automatically loads the shelf life in months.

### 4. Enter Production Date

You can type the date in this format:

```text
DD/MM/YYYY
```

Example:

```text
05/08/2026
```

Or select a date using the calendar field.

### 5. Choose Calculation Method

Choose one of these:

- **Saudi Hijri Standard**
- **Gregorian Standard**

For Saudi items, the recommended default is **Saudi Hijri Standard**.

### 6. Calculate

Click **Calculate** to generate:

- Production Gregorian date
- Production Hijri date
- Expiry Gregorian date
- Expiry Hijri date

The calculated result is saved to history.

## Settings

Click **Settings** to save:

- Default shelf life
- Default calculation method

Settings are saved in the same browser.

You can also click **Clear CSV Data** to remove the uploaded item list from the browser.

## History

Click **History** to view the latest 100 calculations.

Available actions:

- Load a previous calculation
- Copy a result
- Export history to CSV
- Print history
- Clear history

## Print Current Result

Click **Print** to print the current calculation on A4 paper with normal margins.

## Print Multiple

Click **Print Multiple** to print up to 6 conversions at once.

Each row has:

- Include checkbox
- Production date
- Calculation method
- Shelf life in months

Tick the rows you want to print and click **Print Selected**.

## Hijri to Gregorian Converter

Click **Hijri to Gregorian**.

Enter:

- Hijri year
- Hijri month
- Hijri day

Click **Convert** to get the matching Gregorian date.

## Offline Usage

The app can work offline after saving the HTML file because it does not use any CDN or remote API.

The Hijri conversion uses the browser's built-in Umm Al-Qura calendar support through JavaScript `Intl.DateTimeFormat`.

## Browser Storage Notice

The application saves these in browser localStorage:

- User settings
- Uploaded CSV item list
- Calculation history

Data can be removed if the user clears browser data or uses another browser/computer.





## Security Notes

- Do not store passwords or private/sensitive information in CSV or history.
- Avoid adding unknown third-party scripts.
- Use HTTPS when hosting.
- Data saved in localStorage is accessible to JavaScript on the same site origin.
