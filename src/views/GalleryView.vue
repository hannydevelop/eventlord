<template>
    <div>
        <!-- Header -->
        <header class="header">
            <h1>{{ appTitle }}</h1>
            <p>{{ appSubtitle }}</p>
        </header>

        <!-- Photo Book -->
        <div class="photo-book">
            <!-- Book Navigation -->
            <div class="book-nav">
                <button v-for="chapter in chapters" :key="chapter.id"
                    :class="['chapter-btn', { active: activeChapter === chapter.id }]"
                    @click="switchChapter(chapter.id, $event)">
                    {{ chapter.title }}
                </button>
            </div>

            <!-- Overview Chapter -->
            <div v-show="activeChapter === 'overview'" class="book-chapter"
                :class="{ active: activeChapter === 'overview' }">
                <div class="page" ref="overviewPage1">
                    <div class="page-header">
                        <h2 class="page-title">Welcome to Our Gallery</h2>
                        <p class="page-subtitle">Capturing moments that matter most</p>
                    </div>
                    <div class="photo-spread">
                        <div class="full-spread">
                            <div class="photo-large" @click="showPhotoDetail('Elegant Moments')">
                                <img src="../assets/elegant.jpg" class="img-fluid"/>
                                <div class="photo-caption">Elegant Moments</div>
                            </div>
                            <div class="photo-large" @click="showPhotoDetail('Luxury Events')">
                                <img src="../assets/divo.png" class="img-fluid" />
                                <div class="photo-caption">Luxury Events</div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="page" ref="overviewPage2">
                    <!-- Statistics Section -->
                    <section class="stats-section">
                        <div class="container">
                            <div class="row">
                                <div class="col-md-3" v-for="stat in stats" :key="stat.label">
                                    <div class="stat-item" >
                                        <span class="stat-number" :data-count="stat.number">0</span>
                                        <div class="stat-label">{{ stat.label }}</div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </section>
                </div>
            </div>

            <!-- Weddings Chapter -->
            <div v-show="activeChapter === 'weddings'" class="book-chapter"
                :class="{ active: activeChapter === 'weddings' }">
                <div class="page" ref="weddingPage1">
                    <div class="page-header">
                        <h2 class="page-title">Wedding Celebrations</h2>
                        <p class="page-subtitle">Love stories beautifully told</p>
                    </div>
                    <div class="photo-spread">
                        <div class="full-spread">
                            <div class="photo-large" @click="showPhotoDetail('Sacred Ceremonies')">
                                <img src="../assets/wedding.jpg" class="img-fluid" />
                                <div class="photo-caption">Sacred Ceremonies</div>
                            </div>
                            <div class="photo-large" @click="showPhotoDetail('Eternal Promises')">
                                <img src="../assets/sacred.jpeg" class="img-fluid" />
                                <div class="photo-caption">Eternal Promises</div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="page" ref="weddingPage2">
                    <div class="page-header">
                        <h2 class="page-title">Wedding Moments</h2>
                        <p class="page-subtitle">From vows to celebration</p>
                    </div>
                    <div class="photo-spread">
                        <div class="photo-grid">
                            <div class="photo-small"
                                @click="showPhotoDetail('bride')">
                                <img src="../assets/bride.jpg" class="img-fluid" />
                            </div>
                            <div class="photo-small"
                                @click="showPhotoDetail('groom')">
                                <img src="../assets/groom.jpg" class="img-fluid" />
                            </div>
                            <div class="photo-small"
                                @click="showPhotoDetail('flowers')">
                                <img src="../assets/flower.png" class="img-fluid" />
                            </div>
                            <div class="photo-small"
                                @click="showPhotoDetail('dance')">
                                <img src="../assets/dance.jpg" class="img-fluid" />
                            </div>
                            <div class="photo-small"
                                @click="showPhotoDetail('traditional')">
                                <img src="../assets/traditional.jpeg" class="img-fluid" />
                            </div>
                            <div class="photo-small"
                                @click="showPhotoDetail('transport')">
                                <img src="../assets/transport.jpg" class="img-fluid" />
                            </div>
                        </div>
                        <div class="story-text">
                            <h3>Every Detail Matters</h3>
                            <p>From the bride's first look to the last dance, we capture every precious moment of your
                                special day. Our wedding photography combines candid emotions with elegant portraits,
                                creating a comprehensive visual story of your celebration.</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Memorials Chapter -->
            <div v-show="activeChapter === 'memorials'" class="book-chapter"
                :class="{ active: activeChapter === 'memorials' }">
                <div class="page" ref="memorialPage1">
                    <div class="page-header">
                        <h2 class="page-title">Memorial Services / Funerals</h2>
                        <p class="page-subtitle">Honoring your cherished memories</p>
                    </div>
                    <div class="photo-spread">
                        <div class="story-layout">
                            <div class="story-text">
                                <h3>Celebration of Life</h3>
                                <p>We approach memorial photography with the utmost sensitivity and respect, capturing the
                                    love, memories, and tributes that honor those who have passed.</p>
                                <p>Our goal is to document these meaningful gatherings with dignity, preserving the moments
                                    of remembrance and the comfort found in community during difficult times.</p>
                            </div>
                            <div class="photo-large" @click="showPhotoDetail('Peaceful Remembrance')">
                                <span>🕊️</span>
                                <div class="photo-caption">Peaceful Remembrance</div>
                            </div>
                        </div>
                        <div class="photo-grid">
                            <div class="photo-small">
                                <img src="../assets/depart1.png" class="img-fluid" />
                            </div>
                            <div class="photo-small">
                                <img src="../assets/depart2.png" class="img-fluid" />
                            </div>
                            <div class="photo-small">
                                <img src="../assets/depart3.png" class="img-fluid" />
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Corporate Chapter -->
            <div v-show="activeChapter === 'corporate'" class="book-chapter"
                :class="{ active: activeChapter === 'corporate' }">
                <div class="page" ref="corporatePage1">
                    <div class="page-header">
                        <h2 class="page-title">Corporate Events</h2>
                        <p class="page-subtitle">Professional excellence in every frame</p>
                    </div>
                    <div class="photo-spread">
                        <div class="full-spread">
                            <div class="photo-large" @click="showPhotoDetail('Executive Meetings')">
                                <span>🏢</span>
                                <div class="photo-caption">Executive Meetings</div>
                            </div>
                            <div class="photo-large" @click="showPhotoDetail('Business Partnerships')">
                                <span>🤝</span>
                                <div class="photo-caption">Business Partnerships</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Celebrations Chapter -->
            <div v-show="activeChapter === 'celebrations'" class="book-chapter"
                :class="{ active: activeChapter === 'celebrations' }">
                <div class="page" ref="celebrationPage1">
                    <div class="page-header">
                        <h2 class="page-title">Life Celebrations</h2>
                        <p class="page-subtitle">Joyful moments worth remembering</p>
                    </div>
                    <div class="photo-spread">
                        <div class="timeline">
                            <div v-for="(celebration, index) in celebrations" :key="index" class="timeline-item">
                                <div class="timeline-content">
                                    <h3>{{ celebration.title }}</h3>
                                    <p>{{ celebration.description }}</p>
                                </div>
                                <div class="timeline-photo" @click="showPhotoDetail(celebration.title)">
                                    <span>{{ celebration.emoji }}</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import NavBar from '../components/NavBar.vue';
