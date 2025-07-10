# mortgage--guide
mortgage-guide
<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>מדריך מסמכי משכנתא לחברה בע"מ</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #5a6b8a 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #5a7299 0%, #6b809e 100%);
            color: white;
            padding: 40px;
            text-align: center;
        }

        .header h1 {
            font-size: 2.5em;
            margin-bottom: 15px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .header p {
            font-size: 1.2em;
            opacity: 0.9;
        }

        .intro {
            background: #f8f9fa;
            padding: 30px;
            border-right: 5px solid #6b809e;
        }

        .intro h2 {
            color: #5a7299;
            margin-bottom: 15px;
            font-size: 1.5em;
        }

        .intro p {
            color: #555;
            font-size: 1.1em;
            line-height: 1.6;
        }

        .sections {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            padding: 40px;
        }

        .section {
            flex: 1;
            min-width: 300px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            overflow: hidden;
            transition: transform 0.3s ease;
        }

        .section:hover {
            transform: translateY(-5px);
        }

        .section-header {
            padding: 25px;
            color: white;
            text-align: center;
            position: relative;
        }

        .company-section .section-header {
            background: linear-gradient(135deg, #6b809e 0%, #5a7299 100%);
        }

        .personal-section .section-header {
            background: linear-gradient(135deg, #7a8dab 0%, #6b809e 100%);
        }

        .section-header h3 {
            font-size: 1.4em;
            margin-bottom: 10px;
        }

        .section-header .icon {
            font-size: 2.5em;
            margin-bottom: 10px;
            display: block;
        }

        .section-content {
            padding: 30px;
        }

        .document-group {
            margin-bottom: 30px;
        }

        .document-group h4 {
            color: #5a7299;
            margin-bottom: 15px;
            font-size: 1.2em;
            border-bottom: 2px solid #ecf0f1;
            padding-bottom: 8px;
        }

        .document-list {
            list-style: none;
        }

        .document-item {
            background: #f8f9fa;
            margin-bottom: 12px;
            padding: 15px;
            border-radius: 8px;
            border-right: 4px solid #6b809e;
            position: relative;
        }

        .document-item:before {
            content: "✓";
            position: absolute;
            left: 15px;
            top: 15px;
            color: #5a7299;
            font-weight: bold;
            font-size: 1.2em;
        }

        .document-item strong {
            color: #5a7299;
            display: block;
            margin-bottom: 5px;
        }

        .document-item small {
            color: #7f8c8d;
            font-style: italic;
        }

        .link-box {
            background: #e8f2f7;
            border: 1px solid #b8d4e3;
            border-radius: 8px;
            padding: 15px;
            margin-top: 15px;
        }

        .link-box a {
            color: #5a7299;
            text-decoration: none;
            font-weight: bold;
        }

        .link-box a:hover {
            text-decoration: underline;
        }

        .process-flow {
            background: #f8f9fa;
            padding: 40px;
            margin-top: 20px;
        }

        .process-flow h3 {
            text-align: center;
            color: #5a7299;
            margin-bottom: 30px;
            font-size: 1.6em;
        }

        .steps {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 20px;
        }

        .step {
            flex: 1;
            min-width: 200px;
            text-align: center;
            padding: 20px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
        }

        .step-number {
            background: #6b809e;
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 15px;
            font-weight: bold;
            font-size: 1.2em;
        }

        .step h4 {
            color: #5a7299;
            margin-bottom: 10px;
        }

        .step p {
            color: #555;
            font-size: 0.9em;
        }

        .tips {
            background: linear-gradient(135deg, #7a8dab 0%, #6b809e 100%);
            color: white;
            padding: 40px;
            margin-top: 20px;
        }

        .tips h3 {
            text-align: center;
            margin-bottom: 30px;
            font-size: 1.6em;
        }

        .tips-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .tip-item {
            background: rgba(255,255,255,0.1);
            padding: 20px;
            border-radius: 10px;
            backdrop-filter: blur(5px);
        }

        .tip-item h4 {
            margin-bottom: 10px;
            font-size: 1.1em;
        }

        .footer {
            background: #2c3e50;
            color: white;
            padding: 30px;
            text-align: center;
        }

        @media (max-width: 768px) {
            .sections {
                flex-direction: column;
                padding: 20px;
            }
            
            .steps {
                flex-direction: column;
            }
            
            .tips-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div style="display: flex; align-items: center; justify-content: center; margin-bottom: 20px; flex-wrap: wrap; gap: 20px;">
                <div style="text-align: center;">
                    <h1 style="margin: 0; font-size: 2.5em;">🏢 מדריך מסמכי משכנתא לחברה בע"מ</h1>
                    <p style="margin: 10px 0; font-size: 1.2em; opacity: 0.9;">המדריך המלא והמעשי להכנת כל המסמכים הנדרשים</p>
                </div>
            </div>
        </div>

        <div class="intro">
            <h2>🎯 מה זה משכנתא לחברה?</h2>
            <p>כאשר חברה רוכשת נכס, הבנק בוחן הן את יכולת החברה לפרוע את ההלוואה והן את האנשים שעומדים מאחוריה. לכן תצטרכו להכין מסמכים של החברה ומסמכים של הערבים האישיים.</p>
        </div>

        <div class="sections">
            <div class="section company-section">
                <div class="section-header">
                    <div class="icon">🏢</div>
                    <h3>מסמכי החברה</h3>
                    <p>הדבר הראשון להכין</p>
                </div>
                <div class="section-content">
                    <div class="document-group">
                        <h4>מסמכי זהות החברה</h4>
                        <ul class="document-list">
                            <li class="document-item">
                                <strong>תעודת התאגדות מעודכנת</strong>
                                <small>המסמך הבסיסי שמוכיח שהחברה קיימת</small>
                            </li>
                            <li class="document-item">
                                <strong>תמצית רישום עדכנית</strong>
                                <small>מראה מי המנהלים ובעלי המניות כיום - עד 3 חודשים</small>
                            </li>
                            <li class="document-item">
                                <strong>פרוטוקול מינוי מנכ"ל</strong>
                                <small>מוכיח מי רשאי לחתום בשם החברה</small>
                            </li>
                        </ul>
                        <div class="link-box">
                            💻 <a href="https://www.gov.il/he/service/company_registrar_documents_request" target="_blank">הזמנה אונליין: אתר רשם החברות</a>
                        </div>
                    </div>

                    <div class="document-group">
                        <h4>המצב הכספי</h4>
                        <ul class="document-list">
                            <li class="document-item">
                                <strong>דוחות כספיים מבוקרים</strong>
                                <small>שנתיים אחרונות - הבנק רוצה לראות שהחברה יציבה</small>
                            </li>
                            <li class="document-item">
                                <strong>דוחות רבעוניים</strong>
                                <small>השנה הנוכחית - מצב עדכני</small>
                            </li>
                            <li class="document-item">
                                <strong>דפי חשבון בנק</strong>
                                <small>6 חודשים אחרונים - הבנק בודק איך הכסף זורם</small>
                            </li>
                            <li class="document-item">
                                <strong>אישור יתרות מהבנק</strong>
                                <small>כמה כסף יש בחשבון</small>
                            </li>
                        </ul>
                    </div>

                    <div class="document-group">
                        <h4>מסמכי מס ורישיונות</h4>
                        <ul class="document-list">
                            <li class="document-item">
                                <strong>דוחות מס הכנסה</strong>
                                <small>שנתיים אחרונות</small>
                            </li>
                            <li class="document-item">
                                <strong>אישורי העדר חובות</strong>
                                <small>למס הכנסה וביטוח לאומי</small>
                            </li>
                            <li class="document-item">
                                <strong>רישיון עסק בתוקף</strong>
                                <small>חוזים עיקריים עם לקוחות</small>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>

            <div class="section personal-section">
                <div class="section-header">
                    <div class="icon">👥</div>
                    <h3>מסמכים אישיים</h3>
                    <p>של הערבים</p>
                </div>
                <div class="section-content">
                    <div class="document-group">
                        <h4>מי הם הערבים?</h4>
                        <p style="color: #555; margin-bottom: 20px;">בדרך כלל מנהלי החברה ובעלי המניות העיקריים שיערבו אישית לחוב.</p>
                    </div>

                    <div class="document-group">
                        <h4>מסמכי זהות</h4>
                        <ul class="document-list">
                            <li class="document-item">
                                <strong>תעודת זהות + רישיון נהיגה</strong>
                                <small>לכל הערבים</small>
                            </li>
                            <li class="document-item">
                                <strong>תעודת זהות של בן/בת זוג</strong>
                                <small>במידה ויש</small>
                            </li>
                        </ul>
                    </div>

                    <div class="document-group">
                        <h4>מצב משפחתי</h4>
                        <ul class="document-list">
                            <li class="document-item">
                                <strong>תעודת נישואין/גירושין</strong>
                                <small>משפיע על יכולת הפירעון</small>
                            </li>
                            <li class="document-item">
                                <strong>הסכם ממון</strong>
                                <small>אם יש</small>
                            </li>
                        </ul>
                    </div>

                    <div class="document-group">
                        <h4>הכנסות אישיות</h4>
                        <ul class="document-list">
                            <li class="document-item">
                                <strong>תלושי שכר</strong>
                                <small>3 חודשים אחרונים</small>
                            </li>
                            <li class="document-item">
                                <strong>אישור שכר מהעבודה</strong>
                                <small>אימות רציפות העסקה</small>
                            </li>
                            <li class="document-item">
                                <strong>דוחות שנתיים אישיים</strong>
                                <small>אם הם עוסקים מורשים</small>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>

        <div class="process-flow">
            <h3>🔄 סדר הפעולות המומלץ</h3>
            <div class="steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <h4>מסמכי החברה</h4>
                    <p>תתחילו ממסמכי החברה - הם הכי חשובים</p>
                </div>
                <div class="step">
                    <div class="step-number">2</div>
                    <h4>יועץ המס</h4>
                    <p>פנו ליועץ המס מראש - לוקח זמן להכין אישורים</p>
                </div>
                <div class="step">
                    <div class="step-number">3</div>
                    <h4>רשם החברות</h4>
                    <p>הזמינו מסמכים - יכול לקחת עד שבוע</p>
                </div>
                <div class="step">
                    <div class="step-number">4</div>
                    <h4>מסמכים אישיים</h4>
                    <p>רק אחר כך תתעסקו במסמכים האישיים</p>
                </div>
            </div>
        </div>

        <div class="tips">
            <h3>💡 טיפים חשובים</h3>
            <div class="tips-grid">
                <div class="tip-item">
                    <h4>עדכניות המסמכים</h4>
                    <p>כל המסמכים צריכים להיות עדכניים - לא יותר מ-3 חודשים</p>
                </div>
                <div class="tip-item">
                    <h4>עותקים מאושרים</h4>
                    <p>הכינו עותקים מאושרים של כל המסמכים</p>
                </div>
                <div class="tip-item">
                    <h4>תרגום מסמכים</h4>
                    <p>מסמכים בשפה זרה צריכים תרגום מאושר</p>
                </div>
                <div class="tip-item">
                    <h4>הטיפ הזהב</h4>
                    <p>התייעצו עם יועץ משכנתאות לפני שאתם מתחילים</p>
                </div>
            </div>
        </div>

        <div class="footer">
            <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 30px;">
                <div style="text-align: right; flex: 1;">
                    <h3 style="margin: 0 0 10px 0; color: #ecf0f1;">מישל עדי דוריאן</h3>
                    <p style="margin: 5px 0; font-size: 1.1em;">מומחית לכל היבטי התכנון הפיננסי</p>
                    <div style="margin-top: 15px;">
                        <p style="margin: 5px 0;">📞 054-534-5079</p>
                        <p style="margin: 5px 0;">📧 michelle@wellcome-h.com</p>
                        <p style="margin: 5px 0;">🌐 wellcome-h.com</p>
                    </div>
                </div>
                <div style="text-align: center; flex: 1;">
                    <p style="font-size: 1.1em; margin-bottom: 10px;"><strong>מדריך זה מתאים לכל הבנקים בישראל</strong></p>
                    <p>הדרישות זהות בכל המוסדות הפיננסיים</p>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
