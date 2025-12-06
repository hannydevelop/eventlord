<template>
    <!-- Hidden checkbox for CSS-only toggle -->
    <input type="checkbox" id="menu-toggle">

    <!-- Landing Page -->
    <div class="landing-page">
        <div class="logo-background"></div>
        <div class="landing-content">
            <h1 class="landing-title">EVENTLORD</h1>
            <p class="landing-subtitle">EVENT MANAGEMENT COMPANY LTD</p>
            <label for="menu-toggle" class="view-menu-btn">View Food Menu</label>
        </div>
    </div>

    <!-- Menu Container -->
    <div class="menu-container">
        <!-- Back Button -->
        <label for="menu-toggle" class="back-btn">← Back</label>

        <!-- Logo watermark in menu background -->
        <img src="../assets/background.jpeg" alt="" class="menu-logo-bg" aria-hidden="true">

        <div class="container">
            <!-- Hero Section -->
            <header class="hero">
                <div class="hero-pattern">
                    <svg width="100%" height="100%" viewBox="0 0 100 100" preserveAspectRatio="none">
                        <pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse">
                            <path d="M 10 0 L 0 0 0 10" fill="none" stroke="currentColor" stroke-width="0.5" />
                        </pattern>
                        <rect width="100%" height="100%" fill="url(#grid)" />
                    </svg>
                </div>

                <div class="hero-content">
                    <div class="hero-flourish animate-fade-in delay-500">
                        <svg viewBox="0 0 128 32">
                            <path d="M0 16 Q32 0 64 16 Q96 32 128 16" fill="none" stroke="currentColor" stroke-width="1"
                                opacity="0.5" />
                            <circle cx="64" cy="16" r="3" fill="currentColor" />
                        </svg>
                    </div>

                    <p class="hero-tagline animate-fade-in delay-100">A Beautiful Wedding from Heaven</p>
                    <h1 class="hero-title animate-fade-in-up delay-200">Chinelo & Chigozie</h1>

                    <div class="hero-subtitle animate-fade-in delay-300">
                        <span class="hero-subtitle-line"></span>
                        <span class="hero-subtitle-text">Food Menu</span>
                        <span class="hero-subtitle-line"></span>
                    </div>

                    <div class="hero-details animate-fade-in delay-400">
                        <p class="hero-date">Saturday, December 06th, 2025</p>
                        <p class="hero-venue">The Grand Ballroom, Patterson Hall • 2:00 PM</p>
                    </div>

                    <div class="hero-flourish animate-fade-in delay-500">
                        <svg viewBox="0 0 128 32">
                            <path d="M0 16 Q32 0 64 16 Q96 32 128 16" fill="none" stroke="currentColor" stroke-width="1"
                                opacity="0.5" />
                            <circle cx="64" cy="16" r="3" fill="currentColor" />
                        </svg>
                    </div>
                </div>
            </header>

            <!-- Appetizers Section -->
            <section class="menu-section animate-fade-in-up delay-300">
                <div class="menu-section-header">
                    <h2 class="menu-section-title">To Begin (STARTER)</h2>
                    <div class="menu-divider">
                        <span class="menu-divider-icon">
                            <svg viewBox="0 0 24 24" fill="currentColor">
                                <path
                                    d="M12 2L15.09 8.26L22 9.27L17 14.14L18.18 21.02L12 17.77L5.82 21.02L7 14.14L2 9.27L8.91 8.26L12 2Z" />
                            </svg>
                        </span>
                    </div>
                </div>

                <div class="menu-items">
                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Seafood Pepper Soup with Bread bun</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">PEPPER SOUP</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Seafood Pepper Soup with Bread bun</p>
                    </article>
                </div>

                <div class="menu-items">
                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Assorted Peppersoup and Bread Bun</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">PEPPER SOUP</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Assorted Peppersoup and Bread Bun</p>
                    </article>
                </div>
            </section>

            <!-- Main Course Section (NIGERIAN MEALS) -->
            <section class="menu-section animate-fade-in-up delay-500">
                <div class="menu-section-header">
                    <h2 class="menu-section-title">Main Course (NIGERIAN MEALS)</h2>
                    <div class="menu-divider">
                        <span class="menu-divider-icon">
                            <svg viewBox="0 0 24 24" fill="currentColor">
                                <path
                                    d="M12 2L15.09 8.26L22 9.27L17 14.14L18.18 21.02L12 17.77L5.82 21.02L7 14.14L2 9.27L8.91 8.26L12 2Z" />
                            </svg>
                        </span>
                    </div>
                </div>

                <div class="menu-items">
                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Jollof rice / Fried rice / Moi-Moi / Chicken / Coleslaw </h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">RICE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Jollof rice / Fried rice / Moi-Moi / Chicken / Coleslaw</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Steamed White Rice and Signature Chicken Sauce</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">RICE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Steamed White Rice and Signature Chicken Sauce</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Steamed White Rice and Plain Sauce</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">RICE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Steamed White Rice and Plain Sauce</p>
                    </article>

                    <!---
                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Steamed Basmati Rice / Boneless Chicken Sauce</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">RICE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Steamed Basmati Rice / Boneless Chicken Sauce</p>
                    </article>
                    -->

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Steamed White Rice / Vegetable Stew / Proteins</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">RICE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Steamed White Rice / Vegetable Stew / Proteins </p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Pineapple Rice / Chicken / Salad</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">RICE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Pineapple Rice / Chicken / Salad </p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Coconut Rice / Dry Fish / Prawns / Chicken </h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">RICE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Coconut Rice / Dry Fish / Prawns / Chicken</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Ukwa / Peppered Mangala Fish</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">UKWA</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Ukwa / Peppered Mangala Fish</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Abacha / Ugba / Kpomo</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">ABACHA</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Abacha / Ugba / Kpomo</p>
                    </article>
                </div>
            </section>

            <!-- Main Course Section (NIGERIAN SOUPS) -->
            <section class="menu-section animate-fade-in-up delay-500">
                <div class="menu-section-header">
                    <h2 class="menu-section-title">Main Course (NIGERIAN SOUPS)</h2>
                    <div class="menu-divider">
                        <span class="menu-divider-icon">
                            <svg viewBox="0 0 24 24" fill="currentColor">
                                <path
                                    d="M12 2L15.09 8.26L22 9.27L17 14.14L18.18 21.02L12 17.77L5.82 21.02L7 14.14L2 9.27L8.91 8.26L12 2Z" />
                            </svg>
                        </span>
                    </div>
                </div>

                <div class="menu-items">
                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Egusi Soup & Fufu / Semo</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">EGUSI</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Egusi Soup & Fufu / Semo</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Fresh Vegetables Okro & Fufu / Semo</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">OKRO</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Fresh Vegetables Okro & Fufu / Semo</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Onugbu Soup & Fufu / Semo</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">ONUGBU</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Onugbu Soup & Fufu / Semo</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Nsala Soup & Semo / Fufu</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">NSALA</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Nsala Soup & Semo / Fufu</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Ora Soup & Semo / Fufu</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">ORA</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Ora Soup & Semo / Fufu</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Goat Meat Nsala / Fufu & Semo</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">NSALA</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Goat Meat Nsala / Fufu & Semo</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Goat Meat Vegetable Soup / Fufu & Semo</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">VEGETABLE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Goat Meat Vegetable Soup / Fufu & Semo</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Edikaikong Soup & Semo</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">EDIKAIKONG</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Edikaikong Soup & Semo</p>
                    </article>
                </div>
            </section>

            <!-- Main Course Section (CONTINENTAL MEALS) -->
            <section class="menu-section animate-fade-in-up delay-500">
                <div class="menu-section-header">
                    <h2 class="menu-section-title">Main Course (CONTINENTAL MEALS)</h2>
                    <div class="menu-divider">
                        <span class="menu-divider-icon">
                            <svg viewBox="0 0 24 24" fill="currentColor">
                                <path
                                    d="M12 2L15.09 8.26L22 9.27L17 14.14L18.18 21.02L12 17.77L5.82 21.02L7 14.14L2 9.27L8.91 8.26L12 2Z" />
                            </svg>
                        </span>
                    </div>
                </div>

                <div class="menu-items">
                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Singaporean Noddles / Chinese Rice / Chicken Sauce</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">RICE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Singaporean Noddles / Chinese Rice / Chicken Sauce</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Special Fried Rice & Grilled Prawns</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">RICE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Special Fried Rice & Grilled Prawns</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Tempura Prawns With Sweet Chilli Dip</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">PRAWNS</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Tempura Prawns With Sweet Chilli Dip</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Shawarma Egg Rice / Chicken / Salad </h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">RICE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Shawarma Egg Rice / Chicken / Salad</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Chicken Lollipop on Fruit Salad</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">FRUIT SALAD</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Chicken Lollipop on Fruit Salad</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Creamy Pasta Served With Spicy Large Prawns</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">PASTA</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Creamy Pasta Served With Spicy Large Prawns</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Sweet & Spicy Beef Ribs with Mashed Potatoes and Mushroom Sauce</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">MASHED POTATOES</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Sweet & Spicy Beef Ribs with Mashed Potatoes and Mushroom Sauce</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Spicy Barracuda Steak with Steamed Herb Rice</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">RICE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Spicy Barracuda Steak with Steamed Herb Rice</p>
                    </article>
                </div>
            </section>

            <!-- Sides Section -->
            <section class="menu-section animate-fade-in-up delay-700">
                <div class="menu-section-header">
                    <h2 class="menu-section-title">Sides/Proteins</h2>
                    <div class="menu-divider">
                        <span class="menu-divider-icon">
                            <svg viewBox="0 0 24 24" fill="currentColor">
                                <path
                                    d="M12 2L15.09 8.26L22 9.27L17 14.14L18.18 21.02L12 17.77L5.82 21.02L7 14.14L2 9.27L8.91 8.26L12 2Z" />
                            </svg>
                        </span>
                    </div>
                </div>

                <div class="menu-items">
                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Full Vegetable Salad</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">VEGETABLE SALAD</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Full Vegetable Salad</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Peppered Crocker Fish</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">CROCKER FISH</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Peppered Crocker Fish</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Peppered Goat Meat</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">GOAT MEAT</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Peppered Goat Meat</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Peppered Chicken</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">CHICKEN</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Peppered Chicken</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Sauced Snails</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">SNAILS</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Sauced Snails</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Grilled Prawns</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">PRAWNS</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Grilled Prawns</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Grilled Catfish</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">CATFISH</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Grilled Catfish</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Nigerian Fresh Vegetables Salad</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">NIGERIAN SALAD</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Nigerian Fresh Vegetables Salad</p>
                    </article>
                </div>
            </section>

            <!-- Grills Section -->
            <section class="menu-section animate-fade-in-up delay-700">
                <div class="menu-section-header">
                    <h2 class="menu-section-title">GRILLS</h2>
                    <div class="menu-divider">
                        <span class="menu-divider-icon">
                            <svg viewBox="0 0 24 24" fill="currentColor">
                                <path
                                    d="M12 2L15.09 8.26L22 9.27L17 14.14L18.18 21.02L12 17.77L5.82 21.02L7 14.14L2 9.27L8.91 8.26L12 2Z" />
                            </svg>
                        </span>
                    </div>
                </div>

                <div class="menu-items">
                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Spicy Grilled Ram</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">RAM</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Spicy Grilled Ram</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Grilled Turkey and Chips</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">TURKEY</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Grilled Turkey and Chips</p>
                    </article>
                </div>
            </section>

            <!-- Desserts Section -->
            <section class="menu-section animate-fade-in-up delay-700">
                <div class="menu-section-header">
                    <h2 class="menu-section-title">To Finish (DESSERT)</h2>
                    <div class="menu-divider">
                        <span class="menu-divider-icon">
                            <svg viewBox="0 0 24 24" fill="currentColor">
                                <path
                                    d="M12 2L15.09 8.26L22 9.27L17 14.14L18.18 21.02L12 17.77L5.82 21.02L7 14.14L2 9.27L8.91 8.26L12 2Z" />
                            </svg>
                        </span>
                    </div>
                </div>

                <div class="menu-items">
                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Creamy Ice Cream in Plates & Cones </h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">ICE CREAM</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Creamy Ice Cream in Plates & Cones</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Red Velvet Cake and Ice Cream</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">ICE CREAM</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Red Velvet Cake and Ice Cream</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Belgian Waffle in Pan</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">WAFFLE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Belgian Waffle in Pan</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Milkshake </h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">MILKSHAKE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Milkshake </p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Chocolate Cake and Ice Cream</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">CAKE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Chocolate Cake and Ice Cream</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Apple Crumble</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">CRUMBLE</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Apple Crumble</p>
                    </article>
                </div>
            </section>

            <!-- Afterparty Section -->
            <section class="menu-section animate-fade-in-up delay-700">
                <div class="menu-section-header">
                    <h2 class="menu-section-title">To Finish (AFTERPARTY MEAL)</h2>
                    <div class="menu-divider">
                        <span class="menu-divider-icon">
                            <svg viewBox="0 0 24 24" fill="currentColor">
                                <path
                                    d="M12 2L15.09 8.26L22 9.27L17 14.14L18.18 21.02L12 17.77L5.82 21.02L7 14.14L2 9.27L8.91 8.26L12 2Z" />
                            </svg>
                        </span>
                    </div>
                </div>

                <div class="menu-items">
                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Pizza Slice</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">PIZZA</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Pizza Slice</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Chocolate Coated Puff Puff</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">PUFF-PUFF</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Chocolate Coated Puff Puff</p>
                    </article>

                    <article class="menu-item">
                        <div class="menu-item-header">
                            <div class="menu-item-title-group">
                                <h3 class="menu-item-title">Hot Spicy Noddles with Diced Chicken</h3>
                                <div class="menu-item-tags">
                                    <span class="menu-item-tag">NODDLES</span>
                                </div>
                            </div>
                        </div>
                        <p class="menu-item-description">Hot Spicy Noddles with Diced Chicken</p>
                    </article>
                </div>
            </section>

            <!-- Footer -->
            <footer class="menu-footer animate-fade-in delay-800">
                <svg class="footer-star" viewBox="0 0 40 40" fill="currentColor">
                    <path d="M20 4L24 12H36L27 20L31 32L20 25L9 32L13 20L4 12H16L20 4Z" opacity="0.6" />
                </svg>

                <p class="footer-note">
                    Please inform your server of any dietary restrictions or allergies.
                    Our kitchen will be happy to accommodate your needs.
                </p>

                <div class="footer-closing">
                    <p class="footer-closing-title">Thank you for joining us</p>
                    <p class="footer-closing-text">We hope you enjoy this event</p>
                </div>
            </footer>
        </div>
    </div>
    <FooterView />
