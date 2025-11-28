
# ArteIDEAS - Web Application

This project is a React-based e-commerce platform for personalized photo products (Frames, Prints, Collages), featuring advanced image editing capabilities and AI integration.

## 🚀 Features Implemented

### 1. UI/UX Design
- **Landing Page**: 
  - Custom gradient Hero section (Cyan to Orange).
  - Redesigned Product Cards for better visual impact (larger images, cleaner text).
  - Responsive Navigation Bar with persistent search and icons.
- **Brand Identity**: 
  - Consistent color palette using Orange (`#FF7F40`) and Teal (`#00A9C3`).
  - Removal of generic gradients in favor of solid brand colors for buttons and UI elements.

### 2. Product Customization Flow
- **Product Detail**: Detailed view with image galleries, pricing, and promotion badges.
- **Customizer**: 
  - File upload drag-and-drop interface.
  - **Dynamic Cropping**: Draggable crop overlay that adapts to selected print formats (e.g., 10x15, 13x18).
  - **Format & Paper Selection**: Logic to calculate prices based on size and paper type (Matte/Glossy).
  - **Validation**: Prevents adding to cart without required fields (Image, Paper Type, Project Name).

### 3. Advanced Image Editing
- **Manual Editor**:
  - Brightness, Contrast, and Saturation sliders with custom-styled range inputs.
  - Client-side image processing using HTML Canvas.
- **AI Editor (Gemini API)**:
  - Integrated `gemini-2.5-flash-image` model.
  - **Chat Interface**: Users can instruct the AI to modify images (e.g., "Add a hat", "Change background") via natural language.
  - **Version History**: Strip of thumbnails allowing users to revert to previous versions of the AI edits.
  - Optimized layout for both mobile (vertical stack) and desktop.

### 4. Cart & Checkout Process
- **Shopping Cart**:
  - Quantity management and item removal.
  - Real-time subtotal calculation.
- **Checkout**:
  - **Delivery Options**: Toggle between "Home Delivery" (dynamic fee) and "Store Pickup" (Free).
  - **Validation**: Strict rules for Phone/DNI (9 digits only) and Email format.
  - **Store Info**: Displays store address and map when Pickup is selected.
- **Payment**:
  - **Input Formatting**: Auto-spacing for Credit Card numbers (groups of 4) and Expiry Date (MM/YY).
  - Summary of the final order total.

### 5. Order Management
- **Order Confirmation**: Success screen with "What's Next" steps and summary.
- **My Orders**:
  - Order history accessible via the Box icon in the header.
  - Displays order status badges (e.g., "Processing").
  - "View Details" functionality to revisit the confirmation receipt of past orders.

## 🛠 Technologies Used
- **Frontend**: React 19, TypeScript
- **Styling**: Tailwind CSS
- **Icons**: Lucide React
- **AI**: @google/genai SDK
- **State Management**: React `useState` & `useRef`

## 📦 Data Structure
- **Cart**: Persists items with specific customization options.
- **Orders**: In-memory history of confirmed purchases.
- **Validation**: Regex patterns for form integrity.
