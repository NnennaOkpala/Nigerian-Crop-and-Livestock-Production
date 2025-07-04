# 🌾 Nigerian-Crop-and-Livestock-Production

## 📘 NGN-CROP & LIVESTOCK ANALYSIS (1985–2023)

### 📘 Introduction
Agriculture plays a vital role in Nigeria's economy—sustaining rural livelihoods, fueling food systems, and positioning the country as a global leader in select commodities. With rising population pressures and shifts in dietary demand, tracking crop and livestock production trends is essential for strategic planning and food security.

This analysis explores Nigeria’s top-performing crop and livestock outputs—highlighting global rankings, national trends, year-over-year growth, and emerging agricultural opportunities.

---

### ❓ Problem Statement
Despite Nigeria’s dominance in producing key crops like cassava, yam, and cowpea, challenges persist in livestock development, value addition, and data-driven policy formulation. To fully harness its agri-potential, Nigeria needs detailed production insights across time and space.

**Research Questions**
- What crops and livestock products does Nigeria dominate globally, and why?
- Which products show the highest growth, and where are opportunities lagging?
- How have trends changed over time—what patterns emerge?
- How can insights guide investment, policy, and market expansion?

---

### 🧰 Tools Used
- **Microsoft Excel** – Data cleaning and historical trend prep
- **Power BI** – Dashboard development and interactive visual analysis
- **DAX Calculations** – Growth rates, rankings, and performance flags

---

### 🧪 Skills Demonstrated
- Data Cleaning & Structuring
- Time Series Analysis
- Interactive Filtering & Visual Navigation
- Insight Communication through Storytelling
- Global Comparative Benchmarking
- Dashboard Design with Stakeholder Usability in Mind

---

### 🧹 Data Cleaning Steps
Performed in Excel and Power BI:
- Removed duplicates and irrelevant columns (`Domain`, `Element Code`, `Item Code`, `Year Code`, `Note`)
- Standardized product naming across years
- Converted units (e.g., tons) for consistency
- Added metadata like year and ranking status

**Visual Examples**  
![Cleaned Crop File](https://github.com/user-attachments/assets/ae94ce61-6d57-4db8-a465-e3d657eefe5c)  
![Uncleaned Crop File](https://github.com/user-attachments/assets/0baf6a4b-2edf-4a7d-a6bb-a1255c2e1879)

_CLEANED EXCEL FILE FOR ANIMAL PRODUCTION DATASET_

---

### 📊 Analysis Questions
- What commodities place Nigeria in the top 10 globally?
- Which crops and livestock products have shown significant growth over the decades?
- What trends have emerged in Nigeria’s agricultural output since 1985?
- Which niche agricultural sectors show untapped potential for scale?
- How does urban vs. rural demand influence production and investment?
- What strategic actions can enhance Nigeria’s competitiveness in global agriculture?

---

### 📈 Visualizations

**Nigerian Crop Production Dashboard**  
![Crop Dashboard](https://github.com/user-attachments/assets/56871cf7-07fd-44df-8508-32192115c496)

**Nigerian Animal Production Dashboard**  
![Animal Dashboard](https://github.com/user-attachments/assets/fe5a59a5-3d97-48be-a2a8-19a838667f87)

---

### 🔍 Key Insights

#### 🌱 Crops
- 🥇 #1 globally in: **Cassava (fresh), Cowpeas (dry), Yams, Kola nuts, Taro**
- 🌟 Strong output in: **Melonseed, Ginger, Karite nuts**
- 🌾 Mid-range volumes in: **Maize, Rice, Oil Palm**
- 🔬 Emerging presence in: **Fonio, Jojoba, Okra**

#### 🐄 Livestock
- 🥚 High production of **Hen eggs**
- 🐐 Robust national output of **Goat meat**, **Raw cattle milk**
- 🐓 Steady growth in **Poultry and pig meats**
- 🦌 Niche expansion into **Snail meat, Game meats, Camelids**

---

### 🕰️ Production Trends (1985–2023)

| Decade       | Trends                                                 |
|--------------|--------------------------------------------------------|
| 1985–2000    | Stable crop volumes, particularly root staples         |
| 2000–2010    | Poultry and dairy expansion begins                     |
| 2010–2021    | Rapid growth in livestock product diversity            |
| 2023 →       | Introduction of niche meats & global scale ambition    |

---

### 🌍 Nigeria’s Global Standing
- Ranked **Top 5 globally** in multiple key commodities
- Outperformed in **cassava, cowpeas, eggs, and yams**
- Competitive presence alongside: **China, India, Brazil, USA**

---

### 🏙️ Urban vs. Rural Production Dynamics
- **Urban hubs** (e.g., Lagos, Abuja): Dominant in dairy, poultry, and niche meat production  
- **Rural zones**: Stronghold of root crops and traditional staples  
- **Infrastructure challenges**: Affect value chain performance and product mobility

---

### 📌 Observations & Gaps
- 🧊 Livestock remains underdeveloped compared to crops
- 💡 Niche products like snail and game meats are underrepresented
- 🧊 Cold chain logistics are insufficient for dairy and eggs
- 📉 Smallholder performance data lacks transparency

---

### 🧭 Recommendations
- 📦 Expand agro-processing for cassava, yams, cowpeas
- 🧊 Invest in cold-chain infrastructure for perishables
- 🛠️ Develop emerging sectors (Fonio, snail meat, game meat)
- 🧪 Enhance agricultural data systems
- 🚜 Improve transport infrastructure to support rural-urban flows
- 🤝 Foster public-private partnerships for scale and innovation
- 🌍 Elevate Nigeria’s export readiness through strategic branding

---

### 📐 DAX Calculations Used

```dax
-- Nigeria Rank Per Crop
Nigeria Rank Per Crop = 
VAR CurrentCrop = SELECTEDVALUE('Crops from 023 to 1985'[Item])
RETURN
CALCULATE(
    RANKX(
        FILTER(
            ALL('Crops from 023 to 1985'),
            'Crops from 023 to 1985'[Item] = CurrentCrop
        ),
        CALCULATE(SUM('Crops from 023 to 1985'[Value])),
        ,
        DESC
    ),
    'Crops from 023 to 1985'[Area] = "Nigeria"
)

-- Nigeria Rank Per Livestock
Nigeria Rank Per Livestock = 
VAR CurrentCrop = SELECTEDVALUE('livestock from 023 to 1985'[Item])
RETURN
CALCULATE(
    RANKX(
        FILTER(
            ALL('livestock from 023 to 1985'),
            'livestock from 023 to 1985'[Item] = CurrentCrop
        ),
        CALCULATE(SUM('livestock from 023 to 1985'[Value])),
        ,
        DESC
    ),
    'livestock from 023 to 1985'[Area] = "Nigeria"
)



---
