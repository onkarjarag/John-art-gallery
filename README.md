<!DOCTYPE html> 
<html lang="en"> 
<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    <title>Artistry Gallery | Discover & Showcase</title> 
    <link rel="stylesheet" 
href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"> 
    <link 
href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Ra
 leway:wght@300;400;600&display=swap" rel="stylesheet"> 
    <style> 
        :root { 
            --dark-bg: #121212; 
            --dark-accent: #1e1e1e; 
            --primary: #e63946; 
            --secondary: #457b9d; 
            --gold: #e9c46a; 
            --light: #f8f9fa; 
            --transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275); 
        } 
         
        * { 
            margin: 0; 
            padding: 0; 
            box-sizing: border-box; 
        } 
         
        body { 
            font-family: 'Raleway', sans-serif; 
            background-color: var(--dark-bg); 
            color: var(--light); 
            line-height: 1.6; 
            overflow-x: hidden; 
        } 
         
        h1, h2, h3, h4, h5 { 
            font-family: 'Playfair Display', serif; 
            font-weight: 700; 
            letter-spacing: 1px; 
        } 
         
        .container { 
            width: 90%; 
            max-width: 1400px; 
            margin: 0 auto; 
        } 
         
        /* Header & Navigation */ 
        header { 
            background: rgba(18, 18, 18, 0.95); 
            backdrop-filter: blur(10px); 
            position: fixed; 
            width: 100%; 
            z-index: 1000; 
            padding: 20px 0; 
            border-bottom: 1px solid rgba(255, 255, 255, 0.1); 
        } 
         
        .nav-container { 
            display: flex; 
            justify-content: space-between; 
            align-items: center; 
        } 
         
        .logo { 
            font-family: 'Playfair Display', serif; 
            font-size: 2.2rem; 
            font-weight: 900; 
            background: linear-gradient(45deg, var(--gold), var(--primary)); 
            -webkit-background-clip: text; 
            -webkit-text-fill-color: transparent; 
            text-decoration: none; 
        } 
         
        .nav-links { 
            display: flex; 
            list-style: none; 
            gap: 30px; 
        } 
         
        .nav-links a { 
            color: var(--light); 
            text-decoration: none; 
            font-weight: 400; 
            text-transform: uppercase; 
            letter-spacing: 1px; 
            font-size: 0.9rem; 
            transition: var(--transition); 
            position: relative; 
            padding: 5px 0; 
        } 
         
        .nav-links a:after { 
            content: ''; 
            position: absolute; 
            bottom: 0; 
            left: 0; 
            width: 0; 
            height: 1px; 
            background: var(--gold); 
            transition: var(--transition); 
        } 
         
        .nav-links a:hover:after { 
            width: 100%; 
        } 
         
        .nav-links a:hover { 
            color: var(--gold); 
        } 
         
        .user-actions { 
            display: flex; 
            gap: 15px; 
        } 
         
        .btn { 
            padding: 10px 25px; 
            border-radius: 30px; 
            text-decoration: none; 
            font-weight: 600; 
            text-transform: uppercase; 
            letter-spacing: 1px; 
            font-size: 0.85rem; 
            transition: var(--transition); 
            display: inline-block; 
        } 
         
        .btn-outline { 
            border: 2px solid var(--gold); 
            color: var(--gold); 
            background: transparent; 
        } 
         
        .btn-outline:hover { 
            background: var(--gold); 
            color: var(--dark-bg); 
        } 
         
        .btn-primary { 
            background: var(--primary); 
            color: var(--light); 
            border: 2px solid var(--primary); 
        } 
         
        .btn-primary:hover { 
            background: transparent; 
            color: var(--primary); 
        } 
         
        /* Hero Section */ 
        .hero { 
            min-height: 100vh; 
            display: flex; 
            align-items: center; 
            padding-top: 80px; 
            position: relative; 
            overflow: hidden; 
        } 
         
        .hero-content { 
            max-width: 650px; 
            z-index: 2; 
            padding: 40px 0; 
        } 
         
        .hero h1 { 
            font-size: 4.5rem; 
            line-height: 1.1; 
            margin-bottom: 25px; 
            background: linear-gradient(45deg, var(--light), var(--gold)); 
            -webkit-background-clip: text; 
            -webkit-text-fill-color: transparent; 
        } 
         
        .hero p { 
            font-size: 1.2rem; 
            margin-bottom: 40px; 
            opacity: 0.9; 
        } 
         
        .hero-btns { 
            display: flex; 
            gap: 20px; 
        } 
         
        .hero-bg { 
            position: absolute; 
            top: 0; 
            right: 0; 
            height: 100%; 
            width: 50%; 
            background: linear-gradient(45deg, var(--dark-accent), var(--dark-bg)); 
            clip-path: polygon(25% 0%, 100% 0%, 100% 100%, 0% 100%); 
            z-index: 1; 
        } 
         
        .floating-art { 
            position: absolute; 
            z-index: 3; 
            transition: var(--transition); 
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5); 
            border: 5px solid rgba(255, 255, 255, 0.05); 
        } 
         
        .art-1 { 
            top: 20%; 
            right: 10%; 
            width: 300px; 
            transform: rotate(5deg); 
        } 
         
        .art-2 { 
            top: 50%; 
            right: 25%; 
            width: 250px; 
            transform: rotate(-3deg); 
        } 
         
        .art-3 { 
            top: 30%; 
            right: 5%; 
            width: 200px; 
            transform: rotate(8deg); 
        } 
         
        /* Gallery Section */ 
        .section { 
            padding: 100px 0; 
        } 
         
        .section-title { 
            text-align: center; 
            margin-bottom: 70px; 
        } 
         
        .section-title h2 { 
            font-size: 2.8rem; 
            margin-bottom: 15px; 
            position: relative; 
            display: inline-block; 
        } 
         
        .section-title h2:after { 
            content: ''; 
            position: absolute; 
            bottom: -10px; 
            left: 50%; 
            transform: translateX(-50%); 
            width: 100px; 
            height: 3px; 
            background: var(--gold); 
        } 
         
        .section-title p { 
            max-width: 600px; 
            margin: 25px auto 0; 
            opacity: 0.8; 
        } 
         
        .gallery-filters { 
            display: flex; 
            justify-content: center; 
            gap: 15px; 
            margin-bottom: 50px; 
            flex-wrap: wrap; 
        } 
         
        .filter-btn { 
            background: var(--dark-accent); 
            color: var(--light); 
            border: none; 
            padding: 10px 25px; 
            border-radius: 30px; 
            cursor: pointer; 
            transition: var(--transition); 
            font-family: 'Raleway', sans-serif; 
            font-size: 0.9rem; 
        } 
         
        .filter-btn.active, .filter-btn:hover { 
            background: var(--gold); 
            color: var(--dark-bg); 
        } 
         
        .gallery-grid { 
            display: grid; 
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); 
            gap: 30px; 
        } 
         
        .art-card { 
            background: var(--dark-accent); 
            border-radius: 10px; 
            overflow: hidden; 
            transition: var(--transition); 
            transform: translateY(0); 
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3); 
        } 
         
        .art-card:hover { 
            transform: translateY(-10px); 
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4); 
        } 
         
        .art-img { 
            width: 100%; 
            height: 300px; 
            background-size: cover; 
            background-position: center; 
            position: relative; 
        } 
         
        .art-overlay { 
            position: absolute; 
            top: 0; 
            left: 0; 
            width: 100%; 
            height: 100%; 
            background: rgba(0, 0, 0, 0.5); 
            display: flex; 
            align-items: center; 
            justify-content: center; 
            opacity: 0; 
            transition: var(--transition); 
        } 
         
        .art-card:hover .art-overlay { 
            opacity: 1; 
        } 
         
        .view-btn { 
            background: var(--gold); 
            color: var(--dark-bg); 
            border: none; 
            padding: 12px 25px; 
            border-radius: 30px; 
            cursor: pointer; 
            font-weight: 600; 
            font-family: 'Raleway', sans-serif; 
            transition: var(--transition); 
        } 
         
        .view-btn:hover { 
            transform: scale(1.05); 
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2); 
        } 
         
        .art-info { 
            padding: 20px; 
        } 
         
        .art-info h3 { 
            font-size: 1.4rem; 
            margin-bottom: 10px; 
        } 
         
        .artist-info { 
            display: flex; 
            align-items: center; 
            margin-top: 15px; 
            padding-top: 15px; 
            border-top: 1px solid rgba(255, 255, 255, 0.1); 
        } 
         
        .artist-avatar { 
            width: 40px; 
            height: 40px; 
            border-radius: 50%; 
            background-size: cover; 
            margin-right: 15px; 
        } 
         
        /* Artists Section */ 
        .artists-grid { 
            display: grid; 
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); 
            gap: 30px; 
        } 
         
        .artist-card { 
            background: var(--dark-accent); 
            border-radius: 10px; 
            padding: 30px; 
            text-align: center; 
            transition: var(--transition); 
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3); 
        } 
         
        .artist-card:hover { 
            transform: translateY(-10px); 
        } 
         
        .artist-avatar-lg { 
            width: 120px; 
            height: 120px; 
            border-radius: 50%; 
            background-size: cover; 
            margin: 0 auto 20px; 
            border: 3px solid var(--gold); 
        } 
         
        .artist-name { 
            font-size: 1.4rem; 
            margin-bottom: 10px; 
        } 
         
        .artist-stats { 
            display: flex; 
            justify-content: center; 
            gap: 25px; 
            margin-top: 20px; 
        } 
         
        .stat { 
            text-align: center; 
        } 
         
        .stat-value { 
            font-size: 1.5rem; 
            font-weight: 700; 
            color: var(--gold); 
        } 
         
        .stat-label { 
            font-size: 0.85rem; 
            opacity: 0.7; 
            text-transform: uppercase; 
            letter-spacing: 1px; 
        } 
         
        /* CTA Section */ 
        .cta { 
            background: linear-gradient(rgba(30, 30, 30, 0.9), rgba(30, 30, 30, 0.9)), 
url('https://images.unsplash.com/photo-1547891654-e66ed7ebb968?ixlib=rb-4.0.3') 
center/cover; 
            text-align: center; 
            padding: 120px 0; 
            border-radius: 20px; 
            margin: 100px 0; 
        } 
         
        .cta h2 { 
            font-size: 3.2rem; 
            margin-bottom: 25px; 
        } 
         
        .cta p { 
            max-width: 600px; 
            margin: 0 auto 40px; 
            font-size: 1.1rem; 
        } 
         
        /* Footer */ 
        footer { 
            background: var(--dark-accent); 
            padding: 70px 0 30px; 
        } 
         
        .footer-grid { 
            display: grid; 
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); 
            gap: 40px; 
            margin-bottom: 60px; 
        } 
         
        .footer-col h3 { 
            font-size: 1.4rem; 
            margin-bottom: 25px; 
            position: relative; 
            padding-bottom: 15px; 
        } 
         
        .footer-col h3:after { 
            content: ''; 
            position: absolute; 
            bottom: 0; 
            left: 0; 
            width: 50px; 
            height: 2px; 
            background: var(--gold); 
        } 
         
        .footer-links { 
            list-style: none; 
        } 
         
        .footer-links li { 
            margin-bottom: 12px; 
        } 
         
        .footer-links a { 
            color: var(--light); 
            text-decoration: none; 
            opacity: 0.8; 
            transition: var(--transition); 
        } 
         
        .footer-links a:hover { 
            opacity: 1; 
            color: var(--gold); 
            padding-left: 5px; 
        } 
         
        .social-links { 
            display: flex; 
            gap: 15px; 
            margin-top: 20px; 
        } 
         
        .social-links a { 
            display: flex; 
            align-items: center; 
            justify-content: center; 
            width: 40px; 
            height: 40px; 
            border-radius: 50%; 
            background: rgba(255, 255, 255, 0.1); 
            color: var(--light); 
            transition: var(--transition); 
        } 
         
        .social-links a:hover { 
            background: var(--gold); 
            color: var(--dark-bg); 
            transform: translateY(-5px); 
        } 
         
        .copyright { 
            text-align: center; 
            padding-top: 30px; 
            border-top: 1px solid rgba(255, 255, 255, 0.1); 
            font-size: 0.9rem; 
            opacity: 0.7; 
        } 
         
        /* Responsive */ 
        @media (max-width: 992px) { 
            .hero h1 { 
                font-size: 3.5rem; 
            } 
             
            .art-1, .art-2, .art-3 { 
                display: none; 
            } 
             
            .hero-bg { 
                width: 100%; 
                clip-path: none; 
                opacity: 0.3; 
            } 
        } 
         
        @media (max-width: 768px) { 
            .nav-links { 
                display: none; 
            } 
             
            .hero h1 { 
                font-size: 2.8rem; 
            } 
             
            .hero-btns { 
                flex-direction: column; 
            } 
             
            .gallery-grid { 
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); 
            } 
        } 
    </style> 
