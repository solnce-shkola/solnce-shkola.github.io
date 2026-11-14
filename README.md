# Shkola-SOlNCe
Сайт школы СОлНЦе казанское солнце
# МАОУ СОШИ СОлНЦе
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>МАОУ СОШИ СОлНЦе – Казань – Официальный интерфейс</title>
    <!-- Подключение Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        sunYellow: '#FBBF24',
                        sunOrange: '#F59E0B',
                        sunDark: '#1E293B',
                        sunAmber: '#FFFBEB'
                    }
                }

            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        body {
            font-family: 'Inter', sans-serif;
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800 flex flex-col min-h-screen">

    <!-- Верхняя информационная панель -->
    <div class="bg-sunDark text-white text-xs py-2 px-4">
        <div class="max-w-7xl mx-auto flex flex-col sm:flex-row justify-between items-center gap-2">
            <div class="flex items-center gap-4">
                <span>📍 г. Казань, Вахитовский район, ул. Кави Наджми, д. 18</span>
                <span class="hidden md:inline">📞 +7 (843) 292-41-90, 292-42-60</span>

            </div>
            <div class="flex items-center gap-4">
                <a href="https://shkolasolnce.ru/main/" target="_blank" rel="noopener noreferrer" class="hover:text-sunYellow transition-colors">Официальный сайт ↗</a>
                <a href="https://vk.ru/kznsun" target="_blank" rel="noopener noreferrer" class="hover:text-sunYellow transition-colors">ВКонтакте ↗</a>
            </div>
        </div>
    </div>

    <!-- Навигационная панель (Header) -->
    <header class="bg-white shadow-md sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 py-3 flex justify-between items-center">
            <!-- Логотип и Название -->
            <a href="#hero" class="flex items-center gap-3 group">
                <div class="w-12 h-12 bg-sunYellow rounded-full flex items-center justify-center shadow-md group-hover:scale-105 transition-transform">
                    <svg class="w-8 h-8 text-sunDark" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <circle cx="12" cy="12" r="5" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                        <path d="M12 1v2M12 21v2M4.22 4.22l1.42 1.42M18.36 18.36l1.42 1.42M1 12h2M21 12h2M4.22 19.78l1.42-1.42M18.36 5.64l1.42-1.42" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                </div>

                <div>
                    <span class="text-xl font-bold tracking-tight text-sunDark block leading-none">СОлНЦе</span>
                    <span class="text-[10px] text-gray-500 uppercase tracking-wider block mt-1">Специализированный Олимпиадно-Научный Центр</span>
                </div>
            </a>

            <!-- Десктопное меню -->
            <nav class="hidden lg:flex items-center gap-6 font-medium text-gray-700">
                <a href="#about" class="hover:text-sunOrange transition-colors">О школе</a>
                <a href="#teachers" class="hover:text-sunOrange transition-colors">Педагоги</a>
                <a href="#admissions" class="hover:text-sunOrange transition-colors">Приемная кампания</a>
                <a href="#exam-tasks" class="hover:text-sunOrange transition-colors">Примеры заданий</a>
                <a href="#clubs" class="hover:text-sunOrange transition-colors">Кружки</a>
                <a href="#contacts" class="hover:text-sunOrange transition-colors">Контакты</a>
                <button onclick="openModal()" class="bg-sunOrange text-white px-4 py-2 rounded-lg shadow hover:bg-opacity-90 transition-all text-sm">Запись на тест</button>
            </nav>

            <!-- Мобильная кнопка меню -->
            <button onclick="toggleMobileMenu()" class="lg:hidden text-sunDark focus:outline-none" aria-label="Открыть меню">

                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path id="menu-icon" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16"/>
                </svg>
            </button>
        </div>

        <!-- Мобильное меню -->
        <div id="mobile-menu" class="hidden lg:hidden bg-white border-t border-gray-100 px-4 py-4 space-y-3 shadow-inner">
            <a href="#about" onclick="toggleMobileMenu()" class="block font-medium text-gray-700 hover:text-sunOrange">О школе</a>
            <a href="#teachers" onclick="toggleMobileMenu()" class="block font-medium text-gray-700 hover:text-sunOrange">Педагоги</a>
            <a href="#admissions" onclick="toggleMobileMenu()" class="block font-medium text-gray-700 hover:text-sunOrange">Приемная кампания</a>
            <a href="#exam-tasks" onclick="toggleMobileMenu()" class="block font-medium text-gray-700 hover:text-sunOrange">Примеры заданий</a>
            <a href="#clubs" onclick="toggleMobileMenu()" class="block font-medium text-gray-700 hover:text-sunOrange">Кружки</a>
            <a href="#contacts" onclick="toggleMobileMenu()" class="block font-medium text-gray-700 hover:text-sunOrange">Контакты</a>
            <button onclick="openModal(); toggleMobileMenu()" class="w-full bg-sunOrange text-white px-4 py-2 rounded-lg text-center font-medium">Запись на входной тест</button>
        </div>
    </header>

    <main class="flex-grow">

        <!-- Секция Hero -->
        <section id="hero" class="relative bg-gradient-to-br from-amber-400 via-orange-400 to-yellow-500 py-16 md:py-24 text-sunDark overflow-hidden">
            <div class="max-w-7xl mx-auto px-4 relative z-10 grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div class="space-y-6">
                    <div class="inline-block bg-white bg-opacity-30 backdrop-blur-sm text-xs font-semibold uppercase tracking-widest px-3 py-1 rounded-full text-sunDark border border-white border-opacity-40">
                        МАОУ «СОШИ «СОлНЦе»
                    </div>
                    <h1 class="text-3xl md:text-5xl font-extrabold tracking-tight leading-tight">
                        Интеллектуальная увлеченность и свобода творчества
                    </h1>
                    <p class="text-lg md:text-xl opacity-90 max-w-xl font-light">
                        Камерное нетиповое муниципальное образовательное учреждение Казани. Бесплатное обучение увлеченных детей с 5 по 11 классы на основе конкурсного отбора.
                    </p>
                    <div class="flex flex-wrap gap-4">
                        <a href="#exam-tasks" class="bg-sunDark text-white px-6 py-3 rounded-xl font-medium shadow-lg hover:bg-opacity-90 transition-all">
                            Решать примеры задач
                        </a>
                        <a href="#admissions" class="bg-white text-sunDark px-6 py-3 rounded-xl font-medium shadow-md hover:bg-gray-100 transition-all">
                            Этапы и правила приема

                        </a>
                    </div>
                </div>
                <div class="bg-white bg-opacity-20 backdrop-blur-md border border-white border-opacity-30 p-6 md:p-8 rounded-2xl shadow-2xl space-y-4">
                    <h3 class="text-xl font-bold flex items-center gap-2">
                        <span>📢</span> Оперативная информация (Ноябрь 2026)
                    </h3>
                    <p class="text-sm">
                        В школе проходит плановый осенне-зимний тур открытых академических собеседований и тестирований для поступающих. У вас есть возможность зарегистрировать ребенка на пробные испытания.
                    </p>
                    <div class="p-4 bg-white bg-opacity-40 rounded-xl text-xs space-y-2">
                        <div class="flex justify-between"><span>Ближайший тест:</span> <strong>21 ноября 2026 г.</strong></div>
                        <div class="flex justify-between"><span>Классы:</span> <strong>4, 5, 6, 7, 8</strong></div>
                        <div class="flex justify-between"><span>Стоимость:</span> <strong>Бесплатно</strong></div>
                    </div>
                    <button onclick="openModal()" class="w-full bg-sunDark text-white text-center py-3 rounded-xl font-semibold shadow hover:bg-slate-800 transition-all">Заполнить анкету участника</button>
                </div>
            </div>
        </section>


        <!-- О школе -->
        <section id="about" class="py-16 max-w-7xl mx-auto px-4">
            <h2 class="text-3xl font-bold text-sunDark text-center mb-12">Уникальная экосистема школы «СОлНЦе»</h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-100">
                    <div class="text-3xl mb-4">🏆</div>
                    <h3 class="text-lg font-bold text-sunDark mb-2">Высокие результаты</h3>
                    <p class="text-gray-600 text-sm">Школа регулярно входит в число лидеров Республики Татарстан по количеству победителей и призеров Всероссийской олимпиады школьников по математике, физике, химии и астрономии.</p>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-100">
                    <div class="text-3xl mb-4">🤝</div>
                    <h3 class="text-lg font-bold text-sunDark mb-2">Камерная атмосфера</h3>
                    <p class="text-gray-600 text-sm">У нас нет традиционной строгой иерархии и школьной формы. Обучение строится на принципах взаимного уважения, партнерства педагога и ученика и раскрытия личного потенциала.</p>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-100">
                    <div class="text-3xl mb-4">🧪</div>
                    <h3 class="text-lg font-bold text-sunDark mb-2">Индивидуальный трек</h3>
                    <p class="text-gray-600 text-sm">Каждый ученик может формировать углубленное расписание, посещать олимпиадные интенсивы, кружки и заниматься исследовательской деятельностью под кураторством ученых.</p>
                </div>

            </div>
        </section>

        <!-- Педагогический состав -->
        <section id="teachers" class="py-16 bg-gray-100">
            <div class="max-w-7xl mx-auto px-4">
                <h2 class="text-3xl font-bold text-sunDark text-center mb-4">Наши преподаватели</h2>
                <p class="text-gray-600 text-center max-w-2xl mx-auto mb-12">Преподаватели вузов, ведущие олимпиадные тренеры и вдохновленные наставники, которые говорят с детьми на одном языке.</p>
                
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
                    <div class="bg-white rounded-xl overflow-hidden shadow-sm">
                        <img src="https://placehold.co/300x350/e2e8f0/1e293b?text=Шмаков+П.А." alt="Павел Шмаков" class="w-full h-64 object-cover">
                        <div class="p-4">
                            <h4 class="font-bold text-base text-sunDark">Шмаков Павел Анатольевич</h4>
                            <p class="text-xs text-amber-600 font-semibold mb-2">Директор, основатель школы</p>
                            <p class="text-xs text-gray-500">Учитель физики и химии, известный педагог-новатор, многократно доказавший приоритет интересов ребенка.</p>
                        </div>
                    </div>
                    <div class="bg-white rounded-xl overflow-hidden shadow-sm">

                        <img src="https://placehold.co/300x350/e2e8f0/1e293b?text=Математика" alt="Преподаватель" class="w-full h-64 object-cover">
                        <div class="p-4">
                            <h4 class="font-bold text-base text-sunDark">Галиуллин Рашит Анварович</h4>
                            <p class="text-xs text-amber-600 font-semibold mb-2">Учитель математики</p>
                            <p class="text-xs text-gray-500">Заслуженный учитель РТ, тренер сборных команд на всероссийских математических турнирах.</p>
                        </div>
                    </div>
                    <div class="bg-white rounded-xl overflow-hidden shadow-sm">
                        <img src="https://placehold.co/300x350/e2e8f0/1e293b?text=Физика" alt="Преподаватель" class="w-full h-64 object-cover">
                        <div class="p-4">
                            <h4 class="font-bold text-base text-sunDark">Иванов Сергей Владимирович</h4>
                            <p class="text-xs text-amber-600 font-semibold mb-2">Преподаватель физики</p>
                            <p class="text-xs text-gray-500">Кандидат физико-математических наук, доцент, готовит учеников к экспериментальным турам олимпиад.</p>
                        </div>
                    </div>
                    <div class="bg-white rounded-xl overflow-hidden shadow-sm">
                        <img src="https://placehold.co/300x350/e2e8f0/1e293b?text=Лингвистика" alt="Преподаватель" class="w-full h-64 object-cover">
                        <div class="p-4">
                            <h4 class="font-bold text-base text-sunDark">Ахметова Лилия Маратовна</h4>

                            <p class="text-xs text-amber-600 font-semibold mb-2">Преподаватель русского языка</p>
                            <p class="text-xs text-gray-500">Эксперт по подготовке к высокобалльной сдаче госэкзаменов и олимпиадам по лингвистике.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Приемная кампания -->
        <section id="admissions" class="py-16 max-w-7xl mx-auto px-4">
            <h2 class="text-3xl font-bold text-sunDark text-center mb-2">Приемная кампания 2026/2027</h2>
            <p class="text-gray-600 text-center mb-12">Поступление проходит прозрачно, в несколько этапов на конкурсной основе</p>
            
            <div class="relative border-l-2 border-sunOrange ml-4 md:ml-32 space-y-8">
                <div class="relative pl-6">
                    <div class="absolute -left-2 top-1.5 w-4 h-4 bg-sunOrange rounded-full"></div>
                    <span class="text-xs font-bold text-amber-600 block uppercase">Этап 1: Регистрация</span>
                    <h4 class="text-lg font-bold text-sunDark">Подача онлайн-заявления</h4>
                    <p class="text-sm text-gray-600 max-w-2xl">Родители заполняют электронную форму, выбирая профильные направления и класс, в который планируется поступление.</p>

                </div>
                <div class="relative pl-6">
                    <div class="absolute -left-2 top-1.5 w-4 h-4 bg-sunOrange rounded-full"></div>
                    <span class="text-xs font-bold text-amber-600 block uppercase">Этап 2: Письменный тур</span>
                    <h4 class="text-lg font-bold text-sunDark">Входное тестирование по математике и логике</h4>
                    <p class="text-sm text-gray-600 max-w-2xl">Проводится очно в здании школы. Проверяется базовая математическая грамотность, нестандартное и пространственное мышление.</p>
                </div>
                <div class="relative pl-6">
                    <div class="absolute -left-2 top-1.5 w-4 h-4 bg-sunOrange rounded-full"></div>
                    <span class="text-xs font-bold text-amber-600 block uppercase">Этап 3: Собеседование</span>
                    <h4 class="text-lg font-bold text-sunDark">Академическое знакомство с директором и психологом</h4>
                    <p class="text-sm text-gray-600 max-w-2xl">Индивидуальная беседа с кандидатом для определения уровня его познавательной мотивации, психологической готовности к нагрузкам.</p>
                </div>
                <div class="relative pl-6">
                    <div class="absolute -left-2 top-1.5 w-4 h-4 bg-sunOrange rounded-full"></div>
                    <span class="text-xs font-bold text-amber-600 block uppercase">Этап 4: Пробные дни</span>
                    <h4 class="text-lg font-bold text-sunDark">Тест-драйв обучения</h4>
                    <p class="text-sm text-gray-600 max-w-2xl">Рекомендуемые кандидаты приглашаются на 2-3 учебных дня, чтобы погрузиться в реальные уроки школы «СОлНЦе» и сделать осознанный выбор.</p>
                </div>

            </div>
        </section>

        <!-- Примеры заданий -->
        <section id="exam-tasks" class="py-16 bg-sunAmber border-y border-orange-100">
            <div class="max-w-4xl mx-auto px-4">
                <h2 class="text-3xl font-bold text-sunDark text-center mb-4">Что в тестах? Примеры олимпиадных задач</h2>
                <p class="text-gray-600 text-center mb-8 text-sm">Попробуйте решить типовые задания прошлых лет для учеников 4–5 классов</p>
                
                <div class="space-y-6">
                    <div class="bg-white p-6 rounded-xl shadow-sm border border-orange-200">
                        <div class="flex justify-between items-center mb-3">
                            <span class="bg-amber-100 text-amber-800 text-xs font-bold px-2.5 py-1 rounded">Задача 1. Логика</span>
                            <span class="text-xs text-gray-400">Сложность: Средняя</span>
                        </div>
                        <p class="text-sm text-gray-700 leading-relaxed mb-4">
                            В коробке лежат 4 красных, 5 синих и 6 зеленых карандашей. Какое наименьшее количество карандашей нужно вытащить в темноте, чтобы среди них обязательно оказалось хотя бы 2 карандаша одного цвета?
                        </p>
                        <button onclick="toggleAnswer('ans1')" class="text-xs font-bold text-sunOrange hover:underline focus:outline-none">Показать правильный ответ и разбор</button>

                        <div id="ans1" class="hidden mt-3 p-3 bg-gray-50 rounded-lg text-xs text-gray-600 border-l-2 border-sunOrange">
                            <strong>Ответ: 4 карандаша.</strong><br>Разбор: По принципу Дирихле (худший случай), если мы вытащим 3 карандаша, они все могут оказаться разных цветов (1 красный, 1 синий, 1 зеленый). Любой следующий 4-й карандаш неизбежно повторит один из уже вытащенных цветов.
                        </div>
                    </div>

                    <div class="bg-white p-6 rounded-xl shadow-sm border border-orange-200">
                        <div class="flex justify-between items-center mb-3">
                            <span class="bg-amber-100 text-amber-800 text-xs font-bold px-2.5 py-1 rounded">Задача 2. Математика</span>
                            <span class="text-xs text-gray-400">Сложность: Высокая</span>
                        </div>
                        <p class="text-sm text-gray-700 leading-relaxed mb-4">
                            Будильник отстает на 4 минуты за каждый час. Сейчас он показывает ровно 12:00, и это точное время. Какое реальное время будет в тот момент, когда этот будильник впервые покажет 13:00?
                        </p>
                        <button onclick="toggleAnswer('ans2')" class="text-xs font-bold text-sunOrange hover:underline focus:outline-none">Показать правильный ответ и разбор</button>
                        <div id="ans2" class="hidden mt-3 p-3 bg-gray-50 rounded-lg text-xs text-gray-600 border-l-2 border-sunOrange">
                            <strong>Ответ: 13:04 и 17 секунд (примерно 13:04).</strong><br>Разбор: За один астрономический час (60 минут) будильник проходит только 56 своих минут. Чтобы показать час (60 своих минут), ему требуется 60 * (60 / 56) = 64.28 реальных минут.
                        </div>
                    </div>
                </div>

            </div>
        </section>

        <!-- Кружки и секции -->
        <section id="clubs" class="py-16 max-w-7xl mx-auto px-4">
            <h2 class="text-3xl font-bold text-sunDark text-center mb-2">Наши бесплатные кружки</h2>
            <p class="text-gray-600 text-center mb-8 text-sm">Дополнительное образование открыто как для учащихся школы, так и для всех школьников Казани</p>
            
            <!-- Фильтры кружков -->
            <div class="flex flex-wrap justify-center gap-2 mb-8">
                <button onclick="filterClubs('all')" class="club-filter-btn bg-sunDark text-white px-4 py-1.5 rounded-full text-xs font-medium">Все</button>
                <button onclick="filterClubs('math')" class="club-filter-btn bg-gray-200 text-gray-700 px-4 py-1.5 rounded-full text-xs font-medium hover:bg-gray-300">Точные науки</button>
                <button onclick="filterClubs('it')" class="club-filter-btn bg-gray-200 text-gray-700 px-4 py-1.5 rounded-full text-xs font-medium hover:bg-gray-300">IT и Робототехника</button>
                <button onclick="filterClubs('humanities')" class="club-filter-btn bg-gray-200 text-gray-700 px-4 py-1.5 rounded-full text-xs font-medium hover:bg-gray-300">Гуманитарные</button>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
                <div class="club-card bg-white p-5 rounded-xl shadow-sm border border-gray-100" data-category="math">
                    <span class="text-xs text-amber-600 font-bold uppercase block mb-1">Точные науки</span>

                    <h4 class="font-bold text-lg text-sunDark mb-2">Олимпиадная математика</h4>
                    <p class="text-xs text-gray-500">Глубокий разбор нестандартных задач, подготовка к городским, республиканским и всероссийским этапам ВсОШ.</p>
                </div>
                <div class="club-card bg-white p-5 rounded-xl shadow-sm border border-gray-100" data-category="it">
                    <span class="text-xs text-amber-600 font-bold uppercase block mb-1">IT и Робототехника</span>
                    <h4 class="font-bold text-lg text-sunDark mb-2">Программирование на Python</h4>
                    <p class="text-xs text-gray-500">Изучение синтаксиса языка, базовых алгоритмов, структур данных и создание простейших веб-скриптов.</p>
                </div>
                <div class="club-card bg-white p-5 rounded-xl shadow-sm border border-gray-100" data-category="math">
                    <span class="text-xs text-amber-600 font-bold uppercase block mb-1">Точные науки</span>
                    <h4 class="font-bold text-lg text-sunDark mb-2">Занимательная астрономия</h4>
                    <p class="text-xs text-gray-500">Изучение звездной карты, основ небесной механики, подготовка к профильным астрономическим турнирам.</p>
                </div>
                <div class="club-card bg-white p-5 rounded-xl shadow-sm border border-gray-100" data-category="humanities">
                    <span class="text-xs text-amber-600 font-bold uppercase block mb-1">Гуманитарные</span>
                    <h4 class="font-bold text-lg text-sunDark mb-2">Клуб дебатов и риторики</h4>
                    <p class="text-xs text-gray-500">Развитие навыков публичных выступлений, аргументации, критического мышления и преодоления страха сцены.</p>
                </div>
                <div class="club-card bg-white p-5 rounded-xl shadow-sm border border-gray-100" data-category="it">

                    <span class="text-xs text-amber-600 font-bold uppercase block mb-1">IT и Робототехника</span>
                    <h4 class="font-bold text-lg text-sunDark mb-2">Спортивная робототехника</h4>
                    <p class="text-xs text-gray-500">Конструирование и программирование автономных роботов для участия в профильных соревнованиях.</p>
                </div>
                <div class="club-card bg-white p-5 rounded-xl shadow-sm border border-gray-100" data-category="humanities">
                    <span class="text-xs text-amber-600 font-bold uppercase block mb-1">Гуманитарные</span>
                    <h4 class="font-bold text-lg text-sunDark mb-2">Практическая лингвистика</h4>
                    <p class="text-xs text-gray-500">Анализ структуры редких языков, разбор увлекательных лингвистических шифров и олимпиадных феноменов.</p>
                </div>
            </div>
        </section>

        <!-- Контакты и Карта -->
        <section id="contacts" class="py-16 bg-slate-900 text-white">
            <div class="max-w-7xl mx-auto px-4 grid grid-cols-1 lg:grid-cols-2 gap-12">
                <div class="space-y-6">
                    <h2 class="text-3xl font-bold">Контакты администрации</h2>
                    <p class="text-gray-400 text-sm">Вы можете связаться с нами в рабочие дни с 08:00 до 17:00 или лично посетить приемную директора.</p>
                    

                    <div class="space-y-3 text-sm">
                        <div class="flex items-start gap-3">
                            <span class="text-sunYellow">📍</span>
                            <div>
                                <strong class="block text-white">Адрес:</strong>
                                <span class="text-gray-300">420111, Республика Татарстан, г. Казань, ул. Кави Наджми, д. 18</span>
                            </div>
                        </div>
                        <div class="flex items-start gap-3">
                            <span class="text-sunYellow">📞</span>
                            <div>
                                <strong class="block text-white">Телефоны приемной:</strong>
                                <span class="text-gray-300">+7 (843) 292-41-90, +7 (843) 292-42-60</span>
                            </div>
                        </div>
                        <div class="flex items-start gap-3">
                            <span class="text-sunYellow">✉️</span>
                            <div>
                                <strong class="block text-white">Электронная почта:</strong>

                                <span class="text-gray-300">shkola-solnce@mail.ru</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="rounded-xl overflow-hidden bg-slate-800 h-80 shadow-inner">
                    <!-- Google Maps Embed API -->
                    <iframe
                      width="100%"
                      height="100%"
                      frameborder="0"
                      style="border:0;"
                      referrerpolicy="no-referrer-when-downgrade"
                      loading="lazy"
                      src="https://www.google.com/maps/embed/v1/place?key=__CODING_CANVAS_MAPS_EMBED_API_KEY__&q=Казань,+ул.+Кави+Наджми,+д.+18"
                      allowfullscreen>
                    </iframe>
                </div>
            </div>

        </section>
    </main>

    <!-- Подвал (Footer) -->
    <footer class="bg-slate-950 text-gray-500 text-xs py-8 px-4 border-t border-slate-800">
        <div class="max-w-7xl mx-auto flex flex-col md:flex-row justify-between items-center gap-4">
            <div>
                <p class="font-bold text-gray-400">© 2026 МАОУ «СОШИ «СОлНЦе» Вахитовского района г. Казани.</p>
                <p class="mt-1">Специализированная олимпиадно-научная школа-интернат. Все права защищены.</p>
            </div>
            <div class="flex gap-4">
                <a href="https://shkolasolnce.ru/main/" target="_blank" rel="noopener noreferrer" class="hover:text-white transition-colors">Официальный сайт</a>
                <a href="https://vk.ru/kznsun" target="_blank" rel="noopener noreferrer" class="hover:text-white transition-colors">Сообщество ВК</a>
            </div>
        </div>
    </footer>

    <!-- Модальное окно записи на тест -->
    <div id="register-modal" class="fixed inset-0 bg-black bg-opacity-60 backdrop-blur-sm z-50 flex items-center justify-center hidden p-4">

        <div class="bg-white rounded-2xl max-w-md w-full p-6 relative shadow-2xl max-h-[90vh] overflow-y-auto">
            <button onclick="closeModal()" class="absolute top-4 right-4 text-gray-400 hover:text-gray-600 focus:outline-none" aria-label="Закрыть">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-width="2" stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"/>
                </svg>
            </button>
            
            <h3 class="text-xl font-bold text-sunDark mb-2">Анкета регистрации на тест</h3>
            <p class="text-xs text-gray-500 mb-6">Заполните данные ребенка для распределения в аудиторию.</p>
            
            <!-- Контейнер для сообщений об ошибке или успехе -->
            <div id="modal-message" class="hidden mb-4 p-3 rounded-lg text-xs font-medium"></div>

            <form id="test-registration-form" onsubmit="handleFormSubmit(event)" class="space-y-4">
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">ФИО родителя / законного представителя *</label>
                    <input type="text" id="parent-name" required class="w-full border border-gray-300 px-3 py-2 rounded-lg text-sm focus:outline-none focus:border-sunOrange">
                </div>
                <div>

                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Контактный телефон *</label>
                    <input type="tel" id="parent-phone" placeholder="+7 (999) 000-00-00" required class="w-full border border-gray-300 px-3 py-2 rounded-lg text-sm focus:outline-none focus:border-sunOrange">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Имя и фамилия ребенка *</label>
                    <input type="text" id="child-name" required class="w-full border border-gray-300 px-3 py-2 rounded-lg text-sm focus:outline-none focus:border-sunOrange">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Класс обучения (в настоящее время) *</label>
                    <select id="child-class" required class="w-full border border-gray-300 px-3 py-2 rounded-lg text-sm bg-white focus:outline-none focus:border-sunOrange">
                        <option value="">Выберите класс</option>
                        <option value="4">4 класс</option>
                        <option value="5">5 класс</option>
                        <option value="6">6 класс</option>
                        <option value="7">7 класс</option>
                        <option value="8">8 класс</option>
                    </select>
                </div>
                <div class="flex items-start gap-2 pt-2">

                    <input type="checkbox" id="agreement" required class="mt-0.5 rounded text-sunOrange focus:ring-sunOrange">
                    <label for="agreement" class="text-[10px] text-gray-500 leading-tight">Я даю согласие на обработку персональных данных и получение информационных уведомлений от администрации МАОУ СОШИ СОлНЦе.</label>
                </div>
                <button type="submit" class="w-full bg-sunOrange text-white text-center py-3 rounded-lg font-bold shadow hover:bg-opacity-95 transition-all text-sm mt-4">Отправить заявку</button>
            </form>
        </div>
    </div>

    <!-- Скрипты управления интерфейсом -->
    <script>
        // Переключение мобильного меню
        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        }

        // Открытие/закрытие ответов к задачам
        function toggleAnswer(id) {
            const el = document.getElementById(id);

            el.classList.toggle('hidden');
        }

        // Фильтрация карточек кружков
        function filterClubs(category) {
            const cards = document.querySelectorAll('.club-card');
            const buttons = document.querySelectorAll('.club-filter-btn');
            
            // Смена активного стиля кнопок
            buttons.forEach(btn => {
                if (btn.getAttribute('onclick').includes(`'${category}'`)) {
                    btn.className = "club-filter-btn bg-sunDark text-white px-4 py-1.5 rounded-full text-xs font-medium";
                } else {
                    btn.className = "club-filter-btn bg-gray-200 text-gray-700 px-4 py-1.5 rounded-full text-xs font-medium hover:bg-gray-300";
                }
            });

            // Показ/скрытие карточек
            cards.forEach(card => {

                if (category === 'all' || card.getAttribute('data-category') === category) {
                    card.classList.remove('hidden');
                } else {
                    card.classList.add('hidden');
                }
            });
        }

        // Модальное окно
        function openModal() {
            const modal = document.getElementById('register-modal');
            modal.classList.remove('hidden');
            document.body.style.overflow = 'hidden';
            
            // Сброс сообщений
            const msgBox = document.getElementById('modal-message');
            msgBox.classList.add('hidden');
            msgBox.textContent = '';
        }


        function closeModal() {
            const modal = document.getElementById('register-modal');
            modal.classList.add('hidden');
            document.body.style.overflow = '';
        }

        // Валидация и отправка формы без alert()
        function handleFormSubmit(e) {
            e.preventDefault();
            
            const parentName = document.getElementById('parent-name').value.trim();
            const parentPhone = document.getElementById('parent-phone').value.trim();
            const childName = document.getElementById('child-name').value.trim();
            const childClass = document.getElementById('child-class').value;
            const agreement = document.getElementById('agreement').checked;
            
            const msgBox = document.getElementById('modal-message');
            msgBox.className = "mb-4 p-3 rounded-lg text-xs font-medium"; // Сброс классов


            if (!parentName || !parentPhone || !childName || !childClass || !agreement) {
                msgBox.classList.remove('hidden');
                msgBox.classList.add('bg-red-50', 'text-red-700', 'border', 'border-red-200');
                msgBox.textContent = 'Пожалуйста, заполните все обязательные поля формы и подтвердите согласие.';
                return;
            }

            // Успешная имитация отправки
            msgBox.classList.remove('hidden');
            msgBox.classList.add('bg-green-50', 'text-green-700', 'border', 'border-green-200');
            msgBox.innerHTML = `<strong>Успешно отправлено!</strong><br>Заявка для ребенка (${childName}, ${childClass} класс) зарегистрирована. Администратор свяжется с вами по номеру ${parentPhone} в ближайшее время.`;
            
            // Очистка формы
            document.getElementById('test-registration-form').reset();
        }
    </script>
</body>
</html>



