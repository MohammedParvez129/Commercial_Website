# Ex02 Commercial Website
## Date: 10-05-2026

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ProBiz - Professional Business Solutions</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
        }

        /* Header & Navigation */
        header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            transition: opacity 0.3s ease;
        }

        nav a:hover {
            opacity: 0.8;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 6rem 2rem;
            display: flex;
            align-items: center;
            justify-content: center;
            min-height: 600px;
        }

        .hero-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 4rem;
            max-width: 1200px;
            width: 100%;
        }

        .hero-text {
            flex: 1;
        }

        .hero-text h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            line-height: 1.2;
        }

        .hero-text p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.95;
        }

        .hero-image {
            flex: 1;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            height: 400px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
        }

        .cta-button {
            display: inline-block;
            background: white;
            color: #667eea;
            padding: 0.8rem 2rem;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        /* Services Section */
        .services {
            padding: 4rem 2rem;
            background: #f8f9fa;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }

        .services-grid {
            display: flex;
            gap: 2rem;
            flex-wrap: wrap;
            justify-content: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .service-card {
            flex: 1;
            min-width: 280px;
            background: white;
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .service-card h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: #667eea;
        }

        .service-card p {
            color: #666;
            line-height: 1.8;
        }

        /* Features Section */
        .features {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .features-content {
            display: flex;
            gap: 3rem;
            align-items: center;
            margin-bottom: 4rem;
        }

        .features-content:nth-child(even) {
            flex-direction: row-reverse;
        }

        .feature-image {
            flex: 1;
            background: #667eea;
            border-radius: 10px;
            height: 300px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .feature-text {
            flex: 1;
        }

        .feature-text h2 {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: #333;
        }

        .feature-text p {
            color: #666;
            margin-bottom: 1.5rem;
            line-height: 1.8;
        }

        .feature-list {
            list-style: none;
        }

        .feature-list li {
            padding: 0.5rem 0;
            padding-left: 2rem;
            position: relative;
            color: #333;
        }

        .feature-list li:before {
            content: "✓";
            position: absolute;
            left: 0;
            color: #667eea;
            font-weight: bold;
            font-size: 1.2rem;
        }

        /* Testimonials Section */
        .testimonials {
            background: #f8f9fa;
            padding: 4rem 2rem;
        }

        .testimonials-grid {
            display: flex;
            gap: 2rem;
            flex-wrap: wrap;
            justify-content: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .testimonial-card {
            flex: 1;
            min-width: 300px;
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .stars {
            color: #ffc107;
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }

        .testimonial-text {
            color: #666;
            margin-bottom: 1.5rem;
            font-style: italic;
            line-height: 1.8;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: #667eea;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }

        .author-info h4 {
            color: #333;
            margin-bottom: 0.3rem;
        }

        .author-info p {
            color: #999;
            font-size: 0.9rem;
        }

        /* Pricing Section */
        .pricing {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .pricing-grid {
            display: flex;
            gap: 2rem;
            flex-wrap: wrap;
            justify-content: center;
        }

        .pricing-card {
            flex: 1;
            min-width: 280px;
            border: 2px solid #ddd;
            border-radius: 10px;
            padding: 2rem;
            text-align: center;
            transition: transform 0.3s ease, border-color 0.3s ease;
        }

        .pricing-card:hover {
            transform: scale(1.05);
            border-color: #667eea;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }

        .pricing-card.featured {
            border-color: #667eea;
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.05), rgba(118, 75, 162, 0.05));
        }

        .price {
            font-size: 2.5rem;
            color: #667eea;
            margin: 1rem 0;
            font-weight: bold;
        }

        .price span {
            font-size: 1rem;
            color: #999;
        }

        .pricing-features {
            list-style: none;
            text-align: left;
            margin: 2rem 0;
        }

        .pricing-features li {
            padding: 0.8rem 0;
            border-bottom: 1px solid #eee;
            color: #666;
        }

        /* CTA Section */
        .cta-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 4rem 2rem;
            text-align: center;
        }

        .cta-section h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .cta-section p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.95;
        }

        /* Footer */
        footer {
            background: #2d3436;
            color: white;
            padding: 3rem 2rem;
        }

        .footer-content {
            display: flex;
            flex-wrap: wrap;
            gap: 3rem;
            justify-content: space-around;
            max-width: 1200px;
            margin: 0 auto;
            margin-bottom: 2rem;
        }

        .footer-section {
            flex: 1;
            min-width: 200px;
        }

        .footer-section h3 {
            margin-bottom: 1rem;
            color: #667eea;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 0.5rem;
        }

        .footer-section a {
            color: #bbb;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section a:hover {
            color: white;
        }

        .footer-bottom {
            text-align: center;
            border-top: 1px solid #444;
            padding-top: 2rem;
            color: #999;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            nav ul {
                gap: 1rem;
                font-size: 0.9rem;
            }

            .hero-content {
                flex-direction: column;
                gap: 2rem;
            }

            .hero-text h1 {
                font-size: 2rem;
            }

            .hero-text p {
                font-size: 1rem;
            }

            .features-content {
                flex-direction: column;
            }

            .features-content:nth-child(even) {
                flex-direction: column;
            }

            .services-grid {
                flex-direction: column;
            }

            .service-card {
                max-width: 100%;
            }

            .section-title {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">ProBiz</div>
                <ul>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#pricing">Pricing</a></li>
                    <li><a href="#testimonials">Testimonials</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <div class="hero-text">
                <h1>Transform Your Business</h1>
                <p>Empower your organization with cutting-edge solutions designed for modern enterprises.</p>
                <button class="cta-button">Get Started Today</button>
            </div>
            <div class="hero-image">🚀</div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="services">
        <div class="container">
            <h2 class="section-title">Our Services</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">📊</div>
                    <h3>Business Analytics</h3>
                    <p>Gain deep insights into your business data with our comprehensive analytics platform.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🔒</div>
                    <h3>Security Solutions</h3>
                    <p>Protect your assets with enterprise-grade security infrastructure and protocols.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">☁️</div>
                    <h3>Cloud Services</h3>
                    <p>Scale your operations with flexible, reliable cloud solutions tailored to your needs.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="features">
        <h2 class="section-title">Key Features</h2>
        
        <div class="features-content">
            <div class="feature-image">⚡</div>
            <div class="feature-text">
                <h2>Lightning Fast Performance</h2>
                <p>Our platform is optimized for speed and efficiency, ensuring your operations run smoothly without delays.</p>
                <ul class="feature-list">
                    <li>99.9% Uptime Guarantee</li>
                    <li>Sub-second Response Times</li>
                    <li>Auto-scaling Infrastructure</li>
                </ul>
            </div>
        </div>

        <div class="features-content">
            <div class="feature-image">🎨</div>
            <div class="feature-text">
                <h2>Intuitive Design</h2>
                <p>User-friendly interface that requires minimal training, allowing your team to be productive from day one.</p>
                <ul class="feature-list">
                    <li>Customizable Dashboard</li>
                    <li>Drag & Drop Interface</li>
                    <li>Mobile Responsive</li>
                </ul>
            </div>
        </div>

        <div class="features-content">
            <div class="feature-image">🤝</div>
            <div class="feature-text">
                <h2>24/7 Support</h2>
                <p>Our dedicated support team is always ready to help you achieve your business goals.</p>
                <ul class="feature-list">
                    <li>Dedicated Account Manager</li>
                    <li>Priority Support Queue</li>
                    <li>Custom Training Sessions</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section id="testimonials" class="testimonials">
        <div class="container">
            <h2 class="section-title">What Our Clients Say</h2>
            <div class="testimonials-grid">
                <div class="testimonial-card">
                    <div class="stars">★★★★★</div>
                    <p class="testimonial-text">"ProBiz transformed how we manage our operations. The platform is incredibly intuitive and the support team is exceptional."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">JD</div>
                        <div class="author-info">
                            <h4>John Davis</h4>
                            <p>CEO, Tech Innovations Ltd</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="stars">★★★★★</div>
                    <p class="testimonial-text">"The ROI we've seen in just 6 months has been remarkable. Highly recommend to any growing business."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">SM</div>
                        <div class="author-info">
                            <h4>Sarah Miller</h4>
                            <p>Operations Manager, Global Enterprises</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="stars">★★★★★</div>
                    <p class="testimonial-text">"Best investment we've made. The platform scales with us perfectly as we grow."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">MP</div>
                        <div class="author-info">
                            <h4>Michael Park</h4>
                            <p>Founder, StartUp Solutions</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section id="pricing" class="pricing">
        <div class="container">
            <h2 class="section-title">Simple Pricing</h2>
            <div class="pricing-grid">
                <div class="pricing-card">
                    <h3>Starter</h3>
                    <div class="price">$29<span>/month</span></div>
                    <p>Perfect for small teams</p>
                    <ul class="pricing-features">
                        <li>Up to 5 users</li>
                        <li>5 GB Storage</li>
                        <li>Email Support</li>
                        <li>Basic Analytics</li>
                    </ul>
                    <button class="cta-button">Choose Plan</button>
                </div>
                <div class="pricing-card featured">
                    <h3>Professional</h3>
                    <div class="price">$79<span>/month</span></div>
                    <p>For growing businesses</p>
                    <ul class="pricing-features">
                        <li>Up to 50 users</li>
                        <li>500 GB Storage</li>
                        <li>Priority Support</li>
                        <li>Advanced Analytics</li>
                    </ul>
                    <button class="cta-button">Choose Plan</button>
                </div>
                <div class="pricing-card">
                    <h3>Enterprise</h3>
                    <div class="price">Custom</div>
                    <p>For large organizations</p>
                    <ul class="pricing-features">
                        <li>Unlimited users</li>
                        <li>Unlimited Storage</li>
                        <li>24/7 Phone Support</li>
                        <li>Custom Integrations</li>
                    </ul>
                    <button class="cta-button">Contact Sales</button>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section id="contact" class="cta-section">
        <div class="container">
            <h2>Ready to Grow Your Business?</h2>
            <p>Join thousands of companies already using ProBiz to transform their operations.</p>
            <button class="cta-button">Start Free Trial</button>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3>About ProBiz</h3>
                <p>Delivering innovative business solutions since 2020, trusted by companies worldwide.</p>
            </div>
            <div class="footer-section">
                <h3>Products</h3>
                <ul>
                    <li><a href="#">Platform</a></li>
                    <li><a href="#">Integrations</a></li>
                    <li><a href="#">Pricing</a></li>
                    <li><a href="#">Security</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Company</h3>
                <ul>
                    <li><a href="#">About Us</a></li>
                    <li><a href="#">Blog</a></li>
                    <li><a href="#">Careers</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Legal</h3>
                <ul>
                    <li><a href="#">Privacy Policy</a></li>
                    <li><a href="#">Terms of Service</a></li>
                    <li><a href="#">Cookie Policy</a></li>
                    <li><a href="#">Compliance</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2024 ProBiz. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>

```

## OUTPUT
![alt text](<Screenshot 2026-05-12 131449.png>)
![alt text](<Screenshot 2026-05-12 131501.png>)
![alt text](<Screenshot 2026-05-12 131532.png>)
![alt text](<Screenshot 2026-05-12 131608.png>)
![alt text](<Screenshot 2026-05-12 131633.png>)
![alt text](<Screenshot 2026-05-12 131644.png>)

## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
