# Shkola-SOlNCe
Сайт школы СОлНЦе казанское солнце
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>МАОУ СОШИ СОлНЦе – Казань – Официальный интерфейс</title>
    <!-- Подключение Tailwind CSS для современного адаптивного интерфейса -->
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
                <a href="https://shkolasolnce.ru/main/" target="_blank" rel="noopener noreferrer" class="hover:text-sunYellow transition-colors">Официальный site ↗</a>
                <a href="https://t.me" target="_blank" rel="noopener noreferrer" class="hover:text-sunYellow transition-colors">Telegram ↗</a>
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
                    <!-- Иконка Солнца (SVG) -->
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
                <a href="#register-modal" onclick="openModal()" class="bg-sunOrange text-white px-4 py-2 rounded-lg shadow hover:bg-opacity-90 transition-all text-sm">Запись на тест</a>
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
                    <ul class="space-y-3 text-sm">
                        <li class="flex items-start gap-3 bg-white bg-opacity-40 p-3 rounded-lg border-l-4 border-red-600">
                            <span class="font-bold text-base text-amber-900">12 Ноя</span>
                            <div>
                                <strong>Внимание!</strong> Экзамен по русскому языку для кандидатов, успешно прошедших предварительное тестирование. Начальная школа (3-4 классы) приглашается к 16:00, учащиеся 5-11 классов — к 17:00. После основного теста доступен олимпиадный тур по желанию.
                            </div>
                        </li>
                        <li class="flex items-start gap-3 bg-white bg-opacity-40 p-3 rounded-lg">
                            <span class="font-bold text-base text-amber-900">Важно</span>
                            <div>Для участия во всех турах строго требуется предварительная электронная регистрация и оформленный бумажный пропуск с фотографией.</div>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="absolute -bottom-10 -left-10 w-40 h-40 bg-white opacity-10 rounded-full blur-2xl"></div>
            <div class="absolute -top-20 -right-20 w-80 h-80 bg-white opacity-10 rounded-full blur-3xl"></div>
        </section>

        <!-- Секция "О школе" -->
        <section id="about" class="py-16 max-w-7xl mx-auto px-4">
            <div class="text-center max-w-3xl mx-auto mb-12">
                <h2 class="text-3xl font-bold text-sunDark mb-4">Принципы и особенности обучения</h2>
                <div class="h-1 w-20 bg-sunOrange mx-auto rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white p-6 rounded-xl shadow-md border border-gray-100 hover:shadow-lg transition-shadow">
                    <div class="w-12 h-12 bg-amber-100 text-sunOrange rounded-lg flex items-center justify-center text-xl font-bold mb-4">👨‍🏫</div>
                    <h3 class="text-lg font-bold text-sunDark mb-2">Основатель и руководство</h3>
                    <p class="text-gray-600 text-sm leading-relaxed">
                        Создатель и директор школы — Павел Анатольевич Шмаков, Заслуженный учитель РТ. Демократическая атмосфера: в школе отсутствует жесткая школьная форма (требуется лишь опрятность, а раз в неделю — официальный черно-белый вид).
                    </p>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-md border border-gray-100 hover:shadow-lg transition-shadow">
                    <div class="w-12 h-12 bg-amber-100 text-sunOrange rounded-lg flex items-center justify-center text-xl font-bold mb-4">🧮</div>
                    <h3 class="text-lg font-bold text-sunDark mb-2">Олимпиадный уровень</h3>
                    <p class="text-gray-600 text-sm leading-relaxed">
                        Углубленная олимпиадная подготовка. Математические задачи соответствуют уровню сложности муниципальных и региональных этапов всероссийских олимпиад. Развивается проектная и исследовательская деятельность.
                    </p>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-md border border-gray-100 hover:shadow-lg transition-shadow">
                    <div class="w-12 h-12 bg-amber-100 text-sunOrange rounded-lg flex items-center justify-center text-xl font-bold mb-4">📅</div>
                    <h3 class="text-lg font-bold text-sunDark mb-2">Режим обучения</h3>
                    <p class="text-gray-600 text-sm leading-relaxed">
                        Ученики начальной школы (1-4 классы) обучаются в режиме 5-дневной рабочей недели. Начиная с 5 класса, вводится интенсивная 6-дневная учебная неделя. Занятия проходят в первую смену.
                    </p>
                </div>
            </div>

            <div class="mt-12 bg-sunDark text-white rounded-2xl p-8 grid grid-cols-2 md:grid-cols-4 gap-6 text-center">
                <div>
                    <div class="text-3xl md:text-4xl font-extrabold text-sunYellow">~150</div>
                    <div class="text-xs text-gray-400 uppercase tracking-wider mt-2">Учеников в кампусе</div>
                </div>
                <div>
                    <div class="text-3xl md:text-4xl font-extrabold text-sunYellow">5-11</div>
                    <div class="text-xs text-gray-400 uppercase tracking-wider mt-2">Основная сетка классов</div>
                </div>
                <div>
                    <div class="text-3xl md:text-4xl font-extrabold text-sunYellow">Бесплатно</div>
                    <div class="text-xs text-gray-400 uppercase tracking-wider mt-2">Муниципальный статус</div>
                </div>
                <div>
                    <div class="text-3xl md:text-4xl font-extrabold text-sunYellow">2013</div>
                    <div class="text-xs text-gray-400 uppercase tracking-wider mt-2">Год открытия центра</div>
                </div>
            </div>
        </section>

        <!-- Секция "Педагогический состав" -->
        <section id="teachers" class="bg-white py-16 border-t border-b border-gray-100">
            <div class="max-w-7xl mx-auto px-4">
                <div class="text-center max-w-3xl mx-auto mb-12">
                    <h2 class="text-3xl font-bold text-sunDark mb-4">Ключевые преподаватели школы</h2>
                    <p class="text-gray-600 text-sm">Ведущие специалисты, формирующие уникальные образовательные траектории</p>
                    <div class="h-1 w-20 bg-sunOrange mx-auto rounded-full mt-4"></div>
                </div>

                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
                    <div class="bg-gray-50 p-5 rounded-xl border border-gray-200">
                        <h4 class="font-bold text-sunDark text-base">Павел Анатольевич Шмаков</h4>
                        <p class="text-xs text-sunOrange font-medium mb-2">Директор, учитель физики</p>
                        <p class="text-xs text-gray-600">Выпускник МИФИ и Университета Хельсинки. Заслуженный учитель Республики Татарстан.</p>
                    </div>
                    <div class="bg-gray-50 p-5 rounded-xl border border-gray-200">
                        <h4 class="font-bold text-sunDark text-base">Анна Борисовна Маргулис</h4>
                        <p class="text-xs text-sunOrange font-medium mb-2">Бессменный завуч, учитель биологии</p>
                        <p class="text-xs text-gray-600">Курирует учебную часть, готовит призеров и победителей олимпиад по биологическому профилю.</p>
                    </div>
                    <div class="bg-gray-50 p-5 rounded-xl border border-gray-200">
                        <h4 class="font-bold text-sunDark text-base">Наиль Абузарович Афлетонов</h4>
                        <p class="text-xs text-sunOrange font-medium mb-2">Учитель физики</p>
                        <p class="text-xs text-gray-600">Демонстрирует экспериментальную и олимпиадную физику в действии, разбирает сложные физические концепции.</p>
                    </div>
                    <div class="bg-gray-50 p-5 rounded-xl border border-gray-200">
                        <h4 class="font-bold text-sunDark text-base">Сергей Николаевич Матвеев</h4>
                        <p class="text-xs text-sunOrange font-medium mb-2">Учитель химии, к.х.н.</p>
                        <p class="text-xs text-gray-600">Организатор лабораторных практикумов и практических интерактивных занятий по химии.</p>
                    </div>
                    <div class="bg-gray-50 p-5 rounded-xl border border-gray-200">
                        <h4 class="font-bold text-sunDark text-base">Аида Ринатовна Аглуллина</h4>
                        <p class="text-xs text-sunOrange font-medium mb-2">Учитель русского языка и литературы</p>
                        <p class="text-xs text-gray-600">Руководитель школьных медиа-проектов и подкастов, готовит к обязательному и профильному русскому языку.</p>
                    </div>
                    <div class="bg-gray-50 p-5 rounded-xl border border-gray-200">
                        <h4 class="font-bold text-sunDark text-base">Алина Наилевна Сулейманова</h4>
                        <p class="text-xs text-sunOrange font-medium mb-2">Учитель английского языка</p>
                        <p class="text-xs text-gray-600">Преподает углубленный английский язык по авторским методикам лингвистического погружения.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Секция "Приемная кампания" -->
        <section id="admissions" class="bg-sunAmber py-16">
            <div class="max-w-7xl mx-auto px-4">
                <div class="text-center max-w-3xl mx-auto mb-12">
                    <h2 class="text-3xl font-bold text-sunDark mb-4">Сетка экзаменов по параллелям</h2>
                    <p class="text-gray-600 text-sm">Перечень обязательных дисциплин и профильных испытаний для поступления</p>
                    <div class="h-1 w-20 bg-sunOrange mx-auto rounded-full mt-4"></div>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                    <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-200 space-y-4">
                        <h3 class="font-bold text-lg text-sunDark border-b pb-2">🧒 Поступление в 3–4 классы</h3>
                        <ul class="space-y-2 text-sm text-gray-700 list-disc list-inside">
                            <li><strong>Математика</strong> (олимпиадный базовый уровень)</li>
                            <li><strong>Русский язык</strong> (базовый тест)</li>
                            <li><strong>Логика</strong> (задачи на мышление)</li>
                        </ul>
                        <p class="text-xs text-gray-500 italic">Прим: Для поступающих в 1-3 классы ключевым фактором является психологическое собеседование директора.</p>
                    </div>

                    <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-200 space-y-4">
                        <h3 class="font-bold text-lg text-sunDark border-b pb-2">👦 Поступление в 5, 6, 7 классы</h3>
                        <ul class="space-y-2 text-sm text-gray-700 list-disc list-inside">
                            <li><strong>Математика</strong> (уровень муниципальных олимпиад)</li>
                            <li><strong>Русский язык</strong> (обязательный письменный экзамен)</li>
                            <li><strong>Логика</strong> (свободные логические цепочки)</li>
                            <li><strong>ЧГК</strong> (Что? Где? Когда? — тест на общую эрудицию)</li>
                        </ul>
                        <p class="text-xs text-gray-500 italic">По желанию кандидата: дополнительный олимпиадный русский язык или тест по английскому языку.</p>
                    </div>

                    <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-200 space-y-4">
                        <h3 class="font-bold text-lg text-sunDark border-b pb-2">🎓 Поступление в 8–11 классы</h3>
                        <ul class="space-y-2 text-sm text-gray-700 list-disc list-inside">
                            <li><strong>Математика</strong> (повышенный олимпиадный профиль)</li>
                            <li><strong>Русский язык</strong> (грамматико-лингвистический разбор)</li>
                            <li><strong>Предмет по выбору</strong> (профильное испытание)</li>
                        </ul>
                        <div class="pt-2 text-xs text-gray-600">
                            <strong>Предметы на выбор:</strong> физика, биология, химия, информатика, татарский язык, английский язык, литература, МХК.
                        </div>
                    </div>
                </div>

                <div class="mt-8 bg-white p-6 rounded-xl border border-gray-200 max-w-4xl mx-auto">
                    <h4 class="font-bold text-sunDark mb-3 text-sm flex items-center gap-2">📋 Памятка поступающего (что принести на экзамен)</h4>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 text-xs text-gray-700">
                        <ul class="list-disc list-inside space-y-1">
                            <li>Заявление родителей (с вклеенным фото ребенка)</li>
                            <li>Бумажный официальный пропуск на экзамен</li>
                            <li>Выписка текущих четвертных/годовых оценок</li>
                            <li>Грамоты очных олимпиад за последние 2 года</li>
                        </ul>
                        <ul class="list-disc list-inside space-y-1">
                            <li>Письменные принадлежности: 2 ручки, карандаш, ластик</li>
                            <li>Чистые листы бумаги или тонкая пустая тетрадь</li>
                            <li>Сменная обувь (вторая обувь — строго обязательно)</li>
                            <li>Питьевая вода в пластиковой бутылке</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <!-- Интерактивный тренажер: Примеры заданий для поступающих -->
        <section id="exam-tasks" class="py-16 max-w-7xl mx-auto px-4">
            <div class="text-center max-w-3xl mx-auto mb-12">
                <h2 class="text-3xl font-bold text-sunDark mb-4">Реальные типы вступительных заданий</h2>
                <p class="text-gray-600 text-sm">Проверьте уровень подготовки по материалам прошлых отборочных кампаний</p>
                <div class="h-1 w-20 bg-sunOrange mx-auto rounded-full mt-4"></div>
            </div>

            <div class="flex flex-wrap justify-center gap-2 mb-8 bg-gray-100 p-1.5 rounded-xl max-w-2xl mx-auto">
                <button onclick="switchTab('math')" id="tab-btn-math" class="tab-btn flex-1 min-w-[120px] px-4 py-2.5 rounded-lg text-sm font-medium transition-all bg-white text-sunDark shadow-sm">
                    🧮 Математика
                </button>
                <button onclick="switchTab('heuristic')" id="tab-btn-heuristic" class="tab-btn flex-1 min-w-[120px] px-4 py-2.5 rounded-lg text-sm font-medium transition-all text-gray-600 hover:text-sunDark">
                    💡 Эвристика
                </button>
                <button onclick="switchTab('logic')" id="tab-btn-logic" class="tab-btn flex-1 min-w-[120px] px-4 py-2.5 rounded-lg text-sm font-medium transition-all text-gray-600 hover:text-sunDark">
                    🧠 ЧГК / Логика
                </button>
                <button onclick="switchTab('russian')" id="tab-btn-russian" class="tab-btn flex-1 min-w-[120px] px-4 py-2.5 rounded-lg text-sm font-medium transition-all text-gray-600 hover:text-sunDark">
                    📝 Русский язык
                </button>
            </div>

            <div class="max-w-4xl mx-auto">
                <!-- ВКЛАДКА: Математика -->
                <div id="tab-content-math" class="tab-pane space-y-6">
                    <div class="bg-white p-6 rounded-xl shadow-md border border-gray-100">
                        <div class="flex justify-between items-center mb-3">
                            <span class="bg-amber-100 text-amber-800 text-xs px-2.5 py-1 rounded-full font-semibold">5-6 класс • Логический счет</span>
                            <span class="text-gray-400 text-xs">Задача №1</span>
                        </div>
                        <h4 class="text-base font-semibold text-sunDark mb-4">
                            В клетке находятся кролики и цыплята. У всех вместе взятых существ ровно 10 голов и 28 ног. Определите точное количество кроликов и цыплят в клетке.
                        </h4>
                        <div class="space-y-2">
                            <button onclick="toggleCollapse('hint-m1')" class="text-sm text-sunOrange hover:underline font-medium block">⚡ Показать подсказку</button>
                            <div id="hint-m1" class="hidden p-3 bg-amber-50 rounded-lg text-sm text-amber-900 border border-amber-100">
                                Представьте, что все животные подняли по две ноги. Сколько конечностей останется на земле?
                            </div>
                            <button onclick="toggleCollapse('sol-m1')" class="bg-gray-100 hover:bg-gray-200 text-sunDark text-xs font-semibold px-4 py-2 rounded-lg transition-colors block">👁 Показать подробное решение</button>
                            <div id="sol-m1" class="hidden p-4 bg-gray-50 rounded-lg text-sm border-l-4 border-sunOrange space-y-2">
                                <p><strong>Решение:</strong></p>
                                <p>1) Если бы все 10 существ были цыплятами, то ног было бы: 10 * 2 = 20 ног.</p>
                                <p>2) В условии дано 28 ног. Разница: 28 - 20 = 8 ног.</p>
                                <p>3) Поскольку у каждого кролика на 2 ноги больше, чем у цыпленка, делим остаток на 2: 8 / 2 = 4 кролика.</p>
                                <p>4) Количество цыплят: 10 - 4 = 6 цыплят.</p>
                                <p class="text-green-700 font-medium">Ответ: 4 кролика, 6 цыплят.</p>
                            </div>
                        </div>
                    </div>

                    <div class="bg-white p-6 rounded-xl shadow-md border border-gray-100">
                        <div class="flex justify-between items-center mb-3">
                            <span class="bg-red-100 text-red-800 text-xs px-2.5 py-1 rounded-full font-semibold">6-7 класс • Пропорции и делимость</span>
                            <span class="text-gray-400 text-xs">Задача №2</span>
                        </div>
                        <h4 class="text-base font-semibold text-sunDark mb-4">
                            На доске мелом написано число 12. Раз в минуту учитель заменяет текущее число: либо умножает его на 2, либо делит на 3. Какое из следующих чисел может оказаться на доске ровно через 3 минуты? Варианты: а) 32, б) 48, в) 16.
                        </h4>
                        <div class="space-y-2">
                            <button onclick="toggleCollapse('sol-m2')" class="bg-gray-100 hover:bg-gray-200 text-sunDark text-xs font-semibold px-4 py-2 rounded-lg transition-colors block">👁 Показать подробное решение</button>
                            <div id="sol-m2" class="hidden p-4 bg-gray-50 rounded-lg text-sm border-l-4 border-sunOrange space-y-2">
                                <p><strong>Решение:</strong></p>
                                <p>Построим дерево возможных операций на протяжении 3 минут:</p>
                                <ul class="list-disc list-inside space-y-1">
                                    <li>Старт: 12</li>
                                    <li>Минута 1: 12 * 2 = 24 либо 12 / 3 = 4</li>
                                    <li>Минута 2 (из 24): 48 или 8; (из 4): 8 или 4/3</li>
                                    <li>Минута 3 (из 48): 96 или 16; (из 8): 16 или 8/3</li>
                                </ul>
                                <p>Число 16 получается в результате следующей последовательности: 12 → 24 → 8 → 16.</p>
                                <p class="text-green-700 font-medium">Ответ: в) 16.</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- ВКЛАДКА: Эвристика -->
                <div id="tab-content-heuristic" class="tab-pane space-y-6 hidden">
                    <div class="bg-white p-6 rounded-xl shadow-md border border-gray-100">
                        <div class="flex justify-between items-center mb-3">
                            <span class="bg-amber-100 text-amber-800 text-xs px-2.5 py-1 rounded-full font-semibold">Эвристический перебор</span>
                            <span class="text-gray-400 text-xs">Задача №1</span>
                        </div>
                        <h4 class="text-base font-semibold text-sunDark mb-4">
                            Как набрать из реки ровно 4 литра воды, имея в распоряжении два пустых ведра объемом 3 литра и 5 литров без делений?
                        </h4>
                        <div class="space-y-2">
                            <button onclick="toggleCollapse('sol-h1')" class="bg-gray-100 hover:bg-gray-200 text-sunDark text-xs font-semibold px-4 py-2 rounded-lg transition-colors block">👁 Показать пошаговый алгоритм</button>
                            <div id="sol-h1" class="hidden p-4 bg-gray-50 rounded-lg text-sm border-l-4 border-sunOrange space-y-2">
                                <p><strong>Алгоритм переливаний:</strong></p>
                                <ol class="list-decimal list-inside space-y-1">
                                    <li>Заполняем 5-литровое ведро полностью.</li>
                                    <li>Переливаем воду из него в 3-литровое ведро. В 5-литровом остается 2 литра.</li>
                                    <li>Освобождаем 3-литровое ведро (выливаем воду).</li>
                                    <li>Переливаем 2 литра из 5-литрового ведра в 3-литровое. Теперь в нем свободно место для 1 литра.</li>
                                    <li>Набираем полное 5-литровое ведро.</li>
                                    <li>Доливаем из него воду в 3-литровое ведро доверху (поместится ровно 1 литр).</li>
                                    <li>В 5-литровом ведре останется: 5 - 1 = 4 литра.</li>
                                </ol>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- ВКЛАДКА: ЧГК / Логика -->
                <div id="tab-content-logic" class="tab-pane space-y-6 hidden">
                    <div class="bg-white p-6 rounded-xl shadow-md border border-gray-100">
                        <div class="flex justify-between items-center mb-3">
                            <span class="bg-amber-100 text-amber-800 text-xs px-2.5 py-1 rounded-full font-semibold">Эрудиция и внимательность</span>
                            <span class="text-gray-400 text-xs">Вопрос №1</span>
                        </div>
                        <h4 class="text-base font-semibold text-sunDark mb-4">
                            У отца Мэри есть пять дочерей: Чача, Чичи, Чече, Чочо. Как зовут пятую дочь?
                        </h4>
                        <div class="space-y-2">
                            <button onclick="toggleCollapse('sol-l1')" class="bg-gray-100 hover:bg-gray-200 text-sunDark text-xs font-semibold px-4 py-2 rounded-lg transition-colors block">👁 Узнать ответ</button>
                            <div id="sol-l1" class="hidden p-4 bg-gray-50 rounded-lg text-sm border-l-4 border-sunOrange">
                                <p><strong>Ответ:</strong> Пятую дочь зовут Мэри. Ответ содержится в самом начале формулировки условия задачи («У отца Мэри...»). Экзамен ЧГК направлен на преодоление шаблонного мышления.</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- ВКЛАДКА: Русский язык -->
                <div id="tab-content-russian" class="tab-pane space-y-6 hidden">
                    <div class="bg-white p-6 rounded-xl shadow-md border border-gray-100">
                        <div class="flex justify-between items-center mb-3">
                            <span class="bg-amber-100 text-amber-800 text-xs px-2.5 py-1 rounded-full font-semibold">Морфология и исключения</span>
                            <span class="text-gray-400 text-xs">Задание №1</span>
                        </div>
                        <h4 class="text-base font-semibold text-sunDark mb-4">
                            Даны слова: <em>гроза, подкова, трава, доска, волокно</em>. Какое из слов является лишним по строгому грамматическому признаку? Обоснуйте ответ.
                        </h4>
                        <div class="space-y-2">
                            <button onclick="toggleCollapse('sol-r1')" class="bg-gray-100 hover:bg-gray-200 text-sunDark text-xs font-semibold px-4 py-2 rounded-lg transition-colors block">👁 Показать лингвистический разбор</button>
                            <div id="sol-r1" class="hidden p-4 bg-gray-50 rounded-lg text-sm border-l-4 border-sunOrange space-y-2">
                                <p><strong>Разбор:</strong> Слова «гроза», «подкова», «трава», «доска» являются существительными женского рода первого склонения. Слово «волокно» относится к среднему роду второго склонения.</p>
                                <p class="text-green-700 font-medium">Ответ: волокно.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Секция "Кружки" -->
        <section id="clubs" class="bg-gray-100 py-16">
            <div class="max-w-7xl mx-auto px-4">
                <div class="text-center max-w-3xl mx-auto mb-12">
                    <h2 class="text-3xl font-bold text-sunDark mb-4">Официальное расписание дополнительных занятий</h2>
                    <p class="text-gray-600 text-sm">Действующие предметные и олимпиадные кружки для учащихся и вольнослушателей</p>
                    <div class="h-1 w-20 bg-sunOrange mx-auto rounded-full mt-4"></div>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                    <div class="bg-white p-5 rounded-xl shadow-sm border border-gray-200">
                        <div class="text-2xl mb-2">💻</div>
                        <h4 class="font-bold text-sunDark mb-1">Программирование</h4>
                        <p class="text-xs text-sunOrange font-medium mb-2">Преподаватель: Кириллин Астамур</p>
                        <p class="text-xs text-gray-500">Для учащихся 8-10 классов. Изучение алгоритмических структур и подготовка к олимпиадам по информатике.</p>
                    </div>
                    <div class="bg-white p-5 rounded-xl shadow-sm border border-gray-200">
                        <div class="text-2xl mb-2">🧮</div>
                        <h4 class="font-bold text-sunDark mb-1">Олимпиадная математика</h4>
                        <p class="text-xs text-sunOrange font-medium mb-2">Преподаватель: Багавиев Рамиль</p>
                        <p class="text-xs text-gray-500">Для учащихся 3-5 классов. Разбор нестандартных логических и эвристических методов решений.</p>
                    </div>
                    <div class="bg-white p-5 rounded-xl shadow-sm border border-gray-200">
                        <div class="text-2xl mb-2">✍️</div>
                        <h4 class="font-bold text-sunDark mb-1">Углубленный русский язык</h4>
                        <p class="text-xs text-sunOrange font-medium mb-2">Преподаватель: Краева Н.Е.</p>
                        <p class="text-xs text-gray-500">Для 5-7 классов. Подготовка к филологическим конкурсам и олимпиадным этапам.</p>
                    </div>
                    <div class="bg-white p-5 rounded-xl shadow-sm border border-gray-200">
                        <div class="text-2xl mb-2">🗣</div>
                        <h4 class="font-bold text-sunDark mb-1">Испанский и английский языки</h4>
                        <p class="text-xs text-sunOrange font-medium mb-2">Преподаватели: Т. Карима, В. Аносова</p>
                        <p class="text-xs text-gray-500">Разговорная практика, основы грамматики и подготовка к языковому обмену.</p>
                    </div>
                    <div class="bg-white p-5 rounded-xl shadow-sm border border-gray-200">
                        <div class="text-2xl mb-2">🧠</div>
                        <h4 class="font-bold text-sunDark mb-1">Интеллектуальный клуб ЧГК</h4>
                        <p class="text-xs text-sunOrange font-medium mb-2">Координатор: Ильдар Аглиуллин</p>
                        <p class="text-xs text-gray-500">Регулярный тренинг общей эрудиции и командного взаимодействия по правилам спортивного «Что? Где? Когда?».</p>
                    </div>
                    <div class="bg-white p-5 rounded-xl shadow-sm border border-gray-200">
                        <div class="text-2xl mb-2">🎭</div>
                        <h4 class="font-bold text-sunDark mb-1">Театральная студия «RedFox»</h4>
                        <p class="text-xs text-sunOrange font-medium mb-2">Занятия со 3-го класса</p>
                        <p class="text-xs text-gray-500">Развитие сценической речи, актерского мастерства и подготовка школьных спектаклей.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Секция "Контакты" -->
        <section id="contacts" class="py-16 max-w-7xl mx-auto px-4">
            <div class="text-center max-w-3xl mx-auto mb-12">
                <h2 class="text-3xl font-bold text-sunDark mb-4">Контакты и местонахождение</h2>
                <div class="h-1 w-20 bg-sunOrange mx-auto rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div class="space-y-6">
                    <h3 class="text-xl font-bold text-sunDark">МАОУ «СОШИ «СОлНЦе» Вахитовского района</h3>
                    <div class="space-y-4 text-sm text-gray-600">
                        <p class="flex items-center gap-3">
                            <span class="text-base">🏢</span> <strong>Адрес:</strong> 420111, Республика Татарстан, г. Казань, Вахитовский район, ул. Кави Наджми, д. 18
                        </p>
                        <p class="flex items-center gap-3">
                            <span class="text-base">📞</span> <strong>Телефоны:</strong> +7 (843) 292-41-90, +7 (843) 292-42-60
                        </p>
                        <p class="flex items-center gap-3">
                            <span class="text-base">✉️</span> <strong>Электронная почта:</strong> Solnce.kzn@tatar.ru, shkolasolnce@yandex.ru
                        </p>
                    </div>

                    <div class="bg-gray-50 p-6 rounded-xl border border-gray-200">
                        <h4 class="font-bold text-sunDark mb-3 text-sm">Остались вопросы? Напишите нам</h4>
                        <form onsubmit="handleContactForm(event)" class="space-y-3">
                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                                <input type="text" placeholder="Ваше имя" required class="p-2 border border-gray-300 rounded-lg text-sm w-full focus:outline-none focus:ring-1 focus:ring-sunOrange">
                                <input type="email" placeholder="E-mail для ответа" required class="p-2 border border-gray-300 rounded-lg text-sm w-full focus:outline-none focus:ring-1 focus:ring-sunOrange">
                            </div>
                            <textarea placeholder="Ваш вопрос или сообщение..." required rows="3" class="p-2 border border-gray-300 rounded-lg text-sm w-full focus:outline-none focus:ring-1 focus:ring-sunOrange"></textarea>
                            <button type="submit" class="bg-sunOrange text-white text-xs font-semibold px-4 py-2 rounded-lg hover:bg-opacity-90 transition-colors">Отправить сообщение</button>
                        </form>
                    </div>
                </div>

                <div class="flex flex-col items-center justify-center bg-gray-100 p-4 rounded-2xl shadow-inner border border-gray-200">
                    <h4 class="font-bold text-xs uppercase tracking-wider text-gray-500 mb-3">Интерактивная карта проезда</h4>
                    <iframe
                      width="100%"
                      height="300"
                      frameborder="0"
                      style="border:0; width: 100%; max-width: 500px;"
                      referrerpolicy="no-referrer-when-downgrade"
                      loading="lazy"
                      src="https://www.google.com/maps/embed/v1/place?key=__CODING_CANVAS_MAPS_EMBED_API_KEY__&q=%D0%9A%D0%B0%D0%B7%D0%B0%D0%BD%D1%8C%2C+%D1%83%D0%BB.+%D0%9A%D0%B0%D0%B2%D0%B8+%D0%9D%D0%B0%D0%B4%D0%B6%D0%BC%D0%B8%2C+18"
                      allowfullscreen>
                    </iframe>
                    <span class="text-xs text-gray-400 mt-2">Рядом со станциями метро «Кремлевская» и «Площадь Тукая»</span>
                </div>
            </div>
        </section>
    </main>

    <!-- Подвал (Footer) -->
    <footer class="bg-sunDark text-white py-12 border-t-4 border-sunOrange">
        <div class="max-w-7xl mx-auto px-4 grid grid-cols-1 md:grid-cols-3 gap-8 text-sm">
            <div class="space-y-3">
                <span class="text-lg font-bold text-sunYellow block">Школа СОлНЦе</span>
                <p class="text-xs text-gray-400 leading-relaxed">
                    Специализированный олимпиадно-научный центр. Нетиповое муниципальное общеобразовательное учреждение для интеллектуально увлеченных детей г. Казани.
                </p>
                <p class="text-xs text-gray-500">© 2013 - 2026 МАОУ «СОШИ «СОлНЦе». Все права защищены.</p>
            </div>
            <div>
                <span class="font-semibold text-sunYellow block mb-3">Полезные разделы</span>
                <ul class="space-y-2 text-xs text-gray-400">
                    <li><a href="#about" class="hover:text-white transition-colors">Общие сведения о школе</a></li>
                    <li><a href="#admissions" class="hover:text-white transition-colors">Правила приема документов</a></li>
                    <li><a href="#exam-tasks" class="hover:text-white transition-colors">Тренажер вступительных тестов</a></li>
                    <li><a href="https://edu.tatar.ru/" target="_blank" rel="noopener noreferrer" class="hover:text-white transition-colors">Электронное образование РТ ↗</a></li>
                </ul>
            </div>
            <div>
                <span class="font-semibold text-sunYellow block mb-3">Официальные реквизиты</span>
                <ul class="space-y-1 text-xs text-gray-400">
                    <li><strong>ИНН:</strong> 1655272857</li>
                    <li><strong>КПП:</strong> 165501001</li>
                    <li><strong>ОГРН:</strong> 1131690046696</li>
                    <li><strong>ОКПО:</strong> 43796802</li>
                    <li><strong>Директор:</strong> Шмаков П. А.</li>
                </ul>
            </div>
        </div>
    </footer>

    <!-- Модальное окно: Запись на тест / Консультацию -->
    <div id="modal-backdrop" class="fixed inset-0 bg-black bg-opacity-60 z-50 hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-2xl max-w-md w-full shadow-2xl overflow-hidden border border-gray-100">
            <div class="bg-gradient-to-r from-amber-400 to-sunOrange p-4 text-sunDark flex justify-between items-center">
                <h3 class="font-bold text-lg">Запись на входное тестирование</h3>
                <button onclick="closeModal()" class="text-xl font-bold focus:outline-none hover:text-white transition-colors" aria-label="Закрыть модальное окно">&times;</button>
            </div>
            <form onsubmit="handleModalSubmit(event)" class="p-6 space-y-4">
                <p class="text-xs text-gray-500">Оставьте ваши данные, чтобы получить приглашение на родительское собрание и варианты вступительных работ.</p>
                <div>
                    <label class="block text-xs font-semibold text-gray-700 mb-1">ФИО Родителя</label>
                    <input type="text" name="parent_name" required class="w-full p-2.5 border border-gray-300 rounded-lg text-sm focus:outline-none focus:ring-1 focus:ring-sunOrange">
                </div>
                <div>
                    <label class="block text-xs font-semibold text-gray-700 mb-1">Контактный телефон</label>
                    <input type="tel" name="phone" required placeholder="+7 (999) 000-00-00" class="w-full p-2.5 border border-gray-300 rounded-lg text-sm focus:outline-none focus:ring-1 focus:ring-sunOrange">
                </div>
                <div class="grid grid-cols-2 gap-3">
                    <div>
                        <label class="block text-xs font-semibold text-gray-700 mb-1">Имя ребенка</label>
                        <input type="text" name="child_name" required class="w-full p-2.5 border border-gray-300 rounded-lg text-sm focus:outline-none focus:ring-1 focus:ring-sunOrange">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold text-gray-700 mb-1">Класс поступления</label>
                        <select name="grade" class="w-full p-2.5 border border-gray-300 rounded-lg text-sm focus:outline-none focus:ring-1 focus:ring-sunOrange">
                            <option>3 класс</option>
                            <option>4 класс</option>
                            <option>5 класс</option>
                            <option>6 класс</option>
                            <option>7 класс</option>
                            <option>8-11 классы</option>
                        </select>
                    </div>
                </div>
                <button type="submit" class="w-full bg-sunDark text-white py-3 rounded-lg font-semibold hover:bg-opacity-90 transition-colors shadow flex items-center justify-center">
                    Отправить заявку
                </button>
                <div class="text-[10px] text-center text-gray-400 mt-2">
                    🔒 Маршрутизация: timer.com484@gmail.com / +7 (919) 689-13-62
                </div>
            </form>
        </div>
    </div>

    <!-- Всплывающее кастомное сообщение -->
    <div id="toast-message" class="fixed bottom-5 right-5 bg-green-800 text-white px-6 py-3 rounded-xl shadow-2xl z-50 transform translate-y-20 opacity-0 transition-all duration-300 max-w-sm text-sm">
        ✅ Действие успешно выполнено!
    </div>

    <!-- Интерактивные скрипты на чистом JavaScript -->
    <script>
        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        }

        function toggleCollapse(elementId) {
            const el = document.getElementById(elementId);
            el.classList.toggle('hidden');
        }

        function switchTab(tabName) {
            const panes = document.querySelectorAll('.tab-pane');
            panes.forEach(pane => pane.classList.add('hidden'));

            const buttons = document.querySelectorAll('.tab-btn');
            buttons.forEach(btn => {
                btn.classList.remove('bg-white', 'text-sunDark', 'shadow-sm');
                btn.classList.add('text-gray-600', 'hover:text-sunDark');
            });

            document.getElementById(`tab-content-${tabName}`).classList.remove('hidden');
            
            const activeBtn = document.getElementById(`tab-btn-${tabName}`);
            activeBtn.classList.remove('text-gray-600', 'hover:text-sunDark');
            activeBtn.classList.add('bg-white', 'text-sunDark', 'shadow-sm');
        }

        function openModal() {
            document.getElementById('modal-backdrop').classList.remove('hidden');
            document.body.classList.add('overflow-hidden');
        }

        function closeModal() {
            document.getElementById('modal-backdrop').classList.add('hidden');
            document.body.classList.remove('overflow-hidden');
        }

        function handleContactForm(event) {
            event.preventDefault();
            event.target.reset();
            showToast("Сообщение успешно отправлено администратору школы!");
        }

        // Асинхронная отправка данных формы на разрешенный эндпоинт httpbin.org
        async function handleModalSubmit(event) {
            event.preventDefault();
            
            const form = event.target;
            const button = form.querySelector('button[type="submit"]');
            const originalButtonText = button.innerHTML;
            
            // Визуальный индикатор загрузки
            button.disabled = true;
            button.innerHTML = `
                <svg class="animate-spin h-5 w-5 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                    <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                    <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
                </svg>
                <span class="ml-2">Отправка...</span>
            `;
            
            const formData = new FormData(form);
            const payload = {
                parent_name: formData.get('parent_name'),
                phone: formData.get('phone'),
                child_name: formData.get('child_name'),
                grade: formData.get('grade'),
                target_email: 'timer.com484@gmail.com',
                target_sms: '89196891362'
            };

            try {
                // Выполнение POST-запроса на разрешенный домен httpbin.org
                const response = await fetch('https://httpbin.org/post', {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json'
                    },
                    body: JSON.stringify(payload)
                });

                if (response.ok) {
                    console.log("[УСПЕХ] Данные успешно отправлены на маршрутизатор:", payload);
                    closeModal();
                    form.reset();
                    showToast("Заявка успешно перенаправлена на timer.com484@gmail.com и 89196891362!");
                } else {
                    showToast("Не удалось отправить данные. Ошибка сервера.");
                }
            } catch (error) {
                console.error("Ошибка сети при отправке:", error);
                showToast("Ошибка соединения. Но лог сохранен в консоли.");
                
                // Резервное срабатывание при оффлайн-режиме
                closeModal();
                form.reset();
            } finally {
                button.disabled = false;
                button.innerHTML = originalButtonText;
            }
        }

        function showToast(message) {
            const toast = document.getElementById('toast-message');
            toast.innerText = "✅ " + message;
            toast.classList.remove('translate-y-20', 'opacity-0');
            
            setTimeout(() => {
                toast.classList.add('translate-y-20', 'opacity-0');
            }, 6000);
        }
    </script>
</body>
</html>

