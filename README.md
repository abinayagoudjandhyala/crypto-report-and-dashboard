
# Crypto Report Generator

Welcome to the **Crypto Report Generator**! This project allows users to generate cryptocurrency reports via email, with a clean and interactive interface built using Streamlit. It fetches real-time crypto data and sends detailed reports via email with a CSV attachment. 

Additionally, the project includes a **live crypto dashboard** that visualizes this data, offering insights into the top 10 cryptocurrencies based on their 24-hour price change.  

## Features

- **Real-time Crypto Data**: Fetches the latest market data for over 250 cryptocurrencies using the CoinGecko API.
- **Report Generation**: Generates a detailed cryptocurrency report with the top 10 cryptocurrencies that have seen the highest       price increase and decrease in the last 24 hours.
- **Email Integration**: Sends the generated report via email with the option to attach the full data in CSV format.
- **User Input**: Collects the recipient's email address for sending reports.

## Technologies Used

- **Python**: The main programming language used for backend logic.
- **Streamlit**: For creating the interactive web interface.
- **pandas**: For data manipulation and report generation.
- **requests**: For fetching cryptocurrency data from the CoinGecko API.
- **smtplib**: For sending emails with reports and attachments.
- **dotenv**: To securely store and manage API keys and email credentials.
- **HTML**: For formatting the email body with a rich structure.

## Installation

### Prerequisites

To get started with the project, you need to have **Python** installed on your local machine.

1. **Clone the repository**:

   ```bash
   git clone https://github.com/abinayagoudjandhyala/crypto-report-generator.git
   cd crypto-report-generator
   ```

2. **Create a virtual environment**:

   ```bash
   python -m venv venv
   ```

3. **Activate the virtual environment**:

   - For Windows:

     ```bash
     venv\Scripts\activate
     ```

   - For macOS/Linux:

     ```bash
     source venv/bin/activate
     ```

4. **Install required dependencies**:

   Create a `.env` file in the root of your project directory and add your environment variables like so:

   ```bash
   EMAIL_USER=your-email@gmail.com
   EMAIL_PASSWORD=your-email-password
   ```

   Then install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

5. **Run the Streamlit app**:

   ```bash
   streamlit run app.py
   ```

   This will launch the Streamlit app in your default browser.

## How It Works

1. **User Input**: The user provides their email address in the Streamlit UI.
2. **Data Fetching**: The app fetches real-time cryptocurrency data from the CoinGecko API.
3. **Report Generation**: The app generates a CSV report that includes the top 10 cryptocurrencies with the highest price change (both positive and negative) in the last 24 hours.
4. **Sending Email**: The user can click the "Send Report" button, which triggers the sending of the report via email (with CSV attachment) to the provided email address.

## Features Overview

1. **Top 10 Cryptos with Highest Price Increase**: Displays the top 10 cryptocurrencies that have seen the highest increase in their price in the last 24 hours.
2. **Top 10 Cryptos with Highest Price Decrease**: Displays the top 10 cryptocurrencies that have seen the largest decrease in their price in the last 24 hours.
3. **Crypto Dashboard**: A **live crypto dashboard** provides a real-time view of cryptocurrency market data. [Check it out here](https://crypto-live-dashboard.streamlit.app/).

## File Structure

```plaintext
crypto-report-generator/
│
├── crypto_report.py        # Main Streamlit app to run the UI
├── .env                    # Environment variables for storing email credentials securely
├── requirements.txt        # Python dependencies
├── LICENSE                 # Project license file
├── README.md               # This readme file
```

## License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

## Contributing

1. Fork the repository
2. Clone your fork locally
3. Create a new branch (`git checkout -b feature-branch`)
4. Make your changes and commit them (`git commit -am 'Add feature'`)
5. Push your changes to your fork (`git push origin feature-branch`)
6. Create a new Pull Request

## Acknowledgments

- **CoinGecko API**: For providing free access to cryptocurrency data.
- **Streamlit**: For providing a simple and powerful tool for building interactive web apps.
- **Python libraries**: pandas, requests, smtplib, and others that helped build this project.

