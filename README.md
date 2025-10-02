# SRAT - Simplified Risk Assessment Register & Treatment

A single-file web application that simplifies the ISO 27001-compliant risk assessment process. Build for fun and  "vibe coding".


## Features

### 🎯 Core Functionality
- **Guided Risk Assessment Flow**: Step-by-step process from asset/threat selection to export
- **Independent Asset-Threat Associations**: Define specific threats for each asset individually
- **Flexible Risk Modeling**: Each asset can have completely different threat profiles
- **Pre-populated Lists**: Comprehensive lists of common assets and threats for SMBs
- **Dynamic Risk Scoring**: Real-time likelihood × impact calculation with visual indicators
- **ISO 27001 Controls**: Integrated Annex A controls for treatment planning
- **CSV Export**: Professional risk register export functionality
- **Local Storage**: Save/load assessments using browser localStorage

### 🎨 Design Features
- **Dark Mode Theme**: Sleek, modern dark interface
- **Fully Responsive**: Optimized for mobile and desktop
- **Interactive UI**: Smooth animations and instant feedback
- **Accessibility**: Clean typography with Inter font and proper contrast

### 📊 Assessment Components

#### 1. Asset Categories
**Digital Assets:**
- Customer Database
- Employee Laptops
- Web Server
- Intellectual Property
- Financial Records
- Cloud Services (SaaS)
- Company Website
- Email System
- Backup Systems
- Network Infrastructure

**Physical Assets:**
- Office Building
- Server Room
- Physical Documents
- Mobile Devices
- Storage Media

**Human Assets:**
- Employees
- Contractors
- Third-Party Vendors

#### 2. Threat Categories
**Cyber Threats:**
- Malware/Ransomware (affects digital assets)
- Phishing (affects email systems, employees)
- DDoS Attack (affects web servers, websites)
- SQL Injection (affects databases, web applications)
- Brute Force Attack (affects systems with authentication)
- Data Breach (affects confidential data stores)
- Supply Chain Attack (affects third-party services)

**Human Threats:**
- Insider Threat (Malicious) (affects all asset types)
- Employee Error/Accidental Data Leak (affects human-operated systems)
- Lack of Security Awareness (affects personnel)
- Social Engineering (affects employees and data)

**Physical Threats:**
- Physical Theft of Hardware (affects portable devices)
- Unauthorized Physical Access (affects facilities)
- Device Loss/Misplacement (affects mobile assets)

**Environmental Threats:**
- Fire (affects physical infrastructure)
- Water Damage (affects physical infrastructure)
- Natural Disaster (affects physical locations)
- Power Outage (affects electrical systems)
- Cloud Provider Service Failure (affects cloud services)

**Legal Threats:**
- Regulatory Compliance Violation (affects regulated data)

*Note: Each threat is automatically mapped to relevant assets, so you only see applicable threats for your selected assets.*

#### 3. ISO 27001 Controls
Includes key Annex A controls such as:
- A.5.1.1 - Policies for Information Security
- A.8.1.1 - Inventory of Assets
- A.9.2.1 - User Access Provisioning
- A.12.2.1 - Change Management
- A.16.1.1 - Incident Management Responsibilities
- And more...

## Usage Guide

### Getting Started
1. **Open the Application**: Load `index.html` in a web browser
2. **Start New Assessment**: Click "Start New Assessment" and enter a project name
3. **Define Asset-Threat Combinations**: Click on each asset to define its specific threats independently
4. **Assess Risk Scenarios**: Use sliders to rate impact and likelihood for each asset-threat combination
5. **Plan Treatment**: Choose treatment strategies and select appropriate controls
6. **Export Results**: Generate and download a CSV risk register

### Risk Scoring System
- **Impact Scale**: 1 (Low) to 3 (High)
- **Likelihood Scale**: 1 (Low) to 3 (High)
- **Risk Score**: Impact × Likelihood (1-9)
- **Risk Levels**:
  - Low Risk: 1-3 (Green)
  - Medium Risk: 4-6 (Orange)
  - High Risk: 7-9 (Red)

### Treatment Options
1. **Accept**: Acknowledge and accept the risk as-is
2. **Mitigate**: Implement controls to reduce likelihood or impact
3. **Transfer**: Share risk with third parties (insurance, contracts)
4. **Avoid**: Stop the activity that creates the risk

## Technical Implementation

### Architecture
- **Single-file Application**: Everything in one HTML file for easy deployment
- **Vanilla JavaScript**: No external dependencies (except Firebase for future use)
- **CSS Grid & Flexbox**: Modern responsive layout
- **Local Storage**: Client-side data persistence

### Browser Compatibility
- Chrome/Edge (recommended)
- Firefox
- Safari
- Mobile browsers

### File Structure
```
SRAT/
├── index.html          # Main application file
└── README.md          # Documentation
```

## Customization

### Adding New Assets/Threats
Edit the `predefinedAssets` and `predefinedThreats` arrays in the JavaScript section:

```javascript
predefinedAssets.push({
    id: 'asset_custom',
    name: 'Custom Asset Name',
    category: 'Digital|Physical|Human',
    description: 'Asset description'
});
```

### Adding New Controls
Extend the `iso27001Controls` array:

```javascript
iso27001Controls.push({
    id: 'A.X.X.X',
    name: 'Control Name'
});
```

### Styling Customization
Modify CSS custom properties in the `:root` section:

```css
:root {
    --primary-color: #6366f1;
    --background-dark: #0f172a;
    /* ... other variables */
}
```

### Planned Features
- Real-time collaboration
- Advanced reporting
- Risk trend analysis
- Compliance mapping
- Template assessments

## Security Considerations

### Data Privacy
- All data stored locally in browser (no server transmission)
- No external API calls 
- No user tracking or analytics

## Support

### Browser Requirements
- Modern browser with ES6+ support
- JavaScript enabled
- Local storage enabled


## License

Copyright @ 2026 Claudio Messineo
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.
This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
You should have received a copy of the GNU General Public License along with this program. If not, see <https://www.gnu.org/licenses/>.


---
