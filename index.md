---
layout: default
title: "Give Gifts That Matter"
description: "Discover perfect gifts through social connections. Share wishlists, follow friends, and never give a bad gift again."
---

<style>
    /* Hero Section */
    .hero {
        background: linear-gradient(135deg, 
            rgba(236, 72, 153, 0.1) 0%, 
            rgba(251, 191, 36, 0.1) 50%, 
            rgba(6, 214, 160, 0.1) 100%);
        padding: 6rem 0;
        position: relative;
        overflow: hidden;
    }

    .hero::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ec4899' fill-opacity='0.05'%3E%3Ccircle cx='30' cy='30' r='2'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E") repeat;
        pointer-events: none;
    }

    .hero-content {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
        align-items: center;
        position: relative;
        z-index: 1;
    }

    .hero-text h1 {
        font-size: clamp(3rem, 6vw, 4.5rem);
        font-weight: 700;
        line-height: 1.1;
        margin-bottom: 1.5rem;
        background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .hero-text p {
        font-size: 1.25rem;
        color: var(--text-medium);
        margin-bottom: 2rem;
        max-width: 500px;
    }

    .hero-buttons {
        display: flex;
        gap: 1rem;
        flex-wrap: wrap;
    }

    .hero-image {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .phone-mockup {
        width: 300px;
        height: 600px;
        background: linear-gradient(145deg, #f0f0f0, #ffffff);
        border-radius: 30px;
        padding: 20px;
        box-shadow: var(--shadow-xl);
        position: relative;
        overflow: hidden;
    }

    .phone-screen {
        width: 100%;
        height: 100%;
        background: var(--white);
        border-radius: 25px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-align: center;
        box-shadow: inset 0 2px 10px rgba(0,0,0,0.1);
    }

    .app-icon {
        font-size: 4rem;
        margin-bottom: 1rem;
        background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    /* Features Section */
    .features {
        padding: 6rem 0;
        background: var(--gray-50);
    }

    .section-header {
        text-align: center;
        max-width: 600px;
        margin: 0 auto 4rem;
    }

    .section-header h2 {
        margin-bottom: 1rem;
        color: var(--text-dark);
    }

    .section-header p {
        font-size: 1.1rem;
        color: var(--text-medium);
    }

    .features-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 2rem;
        margin-top: 3rem;
    }

    .feature-card {
        background: var(--white);
        padding: 2.5rem 2rem;
        border-radius: var(--border-radius-xl);
        box-shadow: var(--shadow-md);
        text-align: center;
        transition: all 0.3s ease;
        border: 1px solid var(--gray-100);
    }

    .feature-card:hover {
        transform: translateY(-8px);
        box-shadow: var(--shadow-xl);
        border-color: var(--primary-color);
    }

    .feature-icon {
        font-size: 3rem;
        margin-bottom: 1.5rem;
        background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .feature-card h3 {
        font-size: 1.5rem;
        margin-bottom: 1rem;
        color: var(--text-dark);
    }

    .feature-card p {
        color: var(--text-medium);
        line-height: 1.6;
    }

    /* About Section */
    .about {
        padding: 6rem 0;
        background: var(--white);
    }

    .about-content {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
        align-items: center;
    }

    .about-text h2 {
        margin-bottom: 1.5rem;
        color: var(--text-dark);
    }

    .about-text p {
        font-size: 1.1rem;
        color: var(--text-medium);
        margin-bottom: 1.5rem;
        line-height: 1.7;
    }

    .about-stats {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 2rem;
        margin-top: 2rem;
    }

    .stat-item {
        text-align: center;
        padding: 1.5rem;
        background: var(--gray-50);
        border-radius: var(--border-radius-lg);
    }

    .stat-number {
        font-size: 2.5rem;
        font-weight: 700;
        color: var(--primary-color);
        display: block;
    }

    .stat-label {
        font-size: 0.9rem;
        color: var(--text-medium);
        font-weight: 500;
    }

    .about-image {
        background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
        border-radius: var(--border-radius-xl);
        height: 400px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: white;
        font-size: 6rem;
    }

    /* CTA Section */
    .cta {
        background: linear-gradient(135deg, var(--primary-color), var(--primary-light));
        padding: 6rem 0;
        text-align: center;
        color: white;
    }

    .cta h2 {
        color: white;
        font-size: clamp(2.5rem, 4vw, 3.5rem);
        margin-bottom: 1.5rem;
    }

    .cta p {
        font-size: 1.2rem;
        margin-bottom: 3rem;
        max-width: 600px;
        margin-left: auto;
        margin-right: auto;
        opacity: 0.9;
    }

    .app-badges {
        display: flex;
        gap: 1rem;
        justify-content: center;
        flex-wrap: wrap;
    }

    .app-badge {
        display: inline-block;
        transition: transform 0.3s ease;
    }

    .app-badge:hover {
        transform: translateY(-5px);
    }

    .app-badge img {
        height: 60px;
        border-radius: var(--border-radius-md);
    }

    /* Testimonials Section */
    .testimonials {
        padding: 6rem 0;
        background: var(--gray-50);
    }

    .testimonials-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 2rem;
        margin-top: 3rem;
    }

    .testimonial-card {
        background: var(--white);
        padding: 2.5rem 2rem;
        border-radius: var(--border-radius-xl);
        box-shadow: var(--shadow-md);
        text-align: center;
        border: 1px solid var(--gray-100);
    }

    .testimonial-quote {
        font-size: 1.1rem;
        font-style: italic;
        color: var(--text-medium);
        margin-bottom: 1.5rem;
        line-height: 1.6;
    }

    .testimonial-author {
        font-weight: 600;
        color: var(--text-dark);
        margin-bottom: 0.5rem;
    }

    .testimonial-role {
        font-size: 0.9rem;
        color: var(--text-light);
    }

    /* Responsive Design */
    @media (max-width: 768px) {
        .hero-content {
            grid-template-columns: 1fr;
            gap: 3rem;
            text-align: center;
        }

        .hero-buttons {
            justify-content: center;
        }

        .phone-mockup {
            width: 250px;
            height: 500px;
        }

        .about-content {
            grid-template-columns: 1fr;
            gap: 3rem;
            text-align: center;
        }

        .about-stats {
            grid-template-columns: repeat(2, 1fr);
            gap: 1rem;
        }

        .features-grid {
            grid-template-columns: 1fr;
            gap: 2rem;
        }

        .app-badges {
            flex-direction: column;
            align-items: center;
        }
    }
</style>

<!-- Hero Section -->
<section class="hero">
    <div class="container">
        <div class="hero-content">
            <div class="hero-text">
                <h1>Give Gifts That Matter</h1>
                <p>Transform your gift-giving experience through meaningful social connections. Discover perfect gifts, share wishlists, and never disappoint again.</p>
                <div class="hero-buttons">
                    <a href="{{ site.app_store_url }}" class="btn btn-primary">
                        📱 Download App
                    </a>
                    <a href="#features" class="btn btn-secondary">Learn More</a>
                </div>
            </div>
            <div class="hero-image">
                <div class="phone-mockup">
                    <div class="phone-screen">
                        <div class="app-icon">🎁</div>
                        <h3 style="margin-bottom: 0.5rem; color: var(--gray-900);">{{ site.title }}</h3>
                        <p style="color: var(--gray-600); text-align: center; padding: 0 1rem;">Social Gift Discovery</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Features Section -->
<section id="features" class="features">
    <div class="container">
        <div class="section-header">
            <h2>Why Choose {{ site.title }}?</h2>
            <p>Transform your gift-giving experience with our intelligent social platform designed for modern gift discovery.</p>
        </div>
        
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon">🔍</div>
                <h3>Smart Discovery</h3>
                <p>Discover trending gifts and perfect matches based on your friends' preferences and social connections.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">👥</div>
                <h3>Social Gifting</h3>
                <p>Follow friends, share wishlists, and give gifts that create meaningful connections and lasting memories.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">💝</div>
                <h3>Wishlist Sharing</h3>
                <p>Create and share wishlists for any occasion. Let friends know exactly what would make you happy.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">🎯</div>
                <h3>Perfect Matches</h3>
                <p>Our intelligent algorithm suggests gifts based on personality, interests, and social connections.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">🔔</div>
                <h3>Smart Reminders</h3>
                <p>Never miss another birthday or special occasion with intelligent notifications and planning tools.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">✨</div>
                <h3>Celebration Tracking</h3>
                <p>Keep track of special moments, preferences, and gift history to build stronger relationships.</p>
            </div>
        </div>
    </div>
</section>

<!-- About Section -->
<section id="about" class="about">
    <div class="container">
        <div class="about-content">
            <div class="about-text">
                <h2>Revolutionizing Gift-Giving Through Social Connection</h2>
                <p>{{ site.title }} transforms the way we give and receive gifts by creating meaningful connections between friends, family, and loved ones. Our platform combines social discovery with intelligent recommendations to ensure every gift is thoughtful and appreciated.</p>
                <p>Join thousands of women who have discovered the joy of giving perfect gifts every time. Build stronger relationships, create lasting memories, and never give a disappointing gift again.</p>
                
                <div class="about-stats">
                    <div class="stat-item">
                        <span class="stat-number">10K+</span>
                        <span class="stat-label">Happy Users</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">50K+</span>
                        <span class="stat-label">Perfect Gifts</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">95%</span>
                        <span class="stat-label">Satisfaction Rate</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">24/7</span>
                        <span class="stat-label">Support</span>
                    </div>
                </div>
            </div>
            <div class="about-image">
                🎁
            </div>
        </div>
    </div>
</section>

<!-- Testimonials Section -->
<section class="testimonials">
    <div class="container">
        <div class="section-header">
            <h2>What Our Users Say</h2>
            <p>Real stories from women who transformed their gift-giving experience</p>
        </div>
        
        <div class="testimonials-grid">
            <div class="testimonial-card">
                <div class="testimonial-quote">
                    "Finally, an app that understands what my friends actually want! I've never given better gifts."
                </div>
                <div class="testimonial-author">Sarah Chen</div>
                <div class="testimonial-role">Marketing Manager</div>
            </div>
            
            <div class="testimonial-card">
                <div class="testimonial-quote">
                    "The wishlist sharing feature is genius. No more awkward guessing games at birthdays!"
                </div>
                <div class="testimonial-author">Emily Rodriguez</div>
                <div class="testimonial-role">New Mom</div>
            </div>
            
            <div class="testimonial-card">
                <div class="testimonial-quote">
                    "As someone who travels for work, the reminder feature has saved me countless times."
                </div>
                <div class="testimonial-author">Jessica Kim</div>
                <div class="testimonial-role">Sales Executive</div>
            </div>
        </div>
    </div>
</section>

<!-- Download CTA Section -->
<section id="download" class="cta">
    <div class="container">
        <h2>Ready to Give Better Gifts?</h2>
        <p>Join thousands of users who have revolutionized their gift-giving experience. Download {{ site.title }} today and start discovering perfect gifts.</p>
        
        <div class="app-badges">
            <a href="{{ site.app_store_url }}" class="app-badge" aria-label="Download on App Store">
                <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='60' viewBox='0 0 200 60'%3E%3Crect width='200' height='60' rx='12' fill='%23000'/%3E%3Ctext x='100' y='30' text-anchor='middle' dominant-baseline='middle' fill='white' font-family='Arial' font-size='12'%3EDownload on App Store%3C/text%3E%3C/svg%3E" alt="Download on App Store">
            </a>
            <a href="{{ site.google_play_url }}" class="app-badge" aria-label="Get it on Google Play">
                <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='60' viewBox='0 0 200 60'%3E%3Crect width='200' height='60' rx='12' fill='%23000'/%3E%3Ctext x='100' y='30' text-anchor='middle' dominant-baseline='middle' fill='white' font-family='Arial' font-size='12'%3EGet it on Google Play%3C/text%3E%3C/svg%3E" alt="Get it on Google Play">
            </a>
        </div>
    </div>
</section>