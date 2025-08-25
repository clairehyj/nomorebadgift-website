---
layout: default
title: "Blog - Thoughtful Gift-Giving Tips"
description: "Discover the art of meaningful gift-giving with expert advice, community stories, and thoughtful tips from women who've mastered the joy of giving."
permalink: /blog/
---

<style>
    /* Blog Index Styles */
    .blog-header {
        text-align: center;
        padding: 4rem 0 2rem;
        background: linear-gradient(135deg, 
            rgba(236, 72, 153, 0.05) 0%, 
            rgba(251, 191, 36, 0.05) 100%);
        margin-bottom: 4rem;
        border-radius: var(--border-radius-xl);
    }

    .blog-header h1 {
        font-size: clamp(2.5rem, 5vw, 3.5rem);
        margin-bottom: 1rem;
        background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .blog-header p {
        font-size: 1.2rem;
        color: var(--text-medium);
        max-width: 600px;
        margin: 0 auto;
        line-height: 1.6;
    }

    .blog-container {
        max-width: 900px;
        margin: 0 auto;
        padding: 0 2rem;
    }

    .posts-grid {
        display: grid;
        gap: 3rem;
        margin-bottom: 4rem;
    }

    .post-preview {
        background: var(--white);
        border-radius: var(--border-radius-xl);
        box-shadow: var(--shadow-md);
        padding: 2.5rem;
        transition: all 0.3s ease;
        border: 1px solid var(--gray-100);
        position: relative;
        overflow: hidden;
    }

    .post-preview::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 4px;
        height: 100%;
        background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
        opacity: 0;
        transition: opacity 0.3s ease;
    }

    .post-preview:hover {
        transform: translateY(-8px);
        box-shadow: var(--shadow-xl);
        border-color: var(--primary-color);
    }

    .post-preview:hover::before {
        opacity: 1;
    }

    .post-meta {
        display: flex;
        align-items: center;
        gap: 1rem;
        margin-bottom: 1rem;
        font-size: 0.9rem;
        color: var(--text-light);
    }

    .post-date {
        background: var(--gray-50);
        padding: 0.25rem 0.75rem;
        border-radius: var(--border-radius-md);
        font-weight: 500;
    }

    .post-author {
        color: var(--primary-color);
        font-weight: 600;
    }

    .post-title {
        font-size: 1.8rem;
        margin-bottom: 1rem;
        line-height: 1.3;
    }

    .post-title a {
        color: var(--text-dark);
        text-decoration: none;
        transition: color 0.3s ease;
    }

    .post-title a:hover {
        color: var(--primary-color);
    }

    .post-excerpt {
        font-size: 1.1rem;
        color: var(--text-medium);
        line-height: 1.7;
        margin-bottom: 1.5rem;
    }

    .post-tags {
        display: flex;
        flex-wrap: wrap;
        gap: 0.5rem;
        margin-bottom: 1.5rem;
    }

    .tag {
        background: var(--primary-50);
        color: var(--primary-color);
        padding: 0.25rem 0.75rem;
        border-radius: var(--border-radius-lg);
        font-size: 0.85rem;
        font-weight: 500;
        text-decoration: none;
        transition: all 0.2s ease;
    }

    .tag:hover {
        background: var(--primary-color);
        color: white;
    }

    .read-more {
        display: inline-flex;
        align-items: center;
        gap: 0.5rem;
        color: var(--primary-color);
        text-decoration: none;
        font-weight: 600;
        transition: all 0.3s ease;
    }

    .read-more:hover {
        color: var(--primary-dark);
        transform: translateX(5px);
    }

    .read-more::after {
        content: '→';
        transition: transform 0.3s ease;
    }

    .read-more:hover::after {
        transform: translateX(3px);
    }

    /* Newsletter Section */
    .blog-newsletter {
        background: linear-gradient(135deg, var(--primary-color), var(--primary-light));
        color: white;
        padding: 3rem 2rem;
        border-radius: var(--border-radius-xl);
        text-align: center;
        margin: 4rem 0;
    }

    .blog-newsletter h3 {
        color: white;
        margin-bottom: 1rem;
        font-size: 1.8rem;
    }

    .blog-newsletter p {
        margin-bottom: 2rem;
        opacity: 0.9;
        font-size: 1.1rem;
    }

    .newsletter-form {
        display: flex;
        max-width: 400px;
        margin: 0 auto;
        gap: 1rem;
    }

    .newsletter-form input {
        flex: 1;
        padding: 1rem;
        border: none;
        border-radius: var(--border-radius-lg);
        font-size: 1rem;
    }

    .newsletter-form button {
        background: rgba(255, 255, 255, 0.2);
        color: white;
        border: none;
        padding: 1rem 2rem;
        border-radius: var(--border-radius-lg);
        font-weight: 600;
        cursor: pointer;
        transition: background 0.3s ease;
    }

    .newsletter-form button:hover {
        background: rgba(255, 255, 255, 0.3);
    }

    /* Empty State */
    .no-posts {
        text-align: center;
        padding: 4rem 2rem;
        color: var(--text-medium);
    }

    .no-posts h3 {
        color: var(--text-dark);
        margin-bottom: 1rem;
    }

    /* Responsive Design */
    @media (max-width: 768px) {
        .blog-container {
            padding: 0 1rem;
        }

        .post-preview {
            padding: 2rem;
        }

        .post-title {
            font-size: 1.5rem;
        }

        .newsletter-form {
            flex-direction: column;
        }

        .blog-newsletter {
            padding: 2rem 1rem;
            margin: 3rem 0;
        }
    }
</style>

<div class="blog-container">
    <!-- Blog Header -->
    <header class="blog-header">
        <h1>Thoughtful Gift-Giving Stories</h1>
        <p>Discover the art of meaningful gift-giving with expert advice, community stories, and heartfelt tips from women who've mastered the joy of giving gifts that truly matter.</p>
    </header>

    <!-- Blog Posts -->
    <div class="posts-grid">
        {% if site.posts.size > 0 %}
            {% for post in site.posts %}
                <article class="post-preview">
                    <div class="post-meta">
                        <time class="post-date" datetime="{{ post.date | date_to_xmlschema }}">
                            {{ post.date | date: "%B %d, %Y" }}
                        </time>
                        {% if post.author %}
                            <span class="post-author">by {{ post.author }}</span>
                        {% endif %}
                    </div>
                    
                    <h2 class="post-title">
                        <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
                    </h2>
                    
                    {% if post.excerpt %}
                        <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
                    {% endif %}
                    
                    {% if post.tags.size > 0 %}
                        <div class="post-tags">
                            {% for tag in post.tags %}
                                <span class="tag">{{ tag }}</span>
                            {% endfor %}
                        </div>
                    {% endif %}
                    
                    <a href="{{ post.url | relative_url }}" class="read-more">
                        Read full story
                    </a>
                </article>
            {% endfor %}
        {% else %}
            <div class="no-posts">
                <h3>Coming Soon!</h3>
                <p>We're preparing some beautiful stories and tips about thoughtful gift-giving. Check back soon for inspiring content from our community of caring women.</p>
            </div>
        {% endif %}
    </div>

    <!-- Newsletter Signup -->
    <section class="blog-newsletter">
        <h3>Get Thoughtful Gift Ideas Weekly</h3>
        <p>Join thousands of women who receive weekly inspiration for meaningful gift-giving and relationship building.</p>
        <form class="newsletter-form" action="#" method="post">
            <input type="email" placeholder="Enter your email" required>
            <button type="submit">Subscribe</button>
        </form>
    </section>
</div>