</template>

<script>
import NavBar from '../components/NavBar.vue';
import FooterView from '../components/FooterView.vue';

export default {
    name: 'MenuView',
    components: { NavBar, FooterView },
}
</script>

<style scoped>
/* Reset & Base */
*,
*::before,
*::after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: var(--font-body);
    background-color: var(--background);
    color: var(--foreground);
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}

/* Hidden checkbox for toggle */
#menu-toggle {
    display: none;
}

/* Landing Page */
.landing-page {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: relative;
    background-color: var(--background);
    overflow: hidden;
    transition: opacity 0.5s ease, visibility 0.5s ease;
}

/* Logo Background */
.logo-background {
    position: absolute;
    inset: 0;
    background-image: url('../assets/logo.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: 60%;
    opacity: 0.08;
    pointer-events: none;
}

@media (max-width: 768px) {
    .logo-background {
        background-size: 90%;
    }
}

.landing-content {
    position: relative;
    z-index: 1;
    text-align: center;
    padding: 40px;
}

.landing-logo {
    width: 200px;
    height: 200px;
    margin-bottom: 40px;
    animation: fadeIn 1s ease-out forwards;
}

.landing-title {
    font-family: var(--font-display);
    font-size: clamp(46px, 8vw, 74px);
    color: var(--primary);
    margin-bottom: 16px;
    letter-spacing: -0.02em;
    opacity: 0;
    animation: fadeInUp 0.8s ease-out 0.3s forwards;
}

.landing-subtitle {
    font-family: var(--font-display);
    font-style: italic;
    font-size: 20px;
    color: var(--muted);
    margin-bottom: 48px;
    opacity: 0;
    animation: fadeIn 1s ease-out 0.5s forwards;
}

.view-menu-btn {
    display: inline-block;
    font-family: var(--font-body);
    font-size: 14px;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 0.2em;
    color: var(--background);
    background: linear-gradient(135deg, var(--accent), var(--accent-light));
    padding: 18px 48px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 4px 20px rgba(201, 162, 39, 0.3);
    opacity: 0;
    animation: fadeInUp 0.8s ease-out 0.7s forwards;
}

.view-menu-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 30px rgba(201, 162, 39, 0.4);
}

