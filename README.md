# StyleHub - Salon Booking & Management App

A complete, production-ready Flutter mobile application for salon booking and management with Firebase backend.

## Features

### 🎯 Core Features
- **Multi-role Support**: Admin, Salon Owner, Helper/Staff, Customer
- **Authentication**: Phone OTP + Google Sign-In
- **Real-time Token System**: Queue management with live tracking
- **Salon Management**: Create and manage salon profiles
- **Service Management**: Add/edit services with pricing
- **Staff Management**: Assign and manage helpers
- **Booking System**: Token-based booking with real-time updates
- **Analytics**: Firebase Analytics integration
- **Push Notifications**: FCM integration
- **Dark/Light Theme**: System theme support
- **Beautiful UI**: Modern design with animations

### 👤 User Roles

#### Customer
- Browse salons
- View salon details and services
- Book services and get tokens
- Track token status in real-time
- View booking history

#### Salon Owner
- Create and manage salon profile
- Add/edit services
- Manage staff/helpers
- View token queue
- Track revenue and analytics
- Open/close salon status

#### Helper/Staff
- View assigned tokens
- Start and complete services
- Update availability status

#### Admin
- Full platform access
- Manage all salons and users

## 🚀 Setup Instructions

### Prerequisites
- Flutter 3.8.0 or higher
- Dart 3.0.0 or higher
- Firebase project
- Android Studio / Xcode (for mobile development)

### 1. Clone the Repository
```bash
git clone <repository-url>
cd shergillunisexsalloon
```

### 2. Install Dependencies
```bash
flutter pub get
```

### 3. Firebase Setup

#### Android
1. Download `google-services.json` from Firebase Console
2. Place it in `android/app/`
3. Update `android/build.gradle`:
   ```gradle
   dependencies {
       classpath 'com.google.gms:google-services:4.4.0'
   }
   ```
4. Update `android/app/build.gradle`:
   ```gradle
   apply plugin: 'com.google.gms.google-services'
   ```

#### iOS
1. Download `GoogleService-Info.plist` from Firebase Console
2. Place it in `ios/Runner/`
3. Update `ios/Podfile`:
   ```ruby
   platform :ios, '12.0'
   ```

### 4. Configure Firebase

1. Enable Authentication:
   - Phone Authentication
   - Google Sign-In

2. Create Firestore Database:
   - Start in test mode (then apply security rules from `FIREBASE_RULES.md`)

3. Enable Storage:
   - Create storage bucket
   - Apply security rules from `FIREBASE_RULES.md`

4. Enable Cloud Messaging:
   - Configure FCM for push notifications

5. Enable Analytics:
   - Analytics will work automatically

### 5. Add Assets

#### Images
Place images in `assets/images/`:
- `google_logo.png` (for Google Sign-In button)

#### Animations
Download Lottie animations from [LottieFiles](https://lottiefiles.com/) and place in `assets/animations/`:
- `onboarding_welcome.json`
- `success.json`
- `loading.json`
- `empty.json`

#### Fonts
Download Poppins font from [Google Fonts](https://fonts.google.com/specimen/Poppins) and place in `assets/fonts/`:
- `Poppins-Regular.ttf`
- `Poppins-Medium.ttf`
- `Poppins-SemiBold.ttf`
- `Poppins-Bold.ttf`

### 6. Run the App
```bash
flutter run
```

## 📁 Project Structure

```
lib/
├── core/
│   ├── constants/      # App constants
│   ├── theme/          # Theme configuration
│   └── utils/          # Utility functions
├── data/
│   ├── models/         # Data models
│   ├── repositories/   # Data repositories
│   └── services/       # Firebase services
├── presentation/
│   ├── auth/           # Authentication screens
│   ├── booking/        # Booking screens
│   ├── helpers/        # Helper management
│   ├── home/           # Home screens
│   ├── onboarding/     # Onboarding screens
│   ├── profile/        # Profile screens
│   ├── salon/          # Salon screens
│   ├── services/       # Service management
│   └── tokens/         # Token management
└── widgets/            # Reusable widgets
```

## 🔐 Security

Firebase Security Rules are provided in `FIREBASE_RULES.md`. Make sure to apply them in Firebase Console.

## 📱 Features in Detail

### Token System
- Automatic token number generation (S-001, S-002, etc.)
- Real-time status updates
- Estimated wait time calculation
- Automatic helper assignment

### Booking Flow
1. Customer selects salon
2. Views available services
3. Selects service
4. Receives token number
5. Tracks token status in real-time
6. Service completion

### Owner Dashboard
- Today's statistics
- Token queue management
- Revenue tracking
- Service and staff management

## 🛠️ Technologies Used

- **Flutter**: UI framework
- **Firebase Auth**: Authentication
- **Cloud Firestore**: Database
- **Firebase Storage**: File storage
- **Firebase Analytics**: Analytics
- **Firebase Cloud Messaging**: Push notifications
- **Provider**: State management
- **Lottie**: Animations
- **Google Fonts**: Typography
- **SharedPreferences**: Local storage

## 📝 Notes

- Payment integration is currently a placeholder (dummy implementation)
- Images use Unsplash URLs as placeholders - replace with actual images
- Lottie animations need to be downloaded and added to assets
- Google Sign-In requires proper OAuth configuration

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📄 License

This project is licensed under the MIT License.

## 👨‍💻 Author

Built with ❤️ using Flutter
