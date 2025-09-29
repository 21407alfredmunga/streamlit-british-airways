# ✈️ British Airways Customer Feedback Dashboard

A comprehensive Streamlit web application for analyzing British Airways customer reviews and sentiment patterns. This interactive dashboard provides insights into customer feedback collected from Skytrax, featuring sentiment analysis, filtering capabilities, and data visualizations.

## 🚀 Features

- **Sentiment Analysis**: Automated sentiment scoring using NLTK's VADER analyzer
- **Interactive Filtering**: Filter reviews by verification status, sentiment, and word count
- **Real-time Metrics**: Display key metrics including review counts, average sentiment, and positive share
- **Data Visualizations**: 
  - Sentiment distribution pie charts
  - Verification status breakdown with stacked bar charts
- **Review Explorer**: Browse and examine individual reviews with detailed metadata
- **Responsive Design**: Clean, user-friendly interface with sidebar controls

## 📊 Dashboard Components

### Key Metrics
- Total number of reviews displayed
- Average sentiment compound score
- Percentage of positive reviews

### Visualizations
- **Sentiment Distribution**: Pie chart showing positive, neutral, and negative review proportions
- **Verification Breakdown**: Stacked bar chart comparing sentiment across verified vs non-verified reviews
- **Sample Reviews**: Display of longest and shortest reviews in the filtered dataset

### Interactive Filters
- **Verification Status**: Filter by "Trip Verified" vs "Not Verified" reviews
- **Sentiment Categories**: Select positive, neutral, and/or negative reviews
- **Word Count Range**: Adjust minimum and maximum word counts via slider

## 🛠️ Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Setup Instructions

1. **Clone the repository**:
   ```bash
   git clone https://github.com/21407alfredmunga/streamlit-british-airways.git
   cd streamlit-british-airways
   ```

2. **Create a virtual environment** (recommended):
   ```bash
   python -m venv datascience_env
   source datascience_env/bin/activate  # On Windows: datascience_env\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**:
   ```bash
   streamlit run app.py
   ```

5. **Open your browser** and navigate to `http://localhost:8501`

## 📁 Project Structure

```
streamlit-british-airways/
├── app.py                          # Main Streamlit application
├── requirements.txt                # Python dependencies
├── create_datascience_env.sh       # Environment setup script
├── data/                           # Dataset directory
│   ├── BA_reviews_cleaned.csv      # Cleaned review dataset
│   ├── BA_reviews.csv              # Raw review dataset
│   └── [other data files...]       # Additional datasets
├── notebooks/                      # Jupyter notebooks
│   ├── british_airways.ipynb       # Data exploration notebook
│   └── British_airways_model.ipynb # Modeling notebook
└── datascience_env/                # Virtual environment (if created locally)
```

## 📊 Data Source

The application uses British Airways customer review data scraped from Skytrax. The dataset includes:
- Customer review text
- Verification status (Trip Verified vs Not Verified)
- Review metadata and ratings

## 🔧 Technical Implementation

### Core Technologies
- **Streamlit**: Web application framework
- **Pandas**: Data manipulation and analysis
- **NLTK**: Natural language processing and sentiment analysis
- **Plotly**: Interactive data visualizations
- **Python**: Core programming language

### Sentiment Analysis
- Uses NLTK's VADER (Valence Aware Dictionary and sEntiment Reasoner) analyzer
- Generates compound sentiment scores ranging from -1 (most negative) to +1 (most positive)
- Categorizes reviews into Positive (>0.05), Neutral (-0.05 to 0.05), and Negative (<-0.05)

### Performance Optimizations
- `@st.cache_resource` for loading the sentiment analyzer
- `@st.cache_data` for loading and processing review data
- Efficient data filtering and aggregation

## 📈 Usage Examples

### Basic Analysis
1. Launch the dashboard
2. Use sidebar filters to focus on specific review types
3. Examine key metrics and visualizations
4. Explore individual reviews in the expandable section

### Advanced Filtering
- **Verified Reviews Only**: Select only "Trip Verified" in verification filter
- **Negative Feedback Analysis**: Filter to show only "Negative" sentiment
- **Detailed Reviews**: Adjust word count slider to focus on longer, more detailed reviews

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Development Setup
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
5. Push to the branch (`git push origin feature/AmazingFeature`)
6. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 📧 Contact

- **Author**: Alfred Munga
- **GitHub**: [@21407alfredmunga](https://github.com/21407alfredmunga)
- **Repository**: [streamlit-british-airways](https://github.com/21407alfredmunga/streamlit-british-airways)

## 🎯 Future Enhancements

- [ ] Add time-series analysis for review trends
- [ ] Implement topic modeling for review themes
- [ ] Add export functionality for filtered datasets
- [ ] Include rating analysis alongside text sentiment
- [ ] Add comparison with other airlines
- [ ] Implement user authentication and personalized dashboards

---

*Built with ❤️ using Streamlit and Python*