/* Menu Container */
.menu-container {
    margin-top: 100px;
    position: fixed;
    inset: 0;
    background-color: var(--background);
    overflow-y: auto;
    opacity: 0;
    visibility: hidden;
    transition: opacity 0.5s ease, visibility 0.5s ease;
}

/* Toggle States */
#menu-toggle:checked~.landing-page {
    opacity: 0;
    visibility: hidden;
    pointer-events: none;
}

#menu-toggle:checked~.menu-container {
    opacity: 1;
    visibility: visible;
}

/* Back Button */
.back-btn {
    position: fixed;
    top: 24px;
    left: 24px;
    z-index: 100;
    font-family: var(--font-body);
    font-size: 12px;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--muted);
    background: var(--cream);
    padding: 12px 20px;
    border: 1px solid var(--border);
    border-radius: 4px;
    cursor: pointer;
    transition: all 0.3s ease;
    text-decoration: none;
}

.back-btn:hover {
    background: var(--cream-dark);
    color: var(--primary);
}

/* Container */
.container {
    max-width: 768px;
    margin: 0 auto;
    padding: 0 24px;
}

/* Typography */
h1,
h2,
h3 {
    font-family: var(--font-display);
    font-weight: 500;
}

/* Animations */
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(20px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes fadeIn {
    from {
        opacity: 0;
    }

    to {
        opacity: 1;
    }
}

.animate-fade-in {
    animation: fadeIn 1s ease-out forwards;
}

.animate-fade-in-up {
    animation: fadeInUp 0.8s ease-out forwards;
}

.delay-100 {
    animation-delay: 100ms;
}

.delay-200 {
    animation-delay: 200ms;
}

.delay-300 {
    animation-delay: 300ms;
}

.delay-400 {
    animation-delay: 400ms;
}

.delay-500 {
    animation-delay: 500ms;
}

.delay-600 {
    animation-delay: 600ms;
}

.delay-700 {
    animation-delay: 700ms;
}

.delay-800 {
    animation-delay: 800ms;
}

/* Hero Section */
.hero {
    position: relative;
    padding: 80px 0 60px;
    text-align: center;
    overflow: hidden;
}

.hero-pattern {
    position: absolute;
    inset: 0;
    opacity: 0.04;
    pointer-events: none;
}

/* Logo watermark in menu */
.menu-logo-bg {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 50%;
    max-width: 500px;
    opacity: 0.09;
    pointer-events: none;
    z-index: 0;
}

.hero-content {
    position: relative;
    z-index: 1;
}

.hero-star {
    width: 64px;
    height: 64px;
    color: var(--accent);
    margin-bottom: 32px;
    opacity: 0;
}

.hero-tagline {
    font-family: var(--font-body);
    font-size: 12px;
    font-weight: 400;
    text-transform: uppercase;
    letter-spacing: 0.3em;
    color: var(--muted);
    margin-bottom: 16px;
    opacity: 0;
}

.hero-title {
    font-size: clamp(48px, 10vw, 96px);
    color: var(--primary);
    margin-bottom: 24px;
    letter-spacing: -0.02em;
    opacity: 0;
}

.hero-subtitle {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 16px;
    margin-bottom: 32px;
    opacity: 0;
}

.hero-subtitle-line {
    width: 48px;
    height: 1px;
    background-color: var(--border);
}

.hero-subtitle-text {
    font-family: var(--font-display);
    font-style: italic;
    font-size: 18px;
    color: var(--muted);
}

.hero-details {
    opacity: 0;
}

.hero-date {
    color: var(--muted);
    font-size: 16px;
    margin-bottom: 8px;
}

.hero-venue {
    font-size: 14px;
    color: var(--muted);
    letter-spacing: 0.05em;
}

.hero-flourish {
    margin-top: 48px;
    opacity: 0;
}

.hero-flourish svg {
    width: 128px;
    height: 32px;
    color: var(--accent);
}

/* Menu Section */
.menu-section {
    padding: 40px 0;
    opacity: 0;
    position: relative;
    z-index: 1;
}

.menu-section-header {
    text-align: center;
    margin-bottom: 40px;
}

.menu-section-title {
    font-size: clamp(28px, 5vw, 36px);
    color: var(--primary);
    letter-spacing: 0.05em;
}

.menu-divider {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 16px;
}

.menu-divider::before,
.menu-divider::after {
    content: '';
    flex: 1;
    max-width: 200px;
    height: 1px;
    background-color: var(--border);
}

.menu-divider-icon {
    margin: 0 16px;
    color: var(--accent);
}

.menu-divider-icon svg {
    width: 24px;
    height: 24px;
}

/* Menu Item */
.menu-items {
    display: flex;
    flex-direction: column;
    gap: 32px;
}

.menu-item {
    padding: 16px;
    margin: 0 -16px;
    border-radius: 8px;
    transition: background-color 0.3s ease;
}

.menu-item:hover {
    background-color: var(--cream);
}

.menu-item-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 16px;
    flex-wrap: wrap;
}

