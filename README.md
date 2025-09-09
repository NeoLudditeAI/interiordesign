<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# Home Canvas - AI Interior Design Tool

An AI-powered interior design application that uses Google's Gemini AI to create photorealistic composite images. Simply upload a product image and a scene image, then drag the product onto any location in the scene. The AI will intelligently place the product with proper lighting, shadows, and perspective.

## Features

- 🎨 **AI-Powered Composition**: Uses Google Gemini 2.5 Flash models for realistic image generation
- 📱 **Multi-Platform Support**: Works on desktop (drag & drop) and mobile (touch gestures)
- 🔍 **Semantic Analysis**: AI analyzes placement locations contextually for better results
- 🛠️ **Debug Mode**: View the AI's analysis and prompts for transparency
- ⚡ **Real-time Processing**: Fast image generation with loading indicators
- 🎯 **Precise Placement**: Click or drag to place products exactly where you want them

## Demo

View the live demo: https://ai.studio/apps/bundled/home_canvas

## Run Locally

**Prerequisites:** Node.js 18+ and a Google Gemini API key

### Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/NeoLudditeAI/interiordesign.git
   cd interiordesign
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Get a Gemini API key:**
   - Visit [Google AI Studio](https://ai.google.dev/)
   - Create a new API key
   - Copy the key for the next step

4. **Configure environment:**
   Create a `.env.local` file in the root directory:
   ```bash
   echo "GEMINI_API_KEY=your_api_key_here" > .env.local
   ```
   Replace `your_api_key_here` with your actual Gemini API key.

5. **Run the development server:**
   ```bash
   npm run dev
   ```

6. **Open your browser:**
   Navigate to `http://localhost:5173`

### Quick Start

1. Upload a product image (furniture, decor, etc.)
2. Upload a scene image (room, space, etc.)
3. Drag the product onto the scene where you want it placed
4. Wait for the AI to generate a photorealistic composite
5. Use the debug button to see how the AI analyzed the placement

## Technology Stack

- **Frontend**: React 19 + TypeScript + Vite
- **AI Service**: Google Gemini API (`@google/genai`)
- **Styling**: Tailwind CSS
- **Image Processing**: Canvas API
- **Build Tool**: Vite

## How It Works

1. **Image Processing**: Images are resized to 1024x1024 with padding for consistent AI input
2. **Semantic Analysis**: AI analyzes the exact placement location and describes it contextually
3. **Image Generation**: AI creates a photorealistic composite with proper lighting, shadows, and perspective
4. **Post-Processing**: Generated image is cropped back to original aspect ratio

## Development

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build

### Project Structure

```
├── components/          # React components
│   ├── Header.tsx      # App header
│   ├── ImageUploader.tsx # File upload and drop zones
│   ├── ObjectCard.tsx  # Product display card
│   ├── DebugModal.tsx  # Debug information modal
│   └── TouchGhost.tsx  # Mobile touch interaction
├── services/           # API services
│   └── geminiService.ts # Gemini AI integration
├── assets/            # Sample images
├── types.ts           # TypeScript type definitions
└── App.tsx            # Main application component
```

## License

This project is licensed under the Apache 2.0 License - see the [LICENSE](LICENSE) file for details.

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Support

For issues and questions, please open an issue on GitHub or contact the development team.
