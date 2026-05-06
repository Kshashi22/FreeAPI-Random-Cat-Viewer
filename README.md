
# FreeAPI: Random Cat Viewer

A simple web application that fetches and displays random cat images from a free public API. This project demonstrates API integration, asynchronous JavaScript, and dynamic image rendering in a web interface.

---

## Features

* Fetch random cat images from a public API
* Display images dynamically on the UI
* Load a new cat image on demand
* Responsive and user-friendly interface
* Lightweight and fast performance

---

## Tech Stack

* Frontend: HTML, CSS, JavaScript
* API: Free public cat image API (e.g., The Cat API)
* Tools: VS Code, Git, Browser DevTools

---

## Project Structure

```
FreeAPI-Random-Cat-Viewer/
│── index.html
│── style.css
│── script.js
│── README.md
```

---

## Installation and Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/FreeAPI-Random-Cat-Viewer.git
   ```

2. Navigate to the project directory:

   ```bash
   cd FreeAPI-Random-Cat-Viewer
   ```

3. Open the `index.html` file in your browser

---

## API Integration

Example API used:

```
https://api.thecatapi.com/v1/images/search
```

### Fetch Example

```javascript
fetch('https://api.thecatapi.com/v1/images/search')
  .then(response => response.json())
  .then(data => console.log(data));
```

---

## How It Works

1. The application sends a request to the cat image API
2. The API returns image data in JSON format
3. The application extracts the image URL
4. The image is displayed dynamically on the webpage

---

## Future Improvements

* Add image download functionality
* Add favorites or save feature
* Include image categories or breeds filtering
* Add loading animations
* Improve UI/UX design

---

## Contributing

Contributions are welcome.

1. Fork the repository
2. Create a new branch
3. Commit your changes
4. Submit a pull request


## Acknowledgements

* Public APIs providing free cat images
* Open-source community for tools and inspiration


