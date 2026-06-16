# 🌍 Tree Geo-Tagging & Digitalization Project

An open-source platform designed to map, track, and digitalize local flora using geographic coordinates and dynamic QR codes. This project empowers communities to monitor environmental biodiversity and estimate carbon sequestration.

---

## 🚀 Key Features

*   **Precise Geo-Tagging:** Capture exact GPS coordinates of individual trees.
*   **Dynamic QR Codes:** Generate unique QR tags linking directly to tree profiles.
*   **Carbon Estimation:** Automatically calculate carbon storage based on species and girth (GBH).
*   **Interactive Web Map:** Visualize tagged trees using open-source mapping layers.
*   **Data Export:** Download census data in CSV, KML, and JSON formats.

---

## 🛠️ Tech Stack

*   **Frontend:** React Native (Mobile App) / React.js (Web Dashboard)
*   **Backend:** Node.js (Express)
*   **Database:** PostgreSQL with PostGIS extension (Spatial data)
*   **Mapping:** Leaflet.js / OpenStreetMap
*   **Deployment:** Docker / AWS

---

## 📦 Installation & Setup

### Prerequisites
*   Node.js (v18 or higher)
*   PostgreSQL with PostGIS installed

### Step-by-Step Guide

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com
    cd tree-geotagging-project
    ```

2.  **Install Dependencies:**
    ```bash
    npm install
    ```

3.  **Environment Variables:**
    Create a `.env` file in the root directory and add your credentials:
    ```env
    PORT=5000
    DATABASE_URL=postgres://user:password@localhost:5432/geotag_db
    JWT_SECRET=your_secret_key
    ```

4.  **Run Database Migrations:**
    ```bash
    npm run db:migrate
    ```

5.  **Start the Local Server:**
    ```bash
    npm run dev
    ```

---

## 📊 Data Schema Reference

Every logged tree stores the following core data attributes:

| Field Name | Data Type | Description |
| :--- | :--- | :--- |
| `tree_id` | UUID | Unique identifier for the specimen |
| `species_name` | String | Botanical and common name |
| `coordinates` | Point (PostGIS) | Latitude and Longitude values |
| `girth_cm` | Float | Girth at breast height (GBH) |
| `health_status` | Enum | Healthy / Diseased / Dead |
| `qr_code_url` | String | Link to the generated QR asset |

---

## 🤝 Contributing

We welcome community contributions to expand this environmental tool.
1. Fork this repository.
2. Create your feature branch (`git checkout -b feature/NewFeature`).
3. Commit your changes (`git commit -m 'Add some NewFeature'`).
4. Push to the branch (`git push origin feature/NewFeature`).
5. Open a **Pull Request**.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
