# Puerto Vallarta Weather Widget

A clean, embeddable weather widget displaying current conditions and a 7-day forecast for Puerto Vallarta, Mexico. Designed to match the puertovallarta.net color scheme.

![Widget Preview](https://via.placeholder.com/320x600/007BFF/FFFFFF?text=Weather+Widget)

## Features

- **Current Weather**: Temperature, condition, humidity, wind speed, feels-like temperature
- **Today's High/Low**: Quick view of the day's temperature range
- **7-Day Forecast**: Daily weather outlook with icons and temperatures
- **Responsive Design**: 600px on desktop, adaptive grid on mobile (2-column layout)
- **Auto-refresh**: Weather data updates every 30 minutes

## Quick Start

### 1. Get a Free API Key

1. Visit [WeatherAPI.com](https://www.weatherapi.com/)
2. Click "Sign Up" and create a free account
3. After signing in, your API key will be displayed on the dashboard
4. Copy the API key

### 2. Configure the Widget

Open `index.html` and replace `YOUR_API_KEY` with your actual API key:

```javascript
// Line 180 in index.html
const API_KEY = 'YOUR_API_KEY'; // Replace with your key
```

### 3. Test Locally

Simply open `index.html` in your web browser to test the widget.

## Deployment to GitHub Pages

### Step-by-Step Instructions

1. **Create a GitHub Repository**
   - Go to [github.com/new](https://github.com/new)
   - Name it something like `pv-weather-widget`
   - Make it **Public** (required for free GitHub Pages)
   - Click "Create repository"

2. **Upload Files**
   - Click "uploading an existing file"
   - Drag and drop `index.html` (and optionally this README)
   - Click "Commit changes"

3. **Enable GitHub Pages**
   - Go to repository **Settings**
   - Click **Pages** in the left sidebar
   - Under "Source", select **Deploy from a branch**
   - Choose **main** branch and **/ (root)** folder
   - Click **Save**

4. **Access Your Widget**
   - Wait 1-2 minutes for deployment
   - Your widget will be available at:
   ```
   https://YOUR-USERNAME.github.io/pv-weather-widget/
   ```

## Embedding the Widget

Add this iframe code to your website:

```html
<iframe 
    src="https://YOUR-USERNAME.github.io/pv-weather-widget/"
    width="620"
    height="580"
    style="border: none; border-radius: 12px; box-shadow: 0 2px 10px rgba(0,0,0,0.1);"
    title="Puerto Vallarta Weather"
    loading="lazy">
</iframe>
```

### Embedding Options

**Desktop (fixed 600px width):**
```html
<iframe src="https://YOUR-USERNAME.github.io/pv-weather-widget/" width="620" height="580" style="border:none;"></iframe>
```

**Fully Responsive (adapts to container):**
```html
<div style="max-width: 620px; width: 100%; margin: 0 auto;">
    <iframe src="https://YOUR-USERNAME.github.io/pv-weather-widget/" width="100%" height="580" style="border:none;"></iframe>
</div>
```

**With shadow and rounded corners:**
```html
<iframe 
    src="https://YOUR-USERNAME.github.io/pv-weather-widget/"
    width="620"
    height="580"
    style="border: none; border-radius: 16px; box-shadow: 0 4px 20px rgba(0,0,0,0.15);">
</iframe>
```

**Mobile-optimized (for narrow sidebars):**
```html
<iframe src="https://YOUR-USERNAME.github.io/pv-weather-widget/" width="100%" height="1100" style="border:none; max-width: 400px;"></iframe>
```

## Color Scheme

The widget uses the puertovallarta.net brand colors:

| Color | Hex | Usage |
|-------|-----|-------|
| Blue | `#007BFF` | Headers, primary elements |
| Light Blue | `#5BC0DE` | Accents, borders, low temps |
| Orange | `#FFA500` | High temperatures, highlights, hover effects |
| Yellow | `#FFD700` | Sun decorations |
| Green | `#228B22` | Nature elements |
| White | `#FFFFFF` | Background |

## API Information

This widget uses [WeatherAPI.com](https://www.weatherapi.com/):

- **Free Tier**: 1,000,000 calls/month
- **Data**: Current weather + 3-day forecast (free) or 7-day (with upgraded plan)
- **Updates**: Real-time weather data
- **Coverage**: Worldwide

> **Note**: The free tier includes up to 3-day forecast. For the full 7-day forecast shown in the widget, you may need to upgrade to a paid plan or the forecast will show available days.

## Customization

### Change Location

Edit line 181 in `index.html`:

```javascript
const LOCATION = 'Puerto Vallarta,Mexico';
```

You can use:
- City name: `'Cancun,Mexico'`
- Coordinates: `'20.6534,-105.2253'`
- US Zip: `'10001'`

### Change Temperature Units

The widget displays Celsius by default. To switch to Fahrenheit, modify the render function to use `temp_f`, `maxtemp_f`, `mintemp_f` instead of the `_c` variants.

### Adjust Refresh Rate

Change the interval on line 264:

```javascript
// Current: 30 minutes
setInterval(fetchWeather, 30 * 60 * 1000);

// Example: 15 minutes
setInterval(fetchWeather, 15 * 60 * 1000);
```

## Troubleshooting

### "Weather data unavailable" Error

1. Check that your API key is correctly entered
2. Verify the API key is active at [weatherapi.com](https://www.weatherapi.com/)
3. Check browser console for detailed error messages

### Widget Not Loading in iframe

1. Ensure GitHub Pages is enabled and deployed
2. Check that the repository is public
3. Wait a few minutes after deployment

### CORS Issues (Local Testing)

When testing locally, some browsers may block API requests. Solutions:
- Use a local development server
- Test on GitHub Pages directly
- Use a browser extension to disable CORS (development only)

## License

This widget is free to use for personal and commercial projects. Attribution to WeatherAPI.com is required as per their terms of service.

---

**Created for [puertovallarta.net](https://puertovallarta.net)**
