# belly-button-challenge

This project is part of the Module 14 Assignment, which involves building an interactive web dashboard to visualize the Belly Button Biodiversity dataset. The dashboard features demographic information, a horizontal bar chart showing the top 10 bacterial species (OTUs) found in a sample, and a bubble chart displaying the relative frequency of all bacterial species in the sample. 

## Features

- **Metadata Panel**: Displays demographic information for each sample.
- **Bar Chart**: Shows the top 10 OTUs found in a sample, displayed horizontally.
- **Bubble Chart**: Visualizes all OTUs found in a sample, where the size and color of each marker correspond to the OTU frequency.
- **Dynamic Dropdown**: Allows users to select different samples, updating the metadata panel and both charts in real time.

## Data Source

The data used for this project is the Belly Button Biodiversity dataset, sourced from the following URL:
[https://static.bc-edx.com/data/dl-1-2/m14/lms/starter/samples.json](https://static.bc-edx.com/data/dl-1-2/m14/lms/starter/samples.json)

The dataset contains:
- `samples`: Information about the bacterial species present in each sample.
- `metadata`: Demographic information for each sample.

## Getting Started

### Prerequisites

To run this project locally, you will need the following:

- A web browser (Google Chrome, Firefox, etc.)
- A code editor (VS Code, Sublime Text, etc.)
- Internet access (to load the external data source and libraries)

### Technologies Used

- **D3.js**: For data retrieval and manipulation.
- **Plotly.js**: For creating interactive charts (bar chart and bubble chart).
- **Bootstrap**: For basic styling and layout.
- **GitHub Pages**: For hosting the project.

### Files

- `index.html`: The main HTML file that sets up the structure of the dashboard.
- `app.js`: JavaScript file containing the logic for fetching the data, building the charts, and handling user interaction.
- `samples.json`: Contains the dataset (referenced externally).
- `README.md`: This file, explaining the project's structure and instructions.

## Functionality Overview

### Metadata Panel
The metadata panel displays key demographic information such as ethnicity, gender, age, and location of the selected test subject. The buildMetadata(sample) function retrieves this information and updates the panel dynamically as new samples are selected.

<img width="230" alt="Demographic_Info" src="https://github.com/user-attachments/assets/a8c19eef-e51c-4bce-aff5-7f99cd41ed61">


### Bar Chart
The bar chart shows the top 10 bacterial species (OTUs) found in the selected sample. The buildCharts(sample) function retrieves the data and uses Plotly.js to generate the bar chart, displaying the OTU IDs as labels and their corresponding sample values as bar heights.

### Bubble Chart
The bubble chart visualizes all bacterial species in the selected sample. Each marker’s size represents the OTU’s abundance in the sample, and the color represents the OTU ID. The buildCharts(sample) function also creates this chart using Plotly.js.

