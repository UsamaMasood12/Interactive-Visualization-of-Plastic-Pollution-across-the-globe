# Interactive Visualization of Plastic Pollution Across the Globe

[![D3.js](https://img.shields.io/badge/D3.js-v7-orange)](https://d3js.org/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-4.5.2-purple)](https://getbootstrap.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow)](https://www.javascript.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **MSc Data Science Project** | Teesside University  
> A collaborative team project featuring four interactive D3.js visualizations showcasing global plastic pollution data from 1950-2019

## 🎯 Project Overview

This project presents a comprehensive **interactive web-based visualization** of global plastic pollution using **D3.js**. The project consists of four distinct, interactive charts that tell the story of plastic waste across different dimensions: temporal trends, geographic distribution, waste management methods, and per-capita emissions.

### Live Demo
🌐 **[View Live Project](https://usamamasood12.github.io/Interactive-Visualization-of-Plastic-Pollution-across-the-globe/)**

---

## 👥 Team Members & Contributions

| Team Member | Visualization | Description |
|-------------|---------------|-------------|
| **Karan Gunti** | Line Chart | Global plastic waste production (1950-2019) |
| **Usama Masood** | Choropleth Map | Share of plastic waste emitted to ocean by country (2019) |
| **Kiranmai Kodali** | Stacked Bar Chart | Annual waste management methods (2000-2019) |
| **Rishika Buram** | Bubble Chart | Mismanaged plastic waste per capita by country |

---

## 📊 Visualizations Overview

### 1. Line Chart - Global Plastic Waste Trend (Karan Gunti)
**File:** `student1.html`

**Description:**  
An interactive line chart displaying the progression of global plastic waste production from 1950 to 2019 in million tons.

**Key Features:**
- 📈 Smooth time-series visualization using `curveMonotoneX`
- 🔍 **Zoom and Pan functionality** for detailed exploration
- 💡 **Interactive tooltips** showing year and exact values
- 🎯 **Annotation for 2008** highlighting significant decrease due to Great Recession
- 📊 Grid lines for improved readability
- ⚡ Hover effects with focus indicator

**Insights:**
- Exponential growth in plastic waste from 1950s onwards
- Notable dip in 2008 correlating with global economic recession
- Dramatic increase in production post-2010

**Technologies:**
```javascript
- d3.scaleTime() for temporal x-axis
- d3.scaleLinear() for y-axis
- d3.zoom() for interactive exploration
- d3.curveMonotoneX for smooth curves
```

---

### 2. Choropleth Map - Ocean Plastic Emissions (Usama Masood)
**File:** `student2.html`

**Description:**  
An interactive world map showing the share of global plastic waste emitted to the ocean per capita (kg) for the year 2019.

**Key Features:**
- 🗺️ **Mercator projection** for accurate geographic representation
- 🎨 **Color-coded scale** using d3.schemeBlues (8 color ranges)
- 🌍 **Continent filtering** buttons (Africa, Asia, Europe, etc.)
- 📊 **Value category filtering** (High, Medium, Low)
- 💬 **Hover tooltips** displaying country name and exact values
- ✨ **Interactive highlighting** on mouseover
- 🔄 **Multiple filter combinations** for detailed analysis

**Filtering Options:**
```javascript
Value Categories:
- High: ≥ 1 kg per capita
- Medium: 0.1 - 1 kg per capita  
- Low: < 0.1 kg per capita
```

**Insights:**
- Island nations and coastal countries show higher per-capita emissions
- Significant regional variations in ocean plastic pollution
- Developed nations show varied patterns based on waste management

**Technologies:**
```javascript
- d3.geoMercator() for map projection
- d3.geoPath() for rendering geographic features
- d3.scaleThreshold() for color categorization
- GeoJSON for world country boundaries
```

---

### 3. Stacked Bar Chart - Waste Management Methods (Kiranmai Kodali)
**File:** `student3.html`

**Description:**  
An interactive stacked bar chart showing the annual distribution of different waste management methods across continents from 2000 to 2019.

**Key Features:**
- 📊 **Four waste management categories:**
  - ♻️ Share of waste recycled (Blue)
  - 🔥 Share of waste incinerated (Orange)
  - 🗑️ Share of littered and mismanaged (Green)
  - 🏚️ Share of waste landfilled (Red)
- 🖱️ **Click-through functionality** to view continent-specific details
- 📅 **Temporal drill-down** showing year-by-year data (2000-2019)
- 💡 **Tooltips** showing exact percentages on hover
- 🔙 **Reset button** to return to continent overview
- 🎨 **Color-coded legend** for easy interpretation

**Insights:**
- Recycling rates vary significantly by continent
- Landfill usage declining in developed regions
- Mismanaged waste concentrated in specific continents

**Technologies:**
```javascript
- d3.stack() for stacked bar creation
- d3.scaleBand() for categorical x-axis
- d3.scaleLinear() for percentage y-axis
- Interactive click events for drill-down
```

---

### 4. Bubble Chart - Per Capita Mismanaged Waste (Rishika Buram)
**File:** `student4.html`

**Description:**  
A two-level interactive bubble chart showing mismanaged plastic waste per capita by country and continent.

**Key Features:**
- 🫧 **Dual-view visualization:**
  - **Continent View:** Bubble size represents number of countries
  - **Country View:** Top 10 countries per continent
- 🖱️ **Click to drill-down** from continent to country level
- 📊 **Proportional bubble sizing** based on data values
- 💬 **Rich tooltips** with detailed information
- 🔙 **Back button** for easy navigation
- 🎨 **Smooth transitions** between views
- ⚡ **Hover effects** with visual feedback

**Insights:**
- Continent-level aggregation reveals regional patterns
- Per-capita waste varies dramatically by country
- Top polluters identifiable through interactive exploration

**Technologies:**
```javascript
- d3.scaleSqrt() for bubble radius calculation
- d3.group() for data aggregation
- d3.scaleBand() for x-axis positioning
- Interactive state management
```

---

## 🛠️ Technical Stack

### Core Technologies
```
HTML5          - Structure and semantic markup
CSS3           - Styling and animations
JavaScript ES6 - Interactive functionality
D3.js v7       - Data-driven visualizations
Bootstrap 4.5  - Responsive layout and components
```

### D3.js Features Used
```javascript
// Scales
d3.scaleLinear()      // Numerical scales
d3.scaleTime()        // Temporal scales
d3.scaleBand()        // Categorical scales
d3.scaleThreshold()   // Color thresholds
d3.scaleSqrt()        // Proportional sizing

// Layouts
d3.stack()            // Stacked bar charts
d3.line()             // Line generation
d3.geoMercator()      // Map projection

// Interactions
d3.zoom()             // Zoom and pan
d3.drag()             // Drag interactions
Event listeners       // Click, hover, mouseout

// Utilities
d3.csv()              // Data loading
d3.group()            // Data aggregation
d3.extent()           // Domain calculation
```

### Data Sources
- **Format:** CSV files for structured data
- **Geographic Data:** GeoJSON for world map boundaries
- **Time Period:** 1950-2019 (varies by visualization)
- **Metrics:** Tons, percentages, per capita values

---

## 📁 Project Structure

```
Interactive-Visualization-Plastic-Pollution/
│
├── index.html                    # Main landing page with navigation
├── README.md                     # This file
│
├── visualizations/
│   ├── student1.html            # Line Chart (Karan)
│   ├── student2.html            # Choropleth Map (Usama)
│   ├── student3.html            # Stacked Bar Chart (Kiranmai)
│   └── student4.html            # Bubble Chart (Rishika)
│
├── data/
│   ├── student1.csv             # Global waste data (1950-2019)
│   ├── student2.csv             # Ocean emissions by country (2019)
│   ├── student3.csv             # Waste management methods (2000-2019)
│   ├── student4.csv             # Per capita waste by country
│   └── world.geojson            # World map boundaries
│
├── assets/
│   ├── screenshots/             # Project screenshots
│   └── documentation/           # Additional documentation
│
└── css/
    └── styles.css               # Additional custom styles
```

---

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (for CDN libraries)
- Local web server (optional, for development)

### Installation & Running

#### Option 1: Direct Browser Access
```bash
# Clone the repository
git clone https://github.com/UsamaMasood12/Interactive-Visualization-of-Plastic-Pollution-across-the-globe.git

# Navigate to project directory
cd Interactive-Visualization-Plastic-Pollution

# Open index.html in your browser
# On macOS: open index.html
# On Windows: start index.html
# On Linux: xdg-open index.html
```

#### Option 2: Local Web Server (Recommended)
```bash
# Using Python 3
python -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js
npx http-server

# Then navigate to: http://localhost:8000
```

#### Option 3: VS Code Live Server
```
1. Install "Live Server" extension in VS Code
2. Right-click on index.html
3. Select "Open with Live Server"
```

---

## 💡 How to Use

### Main Page (index.html)
1. **Landing Page Overview:**
   - Four cards representing each visualization
   - Brief description of each chart
   - Click any card to view the corresponding visualization

### Line Chart (student1.html)
1. **Hover** over the line to see year and value tooltips
2. **Scroll** to zoom in/out on specific time periods
3. **Click and drag** to pan across the timeline
4. **Notice** the annotation highlighting the 2008 recession impact

### Choropleth Map (student2.html)
1. **Hover** over countries to see exact emission values
2. **Click continent buttons** to filter by region
3. **Use dropdown** to filter by value category (High/Medium/Low)
4. **Combine filters** for detailed analysis
5. **Click "Show All"** to reset filters

### Stacked Bar Chart (student3.html)
1. **View** continent-level waste management overview
2. **Hover** over segments to see exact percentages
3. **Click any bar** to drill down to yearly data (2000-2019)
4. **Use "Back to Continent View"** button to reset

### Bubble Chart (student4.html)
1. **Initial View:** Bubbles represent continents
2. **Bubble size** indicates number of countries
3. **Click any bubble** to see top 10 countries in that continent
4. **Hover** for detailed information
5. **Click "Back to Continents"** to return to overview

---

## 📊 Data Insights & Key Findings

### Global Trends (Line Chart)
- **Exponential Growth:** Plastic waste increased from ~2M tons (1950) to 353M tons (2019)
- **2008 Anomaly:** Great Recession caused first significant production decrease
- **Acceleration:** Post-2010 shows steeper growth curve

### Geographic Distribution (Choropleth Map)
- **Hotspots:** Southeast Asian countries show highest ocean emissions per capita
- **Island Nations:** Small island developing states disproportionately affected
- **Continental Variation:** Significant differences between developed and developing regions

### Waste Management (Stacked Bar Chart)
- **Recycling Rates:** Vary from <5% to >30% by continent
- **Landfill Dominance:** Still the primary method in most regions
- **Improvement Trends:** Gradual increase in recycling, decrease in mismanagement

### Per Capita Analysis (Bubble Chart)
- **Top Polluters:** Specific countries exceed 5kg per capita annually
- **Regional Patterns:** Coastal countries show higher mismanagement rates
- **Development Correlation:** Varies by waste management infrastructure

---

## 🎨 Design Principles

### User Experience (UX)
- **Progressive Disclosure:** Start with overview, drill down for details
- **Consistent Navigation:** Back buttons and reset options throughout
- **Visual Feedback:** Hover effects, tooltips, and transitions
- **Responsive Design:** Bootstrap grid system ensures mobile compatibility

### Visual Design
- **Color Schemes:** 
  - Blues for water/ocean themes
  - Category-appropriate colors for waste types
  - High contrast for accessibility
- **Typography:** Clear, readable fonts with hierarchical sizing
- **Spacing:** Adequate whitespace for visual clarity
- **Animations:** Smooth transitions (0.3s) for professional feel

### Interaction Design
- **Intuitive Controls:** Click, hover, and scroll interactions
- **Immediate Feedback:** Visual changes on interaction
- **Forgiving Interface:** Easy to undo or reset actions
- **Help Text:** Instructions provided where needed

---

## 🔧 Customization & Extension

### Adding New Visualizations
```javascript
// 1. Create new HTML file (student5.html)
// 2. Add card to index.html
<div class="col-md-3">
    <div class="card">
        <div class="card-body">
            <p class="card-text">Your description</p>
            <a href="student5.html" class="btn btn-primary">View Chart</a>
        </div>
    </div>
</div>

// 3. Implement D3.js visualization
// 4. Add corresponding CSV data file
```

### Modifying Existing Charts
```javascript
// Update color schemes
const colorScale = d3.scaleThreshold()
    .range(d3.schemeGreens[8]); // Change to any D3 color scheme

// Adjust dimensions
const width = 1200; // Modify as needed
const height = 800;

// Change data file
d3.csv("new_data.csv").then(data => {
    // Your visualization code
});
```

---

## 🎓 Academic Context

**Institution:** Teesside University  
**Program:** MSc Data Science  
**Course:** Interactive Data Visualization  
**Type:** Team Project

### Learning Outcomes Demonstrated

**Technical Skills:**
- D3.js library proficiency
- Interactive web development
- Data visualization best practices
- Responsive design principles
- Version control (Git/GitHub)

**Data Skills:**
- Data transformation and aggregation
- Scale selection and application
- Visual encoding of data
- Storytelling with data

**Collaboration:**
- Team coordination
- Consistent design language
- Code integration
- Shared data standards

---

## 📚 Resources & References

### D3.js Documentation
- [D3.js Official Documentation](https://d3js.org/)
- [D3.js Gallery](https://observablehq.com/@d3/gallery)
- [D3.js Tutorials](https://www.d3indepth.com/)

### Plastic Pollution Data
- Our World in Data - Plastic Pollution
- UNEP - Marine Litter and Microplastics
- Ocean Conservancy Reports

### Design Resources
- Bootstrap Documentation
- ColorBrewer (Color Schemes)
- GeoJSON Maps

---

## 🚧 Future Enhancements

### Planned Features
1. **Real-time Data Updates**
   - Integration with live data APIs
   - Automatic refresh mechanism
   - Historical data archiving

2. **Additional Visualizations**
   - Sankey diagram for waste flow
   - Heatmap for temporal patterns
   - Network graph for trade routes

3. **Enhanced Interactivity**
   - Cross-visualization filtering
   - Synchronized tooltips across charts
   - Time-slider for temporal exploration
   - Compare mode for multiple countries

4. **Mobile Optimization**
   - Touch-friendly interactions
   - Responsive chart sizing
   - Simplified mobile interface
   - Progressive Web App (PWA)

5. **Export & Sharing**
   - Download visualizations as PNG/SVG
   - Share buttons for social media
   - Embed codes for external sites
   - PDF report generation

6. **Advanced Analytics**
   - Trend prediction using ML
   - Correlation analysis
   - Statistical significance testing
   - Custom data upload

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Ways to Contribute
- 🐛 Report bugs or issues
- 💡 Suggest new visualizations or features
- 📝 Improve documentation
- 🎨 Enhance designs and UX
- 📊 Add new datasets
- 🔧 Fix bugs or implement features

### Contribution Guidelines
```bash
1. Fork the repository
2. Create a feature branch (git checkout -b feature/AmazingFeature)
3. Commit your changes (git commit -m 'Add some AmazingFeature')
4. Push to the branch (git push origin feature/AmazingFeature)
5. Open a Pull Request
```

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👥 Authors

### Team Members

**Usama Masood** - Choropleth Map
- 📧 Email: usamamasood531@gmail.com
- 💼 LinkedIn: [linkedin.com/in/usama-masood-b4a35014b](https://www.linkedin.com/in/usama-masood-b4a35014b)
- 🐙 GitHub: [@UsamaMasood12](https://github.com/UsamaMasood12)

**Karan Gunti** - Line Chart  
**Kiranmai Kodali** - Stacked Bar Chart  
**Rishika Buram** - Bubble Chart

---

## 🙏 Acknowledgments

- **Teesside University** for project guidance and resources
- **D3.js Community** for excellent documentation and examples
- **Our World in Data** for comprehensive plastic pollution datasets
- **Bootstrap Team** for the responsive framework
- **Open-source Community** for GeoJSON and mapping resources

---

## 📞 Support & Contact

### For Technical Issues
- Open an issue on GitHub
- Check existing issues for solutions
- Review documentation and examples

### For Project Inquiries
- **Email:** usamamasood531@gmail.com
- **LinkedIn:** Professional networking and discussions
- **GitHub:** Code-related questions and contributions

---

## 📊 Project Statistics

![HTML](https://img.shields.io/badge/HTML-40%25-orange)
![JavaScript](https://img.shields.io/badge/JavaScript-50%25-yellow)
![CSS](https://img.shields.io/badge/CSS-10%25-blue)

![Visualizations](https://img.shields.io/badge/Visualizations-4-brightgreen)
![Interactive Features](https://img.shields.io/badge/Interactive%20Features-15%2B-blue)
![Data Points](https://img.shields.io/badge/Data%20Points-10K%2B-red)

---

## 🌟 Star History

If you find this project useful for learning D3.js or understanding plastic pollution trends, please consider giving it a ⭐!

---

**⭐ If you found this visualization project helpful, please star it on GitHub!**

---

*Visualizing Environmental Impact Through Interactive Data Stories*
