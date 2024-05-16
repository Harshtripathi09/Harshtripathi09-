# Harshtripathi09-// map.js

// Initialize the map and set its view to the specified geographical coordinates and a zoom level
var map = L.map('map').setView([51.505, -0.09], 13);

// Add a tile layer to the map (the actual map images)
L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
}).addTo(map);

// Define the corners of the rectangle (house) in LatLng format
var bounds = [
    [51.505, -0.09], // Top left corner
    [51.505, -0.07], // Top right corner
    [51.503, -0.07], // Bottom right corner
    [51.503, -0.09]  // Bottom left corner
];

// Create a polygon (rectangle) and add it to the map
var house = L.polygon(bounds, {color: 'red'}).addTo(map);

// Add a popup to the rectangle
house.bindPopup("21x47 House");

