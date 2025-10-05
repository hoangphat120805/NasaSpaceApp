# 🌸 Florascope - NASA Space Apps Challenge Project

**Florascope** is an interactive web application for tracking and visualizing flower blooming patterns across Vietnam using satellite data and crowdsourced observations. This project was developed for the NASA Space Apps Challenge to help researchers, botanists, and nature enthusiasts monitor plant phenology and biodiversity.

## 🌟 Features

### 🗺️ Interactive Mapping

-   **Real-time bloom visualization** with OpenLayers mapping interface
-   **Species-specific markers** with unique colors for each flower type
-   **Geospatial search** to find blooming locations near you
-   **Custom location creation** for crowdsourced data collection

### 🌺 Species Management

-   Comprehensive **flower species database** with scientific names
-   **Bloom calendar** showing seasonal patterns
-   **Species characteristics** including habitat, color, and bloom time
-   **Image galleries** for species identification

### 👥 Community Features

-   **User reviews and ratings** for bloom locations
-   **Photo uploads** to document bloom observations
-   **Collaborative data collection** from citizen scientists

### 📊 Data Analysis

-   **NDVI satellite data integration** for vegetation monitoring
-   **Predictive bloom forecasting** using machine learning
-   **Regional bloom reports** with data visualization
-   **Export capabilities** for research purposes

## Preview

### 🗺️ Main Map Interface

![Main View](img/firstview.png)

![Chart View](img/chartview.png)

![Watch View](img/watchview.png)

## 🛠️ Tech Stack

### Backend

-   **FastAPI** - High-performance Python web framework
-   **PostgreSQL** - Robust database with JSONB support
-   **SQLAlchemy** - Modern Python SQL toolkit and ORM
-   **Alembic** - Database migration management
-   **Docker** - Containerized deployment

### Frontend

-   **Next.js 15** - React framework with Turbopack
-   **TypeScript** - Type-safe JavaScript development
-   **OpenLayers** - Advanced web mapping library
-   **Tailwind CSS** - Utility-first CSS framework
-   **Leaflet** - Mobile-friendly interactive maps

## 🚀 Quick Start

### Prerequisites

-   Node.js 18+
-   Python 3.12+
-   PostgreSQL 13+
-   Docker (optional)

### Backend Setup

1. **Clone the repository**

    ```bash
    git clone https://github.com/hoangphat120805/NasaSpaceApp.git
    cd NasaSpaceApp/backend
    ```

2. **Create virtual environment**

    ```bash
    python -m venv .venv
    .venv\Scripts\activate  # Windows
    # source .venv/bin/activate  # Linux/Mac
    ```

3. **Install dependencies**

    ```bash
    pip install -r requirements.txt
    ```

4. **Configure environment**

    ```bash
    # Create .env file with your database settings
    DATABASE_URL=postgresql://username:password@localhost:5432/florascope
    ```

5. **Run database migrations**

    ```bash
    alembic upgrade head
    ```

6. **Start the API server**
    ```bash
    python main.py
    ```

### Frontend Setup

1. **Navigate to frontend directory**

    ```bash
    cd ../frontend
    ```

2. **Install dependencies**

    ```bash
    npm install
    ```

3. **Start development server**

    ```bash
    npm run dev
    ```

4. **Open your browser**
    ```
    http://localhost:3000
    ```

### Docker Deployment

```bash
# From the backend directory
docker-compose up -d
```

## 📁 Project Structure

```
NasaSpaceApp/
├── backend/                 # FastAPI backend application
│   ├── app/
│   │   ├── api/            # API route handlers
│   │   ├── core/           # Configuration and security
│   │   ├── db/             # Database connection and dependencies
│   │   ├── models/         # SQLAlchemy database models
│   │   └── schemas/        # Pydantic data validation schemas
│   ├── alembic/            # Database migrations
│   ├── uploads/            # User uploaded images
│   └── requirements.txt    # Python dependencies
├── frontend/               # Next.js frontend application
│   ├── src/
│   │   ├── app/           # Next.js app router pages
│   │   ├── components/    # Reusable React components
│   │   ├── services/      # API service layer
│   │   ├── types/         # TypeScript type definitions
│   │   └── utils/         # Utility functions
│   └── public/            # Static assets and sample data
└── README.md
```

## 🔧 API Endpoints

### Species Management

-   `GET /api/v1/species` - List all flower species
-   `POST /api/v1/species` - Create new species
-   `GET /api/v1/species/{id}` - Get species details

### Location Management

-   `GET /api/v1/locations` - List bloom locations
-   `POST /api/v1/locations` - Add new bloom location
-   `GET /api/v1/locations/species/{id}` - Get locations by species

### User Reviews

-   `GET /api/v1/reviews` - List reviews
-   `POST /api/v1/reviews` - Submit new review
-   `POST /api/v1/reviews/upload` - Upload review photos

## 🌍 Contributing

We welcome contributions from the community! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`)
3. **Commit your changes** (`git commit -m 'Add amazing feature'`)
4. **Push to the branch** (`git push origin feature/amazing-feature`)
5. **Open a Pull Request**

## 📊 Data Sources

-   **Satellite Data**: NASA MODIS vegetation indices (NDVI/EVI)
-   **Climate Data**: Weather station observations and forecasts
-   **Species Database**: Botanical taxonomies and phenology records
-   **Crowdsourced**: Community observations and photos

## 🎯 NASA Space Apps Challenge

This project addresses the **"Leverage Earth Observation Data for Inform Decision Making"** challenge by:

-   Using satellite data to monitor vegetation health and blooming patterns
-   Providing decision support tools for conservation efforts
-   Enabling citizen science participation in biodiversity monitoring
-   Supporting climate change research through phenology tracking

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

-   **NASA** for providing satellite data and hosting the Space Apps Challenge
-   **OpenLayers** and **Leaflet** communities for excellent mapping libraries
-   **FastAPI** and **Next.js** teams for robust development frameworks
-   All **contributors** and **citizen scientists** supporting biodiversity research

## 📞 Contact

-   **GitHub**: [@hoangphat120805](https://github.com/hoangphat120805)
-   **Project Repository**: [NasaSpaceApp](https://github.com/hoangphat120805/NasaSpaceApp)

---

**Built with ❤️ for the NASA Space Apps Challenge 2025**
