# Flask Cafe App README

This README provides an overview of a Flask-based cafe application that allows users to add cafes, rate them, and view a list of all cafes. The application stores cafe data in a CSV file and provides a user-friendly interface using Flask-Bootstrap and Flask-WTF.

## Prerequisites

- Python 3.x
- Flask
- Flask-Bootstrap
- Flask-WTF
- WTForms

## Setup

1. **Clone the repository** (or create a new project and copy the code into it).

2. **Install the required packages**:
    ```sh
    pip install Flask Flask-Bootstrap Flask-WTF WTForms
    ```

3. **Create a CSV file** named `cafe-data.csv` in the project directory with the following headers:
    ```csv
    Cafe Name,Location,Opening Time,Closing Time,Coffee Rating,Wifi Rating,Power Rating
    ```

## Usage

### Running the Application

1. **Run the Flask application**:
    ```sh
    python your_script_name.py
    ```

2. **Open a web browser** and navigate to `http://127.0.0.1:5002/`.

### Features

#### Home Route (`/`)
- Displays the homepage.

#### Add Cafe Route (`/add`)
- A form to add a new cafe.
- Form fields include cafe name, location URL, opening time, closing time, coffee rating, wifi rating, and power rating.
- Validates the form input and appends the new cafe data to the CSV file.

#### Cafes Route (`/cafes`)
- Displays a list of all cafes stored in the CSV file.

### Forms

#### CafeForm
- **cafe**: Input field for the cafe name.
- **location**: Input field for the cafe location URL.
- **open**: Input field for the cafe opening time.
- **close**: Input field for the cafe closing time.
- **coffee_rating**: Select field for the cafe coffee rating.
- **wifi_rating**: Select field for the wifi strength rating.
- **power_rating**: Select field for the power socket availability.
- **submit**: Submit button to add the cafe.

## File Descriptions

### Main Script
- **Imports necessary libraries**: Flask, Bootstrap, WTForms, CSV.
- **Defines Flask application**.
- **Sets up the CafeForm using WTForms**.
- **Defines routes**: `/`, `/add`, `/cafes`.

### Templates
- **index.html**: Displays the homepage.
- **add.html**: Form to add a new cafe.
- **cafes.html**: Displays the list of cafes with their details.

### CSV File
- **cafe-data.csv**: Stores the cafe data with the following headers:
    ```csv
    Cafe Name,Location,Opening Time,Closing Time,Coffee Rating,Wifi Rating,Power Rating
    ```

## Conclusion

This Flask application provides a simple and interactive way to manage a list of cafes, including adding new cafes with their details and viewing a list of all cafes. By using Flask-Bootstrap and Flask-WTF, it offers a user-friendly interface for interacting with the application. Customize the templates and styles as needed to fit your requirements.
