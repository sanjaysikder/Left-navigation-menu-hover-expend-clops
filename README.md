# Oracle APEX Left Navigation Menu Hover Expand/Collapse Implementation

This guide explains how to implement hover-based expand/collapse functionality for the left navigation menu in Oracle APEX using a custom JavaScript file.

## Prerequisites
- Oracle APEX 18.1 or higher
- Access to Application Shared Components
- Navigation Menu component in your application

## Implementation Steps

### Step 1: Upload JavaScript File to Application Static Files
1. Download the JavaScript file (`menu_nav.main.js`) from this repository
2. In your APEX application:
   - Navigate to **Shared Components** > **Static Application Files**
   - Click **Upload File**
   - Select the `menu_nav.main.js` file
   - Click **Upload**

### Step 2: Configure JavaScript File URL
1. Navigate to **Shared Components** > **User Interfaces**
2. Select your user interface (e.g., "Desktop")
3. Under the **JavaScript** section:
   - Locate **File URLs**
   - Add the following URL (replace `APP_FILES` with your workspace name):
     ```
     #APP_FILES#menu_nav.main.js
     ```
   - Click **Apply Changes**

### Step 3: Configure Navigation Menu Template
1. Navigate to **Shared Components** > **Navigation Menu**
2. Select your navigation menu (e.g., "Desktop Navigation Menu")
3. Under the **Template Options** section:
   - Locate **Collapse Mode**
   - Set the value to **Icons**
4. Click **Apply Changes**

## How It Works
The JavaScript file adds event listeners to the navigation menu items:
- On mouse hover (`mouseenter`), submenus expand automatically
- On mouse leave (`mouseleave`), submenus collapse automatically
- Uses APEX's built-in CSS classes (`t-Nav-listItem--isExpanded`) for seamless integration
- Includes a MutationObserver to handle dynamic content updates

## Thank You