</head> 
<body> 
    <!-- Header --> 
    <header> 
        <div class="container nav-container"> 
            <a href="#" class="logo">Artistry</a> 
            <ul class="nav-links"> 
                <li><a href="#">Gallery</a></li> 
                <li><a href="#">Artists</a></li> 
                <li><a href="#">Collections</a></li> 
                <li><a href="#">Exhibitions</a></li> 
                <li><a href="#">About</a></li> 
            </ul> 
            <div class="user-actions"> 
                <a href="#" class="btn btn-outline">Login</a> 
                <a href="#" class="btn btn-primary">Sign Up</a> 
            </div> 
        </div> 
    </header> 
 
    <!-- Hero Section --> 
    <section class="hero"> 
        <div class="container"> 
            <div class="hero-content"> 
                <h1>Where Art Finds Its Audience</h1> 
                <p>Discover and showcase exceptional artwork in a community built for artists and art 
lovers. Join thousands of creators sharing their vision with the world.</p> 
                <div class="hero-btns"> 
                    <a href="#" class="btn btn-primary">Explore Gallery</a> 
                    <a href="#" class="btn btn-outline">Join as Artist</a> 
                </div> 
            </div> 
        </div> 
        <div class="hero-bg"></div> 
        <div class="floating-art art-1" style="background: 
