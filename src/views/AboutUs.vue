<template>
    <div>
        <NavBar />
        <!-- Hero Section -->
        <section class="hero-section">
            <div class="container space-around">
                <div class="row justify-content-center ">
                    <div class="col-lg-8 text-center hero-content">
                        <h1 class="hero-title" data-aos="fade-up" data-aos-duration="1000">
                            {{ about.heroTitle }}
                        </h1>
                        <div class="golden-line" data-aos="zoom-in" data-aos-delay="500"></div>
                        <p class="hero-subtitle" data-aos="fade-up" data-aos-delay="700">
                            {{ about.heroSubtitle }}
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Our Story Section -->
        <section class="story-section section-padding">
            <div class="container">
                <h2 class="section-title" data-aos="fade-up">Our Story</h2>
                <div class="row justify-content-center">
                            <img src="../assets/eventlord1.png" class="img-fluid image-size"/>
                        <div class="col-lg-10">
                            <div class="story-content" data-aos="fade-up" data-aos-delay="200">
                                <p>
                                    Founded with a passion for creating <span class="story-highlight">extraordinary
                                        moments</span>,
                                    our luxury event planning company has been transforming dreams into reality since 2020.
                                    What started as a vision to bring unparalleled elegance to life's most precious
                                    celebrations
                                    has evolved into a premier destination for discerning clients who demand nothing but
                                    perfection.
                                </p>
                                <p>
                                    Our journey began when our founder recognized the need for a truly personalized approach
                                    to
                                    luxury events.
                                    We believe that every celebration tells a unique story, and our role is to ensure that
                                    story
                                    is told with
                                    <span class="story-highlight">sophistication, style, and impeccable attention to
                                        detail</span>.
                                </p>
                                <p>
                                    Today, we stand as trusted partners to clients who appreciate the finer things in life.
                                    From intimate gatherings to grand celebrations, we craft experiences that not only meet
                                    expectations
                                    but exceed them in ways that create lasting memories for generations to come.
                                </p>
                            </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Our Values Section -->
        <section class="values-section section-padding">
            <div class="container">
                <h2 class="section-title" data-aos="fade-up">Our Values</h2>
                <div class="row">
                    <div class="col-lg-4" v-for="(value, index) in values" :key="value.id" style="margin-top: 10px">
                        <div class="value-card" data-aos="fade-up" :data-aos-delay="index * 200">
                            <i :class="value.icon" class="value-icon"></i>
                            <h3 class="value-title">{{ value.title }}</h3>
                            <p class="value-description">{{ value.description }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Our Journey Timeline -->
        <section class="story-section section-padding">
            <div class="container">
                <h2 class="section-title" data-aos="fade-up">Our Journey</h2>
                <div class="timeline">
                    <div class="timeline-item" v-for="(milestone, index) in timeline" :key="milestone.year">
                        <div class="timeline-year" data-aos="zoom-in" :data-aos-delay="index * 200">
                            {{ milestone.year }}
                        </div>
                        <div class="timeline-content" :data-aos="index % 2 === 0 ? 'fade-right' : 'fade-left'"
                            :data-aos-delay="index * 200">
                            <h4 class="timeline-title">{{ milestone.title }}</h4>
                            <p class="timeline-description">{{ milestone.description }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <FooterView />
    </div>
</template>

<script>
import NavBar from '../components/NavBar.vue';
import FooterView from '../components/FooterView.vue';

export default {
    name: 'AboutUs',
    components: { NavBar, FooterView },
    data() {
        return {
            about: {
                heroTitle: 'About Our Legacy',
                heroSubtitle: 'Crafting Moments That Last a Lifetime'
            },
            values: [
                {
                    id: 1,
                    icon: 'fas fa-gem',
                    title: 'Excellence',
                    description: 'We pursue perfection in every detail, ensuring that each event reflects the highest standards of luxury and sophistication.'
                },
                {
                    id: 2,
                    icon: 'fas fa-heart',
                    title: 'Passion',
                    description: 'Our love for creating extraordinary experiences drives us to go beyond expectations and deliver truly memorable celebrations.'
                },
                {
                    id: 3,
                    icon: 'fas fa-handshake',
                    title: 'Trust',
                    description: 'We build lasting relationships with our clients through transparency, reliability, and unwavering commitment to their vision.'
                },
                {
                    id: 4,
                    icon: 'fas fa-lightbulb',
                    title: 'Innovation',
                    description: 'We constantly evolve our approach, incorporating the latest trends and technologies to create cutting-edge event experiences.'
                },
                {
                    id: 5,
                    icon: 'fas fa-award',
                    title: 'Quality',
                    description: 'From vendor selection to final execution, we maintain the highest quality standards in every aspect of event planning.'
                },
                {
                    id: 6,
                    icon: 'fas fa-users',
                    title: 'Collaboration',
                    description: 'We work closely with our clients as partners, ensuring their vision and preferences guide every decision we make.'
                }
            ],
            timeline: [
                {
                    year: '2020',
                    title: 'The Beginning',
                    description: 'Founded with a vision to transform luxury event planning, starting with intimate celebrations and building a reputation for excellence.'
                },
                {
                    year: '2022',
                    title: 'Expansion',
                    description: 'Expanded our services to include large-scale galas and corporate events, establishing partnerships with premium venues across the region.'
                },
                {
                    year: '2023',
                    title: 'Adaptation',
                    description: 'Successfully adapted to changing times by developing new event formats while maintaining our signature luxury standards.'
                },
                {
                    year: '2024',
                    title: 'Excellence',
                    description: 'Celebrating over 100 successful luxury events and expanding our team of specialized event professionals.'
                },
                {
                    year: '2025',
                    title: 'Recognition',
                    description: 'Received industry recognition for outstanding service and innovation, becoming the preferred choice for high-profile celebrations.'
                }
            ],
        }
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
        }
    },
    mounted() {
        // Initialize AOS
        AOS.init({
            duration: 1000,
            once: true,
            easing: 'ease-out-cubic'
        });

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

<style>
.hero-section {
    background: linear-gradient(135deg, var(--charcoal) 0%, var(--deep-gold) 100%);
    min-height: 70vh;
    display: flex;
    align-items: center;
    position: relative;
}

.hero-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="luxury-pattern" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse"><circle cx="10" cy="10" r="1" fill="%23D4AF37" opacity="0.1"/></pattern></defs><rect width="100" height="100" fill="url(%23luxury-pattern)"/></svg>');
    opacity: 0.3;
}

.hero-content {
    position: relative;
    z-index: 2;
}

.space-around {
    margin: 20px;
}

.hero-title {
    font-family: 'Playfair Display', serif;
    font-size: 4rem;
    font-weight: 700;
    color: var(--primary-gold);
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
    margin-bottom: 1rem;
}

.hero-subtitle {
    font-size: 1.5rem;
    color: var(--cream);
    font-weight: 300;
}

.golden-line {
    width: 100px;
    height: 3px;
    background: var(--primary-gold);
    margin: 2rem 0;
    position: relative;
}

.golden-line::before,
.golden-line::after {
    content: '';
    position: absolute;
    width: 10px;
    height: 10px;
    background: var(--primary-gold);
    border-radius: 50%;
    top: -3.5px;
}

.golden-line::before {
    left: -15px;
}

.golden-line::after {
    right: -15px;
}

.section-padding {
    padding: 100px 0;
}

.section-title {
    font-family: 'Playfair Display', serif;
    font-size: 3rem;
    color: var(--charcoal);
    text-align: center;
    margin-bottom: 4rem;
    position: relative;
}

.story-section {
    background: var(--white);
}

.story-content {
    font-size: 1.2rem;
    line-height: 2;
    color: var(--charcoal);
    margin-bottom: 2rem;
}

.story-highlight {
    font-style: italic;
    color: var(--deep-gold);
    font-weight: 600;
}

.values-section {
    background: var(--cream);
}

.value-card {
    background: var(--white);
    border-radius: 20px;
    padding: 3rem;
    margin-bottom: 2rem;
    box-shadow: 0 10px 30px rgba(44, 44, 44, 0.1);
    border: 2px solid transparent;
    transition: all 0.4s ease;
    position: relative;
    overflow: hidden;
    height: 100%;
}

.value-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(212, 175, 55, 0.1), transparent);
    transition: left 0.6s ease;
}