import FooterView from '../components/FooterView.vue';

export default {
    name: 'GalleryView',
    components: { NavBar, FooterView },

    data() {
        return {
            appTitle: 'Our Photo Book',
            appSubtitle: "A curated collection of life's most precious moments we have covered",
            activeChapter: 'overview',

            chapters: [
                { id: 'overview', title: 'Overview' },
                { id: 'weddings', title: 'Weddings' },
                { id: 'memorials', title: 'Memorials' },
            ],

            weddingPhotos: [
                { emoji: '👰', caption: 'Bride' },
                { emoji: '🤵', caption: 'Groom' },
                { emoji: '🌹', caption: 'Flowers' },
                { emoji: '💐', caption: 'Bouquet' },
                { emoji: '🎂', caption: 'Wedding Cake' },
                { emoji: '💃', caption: 'First Dance' }
            ],
            stats: [
                { number: 100, label: 'Events Completed', delay: 0 },
                { number: 5, label: 'Years of Excellence', delay: 200 },
                { number: 100, label: 'Client Satisfaction', delay: 400 },
                { number: 50, label: 'Trusted Partners', delay: 600 }
            ]
        };
    },

    methods: {
        animateStats() {
            const statNumbers = document.querySelectorAll('.stat-number');
            statNumbers.forEach(stat => {
                const target = parseInt(stat.getAttribute('data-count'));
                let count = 0;
                const increment = target / 100;

                const timer = setInterval(() => {
                    count += increment;
                    if (count >= target) {
                        stat.textContent = target + (stat.parentElement.querySelector('.stat-label').textContent.includes('Satisfaction') ? '%' : '+');
                        clearInterval(timer);
                    } else {
                        stat.textContent = Math.floor(count) + (stat.parentElement.querySelector('.stat-label').textContent.includes('Satisfaction') ? '%' : '+');
                    }
                }, 20);
            });
        },
        switchChapter(chapterId, event) {
            // Add ripple effect
            const button = event.target;
            button.classList.add('ripple');
            setTimeout(() => button.classList.remove('ripple'), 600);

            // Switch chapter
            this.activeChapter = chapterId;

            // Scroll to top
            window.scrollTo({ top: 0, behavior: 'smooth' });

            // Animate pages after update
            this.$nextTick(() => {
                this.animatePages();
            });
        },

        showPhotoDetail(caption) {
            alert(`Viewing: ${caption}\n\nIn a real application, this would open a detailed photo viewer or gallery.`);
        },

        animatePages() {
            const pages = document.querySelectorAll('.page');
            pages.forEach((page, index) => {
                setTimeout(() => {
                    page.classList.add('visible');
                }, index * 200);
            });
        },

        setupIntersectionObserver() {
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };

            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('visible');
                    }
                });
            }, observerOptions);

            document.querySelectorAll('.page').forEach(page => {
                observer.observe(page);
            });
        }
    },

    mounted() {
        setTimeout(this.animatePages, 100);
        this.setupIntersectionObserver();

        // Animate stats when they come into view
        const statsSection = document.querySelector('.stats-section');
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    this.animateStats();
                    observer.unobserve(entry.target);
                }
            });
        });
        observer.observe(statsSection);
    }
}
</script>