url('https://images.unsplash.com/photo-1579783902614-a3fb3927b6a5?ixlib=rb-4.0.3') 
center/cover;"></div> 
        <div class="floating-art art-2" style="background: 
url('https://images.unsplash.com/photo-1543857778-c4a1a569e7bd?ixlib=rb-4.0.3') 
center/cover;"></div> 
        <div class="floating-art art-3" style="background: 
url('https://images.unsplash.com/photo-1578301978693-85fa9c0320b9?ixlib=rb-4.0.3') 
center/cover;"></div> 
    </section> 
 
    <!-- Featured Artworks --> 
    <section class="section"> 
        <div class="container"> 
            <div class="section-title"> 
                <h2>Featured Artworks</h2> 
                <p>Discover the most captivating pieces from our talented community of artists</p> 
            </div> 
             
            <div class="gallery-filters"> 
                <button class="filter-btn active">All</button> 
                <button class="filter-btn">Painting</button> 
                <button class="filter-btn">Photography</button> 
                <button class="filter-btn">Digital</button> 
                <button class="filter-btn">Sculpture</button> 
            </div> 
             
            <div class="gallery-grid"> 
                <div class="art-card"> 
                    <div class="art-img" style="background: 
url('https://images.unsplash.com/photo-1578926375605-eaf7559b1458?ixlib=rb-4.0.3') 
center/cover;"> 
                        <div class="art-overlay"> 
                            <button class="view-btn">View Artwork</button> 
                        </div> 
                    </div> 
                    <div class="art-info"> 
                        <h3>Whispers of the Forest</h3> 
                        <p>Oil on canvas, 2023</p> 
                        <div class="artist-info"> 
                            <div class="artist-avatar" style="background: 
