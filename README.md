#This is a modern, interactive Student Portal built with Tailwind CSS. It features a "glassmorphism" UI with a responsive sidebar, a visual attendance tracker, and a live JavaScript task manager. It’s designed to be fast, mobile-friendly, and more engaging than a standard school page.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nexus Academy Portal</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        .glass-card {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            transition: transform 0.3s ease;
        }
        .glass-card:hover { transform: translateY(-5px); }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 font-sans">

    <div class="flex h-screen overflow-hidden">
        <aside class="w-64 bg-indigo-900 text-white flex-shrink-0 hidden md:flex flex-col">
            <div class="p-6 text-2xl font-bold tracking-wider italic text-indigo-400">NEXUS ACADEMY</div>
            <nav class="flex-1 px-4 space-y-2 mt-4">
                <a href="#" class="flex items-center p-3 bg-indigo-800 rounded-lg"><i class="fas fa-home mr-3"></i> Dashboard</a>
                <a href="#" class="flex items-center p-3 hover:bg-indigo-800 rounded-lg transition"><i class="fas fa-book mr-3"></i> Courses</a>
                <a href="#" class="flex items-center p-3 hover:bg-indigo-800 rounded-lg transition"><i class="fas fa-calendar-alt mr-3"></i> Schedule</a>
                <a href="#" class="flex items-center p-3 hover:bg-indigo-800 rounded-lg transition"><i class="fas fa-user-graduate mr-3"></i> Grades</a>
            </nav>
            <div class="p-6 border-t border-indigo-800">
                <button class="w-full py-2 bg-red-500 hover:bg-red-600 rounded-lg font-semibold transition">Logout</button>
            </div>
        </aside>

        <main class="flex-1 overflow-y-auto p-8">
            <header class="flex justify-between items-center mb-8">
                <div>
                    <h1 class="text-3xl font-bold">Welcome back, Alex! 👋</h1>
                    <p class="text-slate-500">You have 3 assignments due this week.</p>
                </div>
                <div class="flex items-center space-x-4">
                    <button class="p-2 bg-white rounded-full shadow-sm relative">
                        <i class="fas fa-bell text-slate-600"></i>
                        <span class="absolute top-0 right-0 h-2 w-2 bg-red-500 rounded-full"></span>
                    </button>
                    <img src="https://ui-avatars.com/api/?name=Alex+Smith&background=6366f1&color=fff" class="w-10 h-10 rounded-full border-2 border-indigo-500" alt="Profile">
                </div>
            </header>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
                <div class="glass-card p-6 rounded-2xl shadow-sm border border-slate-200">
                    <div class="flex items-center justify-between mb-4">
                        <span class="p-3 bg-blue-100 text-blue-600 rounded-xl"><i class="fas fa-graduation-cap"></i></span>
                        <span class="text-green-500 font-bold">3.8 GPA</span>
                    </div>
                    <h3 class="font-semibold text-slate-500">Current Standing</h3>
                    <p class="text-2xl font-bold">Dean's List</p>
                </div>
                <div class="glass-card p-6 rounded-2xl shadow-sm border border-slate-200">
                    <div class="flex items-center justify-between mb-4">
                        <span class="p-3 bg-purple-100 text-purple-600 rounded-xl"><i class="fas fa-clock"></i></span>
                        <span class="text-slate-400">Next: 10:00 AM</span>
                    </div>
                    <h3 class="font-semibold text-slate-500">Upcoming Class</h3>
                    <p class="text-2xl font-bold">Advanced Physics</p>
                </div>
                <div class="glass-card p-6 rounded-2xl shadow-sm border border-slate-200">
                    <div class="flex items-center justify-between mb-4">
                        <span class="p-3 bg-amber-100 text-amber-600 rounded-xl"><i class="fas fa-tasks"></i></span>
                        <span class="text-red-500 font-bold italic">Urgent</span>
                    </div>
                    <h3 class="font-semibold text-slate-500">Pending Tasks</h3>
                    <p class="text-2xl font-bold">3 Assignments</p>
                </div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                <div class="bg-white p-6 rounded-2xl shadow-sm">
                    <h3 class="text-xl font-bold mb-4">Weekly Attendance</h3>
                    <div class="flex items-end space-x-2 h-48 py-4">
                        <div class="w-full bg-indigo-100 rounded-t-lg relative group h-full">
                            <div class="absolute bottom-0 w-full bg-indigo-500 rounded-t-lg transition-all duration-500" style="height: 90%"></div>
                        </div>
                        <div class="w-full bg-indigo-100 rounded-t-lg relative h-full">
                            <div class="absolute bottom-0 w-full bg-indigo-500 rounded-t-lg" style="height: 75%"></div>
                        </div>
                        <div class="w-full bg-indigo-100 rounded-t-lg relative h-full">
                            <div class="absolute bottom-0 w-full bg-indigo-500 rounded-t-lg" style="height: 95%"></div>
                        </div>
                        <div class="w-full bg-indigo-100 rounded-t-lg relative h-full">
                            <div class="absolute bottom-0 w-full bg-indigo-500 rounded-t-lg" style="height: 80%"></div>
                        </div>
                        <div class="w-full bg-indigo-100 rounded-t-lg relative h-full">
                            <div class="absolute bottom-0 w-full bg-indigo-500 rounded-t-lg" style="height: 100%"></div>
                        </div>
                    </div>
                    <div class="flex justify-between text-xs font-bold text-slate-400 mt-2">
                        <span>MON</span><span>TUE</span><span>WED</span><span>THU</span><span>FRI</span>
                    </div>
                </div>

                <div class="bg-white p-6 rounded-2xl shadow-sm">
                    <h3 class="text-xl font-bold mb-4">Quick Tasks</h3>
                    <ul class="space-y-3" id="task-list">
                        <li class="flex items-center p-3 bg-slate-50 rounded-lg">
                            <input type="checkbox" class="h-5 w-5 rounded border-gray-300 text-indigo-600 focus:ring-indigo-500 mr-3">
                            <span class="flex-1">Finish Calculus Homework</span>
                            <span class="text-xs bg-red-100 text-red-600 px-2 py-1 rounded">Today</span>
                        </li>
                        <li class="flex items-center p-3 bg-slate-50 rounded-lg">
                            <input type="checkbox" class="h-5 w-5 rounded border-gray-300 text-indigo-600 focus:ring-indigo-500 mr-3">
                            <span class="flex-1">Submit Art Project</span>
                            <span class="text-xs bg-amber-100 text-amber-600 px-2 py-1 rounded">2 Days</span>
                        </li>
                    </ul>
                    <button onclick="addTask()" class="mt-4 w-full py-2 border-2 border-dashed border-slate-200 text-slate-400 rounded-lg hover:border-indigo-300 hover:text-indigo-400 transition">
                        + Add Custom Task
                    </button>
                </div>
            </div>
        </main>
    </div>

    <script>
        function addTask() {
            const task = prompt("Enter a new task:");
            if (task) {
                const list = document.getElementById('task-list');
                const li = document.createElement('li');
                li.className = "flex items-center p-3 bg-slate-50 rounded-lg animate-pulse";
                li.innerHTML = `
                    <input type="checkbox" class="h-5 w-5 rounded border-gray-300 text-indigo-600 mr-3">
                    <span class="flex-1">${task}</span>
                    <span class="text-xs bg-slate-200 text-slate-600 px-2 py-1 rounded">New</span>
                `;
                list.appendChild(li);
                setTimeout(() => li.classList.remove('animate-pulse'), 1000);
            }
        }
    </script>
</body>
</html>
