<!-- Tailwind CSS CDN -->

&#x20; <script src="https://cdn.tailwindcss.com"></script>



&#x20; 



&#x20; 









&#x20; <!-- Header -->

&#x20; <header class="sticky top-0 z-50 border-b border-slate-200/80 bg-white/90 backdrop-blur-xl">

&#x20;   <div class="mx-auto max-w-7xl px-4 py-4 sm:px-6 lg:px-8">



&#x20;     <div class="flex flex-col gap-4 lg:flex-row lg:items-center lg:justify-between">



&#x20;       <div>

&#x20;         <div class="flex items-center gap-3">

&#x20;           <div class="flex h-11 w-11 items-center justify-center rounded-2xl bg-ca-600 text-xl font-black text-white shadow-lg shadow-ca-600/20">

&#x20;             CA

&#x20;           </div>

&#x20;           <div>

&#x20;             <h1 class="text-xl font-black tracking-tight text-slate-900">

&#x20;               CA Exam Study Tracker

&#x20;             </h1>

&#x20;             <p id="profileSubtitle" class="text-sm text-slate-500">

&#x20;               My CA Final · May 2027

&#x20;             </p>

&#x20;           </div>

&#x20;         </div>

&#x20;       </div>



&#x20;       <!-- Profile Toggle -->

&#x20;       <div class="rounded-2xl bg-slate-100 p-1.5 shadow-inner">

&#x20;         <div class="flex gap-1">

&#x20;           <button

&#x20;             id="finalBtn"

&#x20;             onclick="switchProfile('final')"

&#x20;             class="profile-btn rounded-xl px-4 py-2.5 text-sm font-bold transition"

&#x20;           >

&#x20;             My CA Final

&#x20;             <span class="hidden sm:inline"> (May 2027)</span>

&#x20;           </button>



&#x20;           <button

&#x20;             id="interBtn"

&#x20;             onclick="switchProfile('inter')"

&#x20;             class="profile-btn rounded-xl px-4 py-2.5 text-sm font-bold transition"

&#x20;           >

&#x20;             Sister's CA Inter

&#x20;             <span class="hidden sm:inline"> (Jan Exam)</span>

&#x20;           </button>

&#x20;         </div>

&#x20;       </div>



&#x20;     </div>

&#x20;   </div>

&#x20; </header>



&#x20; <main class="mx-auto max-w-7xl px-4 py-6 sm:px-6 lg:px-8">



&#x20;   <!-- Dashboard Summary -->

&#x20;   <section class="grid gap-4 sm:grid-cols-2 lg:grid-cols-4">



&#x20;     <div class="glass rounded-3xl border border-slate-200 p-5 shadow-sm">

&#x20;       <div class="mb-3 flex items-center justify-between">

&#x20;         <span class="text-sm font-semibold text-slate-500">Exam Countdown</span>

&#x20;         <span class="rounded-xl bg-blue-50 px-2.5 py-1 text-xs font-bold text-blue-600">DAYS</span>

&#x20;       </div>

&#x20;       <div id="examCountdown" class="text-3xl font-black text-slate-900">--</div>

&#x20;       <div id="examDateLabel" class="mt-1 text-xs text-slate-500">--</div>

&#x20;     </div>



&#x20;     <div class="glass rounded-3xl border border-slate-200 p-5 shadow-sm">

&#x20;       <div class="mb-3 flex items-center justify-between">

&#x20;         <span class="text-sm font-semibold text-slate-500">Class Deadline</span>

&#x20;         <span class="rounded-xl bg-amber-50 px-2.5 py-1 text-xs font-bold text-amber-600">DEC 31</span>

&#x20;       </div>

&#x20;       <div id="classCountdown" class="text-3xl font-black text-slate-900">--</div>

&#x20;       <div class="mt-1 text-xs text-slate-500">Days until class completion deadline</div>

&#x20;     </div>



&#x20;     <div class="glass rounded-3xl border border-slate-200 p-5 shadow-sm">

&#x20;       <div class="mb-3 flex items-center justify-between">

&#x20;         <span class="text-sm font-semibold text-slate-500">Total Lectures</span>

&#x20;         <span class="rounded-xl bg-purple-50 px-2.5 py-1 text-xs font-bold text-purple-600">ALL</span>

&#x20;       </div>

