# 🛒 Grocery Price Tracker Pro

  A smart, mobile-friendly web app that helps you track and compare grocery prices across different stores. Built
  with AI-powered item matching to help you find the best deals!

  ## 🌟 Features

  ### Core Functionality
  - **Price Tracking**: Record item prices from multiple stores with unit price calculations
  - **Smart Comparisons**: Automatically compare prices across stores for the same items
  - **Barcode Scanner**: Scan product barcodes using your phone's camera (HTTPS required)
  - **Flexible Units**: Support for both weight and fluid measurements
    - Weight: kg, lb, 100g, g
    - Fluids: L (liter), mL (milliliter), fl oz (fluid ounce), gal (gallon)
  - **Optional Fields**: All input fields are optional - track as much or as little as you want
  - **Local Storage**: All data saved locally on your device - no server required

  ### AI-Powered Features
  - **Smart Item Matching**: AI detects similar items with different names (e.g., "Rib Steak" vs "Ribeye Steak")
  - **Auto-Linking**: Suggests linking similar products for easy price comparison
  - **Secure API Key Storage**: Your Anthropic API key is encrypted with AES-256 and PIN-protected
  - **Configurable Auto-Lock**: Choose when your API key auto-locks (5 min to never)

  ### Mobile Optimized
  - Responsive design works perfectly on phones and tablets
  - Bottom navigation for easy thumb access
  - Camera integration for barcode scanning
  - Touch-friendly interface

  ## 🚀 How to Use

  ### Access the App
  Simply open the app in your browser:
  - **Live Demo**: `https://terminallychiill.github.io/Grocery/Grocery.html`
  - **Local**: Open `grocery-price-tracker-pro.html` in any modern browser

  ### Adding Items
  1. Tap the **➕ Add** button
  2. (Optional) Scan a barcode or enter item details manually
  3. Fill in any combination of:
     - Item name (e.g., "Gala Apples", "Milk 2%")
     - Store name (e.g., "Costco", "Walmart")
     - Total price paid
     - Weight/volume and unit
  4. The app automatically calculates unit price for easy comparison
  5. Tap **Add Item**

  ### Comparing Prices
  1. The app automatically groups items you've linked
  2. Tap any grouped item badge to see price comparison
  3. See which store has the best price instantly
  4. View savings vs. other stores

  ### Using AI Features (Optional)
  1. Go to **⚙️ Settings**
  2. Get a free Anthropic API key (includes $5 free credit = thousands of checks!)
     - Visit [console.anthropic.com](https://console.anthropic.com)
     - Sign up and copy your API key
  3. Enter your API key and create a 6-digit PIN
  4. Choose your auto-lock preference
  5. When adding items, AI will automatically suggest matching items to link

  ## 🔒 Security & Privacy

  - **100% Local**: All your grocery data stays on your device
  - **Encrypted API Key**: Uses AES-256 encryption with PBKDF2 key derivation
  - **PIN Protection**: Your API key is protected by a 6-digit PIN
  - **Session Storage**: Decrypted key only stored temporarily during use
  - **No Tracking**: No analytics, no data collection, no servers

  ## 📱 Camera/Barcode Requirements

  The barcode scanner requires **HTTPS** to access your camera due to browser security policies:
  - ✅ Works: GitHub Pages, Netlify, Vercel, or any HTTPS hosting
  - ❌ Won't work: Opening file directly (file://) or HTTP servers
  - 💡 Tip: Bookmark the GitHub Pages URL on your phone for easy access

  ## 🛠️ Technical Details

  ### Technologies Used
  - **React 18**: UI framework (loaded via CDN)
  - **Tailwind CSS**: Styling
  - **html5-qrcode**: Barcode scanning library
  - **Web Crypto API**: Secure encryption
  - **LocalStorage**: Data persistence
  - **Anthropic Claude API**: AI-powered item matching

  ### Browser Compatibility
  - Chrome/Edge (recommended for Android)
  - Safari (iOS)
  - Samsung Internet
  - Any modern browser with JavaScript enabled

  ### Data Structure
  All data is stored in your browser's localStorage:
  ```javascript
  {
    itemName: string,
    store: string,
    totalPrice: number,
    weight: number,
    unit: string,
    unitPrice: number,
    barcode: string (optional),
    linkedGroup: number (optional),
    id: number
  }

  📝 Tips for Best Results

  1. Be Consistent: Try to use similar naming across stores for better AI matching
  2. Use Barcodes: Scanning barcodes helps ensure you're comparing the exact same product
  3. Check Units: Make sure you're comparing the same units (kg vs lb, L vs mL)
  4. Update Prices: Prices change! Update your entries when you shop
  5. Link Items: Link similar items together to see price comparisons instantly

  🤝 Contributing

  Found a bug or have a feature request? This is an open-source project - feel free to:
  - Report issues
  - Submit pull requests
  - Fork and customize for your needs

  📄 License

  This project is free to use, modify, and distribute.

  🙋 FAQ

  Q: Do I need an internet connection?
  A: Only for the AI features. Basic price tracking works 100% offline.

  Q: How much does the AI cost?
  A: Anthropic gives $5 free credit (thousands of AI checks). After that, it's pay-as-you-go but very cheap.

  Q: Can I export my data?
  A: Currently data is stored in browser localStorage. Export feature coming soon!

  Q: Why won't the camera work?
  A: The camera requires HTTPS. Use the GitHub Pages link instead of opening the file directly.

  Q: Is my data shared anywhere?
  A: Nope! Everything stays on your device. The only external call is to Anthropic's API if you use AI features.

  ---
  Happy savings! 💰
