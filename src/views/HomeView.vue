<template>
    <div>
        <!-- Navigation -->
        <NavBar/>

        <!-- Hero Section -->
        <section id="home" class="hero">
            <div id="heroCarousel" class="carousel slide carousel-fade" data-bs-ride="carousel" data-bs-interval="6000">
                <div class="carousel-indicators hero-indicators">
                    <button type="button" data-bs-target="#heroCarousel" data-bs-slide-to="0" class="active"></button>
                    <button type="button" data-bs-target="#heroCarousel" data-bs-slide-to="1"></button>
                    <button type="button" data-bs-target="#heroCarousel" data-bs-slide-to="2"></button>
                </div>
                <div class="carousel-inner">
                    <div class="carousel-item active hero-slide-1">
                        <div class="hero-overlay"></div>
                        <div class="container">
                            <div class="row justify-content-center">
                                <div class="col-lg-8">
                                    <div class="hero-content" data-aos="fade-up" data-aos-delay="200">
                                        <h1 class="fade-in-up">-Moments & Memories-</h1>
                                        <p class="fade-in-up" style="animation-delay: 0.3s">Creating unforgettable luxury
                                            experiences across Nigeria with unparalleled elegance and sophistication</p>
                                        <button class="btn btn-luxury fade-in-up" style="animation-delay: 0.5s"
                                            @click="scrollToSection('contact')">
                                            <i class="fas fa-calendar-alt me-2"></i>Plan Your Event
                                        </button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="carousel-item hero-slide-2">
                        <div class="hero-overlay"></div>
                        <div class="container">
                            <div class="row justify-content-center">
                                <div class="col-lg-8">
                                    <div class="hero-content">
                                        <h1>Luxury Weddings</h1>
                                        <p>Where dreams become reality through meticulous planning and breathtaking design
                                            that reflects your unique love story</p>
                                        <button class="btn btn-luxury" @click="scrollToSection('services')">
                                            <i class="fas fa-heart me-2"></i>Explore Wedding Services
                                        </button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="carousel-item hero-slide-3">
                        <div class="hero-overlay"></div>
                        <div class="container">
                            <div class="row justify-content-center">
                                <div class="col-lg-8">
                                    <div class="hero-content">
                                        <h1>Corporate Excellence</h1>
                                        <p>Elevating your business events with sophisticated planning that enhances your
                                            brand and creates lasting impressions</p>
                                        <button class="btn btn-luxury" @click="scrollToSection('portfolio')">
                                            <i class="fas fa-building me-2"></i>View Our Portfolio
                                        </button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <button class="carousel-control-prev" type="button" data-bs-target="#heroCarousel" data-bs-slide="prev">
                    <span class="carousel-control-prev-icon"></span>
                </button>
                <button class="carousel-control-next" type="button" data-bs-target="#heroCarousel" data-bs-slide="next">
                    <span class="carousel-control-next-icon"></span>
                </button>
            </div>
        </section>

        <!-- Services Section -->
        <section id="services" class="services">
            <div class="container">
                <div class="row">
                    <div class="col-lg-12 text-center mb-5">
                        <h2 data-aos="fade-up" style="font-size: 3rem; color: var(--charcoal);">Our Premium Services</h2>
                        <p data-aos="fade-up" data-aos-delay="100" style="font-size: 1.2rem; color: #666;">Elevating every
                            moment with luxury and precision</p>
                    </div>
                </div>
                <div class="row">
                    <div class="col-lg-4 col-md-6 mb-4" v-for="(service, index) in services" :key="index">
                        <div class="service-card" :data-aos="'fade-up'" :data-aos-delay="index * 100">
                            <div class="service-icon floating" :style="{ animationDelay: index * 0.5 + 's' }">
                                <i :class="service.icon"></i>
                            </div>
                            <h3>{{ service.title }}</h3>
                            <p>{{ service.description }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Portfolio Carousel -->
        <section id="portfolio" class="portfolio">
            <div class="container">
                <div class="row">
                    <div class="col-lg-12 text-center mb-5">
                        <h2 data-aos="fade-up" style="font-size: 3rem;">Our Signature Events</h2>
                        <p data-aos="fade-up" data-aos-delay="100" style="font-size: 1.2rem; opacity: 0.8;">Witness the
                            magic we create</p>
                    </div>
                </div>
                <div class="row">
                    <div class="col-lg-10 mx-auto">
                        <div id="portfolioCarousel" class="carousel slide" data-bs-ride="carousel" data-aos="fade-up"
                            data-aos-delay="200">
                            <div class="carousel-indicators">
                                <button type="button" data-bs-target="#portfolioCarousel" data-bs-slide-to="0"
                                    class="active"></button>
                                <button type="button" data-bs-target="#portfolioCarousel" data-bs-slide-to="1"></button>
                                <button type="button" data-bs-target="#portfolioCarousel" data-bs-slide-to="2"></button>
                            </div>
                            <div class="carousel-inner">
                                <div class="carousel-item active portfolio-1">
                                    <div class="carousel-caption">
                                        <h3>Royal Wedding in Lagos</h3>
                                        <p>A majestic celebration bringing together tradition and modern luxury for 500
                                            distinguished guests.</p>
                                    </div>
                                </div>
                                <div class="carousel-item portfolio-2">
                                    <div class="carousel-caption">
                                        <h3>Corporate Gala in Anambra</h3>
                                        <p>An elegant evening of networking and celebration for Nigeria's top business
                                            leaders.</p>
                                    </div>
                                </div>
                                <div class="carousel-item portfolio-3">
                                    <div class="carousel-caption">
                                        <h3>Exclusive Birthday Celebration</h3>
                                        <p>A sophisticated milestone celebration with personalized luxury touches
                                            throughout.</p>
                                    </div>
                                </div>
                            </div>
                            <button class="carousel-control-prev" type="button" data-bs-target="#portfolioCarousel"
                                data-bs-slide="prev">
                                <span class="carousel-control-prev-icon"></span>
                            </button>
                            <button class="carousel-control-next" type="button" data-bs-target="#portfolioCarousel"
                                data-bs-slide="next">
                                <span class="carousel-control-next-icon"></span>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Testimonials -->
        <section id="testimonials" class="testimonials">
            <div class="container">
                <div class="row">
                    <div class="col-lg-12 text-center mb-5">
                        <h2 data-aos="fade-up" style="font-size: 3rem; color: var(--charcoal);">What Our Clients Say</h2>
                        <p data-aos="fade-up" data-aos-delay="100" style="font-size: 1.2rem; color: #666;">Testimonials from
                            our distinguished clientele</p>
                    </div>
                </div>
                <div class="row">
                    <div class="col-lg-4 mb-4" v-for="(testimonial, index) in testimonials" :key="index">
                        <div class="testimonial-card" :data-aos="'fade-up'" :data-aos-delay="index * 150">
                            <div class="stars">
                                <i class="fas fa-star" v-for="star in 5" :key="star"></i>
                            </div>
                            <p style="font-style: italic; font-size: 1.1rem;">{{ testimonial.text }}</p>
                            <div class="client-info">
                                <h5 style="color: var(--primary-gold); margin-bottom: 0;">{{ testimonial.name }}</h5>
                                <small style="color: #666;">{{ testimonial.title }}</small>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="contact">
            <div class="container">
                <div class="row">
                    <div class="col-lg-12 text-center mb-5">
                        <h2 data-aos="fade-up" style="font-size: 3rem;">Let's Create Magic Together</h2>
                        <p data-aos="fade-up" data-aos-delay="100" style="font-size: 1.2rem; opacity: 0.8;">Begin your
                            journey to an extraordinary event</p>
                    </div>
                </div>
                <div class="row justify-content-center">
                    <div class="col-lg-8">
                        <div class="contact-form" data-aos="fade-up" data-aos-delay="200">
                            <form @submit.prevent="submitForm">
                                <div class="row">
                                    <div class="col-md-6">
                                        <input type="text" class="form-control" placeholder="Your Name" v-model="form.name"
                                            required>
                                    </div>
                                    <div class="col-md-6">
                                        <input type="email" class="form-control" placeholder="Your Email"
                                            v-model="form.email" required>
                                    </div>
                                </div>
                                <div class="row">
                                    <div class="col-md-6">
                                        <input type="tel" class="form-control" placeholder="Phone Number"
                                            v-model="form.phone" required>
                                    </div>
                                    <div class="col-md-6">
                                        <select class="form-control" v-model="form.eventType" required>
                                            <option value="">Event Type</option>
                                            <option value="wedding">Wedding</option>
                                            <option value="corporate">Corporate Event</option>
                                            <option value="birthday">Birthday Celebration</option>
                                            <option value="anniversary">Anniversary</option>
                                            <option value="funeral">Funeral</option>
                                        </select>
                                    </div>
                                </div>
                                <textarea class="form-control" rows="5" placeholder="Tell us about your dream event..."
                                    v-model="form.message" required></textarea>
                                <div class="text-center mt-4">
                                    <button type="submit" class="btn btn-luxury">
                                        <i class="fas fa-paper-plane me-2"></i>Send Inquiry
                                    </button>
                                </div>
                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <FooterView/>
    </div>
</template>

<script>
import NavBar from '../components/NavBar.vue';
import FooterView from '../components/FooterView.vue';

export default {
    name: 'HomeView',
    components: {NavBar, FooterView},
    data() {

        return {
            services: [
                {
                    icon: 'fas fa-heart',
                    title: 'Luxury Weddings',
                    description: 'Bespoke wedding celebrations that reflect your unique love story with every detail perfectly orchestrated.'
                },
                {
                    icon: 'fas fa-building',
                    title: 'Corporate Events',
                    description: 'Professional gatherings that enhance your brand image and create lasting business relationships.'
                },
                {
                    icon: 'fas fa-birthday-cake',
                    title: 'Private Celebrations',
                    description: 'Intimate milestone celebrations designed to create cherished memories with your loved ones.'
                },
                {
                    icon: 'fas fa-glass-cheers',
                    title: 'Gala Dinners',
                    description: 'Sophisticated evening events that combine elegance with entertainment for an unforgettable experience.'
                },
                {
                    icon: 'fas fa-theater-masks',
                    title: 'Funerals / Memorial Events',
                    description: 'Celebrating a life well lived with the dignity it deserves. A graceful farewell, thoughtfully planned with cultural sensitivity and heartfelt detail '
                },
                {
                    icon: 'fas fa-gem',
                    title: 'Exclusive Planning',
                    description: 'Comprehensive event management from concept to completion with white-glove service throughout.'
                }
            ],
            testimonials: [
                {
                    text: "Event Lord Events transformed our daughter's wedding into a fairy tale. Every detail was perfect, from the stunning décor to the flawless coordination. Our guests are still talking about it!",
                    name: "Mrs. Adunni Okafor",
                    title: "Mother of the Bride"
                },
                {
                    text: "Our annual corporate gala was elevated to new heights thanks to their exceptional service. The attention to detail and professionalism exceeded our expectations completely.",
                    name: "Chief Executive Emeka Okoli",
                    title: "CEO, Okoli Industries"
                },
                {
                    text: "From the initial consultation to the final toast, everything was seamless. They understood our vision and brought it to life beyond what we could have imagined.",
                    name: "Dr. & Mrs. Babatunde",
                    title: "25th Anniversary Celebration"
                }
            ],
            form: {
                name: '',
                email: '',
                phone: '',
                eventType: '',
                message: ''
            }
        }
    },
    methods: {
        scrollToSection(sectionId) {
            document.getElementById(sectionId).scrollIntoView({
                behavior: 'smooth'
            });
        },
        submitForm() {
            // Simulate form submission
            alert('Thank you for your inquiry! We will redirect you to WhatsApp to complete the message.');
            let res = `Hi, my name is ${this.form.name}, I will like to inquire about an event type: ${this.form.eventType}. Here's my email address: ${this.form.email}, and phone number to contact me: ${this.form.phone}. Here's more info about my inquiry: ${this.form.message}`;
            let encodedMessage = encodeURIComponent(res);
            let phone = '2348101111091'; // Use the recipient's full WhatsApp number with country code
            let url = `https://wa.me/${phone}?text=${encodedMessage}`;

            window.open(url, '_blank');
            // Reset form
            this.form = {
                name: '',
                email: '',
                phone: '',
                eventType: '',
                message: ''
            };
        }
    },
    mounted() {
        // Initialize AOS animations
        AOS.init({
            duration: 1000,
            once: true,
            offset: 100
        });

        // Auto-start carousels
        setTimeout(() => {
            // Portfolio carousel
            const portfolioCarousel = new bootstrap.Carousel(document.getElementById('portfolioCarousel'), {
                interval: 5000,
                ride: 'carousel'
            });

            // Hero carousel
            const heroCarousel = new bootstrap.Carousel(document.getElementById('heroCarousel'), {
                interval: 6000,
                ride: 'carousel'
            });
        }, 1000);
    }
}
</script>