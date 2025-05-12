# Temperature Converter Web App

This is a simple and interactive **Temperature Converter** web application that allows users to convert between three temperature units: **Fahrenheit**, **Celsius**, and **Kelvin**. It provides real-time conversions as you input a value in any of the fields, and the other fields will automatically update.

## Features

- Convert between **Fahrenheit**, **Celsius**, and **Kelvin**.
- Real-time conversion updates with each input.
- Modern, clean UI with responsive design.

## Technologies Used

- **HTML5**: For structuring the content of the web page.
- **CSS3**: For styling the web page with a modern, attractive design.
- **JavaScript**: For handling the temperature conversion logic and interactivity.

## How to Use

1. Enter a temperature value in any of the fields: Fahrenheit, Celsius, or Kelvin.
2. The other two fields will automatically update with the converted values.
3. Enjoy easy and fast temperature conversion!

## Getting Started

To run this project locally:

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/yourusername/temperature-converter.git
   ```

2. Navigate to the project folder:

   ```bash
   cd temperature-converter
   ```

3. Open the `index.html` file in your web browser to view the application:

   ```bash
   open index.html
   ```

## Preview

Here’s a screenshot of how the web app looks:

![Temperature Converter Screenshot](Screenshot 2025-05-12 000654.png)

## Contributions
Feel free to fork the repository and submit pull requests. Contributions are welcome to improve the app or add additional features.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


## full temprature coneverter web code 
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">

    <style>
        * {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            box-sizing: border-box;
        }

        body {
            background-color: #f0f4f8;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            padding: 20px;
        }

        .container {
            width: 100%;
            max-width: 800px;
            background: #ffffff;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            border-radius: 15px;
            padding: 40px 30px;
            text-align: center;
        }

        h1 {
            color: #333;
            font-weight: 700;
            font-size: 30px;
            margin-bottom: 30px;
        }

        .converter-row {
            display: flex;
            justify-content: space-between;
            gap: 20px;
        }

        .col {
            flex-basis: 30%;
            text-align: center;
        }

        .col label {
            font-size: 16px;
            font-weight: 500;
            margin-bottom: 10px;
            color: #555;
        }

        .col input {
            width: 100%;
            height: 40px;
            background-color: #f3f6f9;
            border: 2px solid #ddd;
            border-radius: 10px;
            padding: 0 10px;
            text-align: center;
            font-size: 16px;
            transition: border-color 0.3s ease-in-out;
        }

        .col input:focus {
            border-color: #4CAF50;
            outline: none;
        }

        .converter-row {
            background: linear-gradient(to right, #6a9cfa, #3f79ff);
            border-radius: 15px;
            padding: 30px 20px;
        }
    </style>
</head>

<body>
    <div class="container">
        <h1><b>Dawit</b><br>Temperature Converter</h1>
        <div class="converter-row">
            <div class="col">
                <label>Fahrenheit</label>
                <input type="number" id="fahrenheit">
            </div>

            <div class="col">
                <label>Celsius</label>
                <input type="number" id="celsius">
            </div>

            <div class="col">
                <label>Kelvin</label>
                <input type="number" id="kelvin">
            </div>
        </div>
    </div>

    <script>
        let celsius = document.getElementById('celsius');
        let fahrenheit = document.getElementById('fahrenheit');
        let kelvin = document.getElementById('kelvin');

        celsius.oninput = function () {
            let f = (parseFloat(celsius.value) * 9) / 5 + 32;
            fahrenheit.value = parseFloat(f.toFixed(2));

            let k = (parseFloat(celsius.value) + 273.15);
            kelvin.value = parseFloat(k.toFixed(2));
        }

        fahrenheit.oninput = function () {
            let c = ((parseFloat(fahrenheit.value) - 32) * 5) / 9;
            celsius.value = parseFloat(c.toFixed(2));

            let k = (parseFloat(fahrenheit.value) - 32) * 5 / 9 + 273.15;
            kelvin.value = parseFloat(k.toFixed(2));
        }

        kelvin.oninput = function () {
            let f = (parseFloat(kelvin.value) - 273.15) * 9 / 5 + 32;
            fahrenheit.value = parseFloat(f.toFixed(2));

            let c = (parseFloat(kelvin.value) - 273.15);
            celsius.value = parseFloat(c.toFixed(2));
        }
    </script>
</body>

</html>

