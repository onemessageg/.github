# OneMSG - Secure Messaging Platform

OneMSG is a production-grade, end-to-end encrypted messaging platform with native mobile apps for Android and iOS, built with modern technologies and security-first architecture.

## 🏗️ Project Architecture

```
OneMSG/
├── 📱 Mobile Apps
│   ├── android-app/          # Kotlin + Jetpack Compose
│   └── ios-app/              # Swift + SwiftUI
├── 🌐 Web App
│   └── apps/web/             # Next.js + TypeScript
├── 🔧 Backend Services
│   └── server/mobile-api/    # Node.js + TypeScript
├── 📦 Shared Packages
│   ├── packages/core/         # Shared business logic
│   └── packages/crypto/       # Cryptographic utilities
├── 🔐 Shared Schemas
│   ├── shared-schema/         # Protobuf + SQL Delight
│   └── design-tokens/         # Platform-agnostic design system
└── 🚀 CI/CD & DevOps
    ├── .github/workflows/     # GitHub Actions
    └── fastlane/              # Mobile deployment automation
```

## 🚀 Key Features

### 🔒 Security & Privacy
- **End-to-End Encryption**: Double Ratchet protocol with libsodium
- **Quantum-Resistant Encryption**: Hybrid encryption with post-quantum cryptography (Kyber-768) migration path
- **Screenshot Protection**: Advanced screenshot and screen recording detection with alerts
- **Sealed Sender**: Optional anonymous messaging
- **Key Transparency**: Merkle tree verification
- **Forward Secrecy**: Perfect forward secrecy guarantees
- **Zero-Knowledge**: Server cannot read message content

### 💬 Core Messaging
- **Real-time Chat**: WebSocket-based instant messaging
- **Message Types**: Text, images, files, stories, bot cards, payments
- **Message Scheduling**: Schedule messages for future delivery with time-zone support
- **Advanced Search**: Full-text search with filters, media search, and voice message transcription
- **Group Chats**: Encrypted group conversations with advanced moderation
- **Voice Transcription**: On-device voice-to-text with 50+ language support
- **Read Receipts**: Delivery and read status
- **Typing Indicators**: Real-time typing notifications

### 📱 Mobile-First Design
- **Native Performance**: Platform-optimized apps
- **Modern UI**: Jetpack Compose (Android) + SwiftUI (iOS)
- **Offline Support**: Local message storage and sync
- **Smart Notifications**: AI-powered priority inbox and notification management
- **Push Notifications**: Encrypted push delivery
- **Biometric Auth**: Fingerprint/Face ID integration

### 💾 Backup & Sync
- **Encrypted Backups**: Cloud or self-hosted backup options
- **Selective Backup**: Choose which conversations to backup
- **Incremental Sync**: Efficient sync across devices
- **Multi-Device Support**: Seamless sync across all your devices
- **Smart Media Management**: Auto-organize media with smart folders and storage optimization

### 🎯 User Experience Solutions
- **Solves Notification Overload**: AI-powered priority inbox and smart notifications
- **Advanced Search**: Find messages, media, and voice recordings instantly
- **Message Management**: Extended edit window, undo send, bulk actions
- **Group Management**: Threads, forum channels, advanced moderation tools
- **Privacy Controls**: Disappearing location, screenshot protection, forwarding restrictions

### 🎭 Multi-Persona Support
- **Work Profiles**: Separate work and personal accounts
- **Burner Accounts**: Quick temporary personas
- **Anonymous Mode**: Enhanced privacy features
- **Profile Switching**: Seamless persona management

### 💰 Integrated Wallet
- **Multi-Currency**: USD, EUR, BTC, ETH, ONE tokens
- **Secure Storage**: Hardware keystore integration
- **Payment Messages**: In-chat payments
- **Web3 Integration**: Ethereum and blockchain support

## 🛠️ Technology Stack

### Mobile Apps
- **Android**: Kotlin, Jetpack Compose, SQLDelight, Hilt
- **iOS**: Swift, SwiftUI, GRDB.swift, SwiftSodium
- **Shared**: Kotlin Multiplatform, Protobuf, SQL Delight

### Backend
- **API**: Node.js, TypeScript, Express, Socket.io
- **Database**: PostgreSQL, Redis
- **Authentication**: JWT, OAuth 2.0
- **Real-time**: WebSocket, Socket.io

### Web App
- **Frontend**: Next.js, React, TypeScript, Tailwind CSS
- **State Management**: Zustand, React Query
- **Styling**: Tailwind CSS, CSS Modules

