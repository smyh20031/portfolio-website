<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>سميحة عوض | نظم المعلومات الإدارية</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Color Palette */
        :root {
            --primary: #48b2fe;
            --primary-dark: #ffffff00;
            --dark: #fd5050;
            --white: #ffffff;
            --text: #4b4949;
            --text-light: #7f8c8d;
            --bg: #f9f9f9;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            --shadow-hover: 0 6px 12px rgba(0, 0, 0, 0.15);
            --transition: all 0.3s ease;
        }

        /* Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Tajawal', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text);
            background-color: var(--bg);
            scroll-behavior: smooth;
        }

        h1, h2, h3 {
            line-height: 1.2;
        }

        a {
            text-decoration: none;
            color: inherit;
            transition: var(--transition);
        }

        img {
            max-width: 100%;
            height: auto;
            transition: var(--transition);
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .btn {
            display: inline-block;
            padding: 0.8rem 1.5rem;
            border-radius: 4px;
            background-color: var(--primary);
            color: var(--white);
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }

        .btn:hover, .btn:focus {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: var(--shadow-hover);
            outline: none;
        }

        .section {
            padding: 4rem 0;
        }

        .section-title {
            font-size: 2rem;
            margin-bottom: 2rem;
            color: var(--dark);
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            right: 0;
            width: 60px;
            height: 4px;
            background-color: var(--primary);
            transition: var(--transition);
        }

        .section-title:hover::after {
            width: 80px;
        }

        /* Header */
        header {
            background-color: var(--dark);
            color: var(--white);
            padding: 3rem 0;
            text-align: center;
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid var(--primary);
            margin-bottom: 1.5rem;
            transition: var(--transition);
        }

        .profile-img:hover {
            transform: scale(1.05);
            box-shadow: 0 0 20px rgba(110, 72, 170, 0.6);
        }

        .header-title {
            font-size: 2.2rem;
            margin-bottom: 0.5rem;
        }

        .header-subtitle {
            font-size: 1.2rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }

        .icon {
            margin-left: 0.5rem;
        }

        /* Navigation */
        nav {
            background-color: var(--dark);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
        }

        .nav-container {
            display: flex;
            justify-content: center;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--white);
            padding: 0.5rem 1rem;
            border-radius: 4px;
            display: flex;
            align-items: center;
        }

        .nav-links a:hover {
            background-color: rgba(255, 255, 255, 0.1);
        }

        /* About Section */
        .about-content {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .skill {
            background-color: var(--primary);
            color: var(--white);
            padding: 0.5rem 1rem;
            border-radius: 20px;
            font-size: 0.9rem;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background-color: var(--white);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-hover);
        }

        .project-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .project-info {
            padding: 1.5rem;
        }

        .project-title {
            font-size: 1.3rem;
            margin-bottom: 0.8rem;
        }

        .project-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }

        /* Education Section */
        .education-item {
            background-color: var(--white);
            border-radius: 8px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            box-shadow: var(--shadow);
        }

        .degree-title {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
        }

        .university {
            color: var(--primary);
            margin-bottom: 0.5rem;
            display: block;
        }

        .date {
            color: var(--text-light);
            margin-bottom: 1rem;
            display: block;
        }

        .education-description ul {
            margin-right: 1.5rem;
            margin-bottom: 1rem;
        }

        /* Contact Section */
        .contact-content {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        .contact-form {
            background-color: var(--white);
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: var(--shadow);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        label {
            display: block;
            margin-bottom: 0.5rem;
        }

        input,
        textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-family: inherit;
        }

        textarea {
            min-height: 150px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: var(--white);
            text-align: center;
            padding: 2rem 0;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 1rem 0;
        }

        .footer-links a {
            padding: 0.5rem;
            border-radius: 4px;
            display: flex;
            align-items: center;
        }

        .footer-links a:hover {
            background-color: rgba(255, 255, 255, 0.1);
        }

        .contact-info {
            margin-top: 1.5rem;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1.5rem;
        }

        .contact-info-item {
            display: flex;
            align-items: center;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                gap: 0.5rem;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .section {
                padding: 2rem 0;
            }
            
            .section-title {
                font-size: 1.5rem;
            }
            
            .header-title {
                font-size: 1.8rem;
            }
            
            .profile-img {
                width: 120px;
                height: 120px;
            }

            .contact-info {
                flex-direction: column;
                gap: 0.5rem;
            }
        }

        @media (max-width: 480px) {
            .nav-links a {
                font-size: 0.8rem;
                padding: 0.3rem;
            }
            
            .btn {
                padding: 0.6rem 1rem;
                font-size: 0.9rem;
            }
            
            .skill {
                font-size: 0.8rem;
                padding: 0.4rem 0.8rem;
            }
            
            .footer-links {
                flex-wrap: wrap;
                gap: 0.8rem;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700&display=swap" rel="stylesheet">
</head>
<body>
    <header>
        <div class="container">
            <img src="https://images.unsplash.com/photo-1573497019940-1c28c88b4f3e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80" alt="سميحة عوض" class="profile-img">
            <h1 class="header-title">سميحة عوض توفيق عياد</h1>
            <p class="header-subtitle">
                <i class="fas fa-graduation-cap icon"></i>
                طالبة نظم المعلومات الإدارية المعاصرة | جامعة الأقصى
            </p>
            <p><i class="fas fa-map-marker-alt icon"></i> غزة، فلسطين</p>
        </div>
    </header>

    <nav>
        <div class="container nav-container">
            <ul class="nav-links">
                <li><a href="#about"><i class="fas fa-user icon"></i> عني</a></li>
                <li><a href="#skills"><i class="fas fa-tools icon"></i> المهارات</a></li>
                <li><a href="#projects"><i class="fas fa-laptop-code icon"></i> المشاريع</a></li>
                <li><a href="#education"><i class="fas fa-graduation-cap icon"></i> التعليم</a></li>
                <li><a href="#contact"><i class="fas fa-envelope icon"></i> التواصل</a></li>
            </ul>
        </div>
    </nav>

    <main>
        <section id="about" class="section">
            <div class="container">
                <h2 class="section-title">نبذة عني</h2>
                <div class="about-content">
                    <div class="about-text">
                        <p><i class="fas fa-hand-paper icon"></i> مرحباً! أنا سميحة عوض توفيق عياد، طالبة في السنة الثالثة من تخصص نظم المعلومات الإدارية المعاصرة بجامعة الأقصى.</p>
                        <p><i class="fas fa-lightbulb icon"></i> لدي شغف كبير بتطبيق المعرفة النظرية في مشاريع عملية تساهم في تحسين كفاءة المنظمات. أهتم بكل ما يتعلق بأنظمة المعلومات وتكنولوجيا الأعمال الحديثة.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="skills" class="section">
            <div class="container">
                <h2 class="section-title">المهارات والشهادات</h2>
                
                <h3><i class="fas fa-code icon"></i> لغات البرمجة</h3>
                <div class="skills">
                    <span class="skill">C# <i class="fas fa-cog icon"></i></span>
                    <span class="skill">HTML <i class="fab fa-html5 icon"></i></span>
                    <span class="skill">CSS <i class="fab fa-css3-alt icon"></i></span>
                    <span class="skill">JavaScript <i class="fab fa-js icon"></i></span>
                </div>
                
                <h3 style="margin-top: 2rem;"><i class="fas fa-chart-bar icon"></i> مهارات أخرى</h3>
                <div class="skills">
                    <span class="skill">تحليل النظم <i class="fas fa-project-diagram icon"></i></span>
                    <span class="skill">إدارة قواعد البيانات <i class="fas fa-database icon"></i></span>
                    <span class="skill">أنظمة ERP <i class="fas fa-cogs icon"></i></span>
                    <span class="skill">إدارة المشاريع <i class="fas fa-tasks icon"></i></span>
                </div>
            </div>
        </section>

        <section id="projects" class="section">
            <div class="container">
                <h2 class="section-title">مشاريعي</h2>
                <div class="projects-grid">
                    <article class="project-card">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="نظام إدارة المخزون" class="project-img">
                        <div class="project-info">
                            <h3 class="project-title"><i class="fas fa-boxes icon"></i> نظام إدارة المخزون</h3>
                            <p>تصميم وتنفيذ نظام مبسط لإدارة المخزون باستخدام Microsoft Access يتضمن تتبع المخزون، إدارة الطلبات، وإنشاء تنبيهات لإعادة الطلب.</p>
                        </div>
                    </article>
                    
                    <article class="project-card">
                        <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1415&q=80" alt="تحليل البيانات" class="project-img">
                        <div class="project-info">
                            <h3 class="project-title"><i class="fas fa-chart-line icon"></i> تحليل البيانات باستخدام Power BI</h3>
                            <p>إنشاء لوحات تحكم تفاعلية لعرض مؤشرات الأداء الرئيسية لمؤسسة افتراضية باستخدام Microsoft Power BI.</p>
                        </div>
                    </article>
                    
                    <article class="project-card">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="دراسة جدوى لنظام ERP" class="project-img">
                        <div class="project-info">
                            <h3 class="project-title"><i class="fas fa-cogs icon"></i> دراسة جدوى لنظام ERP</h3>
                            <p>إعداد دراسة جدوى لتنفيذ نظام تخطيط موارد المؤسسات (ERP) في شركة صغيرة، مع تحليل التكاليف والفوائد المتوقعة.</p>
                        </div>
                    </article>
                </div>
            </div>
        </section>

        <section id="education" class="section">
            <div class="container">
                <h2 class="section-title">التعليم</h2>
                
                <article class="education-item">
                    <h3 class="degree-title"><i class="fas fa-school icon"></i> الثانوية العامة</h3>
                    <span class="university"><i class="fas fa-university icon"></i> مدرسة بنات غزة الثانوية</span>
                    <span class="date"><i class="fas fa-calendar-alt icon"></i> تخرجت عام 2019</span>
                    <div class="education-description">
                        <p>أكملت تعليمي الثانوي بتفوق في الفرع العلمي.</p>
                        <ul>
                            <li>التركيز على الرياضيات وعلوم الحاسوب</li>
                            <li>المشاركة في مسابقات البرمجة</li>
                        </ul>
                    </div>
                </article>
                
                <article class="education-item">
                    <h3 class="degree-title"><i class="fas fa-graduation-cap icon"></i> بكالوريوس نظم المعلومات الإدارية المعاصرة</h3>
                    <span class="university"><i class="fas fa-university icon"></i> جامعة الأقصى، غزة</span>
                    <span class="date"><i class="fas fa-calendar-alt icon"></i> 2019 - حتى الآن</span>
                    <div class="education-description">
                        <p>أدرس حالياً للحصول على درجة البكالوريوس مع التركيز على نظم المعلومات وتطبيقاتها الإدارية.</p>
                        <ul>
                            <li>إدارة وتصميم قواعد البيانات</li>
                            <li>تحليل وتصميم النظم</li>
                            <li>برمجة الأعمال باستخدام C#</li>
                            <li>تطوير الويب (HTML5, CSS3, JavaScript)</li>
                        </ul>
                    </div>
                </article>
            </div>
        </section>

        <section id="contact" class="section">
            <div class="container">
                <h2 class="section-title">تواصل معي</h2>
                <div class="contact-content">
                    <div class="contact-form">
                        <form id="contactForm">
                            <div class="form-group">
                                <label for="name"><i class="fas fa-user icon"></i> اسمك</label>
                                <input type="text" id="name" required>
                            </div>
                            
                            <div class="form-group">
                                <label for="email"><i class="fas fa-envelope icon"></i> البريد الإلكتروني</label>
                                <input type="email" id="email" required>
                            </div>
                            
                            <div class="form-group">
                                <label for="message"><i class="fas fa-comment icon"></i> الرسالة</label>
                                <textarea id="message" required></textarea>
                            </div>
                            
                            <button type="submit" class="btn">
                                <i class="fas fa-paper-plane icon"></i> إرسال الرسالة
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>لنتواصل ونعمل معاً لصنع الفرق</p>
            
            <div class="footer-links">
                <a href="https://github.com" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
                    <i class="fab fa-github icon"></i> GitHub
                </a>
                <a href="https://linkedin.com" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
                    <i class="fab fa-linkedin icon"></i> LinkedIn
                </a>
                <a href="mailto:sameha.awad@example.com" aria-label="Email">
                    <i class="fas fa-envelope icon"></i> Email
                </a>
            </div>
            
            <div class="contact-info">
                <div class="contact-info-item">
                    <i class="fas fa-envelope icon"></i> sameha.awad@example.com
                </div>
                <div class="contact-info-item">
                    <i class="fas fa-map-marker-alt icon"></i> غزة، فلسطين
                </div>
                <div class="contact-info-item">
                    <i class="fas fa-phone icon"></i> 972 59-561-8818+
                </div>
            </div>
            
            <p>&copy; 2025 سميحة عوض. جميع الحقوق محفوظة.</p>
        </div>
    </footer>

    <script>
        // Simple form handler to prevent default submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('شكراً على رسالتك! سأتواصل معك قريباً.');
            this.reset();
        });
    </script>
</body>
</html>
