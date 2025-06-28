# 🤚 Hand Gesture Website Navigator

> **Navigate the web with just your hands!** A revolutionary browser-based application that uses computer vision to detect hand gestures and automatically redirect you to your favorite websites.

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![MediaPipe](https://img.shields.io/badge/Powered%20by-MediaPipe-blue)](https://mediapipe.dev/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![HTML5](https://img.shields.io/badge/HTML5-Canvas-orange)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)

---

## 🚀 **What is Hand Gesture Navigator?**

Hand Gesture Navigator is a cutting-edge web application that transforms how you interact with the internet. Simply show different hand gestures to your camera, and watch as the system automatically detects them and navigates you to corresponding websites. No clicks, no typing – just pure hand gesture magic!

### 🎯 **Perfect for:**
- **Accessibility** - Hands-free web navigation for users with mobility limitations
- **Presentations** - Navigate seamlessly during live demos without touching devices
- **Cool Factor** - Impress friends and colleagues with futuristic web interaction
- **Efficiency** - Lightning-fast access to your most-used websites

---

## ✨ **Features**

### 🔥 **Core Functionality**
- **Real-time Hand Detection** - Powered by Google's MediaPipe for accurate finger tracking
- **5 Gesture Recognition** - One through five fingers for different websites
- **Instant Navigation** - 2-second confirmation prevents accidental triggers
- **Visual Feedback** - Live hand skeleton overlay and gesture indicators

### 🎨 **User Experience**
- **Modern UI Design** - Beautiful gradient backgrounds and glassmorphism effects
- **Responsive Layout** - Works perfectly on desktop, tablet, and mobile devices
- **Real-time Feedback** - Visual countdown and detection confirmations
- **Error Handling** - Graceful camera permission and error management

### ⚡ **Performance**
- **Browser-based** - No installation required, runs directly in your web browser
- **Lightweight** - Optimized for smooth real-time performance
- **Cross-platform** - Compatible with Chrome, Firefox, Safari, and Edge

---

## 🎮 **How It Works**

| Gesture | Fingers Extended | Destination | Use Case |
|---------|------------------|-------------|----------|
| 👆 | **1 Finger** | YouTube | Entertainment & Learning |
| ✌️ | **2 Fingers** | Instagram | Social Media |
| 🤟 | **3 Fingers** | Twitter/X | News & Updates |
| 🖖 | **4 Fingers** | Google | Search & Research |
| 🖐️ | **5 Fingers** | GitHub | Development & Code |

### 🔄 **Simple Workflow**
1. **Click "Start Camera"** to initialize the system
2. **Allow camera permissions** when prompted
3. **Show your hand gesture** clearly to the camera
4. **Hold steady for 2 seconds** while the countdown runs
5. **Automatic navigation** to your chosen website!

---

## 🛠️ **Quick Start**

### **Option 1: Direct Access**
Simply open the `index.html` file in any modern web browser - that's it! No installation required.

### **Option 2: Local Server (Recommended)**
For the best experience with camera permissions:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js
npx http-server

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000` in your browser.

### **Prerequisites**
- Modern web browser (Chrome 90+, Firefox 88+, Safari 14+, Edge 90+)
- Webcam or built-in camera
- HTTPS connection (for camera access in production)

---

## 🔧 **Technical Architecture**

### **Core Technologies**
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Computer Vision**: Google MediaPipe Hands
- **Camera Access**: WebRTC getUserMedia API
- **Real-time Processing**: Canvas API for rendering

### **Key Components**

```javascript
// Core gesture detection algorithm
detectGesture(landmarks) {
    const fingerTips = [4, 8, 12, 16, 20];  // Landmark indices
    const fingerPIPs = [3, 6, 10, 14, 18];  // Joint indices
    
    let extendedFingers = 0;
    // Finger extension detection logic...
    
    return gestureMapping[extendedFingers];
}
```

### **Performance Optimizations**
- **Efficient landmark processing** with optimized finger counting algorithms
- **Debounced gesture detection** to prevent false positives
- **Canvas-based rendering** for smooth 60fps hand tracking visualization
- **Memory management** with proper cleanup of intervals and event listeners

---

## 🎨 **Customization**

### **Adding New Websites**
Easily customize the website destinations by modifying the `websites` object:

```javascript
this.websites = {
    'one': 'https://your-favorite-site.com',
    'two': 'https://another-site.com',
    // Add more mappings...
};
```

### **Adjusting Gesture Sensitivity**
Fine-tune detection parameters in the MediaPipe configuration:

```javascript
this.hands.setOptions({
    maxNumHands: 1,
    modelComplexity: 1,
    minDetectionConfidence: 0.7,  // Increase for stricter detection
    minTrackingConfidence: 0.5
});
```

### **Styling Customization**
- Modify CSS variables for colors and themes
- Adjust countdown timing and visual effects
- Customize hand skeleton visualization colors

---

## 🚀 **Deployment**

### **GitHub Pages**
1. Push your code to a GitHub repository
2. Go to Settings → Pages
3. Select source branch (usually `main`)
4. Your app will be available at `https://yourusername.github.io/repository-name`

### **Netlify**
1. Connect your GitHub repository to Netlify
2. Deploy with default settings
3. Automatic HTTPS and custom domain support

### **Vercel**
```bash
npm i -g vercel
vercel --name hand-gesture-navigator
```

---

## 🤝 **Contributing**

We welcome contributions! Here's how you can help:

### **🐛 Bug Reports**
- Use the GitHub Issues tab
- Include browser version and error details
- Provide steps to reproduce the issue

### **✨ Feature Requests**
- Suggest new gesture patterns
- Propose additional website integrations
- Request accessibility improvements

### **🔧 Development Setup**
```bash
git clone https://github.com/yourusername/hand-gesture-navigator.git
cd hand-gesture-navigator
# No build process needed - open index.html!
```

### **Pull Request Guidelines**
1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Make your changes and test thoroughly
4. Submit a pull request with a clear description

---

## 🔒 **Privacy & Security**

### **Camera Privacy**
- **Local Processing**: All hand detection happens locally in your browser
- **No Data Transmission**: Camera feed never leaves your device
- **Permission Control**: Full user control over camera access
- **No Storage**: No images or video data is stored anywhere

### **Open Source Transparency**
- Complete source code available for inspection
- No hidden tracking or analytics
- MIT License ensures freedom to modify and distribute

---

## 🎯 **Roadmap**

### **Version 2.0 Features**
- [ ] **Custom Gesture Training** - Train your own hand poses
- [ ] **Voice Commands Integration** - Combine gestures with voice
- [ ] **Mobile App Version** - Native iOS and Android apps
- [ ] **Gesture Macros** - Chain multiple gestures for complex actions

### **Advanced Features**
- [ ] **Multi-hand Detection** - Use both hands for more gestures
- [ ] **Gesture History** - Track and analyze usage patterns
- [ ] **Cloud Sync** - Sync preferences across devices
- [ ] **Plugin System** - Extensible architecture for third-party gestures

---

## 📊 **Browser Compatibility**

| Browser | Version | Status | Notes |
|---------|---------|--------|--------|
| Chrome | 90+ | ✅ Full Support | Recommended |
| Firefox | 88+ | ✅ Full Support | Great performance |
| Safari | 14+ | ✅ Full Support | iOS 14.3+ |
| Edge | 90+ | ✅ Full Support | Chromium-based |
| Mobile | Various | ⚠️ Limited | Camera orientation issues |

---

## 📄 **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

---

## 🙏 **Acknowledgments**

- **Google MediaPipe Team** - For the incredible hand tracking technology
- **Web Standards Community** - For WebRTC and Canvas API specifications
- **Open Source Contributors** - For inspiration and code references
- **Accessibility Advocates** - For promoting inclusive web design

---

## 📞 **Support & Contact**

### **Get Help**
- 📚 [Documentation](https://github.com/yourusername/hand-gesture-navigator/wiki)
- 🐛 [Report Issues](https://github.com/yourusername/hand-gesture-navigator/issues)
- 💬 [Discussions](https://github.com/yourusername/hand-gesture-navigator/discussions)

### **Connect With Us**
- 🐦 [Twitter](https://twitter.com/yourusername)
- 💼 [LinkedIn](https://linkedin.com/in/yourusername)
- 📧 [Email](mailto:your.email@example.com)

---

<div align="center">

**⭐ Star this project if you found it useful!**

*Made with ❤️ and cutting-edge web technologies*

[⬆ Back to Top](#-hand-gesture-website-navigator)

</div>
