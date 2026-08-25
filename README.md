# Ground Truth Validation

A data collection and monitoring system for crop mapping surveys using Kobo Toolbox. This project enables field data collection for ground truth validation of agricultural land use and crop types across multiple regions in Nepal and Mexico.

## Features

- **Real-time data retrieval** from Kobo Toolbox API
- **Interactive map visualizations** of survey points and field polygons
- **Regional analysis** of crop samples by enumerators and geographic areas
- **Multi-region monitoring** for Nepal and Mexico projects
- **Secure credential management** using environment variables

## Project Structure

- **Crop Mapping data collection - Monitoring notebook Saral.ipynb** - Nepal crop mapping survey monitoring and visualization
- **ground_truth_validation_Mexico.ipynb** - Mexico crop mapping survey monitoring and visualization
- **.env** - Configuration file for Kobo credentials (not tracked in git)

## Setup

1. Create a `.env` file in the project root with your Kobo credentials:
   ```
   # Nepal Kobo Project
   KOBO_USERNAME=your_username
   KOBO_PASSWORD=your_password
   KOBO_DATA_URL=your_kobo_api_url
   
   # Mexico Kobo Project
   KOBO_USERNAME_MEXICO=your_mexico_username
   KOBO_PASSWORD_MEXICO=your_mexico_password
   KOBO_DATA_URL_MEXICO=your_mexico_kobo_api_url
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   # or with uv
   uv sync
   ```

3. Open the Jupyter notebooks to run surveys and visualizations:
   - For Nepal data: Open `Crop Mapping data collection - Monitoring notebook Saral.ipynb`
   - For Mexico data: Open `ground_truth_validation_Mexico.ipynb`

## Data Collection

The notebooks enable:
- Retrieving survey data from Kobo Toolbox servers
- Parsing GPS points and polygon geometries from ODK format
- Analyzing crop types by region and enumerator
- Visualizing survey locations on interactive Folium maps

### Data Types Collected

#### Point Data
GPS coordinates collected 7 meters inside each surveyed plot. Used for:
- Quick location reference of sampled fields
- Quality assurance of survey coverage
- Mapping of sample distribution across regions
- Ground truthing against satellite imagery

#### Polygon Data
Field boundary geometries digitized by tapping corners of each plot on mobile devices. Used for:
- Precise field boundary mapping
- Calculating plot area
- Analyzing fragmentation and plot sizes by region
- Detailed spatial validation against remote sensing data
- Land use and land cover classification verification

## Sample Visualizations

### Nepal Survey Data

**Point Data - Nepal**
![Nepal Point Data](images/point_data_np.png)

**Polygon Data - Nepal**
![Nepal Polygon Data 1](images/polygon_data_nepal_1.png)
![Nepal Polygon Data 2](images/polygon_data_nepal_2.png)

### Mexico Survey Data

**Point Data - Mexico**
![Mexico Point Data](images/Mexico%20Point%20data.png)

**Polygon Data - Mexico**
![Mexico Polygon Data](images/Mexico%20Polygon%20data.png)

## Contributors

- Krishna Kafle
- Saral Karki