.menu-item-title-group {
    display: flex;
    align-items: center;
    gap: 12px;
    flex-wrap: wrap;
}

.menu-item-title {
    font-size: 20px;
    color: var(--foreground);
    transition: color 0.3s ease;
}

.menu-item:hover .menu-item-title {
    color: var(--primary);
}

.menu-item-tags {
    display: flex;
    gap: 8px;
}

.menu-item-tag {
    font-size: 10px;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--accent);
    background-color: rgba(201, 162, 39, 0.1);
    padding: 4px 8px;
    border-radius: 4px;
}

.menu-item-price {
    font-family: var(--font-display);
    font-size: 18px;
    color: var(--accent);
    white-space: nowrap;
}

.menu-item-description {
    margin-top: 8px;
    font-size: 15px;
    font-weight: 300;
    color: var(--muted);
    line-height: 1.7;
}

/* Footer */
.menu-footer {
    padding: 64px 0;
    text-align: center;
    border-top: 1px solid var(--border);
    margin-top: 64px;
    opacity: 0;
    position: relative;
    z-index: 1;
}

.footer-star {
    width: 40px;
    height: 40px;
    color: var(--accent);
    margin-bottom: 24px;
}

.footer-note {
    font-size: 14px;
    color: var(--muted);
    max-width: 480px;
    margin: 0 auto 24px;
    line-height: 1.8;
}

.footer-legend {
    display: flex;
    justify-content: center;
    gap: 24px;
    font-size: 12px;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--muted);
}

.footer-legend-item {
    display: flex;
    align-items: center;
    gap: 8px;
}

.footer-legend-dot {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background-color: var(--accent);
    opacity: 0.6;
}

.footer-closing {
    margin-top: 40px;
    padding-top: 32px;
    border-top: 1px solid var(--cream-dark);
}

.footer-closing-title {
    font-family: var(--font-display);
    font-size: 18px;
    color: var(--primary);
    margin-bottom: 8px;
}

.footer-closing-text {
    font-size: 14px;
    color: var(--muted);
}

/* Responsive */
@media (max-width: 640px) {
    .hero {
        padding: 60px 0 40px;
    }

    .menu-item-header {
        flex-direction: column;
        gap: 8px;
    }

    .menu-item-price {
        align-self: flex-start;
    }

    .footer-legend {
        flex-direction: column;
        gap: 12px;
    }

    .back-btn {
        top: 16px;
        left: 16px;
        padding: 10px 16px;
    }

    .landing-logo {
        width: 150px;
        height: 150px;
    }
}</style>