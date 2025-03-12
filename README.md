<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern Dashboard</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script> <!-- For charts -->
</head>

<body class="bg-gray-100 dark:bg-gray-900">
    <!-- Dashboard Container -->
    <div class="min-h-screen flex flex-col md:flex-row">
        <!-- Sidebar -->
        <aside class="bg-gray-800 text-white w-full md:w-64 p-4">
            <div class="text-xl font-bold mb-6">Modern Dashboard</div>
            <nav>
                <ul class="space-y-2">
                    <li>
                        <a href="#overview" class="flex items-center p-2 hover:bg-gray-700 rounded">
                            <span>📈</span>
                            <span class="ml-2">Overview</span>
                        </a>
                    </li>
                    <li>
                        <a href="#stats" class="flex items-center p-2 hover:bg-gray-700 rounded">
                            <span>📊</span>
                            <span class="ml-2">Statistics</span>
                        </a>
                    </li>
                    <li>
                        <a href="#reports" class="flex items-center p-2 hover:bg-gray-700 rounded">
                            <span>📑</span>
                            <span class="ml-2">Reports</span>
                        </a>
                    </li>
                    <li>
                        <a href="#team" class="flex items-center p-2 hover:bg-gray-700 rounded">
                            <span>👥</span>
                            <span class="ml-2">Team</span>
                        </a>
                    </li>
                    <li>
                        <a href="#settings" class="flex items-center p-2 hover:bg-gray-700 rounded">
                            <span>⚙️</span>
                            <span class="ml-2">Settings</span>
                        </a>
                    </li>
                </ul>
            </nav>
        </aside>

        <!-- Main Content -->
        <div class="flex-1 flex flex-col">
            <!-- Header -->
            <header class="bg-white dark:bg-gray-800 shadow p-4">
                <div class="flex items-center justify-between">
                    <h1 class="text-xl font-bold dark:text-white">Dashboard</h1>
                    <div class="flex items-center space-x-4">
                        <!-- Dark Mode Toggle -->
                        <button id="theme-toggle" class="p-2 rounded-lg bg-gray-200 dark:bg-gray-700">
                            <span id="theme-icon">🌙</span>
                        </button>
                        <!-- Search Bar -->
                        <input type="text" placeholder="Search..."
                            class="p-2 border border-gray-300 rounded-lg dark:bg-gray-700 dark:text-white">
                        <button class="bg-blue-600 text-white p-2 rounded-lg hover:bg-blue-700">Search</button>
                    </div>
                </div>
            </header>

            <!-- Main Content Area -->
            <main class="flex-1 p-6">
                <!-- Overview Section -->
                <section id="overview" class="mb-8">
                    <h2 class="text-2xl font-bold mb-4 dark:text-white">Overview</h2>
                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                        <!-- Card 1 -->
                        <div class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-lg">
                            <h2 class="text-xl font-bold mb-4 dark:text-white">Total Sales</h2>
                            <p class="text-gray-700 dark:text-gray-300">$25,000</p>
                        </div>
                        <!-- Card 2 -->
                        <div class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-lg">
                            <h2 class="text-xl font-bold mb-4 dark:text-white">Active Users</h2>
                            <p class="text-gray-700 dark:text-gray-300">1,234</p>
                        </div>
                        <!-- Card 3 -->
                        <div class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-lg">
                            <h2 class="text-xl font-bold mb-4 dark:text-white">Tasks Completed</h2>
                            <p class="text-gray-700 dark:text-gray-300">56</p>
                        </div>
                        <!-- Card 4 -->
                        <div class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-lg">
                            <h2 class="text-xl font-bold mb-4 dark:text-white">Pending Issues</h2>
                            <p class="text-gray-700 dark:text-gray-300">12</p>
                        </div>
                    </div>
                </section>

                <!-- Statistics Section -->
                <section id="stats" class="mb-8">
                    <h2 class="text-2xl font-bold mb-4 dark:text-white">Statistics</h2>
                    <div class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-lg">
                        <canvas id="myChart" class="w-full h-64"></canvas>
                    </div>
                </section>

                <!-- Reports Section -->
                <section id="reports" class="mb-8">
                    <h2 class="text-2xl font-bold mb-4 dark:text-white">Reports</h2>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <!-- Report Card 1 -->
                        <div class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-lg">
                            <h2 class="text-xl font-bold mb-4 dark:text-white">Monthly Report</h2>
                            <p class="text-gray-700 dark:text-gray-300">Download the latest monthly report.</p>
                            <button
                                class="mt-4 bg-blue-600 text-white p-2 rounded-lg hover:bg-blue-700">Download</button>
                        </div>
                        <!-- Report Card 2 -->
                        <div class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-lg">
                            <h2 class="text-xl font-bold mb-4 dark:text-white">Annual Report</h2>
                            <p class="text-gray-700 dark:text-gray-300">Download the latest annual report.</p>
                            <button
                                class="mt-4 bg-blue-600 text-white p-2 rounded-lg hover:bg-blue-700">Download</button>
                        </div>
                    </div>
                </section>

                <!-- Team Section -->
                <section id="team" class="mb-8">
                    <h2 class="text-2xl font-bold mb-4 dark:text-white">Team Members</h2>
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                        <!-- Team Member 1 -->
                        <div class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-lg">
                            <h2 class="text-xl font-bold mb-4 dark:text-white">John Doe</h2>
                            <p class="text-gray-700 dark:text-gray-300">Project Manager</p>
                        </div>
                        <!-- Team Member 2 -->
                        <div class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-lg">
                            <h2 class="text-xl font-bold mb-4 dark:text-white">Jane Smith</h2>
                            <p class="text-gray-700 dark:text-gray-300">UI/UX Designer</p>
                        </div>
                        <!-- Team Member 3 -->
                        <div class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-lg">
                            <h2 class="text-xl font-bold mb-4 dark:text-white">Alice Johnson</h2>
                            <p class="text-gray-700 dark:text-gray-300">Software Engineer</p>
                        </div>
                    </div>
                </section>
            </main>

            <!-- Footer -->
            <footer class="bg-white dark:bg-gray-800 shadow p-4">
                <div class="text-center text-gray-600 dark:text-gray-300">
                    &copy; 2023 Modern Dashboard. All rights reserved.
                </div>
            </footer>
        </div>
    </div>

    <!-- Dark Mode Toggle Script -->
    <script>
        const themeToggle = document.getElementById('theme-toggle');
        const themeIcon = document.getElementById('theme-icon');
        const body = document.body;

        themeToggle.addEventListener('click', () => {
            body.classList.toggle('dark');
            themeIcon.textContent = body.classList.contains('dark') ? '☀️' : '🌙';
        });
    </script>

    <!-- Chart Script -->
    <script>
        const ctx = document.getElementById('myChart').getContext('2d');
        const myChart = new Chart(ctx, {
            type: 'line',
            data: {
                labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun'],
                datasets: [{
                    label: 'Sales',
                    data: [12000, 19000, 3000, 5000, 2000, 3000],
                    borderColor: 'rgba(75, 192, 192, 1)',
                    tension: 0.1
                }]
            },
            options: {
                scales: {
                    y: {
                        beginAtZero: true
                    }
                }
            }
        });
    </script>
</body>

</html>