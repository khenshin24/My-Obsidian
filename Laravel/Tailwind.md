
```css
How to Install Tailwind
	npm install tailwindcss @tailwindcss/vite
	
	vite.config.ts
			import { defineConfig } from 'vite'
			import tailwindcss from '@tailwindcss/vite'
			
			export default defineConfig({
			  plugins: [
			    tailwindcss(),
			  ],
			})
			
	 resource/app/app.css
	 @import "tailwindcss";

	 resource/app/app.js
	 import '../css/app.css';
	 
	 npm run build
	 npm run dev
	 
	 add this in head of your index.blade.php
	 @vite(['resources/css/app.css', 'resources/js/app.js'])
```


