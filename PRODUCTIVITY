<!doctype html>
<html lang="en" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Productivity Tools Quiz</title>
  <script src="https://cdn.tailwindcss.com/3.4.17"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&amp;family=JetBrains+Mono:wght@400;500&amp;display=swap" rel="stylesheet">
  <style>
    * { font-family: 'Space Grotesk', sans-serif; }
    .mono { font-family: 'JetBrains Mono', monospace; }
    
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    
    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.02); }
    }
    
    @keyframes slideIn {
      from { opacity: 0; transform: translateX(-20px); }
      to { opacity: 1; transform: translateX(0); }
    }
    
    @keyframes confetti {
      0% { transform: translateY(0) rotate(0deg); opacity: 1; }
      100% { transform: translateY(-100px) rotate(720deg); opacity: 0; }
    }
    
    .animate-fade { animation: fadeIn 0.5s ease-out forwards; }
    .animate-slide { animation: slideIn 0.3s ease-out forwards; }
    .animate-pulse-soft { animation: pulse 2s ease-in-out infinite; }
    
    .option-btn {
      transition: all 0.2s ease;
    }
    
    .option-btn:hover:not(:disabled) {
      transform: translateX(8px);
      box-shadow: 0 4px 20px rgba(99, 102, 241, 0.3);
    }
    
    .progress-fill {
      transition: width 0.5s ease;
    }
    
    .gradient-border {
      background: linear-gradient(135deg, #6366f1, #8b5cf6, #a855f7);
      padding: 2px;
      border-radius: 16px;
    }
    
    .confetti-piece {
      position: absolute;
      width: 10px;
      height: 10px;
      animation: confetti 1s ease-out forwards;
    }
  </style>
  <style>body { box-sizing: border-box; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body class="h-full bg-gray-100 overflow-auto">
  <div id="app" class="w-full min-h-full bg-gray-100 p-4 md:p-8"><!-- Start Screen -->
   <div id="start-screen" class="max-w-2xl mx-auto text-center py-12 animate-fade">
    <div class="mb-8">
     <div class="inline-flex items-center justify-center w-24 h-24 rounded-2xl bg-gradient-to-br from-indigo-500 to-purple-600 mb-6 animate-pulse-soft">
      <svg class="w-12 h-12 text-white" fill="none" stroke="currentColor" viewbox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"></path>
      </svg>
     </div>
     <h1 id="quiz-title" class="text-4xl md:text-5xl font-bold text-gray-800 mb-4">Productivity Tools Quiz</h1>
     <p class="text-gray-600 text-lg max-w-md mx-auto">Test your knowledge of the most popular productivity tools and software!</p>
    </div>
    <div class="gradient-border inline-block mb-8 w-full max-w-md">
     <div class="bg-white rounded-xl px-8 py-6 space-y-4">
      <div>
       <label class="block text-sm text-gray-700 mb-2 text-left">Full Name</label> <input id="student-name" type="text" placeholder="Enter your name" class="w-full px-4 py-2 bg-white border border-gray-300 rounded-lg text-gray-800 placeholder-gray-400 focus:outline-none focus:border-indigo-500">
      </div>
      <div>
       <label class="block text-sm text-gray-700 mb-2 text-left">Grade</label> <input id="student-grade" type="text" placeholder="e.g., 10-A" class="w-full px-4 py-2 bg-white border border-gray-300 rounded-lg text-gray-800 placeholder-gray-400 focus:outline-none focus:border-indigo-500">
      </div>
      <div>
       <label class="block text-sm text-gray-700 mb-2 text-left">Section</label> <input id="student-section" type="text" placeholder="e.g., Section B" class="w-full px-4 py-2 bg-white border border-gray-300 rounded-lg text-gray-800 placeholder-gray-400 focus:outline-none focus:border-indigo-500">
      </div>
     </div>
    </div>
    <div class="gradient-border inline-block mb-8 hidden sm:inline-block">
     <div class="bg-white rounded-xl px-8 py-6">
      <div class="flex items-center justify-center gap-8 text-gray-700">
       <div class="text-center">
        <div class="text-3xl font-bold text-indigo-600 mono">
         20
        </div>
        <div class="text-sm">
         Questions
        </div>
       </div>
       <div class="w-px h-12 bg-gray-300"></div>
       <div class="text-center">
        <div class="text-3xl font-bold text-purple-600 mono">
         4
        </div>
        <div class="text-sm">
         Options Each
        </div>
       </div>
       <div class="w-px h-12 bg-gray-300"></div>
       <div class="text-center">
        <div class="text-3xl font-bold text-pink-600 mono">
         ∞
        </div>
        <div class="text-sm">
         No Time Limit
        </div>
       </div>
      </div>
     </div>
    </div><button id="start-btn" onclick="startQuiz()" class="px-12 py-4 bg-gradient-to-r from-indigo-500 to-purple-600 text-white text-xl font-semibold rounded-xl hover:from-indigo-600 hover:to-purple-700 transition-all hover:scale-105 hover:shadow-xl hover:shadow-indigo-500/30"> Start Quiz </button>
   </div><!-- Quiz Screen -->
   <div id="quiz-screen" class="hidden max-w-3xl mx-auto py-8"><!-- Progress Bar -->
    <div class="mb-8">
     <div class="flex justify-between items-center mb-2"><span class="text-gray-600 text-sm mono">Question <span id="current-q" class="text-indigo-600">1</span>/20</span> <span id="score-display" class="text-gray-600 text-sm mono">Score: <span class="text-emerald-600">0</span></span>
     </div>
     <div class="h-2 bg-gray-300 rounded-full overflow-hidden">
      <div id="progress-bar" class="progress-fill h-full bg-gradient-to-r from-indigo-500 to-purple-500 rounded-full" style="width: 5%"></div>
     </div>
    </div><!-- Question Card -->
    <div class="gradient-border mb-6">
     <div class="bg-slate-800 rounded-xl p-6 md:p-8">
      <div class="flex items-start gap-4 mb-6">
       <div id="q-number" class="flex-shrink-0 w-10 h-10 rounded-lg bg-indigo-500/20 flex items-center justify-center text-indigo-400 font-bold mono">
        1
       </div>
       <h2 id="question-text" class="text-xl md:text-2xl font-semibold text-white leading-relaxed">Loading question...</h2>
      </div>
     </div>
    </div><!-- Options -->
    <div id="options-container" class="space-y-3"><!-- Options will be inserted here -->
    </div><!-- Feedback -->
    <div id="feedback" class="hidden mt-6 p-4 rounded-xl text-center">
     <p id="feedback-text" class="font-semibold text-lg"></p>
     <p id="feedback-explanation" class="text-sm mt-2 opacity-80"></p>
    </div><!-- Next Button --> <button id="next-btn" onclick="nextQuestion()" class="hidden mt-6 w-full py-4 bg-gradient-to-r from-indigo-500 to-purple-600 text-white text-lg font-semibold rounded-xl hover:from-indigo-600 hover:to-purple-700 transition-all"> Next Question → </button>
   </div><!-- Results Screen -->
   <div id="results-screen" class="hidden max-w-2xl mx-auto text-center py-12 animate-fade">
    <div id="confetti-container" class="fixed inset-0 pointer-events-none overflow-hidden"></div>
    <div class="mb-8">
     <div id="result-icon" class="inline-flex items-center justify-center w-28 h-28 rounded-full mb-6"></div>
     <h2 id="result-title" class="text-4xl md:text-5xl font-bold text-gray-800 mb-4">Quiz Complete!</h2>
     <p id="result-subtitle" class="text-gray-600 text-xl"></p>
    </div>
    <div class="gradient-border inline-block mb-8">
     <div class="bg-white rounded-xl px-12 py-8">
      <div class="text-6xl font-bold mb-2"><span id="final-score" class="bg-gradient-to-r from-indigo-600 to-purple-600 bg-clip-text text-transparent mono">0</span> <span class="text-gray-400 text-3xl">/20</span>
      </div>
      <div id="percentage" class="text-2xl text-gray-700 mono">
       0%
      </div>
     </div>
    </div>
    <div class="flex flex-col sm:flex-row gap-4 justify-center"><button onclick="restartQuiz()" class="px-8 py-4 bg-gradient-to-r from-indigo-500 to-purple-600 text-white text-lg font-semibold rounded-xl hover:from-indigo-600 hover:to-purple-700 transition-all hover:scale-105"> 🔄 Try Again </button> <button onclick="reviewAnswers()" class="px-8 py-4 bg-slate-700 text-white text-lg font-semibold rounded-xl hover:bg-slate-600 transition-all"> 📋 Review Answers </button>
    </div>
   </div><!-- Review Screen -->
   <div id="review-screen" class="hidden max-w-3xl mx-auto py-8 animate-fade">
    <div class="flex items-center justify-between mb-8">
     <h2 class="text-3xl font-bold text-white">Answer Review</h2><button onclick="restartQuiz()" class="px-6 py-2 bg-indigo-500 text-white rounded-lg hover:bg-indigo-600 transition-all"> Try Again </button>
    </div>
    <div id="review-container" class="space-y-4"><!-- Review items will be inserted here -->
    </div><button onclick="restartQuiz()" class="mt-8 w-full py-4 bg-gradient-to-r from-indigo-500 to-purple-600 text-white text-lg font-semibold rounded-xl hover:from-indigo-600 hover:to-purple-700 transition-all"> 🔄 Take Quiz Again </button>
   </div>
  </div>
  <script>
    const defaultConfig = {
      quiz_title: "Productivity Tools Quiz",
      start_button_text: "Start Quiz"
    };

    let currentStudent = { name: "", grade: "", section: "" };

    const questions = [
      {
        q: "Which tool is known for its Kanban-style boards with cards and lists?",
        options: ["Asana", "Trello", "Monday.com", "Basecamp"],
        answer: 1,
        explanation: "Trello is famous for its visual Kanban boards where you organize tasks into cards within lists."
      },
      {
        q: "Notion is best described as what type of tool?",
        options: ["Email client", "All-in-one workspace", "Video conferencing", "Password manager"],
        answer: 1,
        explanation: "Notion combines notes, databases, wikis, and project management in one all-in-one workspace."
      },
      {
        q: "Which keyboard shortcut typically opens Spotlight search on Mac?",
        options: ["Cmd + F", "Cmd + Space", "Cmd + S", "Cmd + Tab"],
        answer: 1,
        explanation: "Cmd + Space opens Spotlight, letting you quickly search and launch apps or files."
      },
      {
        q: "What productivity technique involves working in 25-minute focused intervals?",
        options: ["Time blocking", "Pomodoro Technique", "GTD Method", "Eisenhower Matrix"],
        answer: 1,
        explanation: "The Pomodoro Technique uses 25-minute work sessions followed by short breaks."
      },
      {
        q: "Slack is primarily used for:",
        options: ["Video editing", "Team communication", "Spreadsheet analysis", "Photo storage"],
        answer: 1,
        explanation: "Slack is a team messaging platform designed for workplace communication and collaboration."
      },
      {
        q: "Which tool uses the 'Getting Things Done' (GTD) methodology?",
        options: ["OmniFocus", "Microsoft Word", "Photoshop", "Spotify"],
        answer: 0,
        explanation: "OmniFocus is built around David Allen's GTD methodology for task management."
      },
      {
        q: "What does the 'CC' field mean in email?",
        options: ["Confidential Copy", "Carbon Copy", "Create Copy", "Central Command"],
        answer: 1,
        explanation: "CC stands for Carbon Copy, allowing you to send copies to additional recipients."
      },
      {
        q: "Which cloud storage service is developed by Microsoft?",
        options: ["Google Drive", "Dropbox", "OneDrive", "iCloud"],
        answer: 2,
        explanation: "OneDrive is Microsoft's cloud storage solution, integrated with Windows and Office."
      },
      {
        q: "Todoist is known for being a:",
        options: ["Calendar app", "Task management app", "Email client", "Browser extension"],
        answer: 1,
        explanation: "Todoist is a popular task management app for organizing personal and work tasks."
      },
      {
        q: "What feature allows you to automate workflows between apps?",
        options: ["Copy-paste", "Zapier/Integrations", "Screenshots", "Bookmarks"],
        answer: 1,
        explanation: "Zapier and similar tools create automated workflows connecting different apps."
      },
      {
        q: "Which shortcut typically undoes the last action in most apps?",
        options: ["Ctrl + Z", "Ctrl + X", "Ctrl + C", "Ctrl + V"],
        answer: 0,
        explanation: "Ctrl + Z (or Cmd + Z on Mac) is the universal undo shortcut."
      },
      {
        q: "Calendly is used for:",
        options: ["Note-taking", "Scheduling meetings", "File sharing", "Coding"],
        answer: 1,
        explanation: "Calendly automates meeting scheduling by letting others book time on your calendar."
      },
      {
        q: "What does 'BCC' hide in emails?",
        options: ["The subject line", "The attachment", "Other recipients", "The sender"],
        answer: 2,
        explanation: "BCC (Blind Carbon Copy) hides recipients from each other in the email."
      },
      {
        q: "Which tool is NOT a video conferencing platform?",
        options: ["Zoom", "Microsoft Teams", "Evernote", "Google Meet"],
        answer: 2,
        explanation: "Evernote is a note-taking app, not a video conferencing platform."
      },
      {
        q: "What is the purpose of a password manager like 1Password?",
        options: ["Block ads", "Store passwords securely", "Edit photos", "Send emails"],
        answer: 1,
        explanation: "Password managers securely store and auto-fill your login credentials."
      },
      {
        q: "Which Microsoft Office app is used for presentations?",
        options: ["Word", "Excel", "PowerPoint", "Outlook"],
        answer: 2,
        explanation: "PowerPoint is Microsoft's presentation software for creating slideshows."
      },
      {
        q: "What does the Eisenhower Matrix help you with?",
        options: ["Color coding", "Prioritizing tasks", "Sending emails", "Scheduling meetings"],
        answer: 1,
        explanation: "The Eisenhower Matrix categorizes tasks by urgency and importance for prioritization."
      },
      {
        q: "Which app is known for mind mapping and brainstorming?",
        options: ["Miro", "Gmail", "Slack", "Dropbox"],
        answer: 0,
        explanation: "Miro is a collaborative whiteboard platform great for mind mapping and brainstorming."
      },
      {
        q: "What does 'SaaS' stand for in productivity tools?",
        options: ["Simple as a Service", "Software as a Service", "System as a Standard", "Storage as a Solution"],
        answer: 1,
        explanation: "SaaS (Software as a Service) refers to cloud-based software you access via subscription."
      },
      {
        q: "Which tool is best for creating quick screen recordings?",
        options: ["Microsoft Word", "Loom", "Trello", "Asana"],
        answer: 1,
        explanation: "Loom makes it easy to record your screen and camera for quick video messages."
      }
    ];

    let currentQuestion = 0;
    let score = 0;
    let userAnswers = [];
    let answered = false;

    // Initialize Element SDK
    if (window.elementSdk) {
      window.elementSdk.init({
        defaultConfig,
        onConfigChange: async (config) => {
          document.getElementById('quiz-title').textContent = config.quiz_title || defaultConfig.quiz_title;
          document.getElementById('start-btn').textContent = config.start_button_text || defaultConfig.start_button_text;
        },
        mapToCapabilities: (config) => ({
          recolorables: [],
          borderables: [],
          fontEditable: undefined,
          fontSizeable: undefined
        }),
        mapToEditPanelValues: (config) => new Map([
          ["quiz_title", config.quiz_title || defaultConfig.quiz_title],
          ["start_button_text", config.start_button_text || defaultConfig.start_button_text]
        ])
      });
    }

    // Initialize Data SDK
    if (window.dataSdk) {
      window.dataSdk.init({
        onDataChanged: (data) => {
          // Data loaded from sheet, quiz can proceed
        }
      });
    }

    function startQuiz() {
      const name = document.getElementById('student-name').value.trim();
      const grade = document.getElementById('student-grade').value.trim();
      const section = document.getElementById('student-section').value.trim();

      if (!name || !grade || !section) {
        alert('Please fill in all fields (Name, Grade, Section)');
        return;
      }

      currentStudent = { name, grade, section };

      document.getElementById('start-screen').classList.add('hidden');
      document.getElementById('quiz-screen').classList.remove('hidden');
      currentQuestion = 0;
      score = 0;
      userAnswers = [];
      showQuestion();
    }

    function showQuestion() {
      answered = false;
      const q = questions[currentQuestion];
      
      document.getElementById('current-q').textContent = currentQuestion + 1;
      document.getElementById('q-number').textContent = currentQuestion + 1;
      document.getElementById('question-text').textContent = q.q;
      document.getElementById('score-display').innerHTML = `Score: <span class="text-emerald-400">${score}</span>`;
      document.getElementById('progress-bar').style.width = `${((currentQuestion + 1) / questions.length) * 100}%`;
      
      const optionsHtml = q.options.map((opt, i) => `
        <button onclick="selectAnswer(${i})" class="option-btn w-full p-4 bg-white border-2 border-gray-300 rounded-xl text-left text-gray-800 hover:border-indigo-500 hover:bg-gray-50 flex items-center gap-4 animate-slide" style="animation-delay: ${i * 0.1}s">
          <span class="flex-shrink-0 w-8 h-8 rounded-lg bg-gray-200 flex items-center justify-center text-gray-600 font-semibold mono">${String.fromCharCode(65 + i)}</span>
          <span class="text-lg">${opt}</span>
        </button>
      `).join('');
      
      document.getElementById('options-container').innerHTML = optionsHtml;
      document.getElementById('feedback').classList.add('hidden');
      document.getElementById('next-btn').classList.add('hidden');
    }

    function selectAnswer(index) {
      if (answered) return;
      answered = true;
      
      const q = questions[currentQuestion];
      const isCorrect = index === q.answer;
      
      userAnswers.push({ questionIndex: currentQuestion, selected: index, correct: isCorrect });
      
      if (isCorrect) score++;
      
      const buttons = document.querySelectorAll('.option-btn');
      buttons.forEach((btn, i) => {
        btn.disabled = true;
        if (i === q.answer) {
          btn.classList.remove('border-gray-300', 'bg-white');
          btn.classList.add('border-emerald-500', 'bg-emerald-50');
          btn.querySelector('span:first-child').classList.remove('bg-gray-200', 'text-gray-600');
          btn.querySelector('span:first-child').classList.add('bg-emerald-200', 'text-emerald-700');
        } else if (i === index && !isCorrect) {
          btn.classList.remove('border-gray-300', 'bg-white');
          btn.classList.add('border-red-500', 'bg-red-50');
          btn.querySelector('span:first-child').classList.remove('bg-gray-200', 'text-gray-600');
          btn.querySelector('span:first-child').classList.add('bg-red-200', 'text-red-700');
        }
      });
      
      const feedback = document.getElementById('feedback');
      const feedbackText = document.getElementById('feedback-text');
      const feedbackExplanation = document.getElementById('feedback-explanation');
      
      feedback.classList.remove('hidden', 'bg-emerald-500/20', 'bg-red-500/20');
      
      if (isCorrect) {
        feedback.classList.add('bg-emerald-100');
        feedbackText.textContent = "✅ Correct!";
        feedbackText.className = "font-semibold text-lg text-emerald-700";
      } else {
        feedback.classList.add('bg-red-100');
        feedbackText.textContent = "❌ Incorrect";
        feedbackText.className = "font-semibold text-lg text-red-700";
      }
      
      feedbackExplanation.textContent = q.explanation;
      feedbackExplanation.className = "text-sm mt-2 text-gray-700";
      
      document.getElementById('score-display').innerHTML = `Score: <span class="text-emerald-400">${score}</span>`;
      
      const nextBtn = document.getElementById('next-btn');
      nextBtn.classList.remove('hidden');
      nextBtn.textContent = currentQuestion < questions.length - 1 ? "Next Question →" : "See Results →";
    }

    function nextQuestion() {
      currentQuestion++;
      if (currentQuestion < questions.length) {
        showQuestion();
      } else {
        showResults();
      }
    }

    function showResults() {
      document.getElementById('quiz-screen').classList.add('hidden');
      document.getElementById('results-screen').classList.remove('hidden');
      document.getElementById('results-screen').classList.add('animate-fade');
      
      const percentage = Math.round((score / questions.length) * 100);
      document.getElementById('final-score').textContent = score;
      document.getElementById('percentage').textContent = `${percentage}%`;
      
      const resultIcon = document.getElementById('result-icon');
      const resultTitle = document.getElementById('result-title');
      const resultSubtitle = document.getElementById('result-subtitle');
      
      if (percentage >= 90) {
        resultIcon.innerHTML = '<span class="text-5xl">🏆</span>';
        resultIcon.className = "inline-flex items-center justify-center w-28 h-28 rounded-full mb-6 bg-gradient-to-br from-yellow-400 to-orange-500";
        resultTitle.textContent = "Outstanding!";
        resultSubtitle.textContent = "You're a productivity tools expert!";
        createConfetti();
      } else if (percentage >= 70) {
        resultIcon.innerHTML = '<span class="text-5xl">⭐</span>';
        resultIcon.className = "inline-flex items-center justify-center w-28 h-28 rounded-full mb-6 bg-gradient-to-br from-indigo-500 to-purple-600";
        resultTitle.textContent = "Great Job!";
        resultSubtitle.textContent = "You know your productivity tools well!";
      } else if (percentage >= 50) {
        resultIcon.innerHTML = '<span class="text-5xl">👍</span>';
        resultIcon.className = "inline-flex items-center justify-center w-28 h-28 rounded-full mb-6 bg-gradient-to-br from-blue-500 to-cyan-500";
        resultTitle.textContent = "Good Effort!";
        resultSubtitle.textContent = "Keep exploring productivity tools!";
      } else {
        resultIcon.innerHTML = '<span class="text-5xl">📚</span>';
        resultIcon.className = "inline-flex items-center justify-center w-28 h-28 rounded-full mb-6 bg-gradient-to-br from-slate-500 to-slate-600";
        resultTitle.textContent = "Keep Learning!";
        resultSubtitle.textContent = "There's so much to discover about productivity tools!";
      }

      // Save results to Data SDK
      saveQuizResults();
    }

    async function saveQuizResults() {
      if (!window.dataSdk) return;

      const percentage = Math.round((score / questions.length) * 100);
      const quizData = {
        name: currentStudent.name,
        grade: currentStudent.grade,
        section: currentStudent.section,
        score: score,
        total: questions.length,
        percentage: percentage,
        completedAt: new Date().toISOString()
      };

      const result = await window.dataSdk.create(quizData);
      if (!result.isOk) {
        console.error('Failed to save quiz results:', result.error);
      }
    }

    function createConfetti() {
      const container = document.getElementById('confetti-container');
      const colors = ['#6366f1', '#8b5cf6', '#a855f7', '#f59e0b', '#10b981', '#ec4899'];
      
      for (let i = 0; i < 50; i++) {
        const confetti = document.createElement('div');
        confetti.className = 'confetti-piece';
        confetti.style.left = Math.random() * 100 + '%';
        confetti.style.top = '100%';
        confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
        confetti.style.animationDelay = Math.random() * 0.5 + 's';
        confetti.style.borderRadius = Math.random() > 0.5 ? '50%' : '0';
        container.appendChild(confetti);
        
        setTimeout(() => confetti.remove(), 1500);
      }
    }

    function reviewAnswers() {
      document.getElementById('results-screen').classList.add('hidden');
      document.getElementById('review-screen').classList.remove('hidden');
      
      const reviewHtml = questions.map((q, i) => {
        const userAnswer = userAnswers.find(a => a.questionIndex === i);
        const isCorrect = userAnswer?.correct;
        const selectedIndex = userAnswer?.selected;
        
        return `
          <div class="bg-white rounded-xl p-5 border-l-4 ${isCorrect ? 'border-emerald-500' : 'border-red-500'}">
            <div class="flex items-start gap-3 mb-3">
              <span class="flex-shrink-0 w-8 h-8 rounded-lg ${isCorrect ? 'bg-emerald-100 text-emerald-700' : 'bg-red-100 text-red-700'} flex items-center justify-center font-bold mono text-sm">${i + 1}</span>
              <p class="text-gray-800 font-medium">${q.q}</p>
            </div>
            <div class="ml-11 space-y-1 text-sm">
              <p class="text-gray-700">Your answer: <span class="${isCorrect ? 'text-emerald-700' : 'text-red-700'}">${selectedIndex !== undefined ? q.options[selectedIndex] : 'Not answered'}</span></p>
              ${!isCorrect ? `<p class="text-gray-700">Correct answer: <span class="text-emerald-700">${q.options[q.answer]}</span></p>` : ''}
              <p class="text-gray-600 italic mt-2">${q.explanation}</p>
            </div>
          </div>
        `;
      }).join('');
      
      document.getElementById('review-container').innerHTML = reviewHtml;
    }

    function restartQuiz() {
      document.getElementById('results-screen').classList.add('hidden');
      document.getElementById('review-screen').classList.add('hidden');
      document.getElementById('start-screen').classList.remove('hidden');
      document.getElementById('confetti-container').innerHTML = '';
    }
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9d3bbadc366a9d21',t:'MTc3MjA2OTk3OS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
