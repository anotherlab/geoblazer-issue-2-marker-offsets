This demo has been updated to include a new problem when parameters are pass as part of the route

# GeoBlazor-issue-3
If a GeoBlazor map is on a page that uses routing to pass in a parameter, the map is not initialized correctly.  Invoking a map before using route parameters will allow the map to display correctly

## What is happening ##
When a page is invoked with parameter passed in as part of the route, no map details are displayed.

## What should happen ##
The map should be displayed.

## Steps to replicate the problems ##
1. Restore the nuget packages
2. Edit [MauiProgram.cs](https://github.com/anotherlab/GeoBlazor-issue-1/blob/main/demo1/MauiProgram.cs#L22) and replace "INSERT-YOUR-ESRI-API-KEY-HERE" with your API key
3. Build and the run app on the platform of your choice
4. Click on the link labelled "Route param". This must be the first page invoked.

# GeoBlazor-issue-2

This demo app illustrates a problem with setting the xOffset or yOffset properties for a PictureMarkerSymbol while using GeoBlazor with a .NET MAUI app

## What is happening ##
Markers will offsets are being placed on the map without the offsets being used

## What should happen ##
Markers should be placed with their positions offset in pixels by the xOffset and yOffset values.

## Steps to replicate the problems ##
1. Restore the nuget packages
2. Edit [MauiProgram.cs](https://github.com/anotherlab/GeoBlazor-issue-1/blob/main/demo1/MauiProgram.cs#L22) and replace "INSERT-YOUR-ESRI-API-KEY-HERE" with your API key
3. Build and the run app on the platform of your choice
4. Click on the "Map Demo" link
5. You should see a map centered on Buffalo, NY.
6. Click the "Offset Marker" button.  A set of lines will be drawn and three markers will be drawn at points from the lines.  The Blue marker uses 0 for the offsets and is roughly centered on the point.  The green marker uses positive offsets and should appear off the line. It appears centered like the blue marker. The red marker uses negatove offsets and also appears to use the same offset as the blue marker

## Screenshot ##

![Markers](/screenshots/image01.png)