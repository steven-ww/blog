# Personal Blog with HTMX

A modern, lightweight blog implementation using HTMX for dynamic content loading without complex JavaScript frameworks.

## Tech Stack

- **HTMX** (v2.0.4) - For dynamic HTML content updates
- **Node.js** with lite-server (v2.6.1) - For local development
- **HTML5/CSS3** - For structure and styling
- **NPM** - Package management

## Features

- Dynamic content loading without full page refreshes
- Responsive design
- Blog post management
- About page
- Featured posts section

## Prerequisites

- Node.js (Latest LTS version recommended)
- NPM (Comes with Node.js)

## Installation

1. Clone the repository:
```
bash git clone [repository-url] cd [repository-name]
```
2. Install dependencies:
```
bash npm install
```
## Running Locally

To start the development server:
```
bash npm start
```
This will start lite-server and open your default browser to `http://localhost:3000`.

## Project Structure
```
├── assets/ # Images and other static assets 
├── posts/ # Blog post HTML files 
├── index.html # Main entry point 
├── style.css # Global styles 
├── about.html # About page 
└── package.json # Project configuration and dependencies
```

## Development

The project uses HTMX for dynamic content loading. Key features:
- Content is loaded dynamically using HTMX attributes
- No complex JavaScript setup required
- Pages update seamlessly without full refreshes

### Adding New Blog Posts

1. Create a new HTML file in the `posts` directory (e.g., `my-new-post.html`)
2. Follow the established HTML structure for blog posts
3. Update `posts/featured.html` to include your new post:
   ```html
   <article class="blog-post">
       <h2>Your New Post Title</h2>
       <p class="post-meta">Date</p>
       <div class="post-excerpt">
           Brief excerpt from your post
       </div>
       <a href="#" 
          hx-get="/posts/my-new-post.html" 
          hx-target="#content" 
          class="read-more">Read More</a>
   </article>
   ```
4. Add necessary HTMX attributes for dynamic loading in both files

Note: The `featured.html` file serves as an index/listing for your blog posts. Each new post must be added here to appear in the featured posts section on the main page.
## Deployment

### Current Status
The project is configured for deployment to AWS S3. Deployment setup is pending.

### Planned Deployment Steps
1. Create an S3 bucket for static website hosting
2. Configure bucket policy for public access
3. Set up CloudFront distribution (optional, for CDN)
4. Configure CI/CD pipeline for automated deployments

### Future Deployment Tasks
- [X] Configure S3 bucket
- [X] Set up domain and DNS
- [ ] Implement deployment automation
- [X] Configure HTTPS with CloudFront

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