### Infrastructure
- **Containerization**: Docker, Docker Compose
- **CI/CD**: GitHub Actions, Fastlane
- **Monitoring**: Sentry, Firebase Analytics
- **Security**: OWASP MASVS compliance

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- Docker & Docker Compose
- Android Studio (for Android development)
- Xcode 15+ (for iOS development)
- Protobuf compiler

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-org/onemsg.git
   cd onemsg
   ```

2. **Start backend services**
   ```bash
   docker-compose up -d
   ```

3. **Install dependencies**
   ```bash
   npm install
   cd apps/web && npm install
   cd ../../server/mobile-api && npm install
   ```

4. **Run the web app**
   ```bash
   cd apps/web
   npm run dev
   ```

5. **Open mobile apps**
   - **Android**: Open `android-app/` in Android Studio
   - **iOS**: Open `ios-app/OneMsg.xcodeproj` in Xcode

### Development Workflow

1. **Feature Development**
   ```bash
   git checkout -b feature/amazing-feature
   # Make changes
   git commit -m "Add amazing feature"
   git push origin feature/amazing-feature
   ```

2. **Mobile Development**
   ```bash
   # Android
   cd android-app
   ./gradlew assembleDebug
   
   # iOS
   cd ios-app
   xcodebuild -scheme OneMsg -destination 'platform=iOS Simulator,name=iPhone 15'
   ```

3. **Design Token Generation**
   ```bash
   cd design-tokens
   npm run generate-android
   npm run generate-ios
   ```

## 📱 Mobile App Development

### Android App
- **Architecture**: Clean Architecture + MVI pattern
- **UI Framework**: Jetpack Compose with Material 3
- **Dependency Injection**: Hilt
- **Database**: SQLDelight with Kotlin Multiplatform
- **Networking**: Retrofit + OkHttp with QUIC support
- **Crypto**: libsodium via JNI

### iOS App
- **Architecture**: Clean Architecture + MVI pattern
- **UI Framework**: SwiftUI with iOS design guidelines
- **Dependency Management**: Swift Package Manager
- **Database**: GRDB.swift with SQLCipher
- **Networking**: Network.framework with QUIC support
- **Crypto**: SwiftSodium

### Shared Components
- **Data Models**: Protobuf-generated classes
- **Database Schema**: SQL Delight shared between platforms
- **Design System**: Platform-agnostic design tokens
- **Crypto Engine**: Cross-platform cryptographic operations

## 🔐 Security Features

### Encryption
- **Double Ratchet**: Signal Protocol implementation
- **Perfect Forward Secrecy**: New keys for each message
- **Sealed Sender**: Optional sender anonymity
- **Key Transparency**: Verifiable key authenticity

### Privacy
- **Zero-Knowledge**: Server cannot access message content
- **Metadata Protection**: Minimal data collection
- **Anonymous Mode**: Enhanced privacy features
- **Local Storage**: Encrypted local message cache

### Compliance
- **GDPR**: European privacy regulation compliance
- **CCPA**: California privacy law compliance
- **SOC 2**: Security and availability controls
- **OWASP MASVS**: Mobile app security verification

## 🧪 Testing

### Test Coverage
- **Unit Tests**: >80% coverage target
- **Integration Tests**: API and database testing
- **UI Tests**: End-to-end user journey testing
- **Security Tests**: Penetration testing and vulnerability scanning

### Testing Tools
- **Android**: Kotest, Turbine, Compose-test-rule
- **iOS**: XCTest, Combine Schedulers, XCUITest
- **Web**: Jest, React Testing Library, Playwright
- **API**: Supertest, Jest

## 🚀 Deployment

### CI/CD Pipeline
- **GitHub Actions**: Automated testing and building
- **Fastlane**: Mobile app deployment automation
- **Docker**: Containerized deployment
- **Monitoring**: Automated health checks and rollbacks

### Release Process
1. **Development**: Feature development on feature branches
2. **Testing**: Automated testing and quality gates
3. **Staging**: Internal testing and QA validation
4. **Production**: Automated deployment with rollback capability

### Deployment Targets
- **Web**: Vercel/Netlify with preview deployments
- **Android**: Google Play Store (internal, beta, production)
- **iOS**: TestFlight and App Store
- **Backend**: Kubernetes clusters with auto-scaling

## 📊 Monitoring & Analytics

### Application Monitoring
- **Error Tracking**: Sentry for crash reporting
- **Performance**: APM tools for mobile and web
- **User Analytics**: Privacy-focused analytics
- **Security Monitoring**: Real-time threat detection

### Infrastructure Monitoring
- **Server Health**: CPU, memory, disk usage
- **Database Performance**: Query optimization and monitoring
- **Network Latency**: API response time tracking
- **Security Events**: Intrusion detection and alerting

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Development Guidelines
- Follow the established architecture patterns
- Write comprehensive tests for new features
- Ensure security best practices
- Update documentation for API changes

### Code Standards
- **Android**: ktlint + detekt
- **iOS**: SwiftLint
- **Web**: ESLint + Prettier
- **Backend**: ESLint + Prettier

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- **Documentation**: [Wiki](../../wiki)
- **Issues**: [GitHub Issues](../../issues)
- **Discussions**: [GitHub Discussions](../../discussions)
- **Security**: security@onemsg.com

## 🙏 Acknowledgments

- Signal Protocol for encryption standards
- libsodium for cryptographic primitives
- Jetpack Compose and SwiftUI teams
- Open source community contributors

---

**OneMSG** - Secure messaging for the modern world 🔐✨