&#x20;       <div id="totalLectures" class="text-3xl font-black text-slate-900">0</div>

&#x20;       <div id="completedLectures" class="mt-1 text-xs text-slate-500">0 completed</div>

&#x20;     </div>



&#x20;     <div class="glass rounded-3xl border border-slate-200 p-5 shadow-sm">

&#x20;       <div class="mb-3 flex items-center justify-between">

&#x20;         <span class="text-sm font-semibold text-slate-500">Today's Pace</span>

&#x20;         <span class="rounded-xl bg-ca-50 px-2.5 py-1 text-xs font-bold text-ca-600">LECTURES/DAY</span>

&#x20;       </div>

&#x20;       <div id="overallPace" class="text-3xl font-black text-slate-900">0</div>

&#x20;       <div class="mt-1 text-xs text-slate-500">Required to finish classes on time</div>

&#x20;     </div>



&#x20;   </section>



&#x20;   <!-- Overall progress -->

&#x20;   <section class="glass mt-5 rounded-3xl border border-slate-200 p-5 shadow-sm">

&#x20;     <div class="mb-3 flex items-center justify-between gap-4">

&#x20;       <div>

&#x20;         <h2 class="font-bold text-slate-900">Overall Class Progress</h2>

&#x20;         <p class="text-xs text-slate-500">Across all 6 subjects</p>

&#x20;       </div>

&#x20;       <div id="overallPercent" class="text-2xl font-black text-ca-600">0%</div>

&#x20;     </div>



&#x20;     <div class="h-3 overflow-hidden rounded-full bg-slate-100">

&#x20;       <div

&#x20;         id="overallProgressBar"

&#x20;         class="progress-bar h-full rounded-full bg-gradient-to-r from-ca-600 to-emerald-400"

&#x20;         style="width: 0%"

&#x20;       ></div>

&#x20;     </div>

&#x20;   </section>



&#x20;   <!-- Subject section -->

&#x20;   <section class="mt-7">



&#x20;     <div class="mb-4 flex flex-col gap-2 sm:flex-row sm:items-end sm:justify-between">

&#x20;       <div>

&#x20;         <h2 class="text-2xl font-black tracking-tight text-slate-900">Your 6 Subjects</h2>

&#x20;         <p class="text-sm text-slate-500">

&#x20;           Update lectures whenever you finish a class. Everything saves automatically.

&#x20;         </p>

&#x20;       </div>



&#x20;       <div class="rounded-xl bg-white px-3 py-2 text-xs font-semibold text-slate-500 shadow-sm ring-1 ring-slate-200">

&#x20;         💾 Auto-saved locally

&#x20;       </div>

&#x20;     </div>



&#x20;     <div id="subjectsGrid" class="grid gap-4 md:grid-cols-2 xl:grid-cols-3"></div>



&#x20;   </section>



&#x20;   <!-- Daily plan -->

&#x20;   <section class="mt-7 grid gap-5 lg:grid-cols-3">



&#x20;     <div class="glass rounded-3xl border border-slate-200 p-6 shadow-sm lg:col-span-2">

&#x20;       <div class="mb-5">

&#x20;         <h2 class="text-lg font-black text-slate-900">Daily Lecture Plan</h2>

&#x20;         <p class="text-sm text-slate-500">

&#x20;           The tracker calculates the pace needed to complete classes by December 31.

&#x20;         </p>

&#x20;       </div>



&#x20;       <div id="dailyPlan" class="space-y-3"></div>

&#x20;     </div>



&#x20;     <div class="glass rounded-3xl border border-slate-200 p-6 shadow-sm">

&#x20;       <h2 class="text-lg font-black text-slate-900">Quick Settings</h2>

&#x20;       <p class="mt-1 text-sm text-slate-500">

&#x20;         Change exam dates or reset this profile.

&#x20;       </p>



&#x20;       <div class="mt-5 space-y-4">



&#x20;         <label class="block">

&#x20;           <span class="mb-1.5 block text-xs font-bold uppercase tracking-wide text-slate-500">

&#x20;             Exam Date

&#x20;           </span>

&#x20;           <input

&#x20;             id="examDateInput"

&#x20;             type="date"

&#x20;             onchange="updateExamDate(this.value)"