.value-card:hover::before {
    left: 100%;
}

.value-card:hover {
    transform: translateY(-10px);
    border-color: var(--primary-gold);
    box-shadow: 0 20px 40px rgba(212, 175, 55, 0.2);
}

.value-icon {
    font-size: 3rem;
    color: var(--primary-gold);
    margin-bottom: 1.5rem;
    display: block;
    text-align: center;
}

.value-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.8rem;
    color: var(--charcoal);
    margin-bottom: 1rem;
    text-align: center;
}

.value-description {
    color: var(--charcoal);
    line-height: 1.8;
    text-align: center;
}

.cta-section {
    background: linear-gradient(135deg, var(--deep-gold), var(--primary-gold));
    padding: 80px 0;
    text-align: center;
}

.cta-title {
    font-family: 'Playfair Display', serif;
    font-size: 2.5rem;
    color: var(--white);
    margin-bottom: 2rem;
}

.luxury-btn {
    background: var(--white);
    color: var(--charcoal);
    padding: 15px 40px;
    border: none;
    border-radius: 50px;
    font-size: 1.1rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
    text-transform: uppercase;
    letter-spacing: 1px;
    position: relative;
    overflow: hidden;
}

.luxury-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
    background: var(--cream);
}

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
    width: 2px;
    background: var(--primary-gold);
    transform: translateX(-50%);
}

.timeline-item {
    position: relative;
    margin-bottom: 4rem;
}

.timeline-content {
    background: var(--white);
    padding: 2rem;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(44, 44, 44, 0.1);
    border: 2px solid var(--primary-gold);
    width: 40%;
    position: relative;
}

.timeline-item:nth-child(odd) .timeline-content {
    margin-left: auto;
}

.timeline-year {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    background: var(--primary-gold);
    color: var(--white);
    padding: 1rem;
    border-radius: 50%;
    width: 80px;
    height: 80px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    font-size: 1.1rem;
}

.timeline-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    color: var(--charcoal);
    margin-bottom: 1rem;
}

.timeline-description {
    color: var(--charcoal);
    line-height: 1.8;
}

@media (max-width: 768px) {
    .hero-title {
        font-size: 2.5rem;
    }

    .hero-subtitle {
        font-size: 1.2rem;
    }

    .section-title {
        font-size: 2rem;
    }

    .timeline::before {
        left: 20px;
    }

    .timeline-content {
        width: calc(100% - 90px);
    }

    .timeline-year {
        left: 20px;
        transform: translateX(-50%);
    }
}</style>