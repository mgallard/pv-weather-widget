# Puerto Vallarta Weather Widget

A clean, responsive Puerto Vallarta weather widget with real-time data, 8-day forecast, and automated daily updates via GitHub Actions.

## Live Demos

- **English Version:** [mgallard.github.io/pv-weather-widget/index.html](https://mgallard.github.io/pv-weather-widget/index.html) (Default: °F)
- **Spanish Version:** [mgallard.github.io/pv-weather-widget/index-es.html](https://mgallard.github.io/pv-weather-widget/index-es.html) (Default: °C)

## Embedding the Widget

You can embed the widget on your website using an `iframe`. Choose the version that matches your site's language.

### Spanish Version (Metric Default)
```html
<iframe src="https://mgallard.github.io/pv-weather-widget/index-es.html" width="620" height="580" frameborder="0" style="border:none; overflow:hidden;" scrolling="no"></iframe>
```

### English Version (Imperial Default)
```html
<iframe src="https://mgallard.github.io/pv-weather-widget/index.html" width="620" height="580" frameborder="0" style="border:none; overflow:hidden;" scrolling="no"></iframe>
```

## Features
- **Real-Time Data:** Updates 6 times daily via GitHub Actions.
- **Dual Language:** Full English and Spanish versions.
- **Dynamic Units:** Switch between °C and °F instantly.
- **8-Day Forecast:** Balanced 4x2 grid on desktop, 2x4 on mobile.
- **Modern UI:** Oswald and Poppins fonts with clean SVG icons.
- **Secure:** API key is hidden in GitHub Secrets.

## Setup Instructions (for Repository Owners)
1. **GitHub Secrets:** Add your `WEATHER_API_KEY` to repository settings (Secrets and variables > Actions).
2. **First Run:** Trigger the "Update Weather Data" workflow manually under the Actions tab to generate `weather.json`.
3. **Automated Updates:** The widget will auto-update every 4 hours starting from 2:00 AM PVR time.

## Color Scheme
- **Primary Blue:** `#007BFF` (Waves/Background)
- **Light Blue:** `#5BC0DE` (Accents)
- **Orange:** `#FFA500` (Seahorse/Highlights)
- **Yellow:** `#FFD700` (Sun)
- **Green:** `#228B22` (Palm Tree)
- **White:** `#FFFFFF` (Background)

## Technical Details
- **Technologies:** HTML5, CSS3, Vanilla JavaScript.
- **Icons:** [Lucide Icons](https://lucide.dev/) for UI, WeatherAPI for conditions.
- **Fonts:** [Oswald](https://fonts.google.com/specimen/Oswald) & [Poppins](https://fonts.google.com/specimen/Poppins).
- **Automation:** GitHub Actions with `cron` schedule.