url('https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-4.0.3') 
center/cover;"></div> 
                            <span>Sophie Williams</span> 
                        </div> 
                    </div> 
                </div> 
                 
                <div class="art-card"> 
                    <div class="art-img" style="background: 
url('https://images.unsplash.com/photo-1501084817091-a4f3d1d19e07?ixlib=rb-4.0.3') 
center/cover;"> 
                        <div class="art-overlay"> 
                            <button class="view-btn">View Artwork</button> 
                        </div> 
                    </div> 
                    <div class="art-info"> 
                        <h3>Urban Reflections</h3> 
                        <p>Digital art, 2023</p> 
                        <div class="artist-info"> 
                            <div class="artist-avatar" style="background: 
url('https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3') 
center/cover;"></div> 
                            <span>Marcus Chen</span> 
                        </div> 
                    </div> 
                </div> 
                 
                <div class="art-card"> 
                    <div class="art-img" style="background: 
url('https://images.unsplash.com/photo-1541963463532-d68292c34b19?ixlib=rb-4.0.3') 
center/cover;"> 
                        <div class="art-overlay"> 
                            <button class="view-btn">View Artwork</button> 
                        </div> 
                    </div> 
                    <div class="art-info"> 
                        <h3>Silent Reader</h3> 
                        <p>Watercolor, 2023</p> 
                        <div class="artist-info"> 
                            <div class="artist-avatar" style="background: 
