# MovieLand

A lightweight React application that allows users to search and browse movies using the [OMDB API](http://www.omdbapi.com/).

## 📁 Project Structure

```
MovieLand/
├─ public/
│  ├─ index.html
│  ├─ manifest.json
│  └─ robots.txt
├─ src/
│  ├─ App.css
│  ├─ App.js
│  ├─ index.js
│  └─ MovieCard.jsx
├─ .env           # contains REACT_APP_OMDB_API_KEY (ignored by git)
├─ package.json
└─ README.md
```

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd MovieLand
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up API key**
   - Create a `.env` file in the project root (it's already ignored via `.gitignore`).
   - Add your OMDB key:
     ```env
     REACT_APP_OMDB_API_KEY=your_api_key_here
     ```
   - Restart the dev server if it is running.

4. **Run the development server**
   ```bash
   npm run dev
   ```

5. **Open in browser**
   Visit `http://localhost:3000` (or the port shown by the terminal) to see the app.

## 🧩 How it works

- The app uses `fetch` to query the OMDB API via the `searchMovies` helper.
- `App.js` stores results in component state and renders a list of `MovieCard` components.
- Search input updates state and triggers a new fetch on change or when the search icon is clicked.
- An initial query ("Batman" by default) loads on mount so the UI isn't empty.

## 🔧 Customization

- Change the default search term by editing `searchTerm` or the `useEffect` call in `App.js`.
- Style modifications can be made in `App.css` or by adjusting the markup.

## ✅ Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start the development server |
| `npm run build` | Build the app for production |
| `npm test` | Run tests (if configured) |

## 📦 Deployment

Build for production and serve the contents of the `/build` directory using a static server or hosting provider like Netlify, Vercel, GitHub Pages, etc.

## 📝 Notes

- Keep your `.env` file secret; do not commit it!
- The OMDB API has usage limits; refer to their documentation for details.

---

Made with React. Happy movie hunting! 🎬
