# 🎬 Degrees of Separation - Movie Database

A modern, interactive web application that finds the shortest connection between any two actors through their shared movies. Based on the famous "Six Degrees of Kevin Bacon" game, this tool visualizes the relationships between Hollywood actors through their filmographies.

## 🌟 Features

- **Interactive Web Interface**: Modern, responsive design with smooth animations
- **Real-time Search**: Find connections between actors instantly
- **Visual Path Display**: Step-by-step visualization of actor connections through movies
- **Comprehensive Database**: 35+ popular actors and 129+ movies with real filmography data
- **Mobile-Friendly**: Responsive design that works on all devices
- **Error Handling**: Graceful handling of missing actors and no-connection scenarios
- **Loading States**: Smooth user experience with animated loading indicators

## 🎭 Actor Database

The application includes a comprehensive database of popular actors including:

### Marvel Cinematic Universe
- Chris Evans, Robert Downey Jr., Chris Hemsworth, Mark Ruffalo, Scarlett Johansson

### Hollywood A-List
- Leonardo DiCaprio, Brad Pitt, Tom Hanks, Meryl Streep, Will Smith, Jennifer Lawrence

### Action Stars
- Hugh Jackman, Ryan Reynolds, Tom Cruise, Harrison Ford, Charlize Theron

### Drama Icons
- Denzel Washington, Morgan Freeman, Christian Bale, Matt Damon, Samuel L. Jackson

### Leading Ladies
- Julia Roberts, Sandra Bullock, Angelina Jolie, Natalie Portman, Cate Blanchett, Emma Stone, Anne Hathaway

### Legendary Performers
- Robert De Niro, Al Pacino, Johnny Depp, Kevin Bacon, George Clooney, Benedict Cumberbatch

## 🚀 How to Use

1. **Open the HTML file** in any modern web browser
2. **Enter two actor names** in the input fields
3. **Click "Find Connection"** or press Enter
4. **View the results** showing the degrees of separation and connection path

### Example Searches

Try these interesting connections:
- `Kevin Bacon` → `Tom Hanks` (Apollo 13)
- `Leonardo DiCaprio` → `Brad Pitt` (Once Upon a Time in Hollywood)  
- `Chris Evans` → `Robert Downey Jr.` (Avengers series)
- `Ryan Gosling` → `Emma Stone` (La La Land)
- `Morgan Freeman` → `Christian Bale` (The Dark Knight)

## 🏗️ Technical Implementation

### Frontend
- **HTML5/CSS3**: Modern responsive design with CSS Grid and Flexbox
- **Vanilla JavaScript**: No external dependencies for core functionality
- **BFS Algorithm**: Breadth-First Search for finding shortest paths
- **Real-time Processing**: Client-side computation for instant results

### Data Structure
```javascript
people: {
  id: {
    name: "Actor Name",
    birth: "Year", 
    movies: Set([movie_ids])
  }
}

movies: {
  id: {
    title: "Movie Title",
    year: "Year",
    stars: Set([person_ids])
  }
}
```

### Algorithm
- Uses **Breadth-First Search (BFS)** to find the shortest path
- Implements a **queue-based frontier** for systematic exploration
- Tracks **explored nodes** to avoid cycles
- Returns **movie-actor pairs** representing the connection path

## 📁 File Structure

```
degrees-of-separation/
├── index.html          # Main application file
├── README.md          # This documentation
└── degrees.py         # Original Python implementation (reference)
```

## 🎨 Design Features

- **Glassmorphism UI**: Modern design with blur effects and transparency
- **Gradient Backgrounds**: Beautiful color transitions
- **Smooth Animations**: Hover effects and loading states
- **Responsive Layout**: Adapts to different screen sizes
- **Interactive Elements**: Touch-friendly buttons and inputs

## 🔧 Customization

### Adding New Actors
```javascript
people['new_id'] = {
  name: 'Actor Name',
  birth: 'Birth Year',
  movies: new Set(['movie_id_1', 'movie_id_2'])
};
```

### Adding New Movies
```javascript
movies['new_movie_id'] = {
  title: 'Movie Title',
  year: 'Release Year',
  stars: new Set(['actor_id_1', 'actor_id_2'])
};
```

### Styling Modifications
- Modify CSS variables in the `<style>` section
- Update color schemes by changing gradient definitions
- Adjust animations by modifying `@keyframes` rules

## 🚀 Integration with Real Data

To integrate with actual CSV data (like the original Python version):

1. **Replace Sample Data**: Substitute the `sampleData` object with your actual data
2. **Add File Upload**: Implement CSV file upload functionality
3. **Data Processing**: Use libraries like PapaParse to process CSV files
4. **Server Integration**: Connect to a backend API for larger datasets

### CSV Data Format Expected
- `people.csv`: id, name, birth
- `movies.csv`: id, title, year  
- `stars.csv`: person_id, movie_id

## 🎯 Use Cases

- **Educational Tool**: Learn about graph theory and BFS algorithms
- **Entertainment**: Play the "Six Degrees" game with friends
- **Film Research**: Explore connections between actors and movies
- **Network Analysis**: Visualize relationships in the entertainment industry

## 🐛 Known Limitations

- **Static Data**: Currently uses hardcoded sample data
- **Memory Usage**: All data stored in browser memory
- **Single Language**: English names and titles only
- **Limited Database**: Subset of actors compared to full IMDb

## 🛠️ Browser Compatibility

- **Chrome** 60+ ✅
- **Firefox** 55+ ✅  
- **Safari** 12+ ✅
- **Edge** 79+ ✅

## 📱 Mobile Support

Fully responsive design tested on:
- iOS Safari
- Android Chrome
- Mobile Firefox

## 🎓 Algorithm Explanation

The application uses the **Breadth-First Search (BFS)** algorithm to find the shortest path:

1. **Initialize**: Start with the source actor in a queue
2. **Explore**: For each actor, find all co-stars from shared movies
3. **Track**: Mark explored actors to avoid revisiting
4. **Goal Check**: Stop when target actor is found
5. **Reconstruct**: Build the path by tracing back through parents

This guarantees finding the **shortest possible connection** between any two actors.

## 🤝 Contributing

To extend this project:

1. **Add More Actors**: Expand the database with additional filmographies
2. **Improve UI**: Enhance the visual design and user experience  
3. **Add Features**: Implement filters, search suggestions, or statistics
4. **Optimize Performance**: Improve algorithms for larger datasets
5. **Mobile App**: Convert to a native mobile application

## 📄 License

This project is open source and available under the MIT License.

## 🙏 Credits

- **Original Concept**: "Six Degrees of Kevin Bacon" parlor game
- **Algorithm**: Based on graph theory and BFS pathfinding
- **Movie Data**: Compiled from public film information
- **Design Inspiration**: Modern web design trends and glassmorphism

---

**Enjoy exploring the connections between your favorite actors!** 🎭✨
