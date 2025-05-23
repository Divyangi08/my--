<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Healthcare Focus - Your Treatment Journey</title>
    <style>
        /* Global Styles */
        :root {
            --primary: #2a7fba;
            --secondary: #1a5f8b;
            --accent: #ff7e33;
            --light: #f8f9fa;
            --dark: #343a40;
            --gray: #6c757d;
            --success: #28a745;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: var(--dark);
            background-color: #f5f7fa;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        section {
            padding: 60px 0;
        }
        
        h1, h2, h3 {
            margin-bottom: 20px;
            color: var(--secondary);
        }
        
        h1 {
            font-size: 2.5rem;
        }
        
        h2 {
            font-size: 2rem;
            text-align: center;
            position: relative;
            padding-bottom: 15px;
        }
        
        h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--accent);
        }
        
        p {
            margin-bottom: 15px;
            color: var(--gray);
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--primary);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: var(--secondary);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .btn-accent {
            background-color: var(--accent);
        }
        
        .btn-accent:hover {
            background-color: #e66a22;
        }
        
        .text-center {
            text-align: center;
        }
        
        /* Header Section */
        .hero {
            background: linear-gradient(135deg, rgba(42, 127, 186, 0.9), rgba(26, 95, 139, 0.9)), url('https://images.unsplash.com/photo-1579684385127-1ef15d508118?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            color: white;
            padding: 100px 0;
            text-align: center;
        }
        
        .hero h1 {
            color: white;
            font-size: 3rem;
            margin-bottom: 30px;
        }
        
        .hero p {
            color: rgba(255, 255, 255, 0.9);
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 40px;
        }
        
        .btn-group {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }
        
        /* User Profile Section */
        .profile {
            background-color: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            margin-top: -50px;
            position: relative;
            z-index: 1;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .profile-header {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .profile-img {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background-color: var(--light);
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 20px;
            color: var(--primary);
            font-weight: bold;
            font-size: 2rem;
        }
        
        .profile-info h3 {
            margin-bottom: 5px;
        }
        
        .profile-info p {
            margin-bottom: 0;
            color: var(--gray);
        }
        
        .search-box {
            display: flex;
            margin-top: 20px;
        }
        
        .search-box input {
            flex: 1;
            padding: 12px 20px;
            border: 1px solid #ddd;
            border-radius: 50px 0 0 50px;
            outline: none;
        }
        
        .search-box button {
            padding: 12px 25px;
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: 0 50px 50px 0;
            cursor: pointer;
        }
        
        .upload-btn {
            display: block;
            width: 100%;
            padding: 15px;
            background-color: var(--light);
            border: 2px dashed #ccc;
            border-radius: 10px;
            text-align: center;
            margin-top: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .upload-btn:hover {
            border-color: var(--primary);
            background-color: rgba(42, 127, 186, 0.05);
        }
        
        /* Treatments Section */
        .treatments {
            background-color: white;
        }
        
        .treatments-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }
        
        .treatment-category {
            background-color: var(--light);
            border-radius: 10px;
            padding: 20px;
            transition: all 0.3s ease;
        }
        
        .treatment-category:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .treatment-category h3 {
            color: var(--primary);
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 1px solid #ddd;
        }
        
        .treatment-list {
            list-style: none;
        }
        
        .treatment-list li {
            margin-bottom: 8px;
            padding-left: 15px;
            position: relative;
        }
        
        .treatment-list li::before {
            content: '•';
            position: absolute;
            left: 0;
            color: var(--accent);
        }
        
        /* Hospitals Section */
        .hospitals {
            background-color: #f5f7fa;
        }
        
        .hospital-cards {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .hospital-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
        }
        
        .hospital-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .hospital-img {
            height: 200px;
            background-color: #ddd;
            background-size: cover;
            background-position: center;
        }
        
        .hospital-info {
            padding: 20px;
        }
        
        .hospital-info h3 {
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .hospital-info p {
            margin-bottom: 8px;
            display: flex;
            align-items: center;
        }
        
        .hospital-info p i {
            margin-right: 8px;
            color: var(--primary);
        }
        
        .more-details {
            display: inline-block;
            margin-top: 15px;
            color: var(--primary);
            font-weight: 600;
            text-decoration: none;
        }
        
        /* Doctors Section */
        .doctors {
            background-color: white;
        }
        
        .doctor-cards {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .doctor-card {
            background-color: var(--light);
            border-radius: 10px;
            padding: 25px;
            transition: all 0.3s ease;
        }
        
        .doctor-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .doctor-header {
            display: flex;
            margin-bottom: 20px;
        }
        
        .doctor-avatar {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            background-color: #ddd;
            margin-right: 15px;
            background-size: cover;
            background-position: center;
        }
        
        .doctor-info h3 {
            margin-bottom: 5px;
            color: var(--secondary);
        }
        
        .doctor-info p {
            color: var(--gray);
            font-size: 0.9rem;
            margin-bottom: 0;
        }
        
        .doctor-details p {
            margin-bottom: 10px;
        }
        
        .doctor-details p strong {
            color: var(--dark);
        }
        
        /* Contact Section */
        .contact {
            background-color: #f5f7fa;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-top: 40px;
        }
        
        .contact-info {
            background-color: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .contact-info h3 {
            margin-bottom: 20px;
            color: var(--secondary);
        }
        
        .contact-details p {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }
        
        .contact-details p i {
            margin-right: 10px;
            color: var(--primary);
            font-size: 1.2rem;
        }
        
        .contact-links {
            margin-top: 30px;
        }
        
        .contact-links h4 {
            margin-bottom: 15px;
            color: var(--secondary);
        }
        
        .link-list {
            list-style: none;
        }
        
        .link-list li {
            margin-bottom: 10px;
        }
        
        .link-list a {
            color: var(--gray);
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .link-list a:hover {
            color: var(--primary);
        }
        
        .bio-section {
            margin-top: 30px;
        }
        
        .bio-section h4 {
            margin-bottom: 15px;
            color: var(--secondary);
        }
        
        /* Footer */
        footer {
            background-color: var(--secondary);
            color: white;
            padding: 30px 0;
            text-align: center;
        }
        
        footer p {
            color: rgba(255, 255, 255, 0.8);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s ease;
        }
        
        .social-links a:hover {
            color: var(--accent);
        }
        
        /* Responsive Adjustments */
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .btn-group {
                flex-direction: column;
                align-items: center;
            }
            
            .profile {
                margin-top: 0;
                border-radius: 0;
            }
            
            .hospital-cards, .doctor-cards {
                grid-template-columns: 1fr;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>We Handle Everything, You Focus on Healing</h1>
            <p>Upload Your Medical Reports to Explore the Best and Most Cost-Effective Treatments in Your Language</p>
            <div class="btn-group">
                <a href="#" class="btn">Upload now</a>
                <a href="#" class="btn btn-accent">Get Started</a>
            </div>
        </div>
    </section>
    
    <!-- Profile Section -->
    <section>
        <div class="container">
            <div class="profile">
                <div class="profile-header">
                    <div class="profile-img">DM</div>
                    <div class="profile-info">
                        <h3>Divyangi Meshram</h3>
                        <p>Location: Nagpur, Maharashtra, India | Language: English, Hindi</p>
                        <p>Age: 25 years | Gender: Female</p>
                    </div>
                </div>
                <div class="search-box">
                    <input type="text" placeholder="Search Your Treatment">
                    <button><i class="fas fa-search"></i></button>
                </div>
                <div class="upload-btn">
                    <i class="fas fa-cloud-upload-alt" style="font-size: 2rem; color: var(--primary); margin-bottom: 10px;"></i>
                    <h3>Upload Your Medical Report</h3>
                    <p>Drag & drop files here or click to browse</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Treatments Section -->
    <section class="treatments">
        <div class="container">
            <h2>Start Your Journey</h2>
            <p class="text-center">Upload your medical report to receive AI-powered insights on the best treatment plans.</p>
            
            <h2 style="margin-top: 60px;">Explore more about Treatments</h2>
            <div class="treatments-grid">
                <div class="treatment-category">
                    <h3>Organ Transplant</h3>
                    <ul class="treatment-list">
                        <li>Cardiology</li>
                        <li>Neurology</li>
                        <li>Orthopedics</li>
                    </ul>
                </div>
                <div class="treatment-category">
                    <h3>Oncology</h3>
                    <ul class="treatment-list">
                        <li>Dermatology</li>
                        <li>Gastroenterology</li>
                        <li>Pulmonology</li>
                    </ul>
                </div>
                <div class="treatment-category">
                    <h3>Endocrinology</h3>
                    <ul class="treatment-list">
                        <li>Nephrology</li>
                        <li>Rheumatology</li>
                        <li>Urology</li>
                    </ul>
                </div>
                <div class="treatment-category">
                    <h3>Psychiatry</h3>
                    <ul class="treatment-list">
                        <li>Ophthalmology</li>
                        <li>Hematology</li>
                        <li>Infectious Diseases</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Hospitals Section -->
    <section class="hospitals">
        <div class="container">
            <h2>Top Hospitals</h2>
            <div class="hospital-cards">
                <div class="hospital-card">
                    <div class="hospital-img" style="background-image: url('https://images.unsplash.com/photo-1579684385127-1ef15d508118?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');"></div>
                    <div class="hospital-info">
                        <h3>Max Super Specialty Hospital</h3>
                        <p><i class="fas fa-calendar-alt"></i> Established: 2011</p>
                        <p><i class="fas fa-bed"></i> Beds: 280 | ICU: 114</p>
                        <p><i class="fas fa-map-marker-alt"></i> Location: India, India</p>
                        <a href="#" class="more-details">More details <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                <div class="hospital-card">
                    <div class="hospital-img" style="background-image: url('https://images.unsplash.com/photo-1581595219315-a187dd40c322?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');"></div>
                    <div class="hospital-info">
                        <h3>Artemis Health Institute</h3>
                        <p><i class="fas fa-calendar-alt"></i> Established: 2007</p>
                        <p><i class="fas fa-bed"></i> Beds: 400 | ICU: 64</p>
                        <p><i class="fas fa-map-marker-alt"></i> Location: Sector 51, India</p>
                        <a href="#" class="more-details">More details <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                <div class="hospital-card">
                    <div class="hospital-img" style="background-image: url('https://images.unsplash.com/photo-1530026186672-2cd00ffc50fe?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');"></div>
                    <div class="hospital-info">
                        <h3>Fortis C Doc</h3>
                        <p><i class="fas fa-calendar-alt"></i> Established: 2012</p>
                        <p><i class="fas fa-bed"></i> Beds: 23</p>
                        <p><i class="fas fa-map-marker-alt"></i> Location: New Delhi, India</p>
                        <a href="#" class="more-details">More details <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Doctors Section -->
    <section class="doctors">
        <div class="container">
            <h2>Top Doctors</h2>
            <div class="doctor-cards">
                <div class="doctor-card">
                    <div class="doctor-header">
                        <div class="doctor-avatar" style="background-image: url('https://randomuser.me/api/portraits/men/32.jpg');"></div>
                        <div class="doctor-info">
                            <h3>Dr. Ashok B C</h3>
                            <p>Plastic Surgery Specialist</p>
                        </div>
                    </div>
                    <div class="doctor-details">
                        <p><strong>Experience:</strong> 33 years of experience</p>
                        <p><strong>Hospital:</strong> Manipal Hospital Old Airport Road Bengaluru</p>
                        <p><strong>Position:</strong> HOD - Department of Plastic Surgery, Reconstructive and Aesthetic Surgery & Chief of Medical Services (at Aster Whitefield Hospital)</p>
                        <a href="#" class="more-details">More details <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                <div class="doctor-card">
                    <div class="doctor-header">
                        <div class="doctor-avatar" style="background-image: url('https://randomuser.me/api/portraits/men/45.jpg');"></div>
                        <div class="doctor-info">
                            <h3>Dr. Ranjan Shetty</h3>
                            <p>Cardiologist</p>
                        </div>
                    </div>
                    <div class="doctor-details">
                        <p><strong>Experience:</strong> 21+ years of experience in intervention...</p>
                        <p><strong>Hospital:</strong> Manipal Hospital Old Airport Road Bengaluru</p>
                        <p><strong>Position:</strong> Consultant - Interventional Cardiologist</p>
                        <a href="#" class="more-details">More details <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                <div class="doctor-card">
                    <div class="doctor-header">
                        <div class="doctor-avatar" style="background-image: url('https://randomuser.me/api/portraits/men/22.jpg');"></div>
                        <div class="doctor-info">
                            <h3>Dr. Lokesh A Veerappa</h3>
                            <p>Orthopedic Surgeon</p>
                        </div>
                    </div>
                    <div class="doctor-details">
                        <p><strong>Experience:</strong> 15 years of experience</p>
                        <p><strong>Hospital:</strong> Manipal Hospital Old Airport Road Bengaluru</p>
                        <p><strong>Position:</strong> Consultant Orthopaedic Robotic Joint Replacement</p>
                        <a href="#" class="more-details">More details <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Contact Section -->
    <section class="contact">
        <div class="container">
            <h2>Let's get in touch!</h2>
            <p class="text-center">Got questions about Treatment or Travel? Our team is here to help. Contact us for quick and friendly support.</p>
            
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Divyangi Meshram</h3>
                    <div class="contact-details">
                        <p><i class="fas fa-phone"></i> +919405468446</p>
                        <p><i class="fas fa-envelope"></i> meshramdivya693@gmail.com</p>
                        <p><i class="fas fa-map-marker-alt"></i> 512, near varsha buddha vihar, 2nd bus stop, gopal nagar, Nagpur, Maharashtra, India</p>
                    </div>
                    
                    <div class="contact-links">
                        <h4>Connect with us</h4>
                        <ul class="link-list">
                            <li><a href="#"><i class="fas fa-chevron-right"></i> Contact HCF</a></li>
                            <li><a href="#"><i class="fas fa-chevron-right"></i> Privacy Policy</a></li>
                            <li><a href="#"><i class="fas fa-chevron-right"></i> Terms of Service</a></li>
                            <li><a href="#"><i class="fas fa-chevron-right"></i> Pricing Policy</a></li>
                            <li><a href="#"><i class="fas fa-chevron-right"></i> Editor Policy</a></li>
                        </ul>
                    </div>
                    
                    <div class="bio-section">
                        <h4>Bio of HCF</h4>
                        <ul class="link-list">
                            <li><a href="#"><i class="fas fa-chevron-right"></i> Location</a></li>
                            <li><a href="#"><i class="fas fa-chevron-right"></i> Language</a></li>
                            <li><a href="#"><i class="fas fa-chevron-right"></i> Gender</a></li>
                            <li><a href="#"><i class="fas fa-chevron-right"></i> N/A</a></li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2025 Healthcare Focus. All rights reserved.</p>
            <div class="social-links">
                <a href="#"><i class="fab fa-facebook"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
        </div>
    </footer>
</body>
</html>
