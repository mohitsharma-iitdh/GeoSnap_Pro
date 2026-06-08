# GeoSnap Project

## What is Remote Sensing?

Remote sensing is collecting information about earth without physically touching it. Satellites,drones,and aircraft collect data from a distance.

## What is Sentinel-2?

Sentinel-2 is a satellite mission developed by ESA(European space agency) that captures Earth images using 13 spectral bands.

## What are spectral bands?

A spectral band is a specific range of light wavelenghts captured by a sensor.

Important bands:
    
    - B2 = Blue
    - B3 = Green
    - B4 = Red
    - B8 = Near Infrared(NIR)
    - B11 = SWIR1
    - B12 = SWIR2

## What is Land Use Classification?

Land use classification is the process of identifying whether an area is forest,water,agriculture,urban area,grassland etc.

## What is NDVI(Normalized Difference Vegetation Index)?

NDVI is used to measure vegetation health.

        NDVI = (NIR - Red)/(NIR + Red)

        where,
        NIR = Near-infrared light refected by vegetation
        Red = Red light reflected by vegetation

    - NDVI ~ 0.8 (Dense healthy forest)
    - NDVI ~ 0.1 (Bare land or urban area)
    - NDVI < 0 (Water body)
    

## What is NDWI(Normalized Difference Water Index)?

NDWI is used to detect water bodies.

    NDWI = (Green - NIR)/(Green + NIR)

    where,
    Green = Green band reflectance
    NIR = Near-infrared band reflectance

- NDWI > 0 (Water bodies likely present)
- NDWI = 0 (Mixed land/water)
- NDWI < 0 (Vegetation,soil,or build-up area)

## Applications:

    - Agriculture monitoring
    - Forest monitoring
    - Urban planning
    - Water analysis
    - Disaster management

## My Understanding 
### Q1. 
why can sentinel-2 detect forests better than a phone camera?

Answer:

A phone camera cannot detect NIR radiation because it only captures visible light (RGB). Sentinel-2 can detect NIR and other spectral bands. Healthy vegetation reflects a lot of NIR radiation , so sentinal-2 can identify forests and crops better than a normal phone camera.

### Q2.
Why is NIR important for vegetation detection?

Answer:

Healthy plants reflects a large amount of NIR radiation . By measuring NIR reflection,satellites can identify healthy vegetation and distinguish it from building,roads,and dry land.

// Forest -> Reflect High NIR (High NIR)
// Water  -> Absorbs NIR (Low NIR)

### Q3.
What is the main objective of the GeoSnap project?

Answer:

The main objective of the GeoSnap project is to use Sentinel-2 satellite imagery and Machine Learning techniques to classify difference land-use categories such as forests,water bodies,agriculture land,urban areas, and bare land. The project aims to generate accurate land-use maps and provide explainable insights into how the AI model makes its predictions.

## How AI Sees Satellites Images?

Humans see forests,water,and,cities.

AI sees numerical values from spectral bands such as Blue,Green,Red,and NIR.

These band values become features for machine learning models.

Each pixel or image region is associated with a land-use lable such as forest,Water,Urban, or agriculture.

## Big Picture Pipeline

    1. Sentinel-2 Image (Satellite captures Earth)
    2. Extract Bands (Get Blue,Green,Red,NIR values)
    3. Create Features (Calculate NDVI,NDWI,etc)
    4. Machine Learning Model (Train Random Forest/XGBoost)
    5. Predict Land Type (Forest,water,Urban,Agriculture)
    6. Land Use Map (Final coloured map output)


    
    