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
4. You should see a map centered on Buffalo, NY.
5. Click the "Offset Marker" button.  A set of lines will be drawn and three markers will be drawn at points from the lines.  The Blue marker uses 0 for the offsets and is roughly centered on the point.  The green marker uses positive offsets and should appear off the line. It appears centered like the blue marker. The red marker uses negatove offsets and also appears to use the same offset as the blue marker

## Screenshot ##

![Markers](/screenshots/image01.png)