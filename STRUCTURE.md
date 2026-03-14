# Website Structure Documentation

## Directory Structure

```
uiux_project/
├── index.html (Home Page)
│
├── pages/
│   ├── movie-detail.html (Single Movie Details Page)
│   ├── search-results.html (Search Results Page)
│   │
│   ├── browse/
│   │   ├── genres.html (All Genres Grid)
│   │   └── movies.html (Latest/Top Rated/Popular - 3 categories on one page)
│   │
│   ├── features/
│   │   ├── smart-discovery.html (AI/OTT Discovery with Movie DNA matcher)
│   │   ├── watchlist.html (User Watchlist)
│   │   ├── downloads.html (Downloads & History)
│   │   ├── movie-map.html (Movie Map)
│   │   └── bundles.html (Movie Bundles/Collections)
│   │
│   ├── tools/
│   │   ├── calendar.html (Release Calendar)
│   │   └── request.html (Movie Request)
│   │
│   └── info/
│       └── about-help.html (About Us & Help Center - Combined)
│
├── css/
│   └── style.css
│
├── js/
│
├── images/
│
└── bootstrap-5.3.8-dist/
```

## Page Details

### 1. Home Page (index.html)
- Main landing page
- Hero carousel
- Featured content sections

### 2. Movie Detail Page (pages/movie-detail.html)
- Single movie details
- Cast, crew, reviews
- Streaming availability

### 3. Search Results (pages/search-results.html)
- Search functionality results
- Filters and sorting

### 4. Browse Section (pages/browse/)
**Genres Page** - All genres in a grid layout
**Movies Page** - Three categories on one page:
  - Latest Movies
  - Top Rated Movies
  - Popular Movies

### 5. Features Section (pages/features/)
**Smart Discovery**
- Personalized "Movie DNA" matcher (3 questions → 10 matches)
- "Feeling Lucky" roulette wheel
- Mood-based discovery (Lazy Sunday, Late Night Thriller, Date Night)
- Interactive timeline slider (explore by decade)

**Watchlist** - User's saved movies (no login required)

**Downloads** - Download history tracking (no login required)

**Movie Map** - Visual movie exploration

**Bundles** - Curated movie collections

### 6. Tools Section (pages/tools/)
**Release Calendar** - Upcoming movie releases

**Request** - Movie request form

### 7. Info Section (pages/info/)
**About & Help** - Combined page with:
- About Us
- Help Center
- FAQ

## Navigation Structure

### Main Nav Menu:
1. **Home** → index.html
2. **Browse** (dropdown)
   - All Genres
   - Latest / Top Rated / Popular
3. **Features** (dropdown)
   - Smart Discovery
   - My Watchlist
   - Downloads & History
   - Movie Map
   - Movie Bundles
4. **Tools** (dropdown)
   - Release Calendar
   - Request Movie
5. **About & Help** → Combined page

### Features:
- All pages have consistent navbar and footer
- Dropdown menus with hover effects
- No authentication required for any feature
- Responsive design with Bootstrap 5.3.8
- Search functionality accessible from navbar

## Color Scheme
- Primary: Red gradient (#dc2626 to #991b1b)
- Background: Dark gradient theme
- Glass-morphism effects on navbar

## Next Steps
All pages are now created with navbar and footer. You can now start building the content for each page based on your requirements.