&#x20;             class="w-full rounded-xl border border-slate-200 bg-white px-3 py-2.5 text-sm font-semibold outline-none focus:border-ca-500 focus:ring-2 focus:ring-ca-500/20"

&#x20;           />

&#x20;         </label>



&#x20;         <button

&#x20;           onclick="resetCurrentProfile()"

&#x20;           class="w-full rounded-xl border border-red-200 bg-red-50 px-4 py-3 text-sm font-bold text-red-600 transition hover:bg-red-100"

&#x20;         >

&#x20;           Reset Current Profile

&#x20;         </button>



&#x20;         <div class="rounded-2xl bg-slate-50 p-4 text-xs leading-5 text-slate-500">

&#x20;           <strong class="text-slate-700">How pace works:</strong><br />

&#x20;           Remaining lectures ÷ remaining days until Dec 31.

&#x20;           If you fall behind, the required lectures/day automatically increases.

&#x20;         </div>



&#x20;       </div>

&#x20;     </div>



&#x20;   </section>



&#x20;   <footer class="py-8 text-center text-xs text-slate-400">

&#x20;     CA Study Tracker · Data stays in this browser using localStorage

&#x20;   </footer>



&#x20; </main>



html {

&#x20;     scroll-behavior: smooth;

&#x20;   }



&#x20;   body {

&#x20;     background:

&#x20;       radial-gradient(circle at top left, rgba(15,159,127,.10), transparent 30%),

&#x20;       radial-gradient(circle at top right, rgba(59,130,246,.08), transparent 28%),

&#x20;       #f8fafc;

&#x20;   }



&#x20;   .glass {

&#x20;     background: rgba(255,255,255,.86);

&#x20;     backdrop-filter: blur(14px);

&#x20;     -webkit-backdrop-filter: blur(14px);

&#x20;   }



&#x20;   .progress-bar {

&#x20;     transition: width .35s ease;

&#x20;   }



&#x20;   input\[type="number"]::-webkit-inner-spin-button,

&#x20;   input\[type="number"]::-webkit-outer-spin-button {

&#x20;     opacity: 1;

&#x20;   }

**tailwind.config = {**

&#x20;     **theme: {**

&#x20;       **extend: {**

&#x20;         **colors: {**

&#x20;           **ca: {**

&#x20;             **50: '#eefbf7',**

&#x20;             **100: '#d7f5ec',**

&#x20;             **500: '#0f9f7f',**

&#x20;             **600: '#087f67',**

&#x20;             **700: '#066653',**

&#x20;             **900: '#063d33'**

&#x20;           **}**

&#x20;         **}**

&#x20;       **}**

&#x20;     **}**

&#x20;   **};**



**/\* =========================================================**

&#x20;      **CA EXAM STUDY TRACKER**

&#x20;      **========================================================= \*/**



&#x20;   **const STORAGE\_KEY = "ca\_exam\_study\_tracker\_v1";**



&#x20;   **const defaultData = {**

&#x20;     **activeProfile: "final",**



&#x20;     **final: {**

&#x20;       **name: "My CA Final",**

&#x20;       **examLabel: "May 2027",**

&#x20;       **examDate: "2027-05-01",**

&#x20;       **classDeadline: "2026-12-31",**



&#x20;       **subjects: \[**

&#x20;         **{ name: "Financial Reporting", short: "FR", color: "blue", total: 100, completed: 0 },**

&#x20;         **{ name: "Strategic Financial Management", short: "SFM", color: "purple", total: 90, completed: 0 },**

&#x20;         **{ name: "Advanced Auditing", short: "Audit", color: "amber", total: 85, completed: 0 },**

&#x20;         **{ name: "Direct Tax", short: "DT", color: "red", total: 100, completed: 0 },**

&#x20;         **{ name: "Indirect Tax", short: "IDT", color: "cyan", total: 90, completed: 0 },**

&#x20;         **{ name: "IBS / Elective", short: "IBS", color: "emerald", total: 70, completed: 0 }**

&#x20;       **]**

&#x20;     **},**



&#x20;     **inter: {**

&#x20;       **name: "Sister's CA Inter",**

&#x20;       **examLabel: "Jan Exam",**

&#x20;       **examDate: "2027-01-15",**

&#x20;       **classDeadline: "2026-12-31",**



&#x20;       **subjects: \[**

&#x20;         **{ name: "Advanced Accounting", short: "Accounts", color: "blue", total: 100, completed: 0 },**

&#x20;         **{ name: "Corporate \& Other Laws", short: "Law", color: "purple", total: 75, completed: 0 },**

&#x20;         **{ name: "Taxation", short: "Tax", color: "red", total: 110, completed: 0 },**

&#x20;         **{ name: "Cost \& Management Accounting", short: "Costing", color: "amber", total: 90, completed: 0 },**

&#x20;         **{ name: "Auditing \& Ethics", short: "Audit", color: "cyan", total: 80, completed: 0 },**

&#x20;         **{ name: "Financial Management \& SM", short: "FM/SM", color: "emerald", total: 85, completed: 0 }**

&#x20;       **]**

&#x20;     **}**

&#x20;   **};**



&#x20;   **let appData = loadData();**



&#x20;   **function deepClone(obj) {**

&#x20;     **return JSON.parse(JSON.stringify(obj));**

&#x20;   **}**



&#x20;   **function loadData() {**

&#x20;     **try {**

&#x20;       **const saved = localStorage.getItem(STORAGE\_KEY);**



&#x20;       **if (!saved) {**

&#x20;         **return deepClone(defaultData);**

&#x20;       **}**



&#x20;       **const parsed = JSON.parse(saved);**



&#x20;       **// Basic migration/safety fallback**

&#x20;       **if (!parsed.final || !parsed.inter) {**

&#x20;         **return deepClone(defaultData);**

&#x20;       **}**



&#x20;       **return parsed;**

&#x20;     **} catch (error) {**

&#x20;       **console.warn("Could not load saved data:", error);**

&#x20;       **return deepClone(defaultData);**

&#x20;     **}**

&#x20;   **}**



&#x20;   **function saveData() {**

&#x20;     **try {**

&#x20;       **localStorage.setItem(STORAGE\_KEY, JSON.stringify(appData));**

&#x20;     **} catch (error) {**

&#x20;       **console.warn("Could not save data:", error);**

&#x20;     **}**

&#x20;   **}**



&#x20;   **function currentProfile() {**

&#x20;     **return appData\[appData.activeProfile];**

&#x20;   **}**



&#x20;   **function switchProfile(profile) {**

&#x20;     **appData.activeProfile = profile;**

&#x20;     **saveData();**

&#x20;     **render();**

&#x20;   **}**



&#x20;   **function updateExamDate(value) {**

&#x20;     **currentProfile().examDate = value;**

&#x20;     **saveData();**

&#x20;     **render();**

&#x20;   **}**



&#x20;   **function resetCurrentProfile() {**

&#x20;     **const profile = appData.activeProfile;**

&#x20;     **const label = currentProfile().name;**



&#x20;     **if (!confirm(`Reset all lecture progress for ${label}?`)) {**

&#x20;       **return;**

&#x20;     **}**



&#x20;     **appData\[profile] = deepClone(defaultData\[profile]);**

&#x20;     **saveData();**

&#x20;     **render();**

&#x20;   **}**



&#x20;   **function updateSubject(index, field, value) {**

&#x20;     **const subject = currentProfile().subjects\[index];**



&#x20;     **let numericValue = Number(value);**



&#x20;     **if (!Number.isFinite(numericValue)) {**

&#x20;       **numericValue = 0;**

&#x20;     **}**



&#x20;     **numericValue = Math.max(0, Math.floor(numericValue));**



&#x20;     **if (field === "completed") {**

&#x20;       **numericValue = Math.min(numericValue, Number(subject.total) || 0);**

&#x20;     **}**



&#x20;     **subject\[field] = numericValue;**



&#x20;     **saveData();**

&#x20;     **render();**

&#x20;   **}**



&#x20;   **function daysBetween(from, to) {**

&#x20;     **const start = new Date(from + "T00:00:00");**

&#x20;     **const end = new Date(to + "T00:00:00");**



&#x20;     **const diff = end.getTime() - start.getTime();**

&#x20;     **return Math.max(0, Math.ceil(diff / (1000 \* 60 \* 60 \* 24)));**

&#x20;   **}**



&#x20;   **function todayISO() {**

&#x20;     **const now = new Date();**



&#x20;     **const year = now.getFullYear();**

&#x20;     **const month = String(now.getMonth() + 1).padStart(2, "0");**

&#x20;     **const day = String(now.getDate()).padStart(2, "0");**



&#x20;     **return `${year}-${month}-${day}`;**

&#x20;   **}**



&#x20;   **function formatDate(dateString) {**

&#x20;     **if (!dateString) return "--";**



&#x20;     **const date = new Date(dateString + "T00:00:00");**



&#x20;     **return date.toLocaleDateString("en-IN", {**

&#x20;       **day: "numeric",**

&#x20;       **month: "short",**

&#x20;       **year: "numeric"**

&#x20;     **});**

&#x20;   **}**



&#x20;   **function calculateDaysRemaining(dateString) {**

&#x20;     **return daysBetween(todayISO(), dateString);**

&#x20;   **}**



&#x20;   **function getSubjectStats(subject) {**

&#x20;     **const total = Math.max(0, Number(subject.total) || 0);**

&#x20;     **const completed = Math.min(**

&#x20;       **total,**

&#x20;       **Math.max(0, Number(subject.completed) || 0)**

&#x20;     **);**



&#x20;     **const remaining = Math.max(0, total - completed);**

&#x20;     **const deadline = currentProfile().classDeadline;**

&#x20;     **const daysLeft = calculateDaysRemaining(deadline);**



&#x20;     **let pace = 0;**



&#x20;     **if (remaining > 0) {**

&#x20;       **if (daysLeft > 0) {**

&#x20;         **pace = remaining / daysLeft;**

&#x20;       **} else {**

&#x20;         **// Deadline passed: show the remaining lecture count as**

&#x20;         **// the minimum urgent daily pace rather than infinity.**

&#x20;         **pace = remaining;**

&#x20;       **}**

&#x20;     **}**



&#x20;     **const percentage = total > 0**

&#x20;       **? Math.min(100, (completed / total) \* 100)**

&#x20;       **: 0;**



&#x20;     **return {**

&#x20;       **total,**

&#x20;       **completed,**

&#x20;       **remaining,**

&#x20;       **daysLeft,**

&#x20;       **pace,**

&#x20;       **percentage**

&#x20;     **};**

&#x20;   **}**



&#x20;   **function getOverallStats() {**

&#x20;     **const subjects = currentProfile().subjects;**



&#x20;     **let total = 0;**

&#x20;     **let completed = 0;**



&#x20;     **subjects.forEach(subject => {**

&#x20;       **total += Number(subject.total) || 0;**

&#x20;       **completed += Math.min(**

&#x20;         **Number(subject.total) || 0,**

&#x20;         **Number(subject.completed) || 0**

&#x20;       **);**

&#x20;     **});**



&#x20;     **const remaining = Math.max(0, total - completed);**

&#x20;     **const daysLeft = calculateDaysRemaining(currentProfile().classDeadline);**



&#x20;     **const pace = remaining > 0**

&#x20;       **? daysLeft > 0**

&#x20;         **? remaining / daysLeft**

&#x20;         **: remaining**

&#x20;       **: 0;**



&#x20;     **const percentage = total > 0**

&#x20;       **? Math.min(100, completed / total \* 100)**

&#x20;       **: 0;**



&#x20;     **return {**

&#x20;       **total,**

&#x20;       **completed,**

&#x20;       **remaining,**

&#x20;       **daysLeft,**

&#x20;       **pace,**

&#x20;       **percentage**

&#x20;     **};**

&#x20;   **}**



&#x20;   **function colorClasses(color) {**

&#x20;     **const colors = {**

&#x20;       **blue: {**

&#x20;         **icon: "bg-blue-50 text-blue-600",**

&#x20;         **bar: "bg-blue-500",**

&#x20;         **badge: "bg-blue-50 text-blue-600",**

&#x20;         **ring: "focus:border-blue-500 focus:ring-blue-500/20"**

&#x20;       **},**

&#x20;       **purple: {**

&#x20;         **icon: "bg-purple-50 text-purple-600",**

&#x20;         **bar: "bg-purple-500",**

&#x20;         **badge: "bg-purple-50 text-purple-600",**

&#x20;         **ring: "focus:border-purple-500 focus:ring-purple-500/20"**

&#x20;       **},**

&#x20;       **amber: {**

&#x20;         **icon: "bg-amber-50 text-amber-600",**

&#x20;         **bar: "bg-amber-500",**

&#x20;         **badge: "bg-amber-50 text-amber-600",**

&#x20;         **ring: "focus:border-amber-500 focus:ring-amber-500/20"**

&#x20;       **},**

&#x20;       **red: {**

&#x20;         **icon: "bg-red-50 text-red-600",**

&#x20;         **bar: "bg-red-500",**

&#x20;         **badge: "bg-red-50 text-red-600",**

&#x20;         **ring: "focus:border-red-500 focus:ring-red-500/20"**

&#x20;       **},**

&#x20;       **cyan: {**

&#x20;         **icon: "bg-cyan-50 text-cyan-600",**

&#x20;         **bar: "bg-cyan-500",**

&#x20;         **badge: "bg-cyan-50 text-cyan-600",**

&#x20;         **ring: "focus:border-cyan-500 focus:ring-cyan-500/20"**

&#x20;       **},**

&#x20;       **emerald: {**

&#x20;         **icon: "bg-emerald-50 text-emerald-600",**

&#x20;         **bar: "bg-emerald-500",**

&#x20;         **badge: "bg-emerald-50 text-emerald-600",**

&#x20;         **ring: "focus:border-emerald-500 focus:ring-emerald-500/20"**

&#x20;       **}**

&#x20;     **};**



&#x20;     **return colors\[color] || colors.emerald;**

&#x20;   **}**



&#x20;   **function renderHeader() {**

&#x20;     **const profile = currentProfile();**



&#x20;     **document.getElementById("profileSubtitle").textContent =**

&#x20;       **`${profile.name} · ${profile.examLabel}`;**



&#x20;     **const finalBtn = document.getElementById("finalBtn");**

&#x20;     **const interBtn = document.getElementById("interBtn");**



&#x20;     **const activeClasses =**

&#x20;       **"bg-white text-slate-900 shadow-sm ring-1 ring-slate-200";**



&#x20;     **const inactiveClasses =**

&#x20;       **"text-slate-500 hover:text-slate-800";**



&#x20;     **finalBtn.className =**

&#x20;       **"profile-btn rounded-xl px-4 py-2.5 text-sm font-bold transition " +**

&#x20;       **(appData.activeProfile === "final"**

&#x20;         **? activeClasses**

&#x20;         **: inactiveClasses);**



&#x20;     **interBtn.className =**

&#x20;       **"profile-btn rounded-xl px-4 py-2.5 text-sm font-bold transition " +**

&#x20;       **(appData.activeProfile === "inter"**

&#x20;         **? activeClasses**

&#x20;         **: inactiveClasses);**

&#x20;   **}**



&#x20;   **function renderSummary() {**

&#x20;     **const profile = currentProfile();**

&#x20;     **const stats = getOverallStats();**



&#x20;     **const examDays = calculateDaysRemaining(profile.examDate);**

&#x20;     **const classDays = stats.daysLeft;**



&#x20;     **document.getElementById("examCountdown").textContent =**

&#x20;       **examDays === 0 ? "TODAY" : examDays;**



&#x20;     **document.getElementById("examDateLabel").textContent =**

&#x20;       **formatDate(profile.examDate);**



&#x20;     **document.getElementById("classCountdown").textContent =**

&#x20;       **classDays === 0 ? "TODAY" : classDays;**



&#x20;     **document.getElementById("totalLectures").textContent =**

&#x20;       **stats.total;**



&#x20;     **document.getElementById("completedLectures").textContent =**

&#x20;       **`${stats.completed} completed · ${stats.remaining} remaining`;**



&#x20;     **document.getElementById("overallPace").textContent =**

&#x20;       **stats.pace.toFixed(1);**



&#x20;     **document.getElementById("overallPercent").textContent =**

&#x20;       **`${stats.percentage.toFixed(0)}%`;**



&#x20;     **document.getElementById("overallProgressBar").style.width =**

&#x20;       **`${stats.percentage}%`;**



&#x20;     **document.getElementById("examDateInput").value =**

&#x20;       **profile.examDate;**

&#x20;   **}**



&#x20;   **function renderSubjects() {**

&#x20;     **const grid = document.getElementById("subjectsGrid");**



&#x20;     **grid.innerHTML = currentProfile().subjects**

&#x20;       **.map((subject, index) => {**

&#x20;         **const stats = getSubjectStats(subject);**

&#x20;         **const colors = colorClasses(subject.color);**



&#x20;         **return `**

&#x20;           **<article class="glass rounded-3xl border border-slate-200 p-5 shadow-sm">**



&#x20;             **<div class="flex items-start justify-between gap-3">**



&#x20;               **<div class="flex min-w-0 items-center gap-3">**

&#x20;                 **<div class="flex h-11 w-11 shrink-0 items-center justify-center rounded-2xl ${colors.icon} font-black">**

&#x20;                   **${escapeHtml(subject.short)}**

&#x20;                 **</div>**



&#x20;                 **<div class="min-w-0">**

&#x20;                   **<h3 class="truncate font-bold text-slate-900">**

&#x20;                     **${escapeHtml(subject.name)}**

&#x20;                   **</h3>**

&#x20;                   **<p class="text-xs text-slate-500">**

&#x20;                     **Subject ${index + 1} of 6**

&#x20;                   **</p>**

&#x20;                 **</div>**

&#x20;               **</div>**



&#x20;               **<span class="shrink-0 rounded-xl px-2.5 py-1 text-xs font-black ${colors.badge}">**

&#x20;                 **${stats.percentage.toFixed(0)}%**

&#x20;               **</span>**



&#x20;             **</div>**



&#x20;             **<div class="mt-5">**



&#x20;               **<div class="mb-2 flex justify-between text-xs font-semibold">**

&#x20;                 **<span class="text-slate-500">**

&#x20;                   **${stats.completed} / ${stats.total} lectures**

&#x20;                 **</span>**

&#x20;                 **<span class="text-slate-400">**

&#x20;                   **${stats.remaining} left**

&#x20;                 **</span>**

&#x20;               **</div>**



&#x20;               **<div class="h-2.5 overflow-hidden rounded-full bg-slate-100">**

&#x20;                 **<div**

&#x20;                   **class="progress-bar h-full rounded-full ${colors.bar}"**

&#x20;                   **style="width:${stats.percentage}%"**

&#x20;                 **></div>**

&#x20;               **</div>**



&#x20;             **</div>**



&#x20;             **<div class="mt-5 grid grid-cols-2 gap-3">**



&#x20;               **<label>**

&#x20;                 **<span class="mb-1.5 block text-\[11px] font-bold uppercase tracking-wide text-slate-400">**

&#x20;                   **Total**

&#x20;                 **</span>**

&#x20;                 **<input**

&#x20;                   **type="number"**

&#x20;                   **min="0"**

&#x20;                   **value="${stats.total}"**

&#x20;                   **onchange="updateSubject(${index}, 'total', this.value)"**

&#x20;                   **class="w-full rounded-xl border border-slate-200 bg-white px-3 py-2.5 text-sm font-bold outline-none transition ${colors.ring} focus:ring-2"**

&#x20;                 **/>**

&#x20;               **</label>**



&#x20;               **<label>**

&#x20;                 **<span class="mb-1.5 block text-\[11px] font-bold uppercase tracking-wide text-slate-400">**

&#x20;                   **Completed**

&#x20;                 **</span>**

&#x20;                 **<input**

&#x20;                   **type="number"**

&#x20;                   **min="0"**

&#x20;                   **max="${stats.total}"**

&#x20;                   **value="${stats.completed}"**

&#x20;                   **onchange="updateSubject(${index}, 'completed', this.value)"**

&#x20;                   **class="w-full rounded-xl border border-slate-200 bg-white px-3 py-2.5 text-sm font-bold outline-none transition ${colors.ring} focus:ring-2"**

&#x20;                 **/>**

&#x20;               **</label>**



&#x20;             **</div>**



&#x20;             **<div class="mt-4 grid grid-cols-2 gap-3">**



&#x20;               **<div class="rounded-2xl bg-slate-50 p-3">**

&#x20;                 **<div class="text-\[11px] font-bold uppercase tracking-wide text-slate-400">**

&#x20;                   **Days left**

&#x20;                 **</div>**

&#x20;                 **<div class="mt-1 text-lg font-black text-slate-900">**

&#x20;                   **${stats.daysLeft}**

&#x20;                 **</div>**

&#x20;               **</div>**



&#x20;               **<div class="rounded-2xl bg-ca-50 p-3">**

&#x20;                 **<div class="text-\[11px] font-bold uppercase tracking-wide text-ca-600">**

&#x20;                   **Daily pace**

&#x20;                 **</div>**

&#x20;                 **<div class="mt-1 text-lg font-black text-ca-700">**

&#x20;                   **${stats.pace.toFixed(1)}**

&#x20;                 **</div>**

&#x20;               **</div>**



&#x20;             **</div>**



&#x20;           **</article>**

&#x20;         **`;**

&#x20;       **})**

&#x20;       **.join("");**

&#x20;   **}**



&#x20;   **function renderDailyPlan() {**

&#x20;     **const container = document.getElementById("dailyPlan");**



&#x20;     **container.innerHTML = currentProfile().subjects**

&#x20;       **.map((subject, index) => {**

&#x20;         **const stats = getSubjectStats(subject);**

&#x20;         **const colors = colorClasses(subject.color);**



&#x20;         **let status = "";**



&#x20;         **if (stats.remaining === 0) {**

&#x20;           **status = `**

&#x20;             **<span class="rounded-lg bg-emerald-50 px-2 py-1 text-xs font-bold text-emerald-600">**

&#x20;               **Complete 🎉**

&#x20;             **</span>**

&#x20;           **`;**

&#x20;         **} else if (stats.daysLeft === 0) {**

&#x20;           **status = `**

&#x20;             **<span class="rounded-lg bg-red-50 px-2 py-1 text-xs font-bold text-red-600">**

&#x20;               **Deadline**

&#x20;             **</span>**

&#x20;           **`;**

&#x20;         **} else {**

&#x20;           **status = `**

&#x20;             **<span class="rounded-lg bg-slate-100 px-2 py-1 text-xs font-bold text-slate-500">**

&#x20;               **${stats.remaining} left**

&#x20;             **</span>**

&#x20;           **`;**

&#x20;         **}**



&#x20;         **return `**

&#x20;           **<div class="flex items-center gap-3 rounded-2xl border border-slate-100 bg-white p-3">**



&#x20;             **<div class="flex h-9 w-9 shrink-0 items-center justify-center rounded-xl ${colors.icon} text-xs font-black">**

&#x20;               **${escapeHtml(subject.short)}**

&#x20;             **</div>**



&#x20;             **<div class="min-w-0 flex-1">**

&#x20;               **<div class="flex items-center justify-between gap-2">**

&#x20;                 **<p class="truncate text-sm font-bold text-slate-800">**

&#x20;                   **${escapeHtml(subject.name)}**

&#x20;                 **</p>**

&#x20;                 **${status}**

&#x20;               **</div>**



&#x20;               **<div class="mt-1 flex items-center gap-2">**

&#x20;                 **<div class="h-1.5 flex-1 overflow-hidden rounded-full bg-slate-100">**

&#x20;                   **<div**

&#x20;                     **class="h-full rounded-full ${colors.bar}"**

&#x20;                     **style="width:${stats.percentage}%"**

&#x20;                   **></div>**

&#x20;                 **</div>**



&#x20;                 **<span class="w-14 text-right text-xs font-black text-slate-600">**

&#x20;                   **${stats.pace.toFixed(1)}/day**

&#x20;                 **</span>**

&#x20;               **</div>**

&#x20;             **</div>**



&#x20;           **</div>**

&#x20;         **`;**

&#x20;       **})**

&#x20;       **.join("");**

&#x20;   **}**



&#x20;   **function escapeHtml(value) {**

&#x20;     **return String(value)**

&#x20;       **.replaceAll("\&", "\&amp;")**

&#x20;       **.replaceAll("<", "\&lt;")**

&#x20;       **.replaceAll(">", "\&gt;")**

&#x20;       **.replaceAll('"', "\&quot;")**

&#x20;       **.replaceAll("'", "\&#039;");**

&#x20;   **}**



&#x20;   **function render() {**

&#x20;     **renderHeader();**

&#x20;     **renderSummary();**

&#x20;     **renderSubjects();**

&#x20;     **renderDailyPlan();**

&#x20;   **}**



&#x20;   **// Initial render**

&#x20;   **render();**



&#x20;   **// Keep countdowns accurate if the browser remains open around midnight.**

&#x20;   **setInterval(render, 60 \* 1000);**

