# 🎬 ShowSync - Movie Database App

<div align="center">
  
![image](https://github.com/user-attachments/assets/dc4d6071-593c-43a7-95c4-5a00e5d5f669)


  
  ### Your personal movie companion
  
  [![API](https://img.shields.io/badge/API-21%2B-brightgreen.svg)](https://android-arsenal.com/api?level=21)
  [![Kotlin](https://img.shields.io/badge/Kotlin-1.9.24-blue.svg)](https://kotlinlang.org)
  [![TMDB](https://img.shields.io/badge/TMDB-API-yellow.svg)](https://www.themoviedb.org/documentation/api)
  
</div>

ShowSync is a feature-rich Android application that lets movie enthusiasts discover, search, and curate their personal movie collection using The Movie Database (TMDB) API. Built with modern Android architecture and best practices.

## ✨ Features

- 🔍 **Search & Discover**: Find any movie from TMDB's extensive database
- 📍 **Nearby Movies**: Discover movies trending in your region
- ❤️ **Favorites**: Build and manage your personal movie collection
- 📱 **Offline Support**: View your saved movies even without internet
- 📝 **Custom Movies**: Add personal movie entries with custom details
- 🌐 **Multi-language**: Full support for English and Hebrew

## 🏗️ Architecture & Tech Stack

<div align="center">
  <img src="https://developer.android.com/topic/libraries/architecture/images/final-architecture.png" width="500" alt="MVVM Architecture">
</div>

ShowSync implements:

- **🏛️ MVVM Architecture**
  - Clear separation of concerns
  - Testable components
  - Lifecycle-aware data handling

- **🧩 Android Jetpack**
  - ↔️ Navigation Component
  - 💾 Room Database
  - 📊 ViewModel & LiveData
  - 🔗 ViewBinding

- **⚡ Modern Android Development**
  - 🧵 Coroutines & Flow
  - 🌐 Retrofit & OkHttp
  - 🖼️ Glide
  - 💉 Dagger Hilt
  - 📍 Google Location Services

## 📱 App Demo

<div align="center">
  <table>
    <tr>
      <td><img src="https://via.placeholder.com/200x400?text=Movie+Search" width="200" alt="Movie Search"></td>
      <td><img src="https://via.placeholder.com/200x400?text=Movie+Details" width="200" alt="Movie Details"></td>
      <td><img src="https://via.placeholder.com/200x400?text=Favorites" width="200" alt="Favorites"></td>
    </tr>
    <tr>
      <td align="center">Search Movies</td>
      <td align="center">Movie Details</td>
      <td align="center">Favorites Collection</td>
    </tr>
    <tr>
      <td><img src="https://via.placeholder.com/200x400?text=Nearby+Movies" width="200" alt="Nearby Movies"></td>
      <td><img src="https://via.placeholder.com/200x400?text=Add+Movie" width="200" alt="Add Movie"></td>
      <td><img src="https://via.placeholder.com/200x400?text=All+Movies" width="200" alt="All Movies"></td>
    </tr>
    <tr>
      <td align="center">Regional Discoveries</td>
      <td align="center">Add Custom Movies</td>
      <td align="center">Movie Collection</td>
    </tr>
  </table>
</div>

<div align="center">
  <p><b>Try the interactive app tour!</b></p>
  <a href="https://youtu.be/your-demo-link">
    <img src="https://img.shields.io/badge/Watch%20Demo-Video-ff0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch Demo Video" width="200">
  </a>
</div>

## 🛠️ Dependencies

<table>
  <tr>
    <td>
      <ul>
        <li>AndroidX Core: 1.15.0</li>
        <li>Lifecycle: 2.8.7</li>
        <li>Room: 2.6.1</li>
        <li>Retrofit: 2.9.0</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Glide: 4.16.0</li>
        <li>Google Play Services: 21.3.0</li>
        <li>Material Design: 1.12.0</li>
        <li>Kotlin Coroutines: 1.6.4</li>
      </ul>
    </td>
  </tr>
</table>

## 🚀 Getting Started

### Prerequisites
- Android Studio Arctic Fox (2020.3.1) or newer
- Android SDK with minimum API 21
- Kotlin 1.9.24 or newer

### Installation

1. **Clone the repo**
   ```bash
   git clone https://github.com/yourusername/showsync.git
   ```

2. **Open in Android Studio**
   
   Open Android Studio, select "Open an existing project" and navigate to the cloned directory.

3. **API Key Setup**
   
   Replace the TMDB API key in `AppModule.kt`:
   ```kotlin
   // Find this line and replace with your key
   val apiKey = "your_tmdb_api_key"
   ```
   
   > 💡 **Tip:** Create a free account at [TMDB](https://www.themoviedb.org/signup) to get your API key!

4. **Build and run**
   
   Connect a device or use the Android Emulator to build and run the application.

## 📂 Project Structure

```
com.example.midproject_imdb/
├── core/                      # Core application components
│   └── MovieApplication.kt    # Application class with Hilt
│
├── data/                      # Data layer
│   ├── local_db/              # Room database implementation
│   │   ├── MovieDao.kt        # Data Access Objects
│   │   ├── MovieTMDBDao.kt
│   │   ├── MovieDataBase.kt   # Local databases
│   │   └── MovieTMDBDatabase.kt
│   │
│   ├── models/                # Data models
│   │   ├── Movie.kt           # Local movie entity
│   │   └── MovieTMDB.kt       # API movie entity
│   │
│   ├── repositories/          # Repository pattern implementation
│   │   ├── MovieRepository.kt    # Local movies repository
│   │   └── MovieTMDbRepo.kt      # TMDB API repository
│   │
│   └── retrofit/              # Network layer
│       └── MovieApiService.kt # API service definitions
│
├── di/                        # Dependency injection
│   └── AppModule.kt           # Hilt module for dependencies
│
└── ui/                        # Presentation layer
    ├── all_movies/            # Movie list feature
    ├── add_movie/             # Add movie feature
    ├── detail_movie/          # Movie details feature
    ├── favorite_movies/       # Favorites feature
    ├── movie_search/          # Search feature
    ├── nearby_movies/         # Location-based movies feature
    └── MovieTMDBDetailed/     # TMDB movie details
```

## 🔐 Permissions

<table>
  <tr>
    <th>Permission</th>
    <th>Why it's needed</th>
  </tr>
  <tr>
    <td><code>INTERNET</code></td>
    <td>To fetch movie data from TMDB API</td>
  </tr>
  <tr>
    <td><code>ACCESS_NETWORK_STATE</code></td>
    <td>To check network connectivity status</td>
  </tr>
  <tr>
    <td><code>ACCESS_COARSE_LOCATION</code></td>
    <td>To determine your region for nearby movies</td>
  </tr>
  <tr>
    <td><code>ACCESS_FINE_LOCATION</code></td>
    <td>For more precise location data (optional)</td>
  </tr>
</table>

> **Note:** The app handles permission requests gracefully and provides alternative functionality when permissions are denied.

## 📄 License

```
MIT License

Copyright (c) 2025 ShowSync Developers

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