url('https://images.unsplash.com/photo-1519085360753-af0119f7cbe7?ixlib=rb-4.0.3') 
center/cover;"></div> 
                            <span>Elena Rodriguez</span> 
                        </div> 
                    </div> 
                </div> 
            </div> 
        </div> 
    </section> 
 
    <!-- Featured Artists --> 
    <section class="section"> 
        <div class="container"> 
            <div class="section-title"> 
                <h2>Featured Artists</h2> 
                <p>Meet the talented creators behind the masterpieces</p> 
            </div> 
             
            <div class="artists-grid"> 
                <div class="artist-card"> 
                    <div class="artist-avatar-lg" style="background: 
url('https://images.unsplash.com/photo-1508214751196-bcfd4ca60f91?ixlib=rb-4.0.3') 
center/cover;"></div> 
                    <h3 class="artist-name">Alex Morgan</h3> 
                    <p>Abstract Painter</p> 
                    <div class="artist-stats"> 
                        <div class="stat"> 
                            <div class="stat-value">127</div> 
                            <div class="stat-label">Artworks</div> 
                        </div> 
                        <div class="stat"> 
                            <div class="stat-value">4.9</div> 
                            <div class="stat-label">Rating</div> 
                        </div> 
                    </div> 
                </div> 
                 
                <div class="artist-card"> 
                    <div class="artist-avatar-lg" style="background: 
url('https://images.unsplash.com/photo-1567532939604-b6b5b0e160de?ixlib=rb-4.0.3') 
center/cover;"></div> 
                    <h3 class="artist-name">Jamal Wright</h3> 
                    <p>Digital Artist</p> 
                    <div class="artist-stats"> 
                        <div class="stat"> 
                            <div class="stat-value">89</div> 
                            <div class="stat-label">Artworks</div> 
                        </div> 
                        <div class="stat"> 
                            <div class="stat-value">4.8</div> 
                            <div class="stat-label">Rating</div> 
                        </div> 
                    </div> 
                </div> 
                 
                <div class="artist-card"> 
                    <div class="artist-avatar-lg" style="background: 
url('https://images.unsplash.com/photo-1614289371518-722f2615943d?ixlib=rb-4.0.3') 
center/cover;"></div> 
                    <h3 class="artist-name">Priya Sharma</h3> 
                    <p>Mixed Media</p> 
                    <div class="artist-stats"> 
                        <div class="stat"> 
                            <div class="stat-value">204</div> 
                            <div class="stat-label">Artworks</div> 
                        </div> 
                        <div class="stat"> 
                            <div class="stat-value">5.0</div> 
                            <div class="stat-label">Rating</div> 
                        </div> 
                    </div> 
                </div> 
                 
                <div class="artist-card"> 
                    <div class="artist-avatar-lg" style="background: 
url('https://images.unsplash.com/photo-1560250097-0b93528c311a?ixlib=rb-4.0.3') 
center/cover;"></div> 
                    <h3 class="artist-name">Thomas Dubois</h3> 
                    <p>Sculptor</p> 
                    <div class="artist-stats"> 
                        <div class="stat"> 
                            <div class="stat-value">56</div> 
                            <div class="stat-label">Artworks</div> 
                        </div> 
                        <div class="stat"> 
                            <div class="stat-value">4.7</div> 
                            <div class="stat-label">Rating</div> 
                        </div> 
                    </div> 
                </div> 
            </div> 
        </div> 
    </section> 
 
    <!-- CTA Section --> 
    <section class="section"> 
        <div class="container"> 
            <div class="cta"> 
                <h2>Ready to Showcase Your Art?</h2> 
                <p>Join our community of artists and art lovers. Create your portfolio, connect with 