<style scoped>
body {
    font-family: 'Georgia', serif;
    background: linear-gradient(135deg, #1a1a1a 0%, var(--charcoal) 100%);
    color: var(--cream);
    overflow-x: hidden;
    perspective: 1000px;
}

/* Header */
.header {
    text-align: center;
    padding: 3rem 2rem;
    background: linear-gradient(45deg, var(--charcoal), var(--deep-gold));
    position: relative;
    margin-bottom: 2rem;
}

.header h1 {
    font-size: 3rem;
    color: var(--primary-gold);
    margin-bottom: 0.5rem;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}

.header p {
    font-size: 1.1rem;
    color: var(--cream);
    font-style: italic;
}

/* Photo Book Container */
.photo-book {
    max-width: 1200px;
    margin: 2rem auto;
    padding: 0 2rem;
    position: relative;
}

/* Book Navigation */
.book-nav {
    display: flex;
    justify-content: center;
    gap: 1rem;
    margin-bottom: 2rem;
    flex-wrap: wrap;
}

.chapter-btn {
    padding: 0.8rem 1.5rem;
    background: linear-gradient(45deg, transparent, rgba(212, 175, 55, 0.1));
    border: 1px solid var(--primary-gold);
    border-radius: 25px;
    color: black;
    cursor: pointer;
    transition: all 0.3s ease;
    font-family: inherit;
    font-size: 0.95rem;
    position: relative;
    overflow: hidden;
}

.chapter-btn:hover,
.chapter-btn.active {
    background: var(--primary-gold);
    color: var(--charcoal);
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(212, 175, 55, 0.3);
}

.chapter-btn::before {
    content: '';
    position: absolute;
    top: 50%;
    left: 50%;
    width: 0;
    height: 0;
    background: rgba(212, 175, 55, 0.6);
    border-radius: 50%;
    transform: translate(-50%, -50%);
    transition: all 0.6s ease;
}

.chapter-btn.ripple::before {
    width: 300px;
    height: 300px;
    opacity: 0;
}

/* Book Pages */
.book-chapter {
    opacity: 0;
    transform: rotateY(-90deg);
    transition: all 0.8s ease-in-out;
    transform-origin: left center;
}

.book-chapter.active {
    opacity: 1;
    transform: rotateY(0deg);
}

/* Page Layouts */
.page {
    background: linear-gradient(145deg, var(--cream), #f8f5e6);
    border-radius: 15px;
    margin-bottom: 3rem;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
    overflow: hidden;
    position: relative;
    border: 3px solid var(--primary-gold);
    opacity: 0;
    transform: translateY(50px) rotateX(10deg);
    transition: all 0.8s ease-out;
}

.page.visible {
    opacity: 1;
    transform: translateY(0) rotateX(0);
}

.page::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(45deg, transparent 49%, rgba(212, 175, 55, 0.1) 50%, transparent 51%);
    pointer-events: none;
}

/* Page Header */
.page-header {
    background: linear-gradient(135deg, var(--charcoal), var(--deep-gold));
    color: var(--cream);
    padding: 2rem;
    text-align: center;
    position: relative;
}

.page-title {
    font-size: 2.5rem;
    font-weight: 300;
    color: var(--primary-gold);
    margin-bottom: 0.5rem;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}

.page-subtitle {
    font-size: 1.1rem;
    color: var(--cream);
    font-style: italic;
}

/* Photo Layouts */
.photo-spread {
    padding: 2rem;
    color: var(--charcoal);
}

/* Full Spread Layout */
.full-spread {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    min-height: 400px;
}

.photo-large {
    background: linear-gradient(45deg, var(--deep-gold), var(--primary-gold));
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 3rem;
    color: var(--white);
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
    position: relative;
    overflow: hidden;
    transition: all 0.3s ease;
    cursor: pointer;
}

.photo-large:hover {
    transform: scale(1.05) rotateZ(1deg);
    box-shadow: 0 15px 30px rgba(212, 175, 55, 0.4);
}

.photo-caption {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background: linear-gradient(transparent, rgba(44, 44, 44, 0.8));
    color: var(--cream);
    padding: 1rem;
    font-size: 1rem;
    text-align: center;
}

/* Grid Layout */
.photo-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
    margin-bottom: 2rem;
}

