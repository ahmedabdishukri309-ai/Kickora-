# Kickora - Live Football Score App

A modern, production-ready Flutter application for live football (soccer) scores, fixtures, standings, and match details.

## Features

✨ **Core Features:**
- 🔴 **Live Matches** - Real-time score updates and match tracking
- 📋 **Fixtures** - Upcoming matches and schedules
- 🏆 **Standings** - League tables and team rankings
- 🎯 **Match Details** - Comprehensive match information
- 🏠 **Multi-League Support** - Premier League, La Liga, Champions League, Serie A, Bundesliga

✨ **App Features:**
- Dark theme with modern UI design
- League filtering with quick access
- Pull-to-refresh functionality
- Responsive layout for all devices
- Professional error handling
- Fast and efficient API integration

## Project Structure

```
lib/
├── main.dart                 # App entry point
├── models/
│   └── models.dart          # Data models (Match, Standing, League)
├── screens/
│   ├── main_screen.dart     # Navigation hub
│   ├── home_screen.dart     # Matches by league
│   ├── live_screen.dart     # Live matches
│   ├── matches_screen.dart  # Fixtures & standings
│   └── settings_screen.dart # App settings
├── services/
│   └── football_api_service.dart  # API integration
└── widgets/
    ├── match_card.dart      # Match display widget
    └── standing_card.dart   # League table widget
```

## API Integration

The app uses [football-data.org](https://www.football-data.org/) API for real-time data:
- Live match scores
- Upcoming fixtures
- League standings
- Match details and statistics

**Note:** API key is not hardcoded. Set your API key via:
- Environment variable: `FOOTBALL_API_KEY`
- Secure storage in production

## Getting Started

### Prerequisites
- Flutter 3.0 or higher
- Dart SDK

### Installation

1. Clone the repository
2. Install dependencies:
```bash
flutter pub get
```

3. Set your API key (environment variable or config file):
```bash
export FOOTBALL_API_KEY="your_api_key_here"
```

4. Run the app:
```bash
flutter run
```

## Supported Leagues

- 🇬🇧 Premier League (PL)
- 🇪🇸 La Liga (LA)
- 🏆 Champions League (CL)
- 🇮🇹 Serie A (SA)
- 🇩🇪 Bundesliga (BL1)

## UI Themes

- **Dark Theme** - Modern dark UI with green accents
- **Colors:**
  - Primary: Green (#00C853)
  - Background: #121212
  - Surface: #1E1E1E
  - Error: Red (#FF5252)

## Architecture

The app follows a clean, modular architecture:
- **Models**: Data structures for API responses
- **Services**: API communication layer
- **Screens**: UI pages and navigation
- **Widgets**: Reusable UI components

## Error Handling

The app includes comprehensive error handling:
- Network error detection
- API rate limit handling
- Graceful error messages to users
- Offline state management

## Production Readiness

✅ Clean code structure  
✅ Modular architecture  
✅ Error handling and logging  
✅ Performance optimization  
✅ Responsive design  
✅ No hardcoded sensitive data  
✅ Ready for scaling  

## Future Enhancements

- 🔔 Push notifications for live updates
- 💾 Local data caching
- 🔍 Search and filter functionality
- ⭐ Favorite teams/leagues
- 📊 Advanced statistics and analytics
- 🎨 Multiple theme options
- 🌍 Multi-language support

## License

MIT License - Feel free to use this project

## Support

For issues or feature requests, please open an issue on GitHub.

---

**Built with ❤️ using Flutter**
