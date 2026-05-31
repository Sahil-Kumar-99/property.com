# Geo-Smart Real Estate & Infrastructure Insights Portal

A web-based platform designed for property dealers and buyers. The system allows an agent to visit a site, capture live coordinates, and upload site photos. The portal then automatically cross-references this location with government infrastructure data to show potential buyers if any government road projects are approved or proposed near the property.

## Features

### Phase A: On-Site Data Collection (Field Agent)
- Live Geo-Tracking: Capture precise Latitude and Longitude using the device's GPS.
- Multimedia Upload: Real-time camera access to capture and upload 2-3 high-quality site photos.
- Property Metadata: Input fields for owner contact details, land size, and price.
- Integration with Google Maps Geocoding API to convert coordinates into a readable address.

### Phase B: Automated Infrastructure Check (The "API Engine")
- Government Road Connectivity: Once a location is submitted, the system triggers a background check to identify nearby infrastructure projects.
- Proximity Analysis: Calculate the distance between the plot and the nearest sanctioned government road.
- Integration with data.gov.in (OGD platform) APIs or State PWD Open Data to fetch road project status.
- Integration with PostGIS / Spatial Query API to calculate the distance from the plot to the infrastructure line.

### Phase C: Buyer's Dashboard (Customer View)
- Interactive Map View: Show the property location on a map with a visual overlay of proposed roads.
- Infrastructure Tagging: Display automated tags like "Plot is 200m away from an approved 60ft Highway."
- Surrounding Amenities: Automatically list nearby Hospitals, Schools, and Markets.
- Integration with Google Places API to fetch nearby points of interest (POIs).
- Integration with Google Street View API for a 360-degree neighborhood tour.

### Phase D: Engagement & Conversion
- Direct Contact: A specialized "WhatsApp Dealer" button that sends the specific Property ID and User Interest to the dealer.
- Dynamic Document Checklist: Generate a list of required legal documents based on the property's district/location.
- Integration with WhatsApp Business API for instant lead generation.

## Technical Stack
- Frontend: Next.js (React) with TypeScript and Tailwind CSS
- Backend: Next.js API Routes (Node.js)
- Database: PostgreSQL with PostGIS extension
- Storage: AWS S3 or Cloudinary for photos
- APIs: Google Maps, HTML5 Geolocation, Data.gov.in, Google Places, WhatsApp Business

## Setup Instructions

1. Install Node.js from https://nodejs.org/ (version 18 or higher)
2. Install PostgreSQL with PostGIS from https://www.postgresql.org/download/ and enable PostGIS extension
3. Clone or navigate to the project directory
4. Run `npm install` to install dependencies
5. Set up environment variables in `.env.local`:
   - GOOGLE_MAPS_API_KEY=your_google_maps_api_key
   - DATABASE_URL=postgresql://user:password@localhost:5432/real_estate_db
   - AWS_S3_ACCESS_KEY=your_aws_key (if using S3)
   - WHATSAPP_API_KEY=your_whatsapp_key
6. Run database migrations (if using Prisma or similar)
7. Run `npm run dev` to start the development server
8. Open http://localhost:3000 in your browser

## Professional Design Features
- **Modern UI**: Clean, responsive design using Tailwind CSS with professional color schemes and typography.
- **Hero Section**: Full-screen landing page with background image and call-to-action buttons.
- **Interactive Elements**: Hover effects, transitions, and intuitive navigation.
- **Icons**: SVG icons for better scalability and professional appearance.
- **Images**: High-quality stock images from Unsplash for visual appeal (replace with your own assets in production).
- **Mobile-First**: Fully responsive design optimized for all devices.
- **Accessibility**: Proper contrast, focus states, and semantic HTML.

## Contributing
Please follow the standard Next.js and TypeScript best practices.