.photo-small {
    background: linear-gradient(45deg, var(--deep-gold), var(--primary-gold));
    border-radius: 8px;
    height: 400px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
    color: var(--white);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
    cursor: pointer;
}

.photo-small:hover {
    transform: scale(1.05) rotateZ(1deg);
    box-shadow: 0 5px 15px rgba(212, 175, 55, 0.4);
}

/* Story Layout */
.story-layout {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 2rem;
    align-items: center;
    margin-bottom: 20px;
}

.story-text {
    background: var(--white);
    padding: 2rem;
    border-radius: 10px;
    border-left: 4px solid var(--primary-gold);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.story-text h3 {
    color: var(--charcoal);
    font-size: 1.5rem;
    margin-bottom: 1rem;
}

.story-text p {
    color: var(--charcoal);
    line-height: 1.6;
    font-size: 1rem;
    margin-bottom: 1rem;
}

.story-text p:last-child {
    margin-bottom: 0;
}

/* Timeline Layout */
.timeline {
    position: relative;
    padding: 2rem 0;
}

.timeline::before {
    content: '';
    position: absolute;
    left: 50%;
    top: 0;
    bottom: 0;
    width: 3px;
    background: var(--primary-gold);
    transform: translateX(-50%);
}

.timeline-item {
    display: flex;
    margin-bottom: 3rem;
    position: relative;
}

.timeline-item:nth-child(odd) {
    flex-direction: row;
}

.timeline-item:nth-child(even) {
    flex-direction: row-reverse;
}

.timeline-content {
    width: 45%;
    background: var(--white);
    padding: 1.5rem;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    position: relative;
}

.timeline-content h3 {
    color: var(--charcoal);
    font-size: 1.3rem;
    margin-bottom: 0.5rem;
}

.timeline-content p {
    color: var(--charcoal);
    line-height: 1.6;
}

.timeline-photo {
    width: 80px;
    height: 80px;
    background: linear-gradient(45deg, var(--deep-gold), var(--primary-gold));
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
    color: var(--white);
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    border: 3px solid var(--cream);
    z-index: 2;
}

/* Animations */
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.fade-in-up {
    animation: fadeInUp 0.8s ease-out forwards;
}

/* Responsive Design */
@media (max-width: 768px) {
    .full-spread {
        grid-template-columns: 1fr;
        gap: 1rem;
    }

    .story-layout {
        grid-template-columns: 1fr;
    }

    .photo-grid {
        grid-template-columns: repeat(2, 1fr);
    }

    .timeline::before {
        left: 20px;
    }

    .timeline-item {
        flex-direction: row !important;
        padding-left: 50px;
    }

    .timeline-content {
        width: 100%;
    }

    .timeline-photo {
        left: 20px;
    }

    .header h1 {
        font-size: 2rem;
    }

    .page-title {
        font-size: 2rem;
    }

    .book-nav {
        gap: 0.5rem;
    }

    .chapter-btn {
        padding: 0.6rem 1rem;
        font-size: 0.85rem;
    }
}

@media (max-width: 480px) {
    .photo-book {
        padding: 0 1rem;
    }

    .header {
        padding: 2rem 1rem;
    }

    .photo-small {
        height: 140px;
    }
}
</style>