collectors, and share your creative journey.</p> 
                <a href="#" class="btn btn-primary">Create Your Profile</a> 
            </div> 
        </div> 
    </section> 
 
    <!-- Footer --> 
    <footer> 
        <div class="container"> 
            <div class="footer-grid"> 
                <div class="footer-col"> 
                    <a href="#" class="logo">Artistry</a> 
                    <p>Connecting artists and art enthusiasts in a vibrant creative ecosystem.</p> 
                    <div class="social-links"> 
                        <a href="#"><i class="fab fa-instagram"></i></a> 
                        <a href="#"><i class="fab fa-facebook-f"></i></a> 
                        <a href="#"><i class="fab fa-twitter"></i></a> 
                        <a href="#"><i class="fab fa-pinterest"></i></a> 
                    </div> 
                </div> 
                 
                <div class="footer-col"> 
                    <h3>Explore</h3> 
                    <ul class="footer-links"> 
                        <li><a href="#">Gallery</a></li> 
                        <li><a href="#">Artists</a></li> 
                        <li><a href="#">Collections</a></li> 
                        <li><a href="#">Exhibitions</a></li> 
                        <li><a href="#">Events</a></li> 
                    </ul> 
                </div> 
                 
                <div class="footer-col"> 
                    <h3>Resources</h3> 
                    <ul class="footer-links"> 
                        <li><a href="#">For Artists</a></li> 
                        <li><a href="#">For Collectors</a></li> 
                        <li><a href="#">Blog</a></li> 
                        <li><a href="#">Tutorials</a></li> 
                        <li><a href="#">Help Center</a></li> 
                    </ul> 
                </div> 
                 
                <div class="footer-col"> 
                    <h3>Contact</h3> 
                    <ul class="footer-links"> 
                        <li><a href="#">info@artistrygallery.com</a></li> 
                        <li><a href="#">+1 (555) 123-4567</a></li> 
                        <li><a href="#">123 Art Street, Creative City</a></li> 
                    </ul> 
                </div> 
            </div> 
             
            <div class="copyright"> 
                <p>&copy; 2023 Artistry Gallery. All rights reserved.</p> 
            </div> 
        </div> 
    </footer> 
 
    <script> 
        // Simple animations and interactions 
        document.addEventListener('DOMContentLoaded', function() { 
            // Filter buttons 
            const filterBtns = document.querySelectorAll('.filter-btn'); 
            filterBtns.forEach(btn => { 
                btn.addEventListener('click', function() { 
                    filterBtns.forEach(b => b.classList.remove('active')); 
                    this.classList.add('active'); 
                }); 
            }); 
             
            // Floating art hover effect 
            const floatingArts = document.querySelectorAll('.floating-art'); 
            floatingArts.forEach(art => { 
                art.addEventListener('mouseenter', function() { 
                    this.style.transform = 'scale(1.05) rotate(0deg)'; 
                    this.style.boxShadow = '0 30px 60px rgba(0, 0, 0, 0.6)'; 
                }); 
                 
                art.addEventListener('mouseleave', function() { 
                    const rotate = this.classList.contains('art-1') ? 5 :  
                                  this.classList.contains('art-2') ? -3 : 8; 
                    this.style.transform = `rotate(${rotate}deg)`; 
                    this.style.boxShadow = '0 20px 50px rgba(0, 0, 0, 0.5)'; 
                }); 
            }); 
             
            // Smooth scrolling for navigation 
            document.querySelectorAll('a[href^="#"]').forEach(anchor => { 
                anchor.addEventListener('click', function(e) { 
                    e.preventDefault(); 
                    document.querySelector(this.getAttribute('href')).scrollIntoView({ 
                        behavior: 'smooth' 
                    }); 
                }); 
            }); 
        }); 
    </script> 
</body> 
</html> 

