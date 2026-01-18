# ColorBlindness Simulator & Filter Tool

A web application that simulates and applies filters for different types of color blindness (color vision deficiency). This tool helps people with Daltonism experience how images appear through different color perception perspectives, enabling better visual accessibility and understanding.

## Features

- **Three Color Blindness Simulations:**
  - Protanopia (Red-blind)
  - Deuteranopia (Green-blind)
  - Tritanopia (Blue-yellow blind)

- **Image Processing:** Upload any image and apply filters in real-time
- **Live Preview:** See the filtered result before downloading
- **User-Friendly Interface:** Clean, intuitive React-based UI
- **RESTful API:** Backend API for scalable image processing

## Tech Stack

**Frontend:**
- React.js
- Tailwind CSS
- Axios (HTTP client)

**Backend:**
- FastAPI (Python)
- Pillow (PIL) for image processing
- NumPy for pixel manipulation

## Installation

### Prerequisites
- Python 3.8+
- Node.js 14+
- npm or yarn

### Backend Setup

1. Navigate to the project root and install Python dependencies:
```bash
pip install -r requirements.txt
```

2. Start the FastAPI server:
```bash
uvicorn main:app --reload
```

The backend will run on `http://localhost:8000`

### Frontend Setup

1. Navigate to the frontend directory:
```bash
cd color-blindness-app
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm start
```

The frontend will run on `http://localhost:3000`

## How to Use

1. Open the application in your browser (`http://localhost:3000`)
2. Upload an image using the upload form
3. Select a color blindness filter from the dropdown
4. Click "Apply Filter" to process the image
5. Preview the result and download if needed

## Project Structure

```
.
├── main.py                          # FastAPI application
├── image_filters.py                 # Filter algorithms
├── requirements.txt                 # Python dependencies
├── uploads/                         # Uploaded images directory
└── color-blindness-app/            # React frontend
    ├── src/
    │   ├── App.js                  # Main component
    │   ├── components/
    │   │   ├── UploadForm.js
    │   │   ├── FilterForm.js
    │   │   └── Description.js
    │   └── index.css
    └── package.json
```

## API Endpoints

- `POST /upload/` - Upload an image file
- `POST /process/` - Apply a color blindness filter
- `GET /upload/{filename}` - Retrieve uploaded image

## Limitations & Future Improvements

- Current filters use simplified RGB transformation algorithms
- Could benefit from more sophisticated color space conversions (e.g., LMS to RGB)
- Performance optimization for batch processing
- Additional filter types and customization options

## License

This project is provided as-is for educational and accessibility purposes.
