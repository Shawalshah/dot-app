<script setup lang="ts">
import { ref } from 'vue'

const billingCycle = ref<'monthly' | 'yearly'>('monthly')


const plans = [
  { name: 'Starter', monthlyPrice: 0, yearlyPrice: 0, description: 'Perfect for exploring', features: ['5 AI Courses', 'Basic Learning Tracks', 'Community Support', 'Progress Tracking'], highlighted: false },
  { name: 'Pro', monthlyPrice: 29, yearlyPrice: 290, description: 'For serious learners', features: ['Unlimited Courses', 'DOT Mentor Voice Bot', 'All Learning Tracks', 'Priority Support', 'Certificates'], highlighted: true },
  { name: 'Enterprise', monthlyPrice: 99, yearlyPrice: 990, description: 'For teams & institutions', features: ['Everything in Pro', 'Editor Role Access', 'Create Custom Courses', 'Team Analytics', 'API Access'], highlighted: false }
]

const stats = [
  { value: '50K+', label: 'Active Learners' },
  { value: '500+', label: 'AI Courses' },
  { value: '98%', label: 'Success Rate' },
  { value: '4.9', label: 'User Rating' }
]
</script>

<template>
  <div class="min-h-screen bg-white text-gray-900">
    
    <!-- Gradient Background with Texture -->
    <div class="fixed inset-0 z-0 bg-linear-to-br from-white via-fuchsia-50/30 to-violet-50/40">
      <!-- Soft gradient blobs -->
      <div class="absolute top-0 right-0 w-[600px] h-[600px] bg-linear-to-br from-fuchsia-200/40 to-violet-200/30 rounded-full blur-[120px] -translate-y-1/3 translate-x-1/4"></div>
      <div class="absolute top-1/2 left-0 w-[500px] h-[500px] bg-linear-to-tr from-violet-200/30 to-fuchsia-100/20 rounded-full blur-[100px] -translate-x-1/3"></div>
      <div class="absolute bottom-0 right-1/4 w-[400px] h-[400px] bg-fuchsia-100/30 rounded-full blur-[80px] translate-y-1/3"></div>
      <!-- Subtle grid pattern -->
      <div class="absolute inset-0 opacity-[0.015]" style="background-image: url('data:image/svg+xml,%3Csvg width=&quot;60&quot; height=&quot;60&quot; viewBox=&quot;0 0 60 60&quot; xmlns=&quot;http://www.w3.org/2000/svg&quot;%3E%3Cg fill=&quot;none&quot; fill-rule=&quot;evenodd&quot;%3E%3Cg fill=&quot;%239C92AC&quot; fill-opacity=&quot;0.4&quot;%3E%3Cpath d=&quot;M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z&quot;/%3E%3C/g%3E%3C/g%3E%3C/svg%3E');"></div>
    </div>
    
    <!-- Navbar -->
    <nav class="fixed top-0 left-0 right-0 z-50 bg-white/20 backdrop-blur-md border-b border-gray-100/50">
      <div class="max-w-6xl mx-auto px-6 h-16 flex items-center justify-between">
        <div class="flex items-center">
          <img src="./assets/images/logo 2.png" alt="DOT APP" class="h-8 sm:h-10 w-auto" />
        </div>
        <a href="#pricing" class="px-5 py-2 bg-linear-to-r from-fuchsia-500 to-violet-600 text-white text-sm font-medium rounded-lg hover:opacity-90 transition-opacity">
          Get Started
        </a>
      </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative pt-24 sm:pt-32 md:pt-40 pb-16 sm:pb-24 md:pb-32 px-4 sm:px-6">
      <div class="max-w-5xl mx-auto text-center">
        <div class="inline-flex items-center gap-2 px-4 py-1.5 bg-fuchsia-50 rounded-full mb-8">
          <span class="w-1.5 h-1.5 bg-fuchsia-500 rounded-full"></span>
          <span class="text-sm text-fuchsia-600 font-medium">AI-Powered Learning Platform</span>
        </div>
        
        <h1 class="text-3xl sm:text-4xl md:text-6xl lg:text-7xl font-semibold leading-[1.15] tracking-tight mb-4 sm:mb-6">
          <span class="block text-gray-900">
            Your Journey to Excellence
            <span class="bg-linear-to-r from-fuchsia-500 to-violet-600 bg-clip-text text-transparent"> Starts Here</span>
          </span>
        </h1>
        
        <p class="text-base sm:text-lg text-gray-500 max-w-2xl mx-auto mb-8 sm:mb-10 leading-relaxed px-2 sm:px-0">
          Expert-led courses, personalized AI mentorship,
          <span class="hidden sm:inline"> </span>
          <span class="block sm:inline">and a community of achievers—all in one platform.</span>
        </p>
        
        <div class="flex flex-col sm:flex-row items-center justify-center gap-3 mb-10 sm:mb-16">
          <a href="#pricing" class="w-full sm:w-auto px-6 py-3 bg-linear-to-r from-fuchsia-500 to-violet-600 text-white font-medium rounded-lg hover:opacity-90 transition-opacity flex items-center justify-center gap-2">
            Start Learning
            <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/></svg>
          </a>
          <a href="#features" class="w-full sm:w-auto px-6 py-3 bg-white border border-gray-200 text-gray-600 font-medium rounded-lg hover:border-fuchsia-200 hover:text-fuchsia-600 transition-colors flex items-center justify-center gap-2">
            <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.752 11.168l-3.197-2.132A1 1 0 0010 9.87v4.263a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z"/><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
            Watch Demo
          </a>
        </div>

        <!-- Stats -->
        <div class="grid grid-cols-2 md:grid-cols-4 gap-4 sm:gap-6 max-w-2xl mx-auto mb-10 sm:mb-16">
          <div v-for="stat in stats" :key="stat.label" class="text-center">
            <div class="text-xl sm:text-2xl md:text-3xl font-semibold text-gray-900">{{ stat.value }}</div>
            <div class="text-sm text-gray-400 mt-1">{{ stat.label }}</div>
          </div>
        </div>
      </div>

      <!-- Hero Dashboard Preview -->
      <div class="max-w-5xl mx-auto relative px-2 sm:px-0 hidden sm:block">
        <div class="relative bg-white border border-gray-200 rounded-2xl shadow-xl">
          <div class="flex items-center gap-2 px-4 py-3 border-b border-gray-100">
            <div class="flex gap-1.5">
              <div class="w-3 h-3 rounded-full bg-gray-200"></div>
              <div class="w-3 h-3 rounded-full bg-gray-200"></div>
              <div class="w-3 h-3 rounded-full bg-gray-200"></div>
            </div>
          </div>
          
          <div class="p-4 sm:p-6 md:p-8">
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4 sm:gap-5">
              <!-- Course Card -->
              <div class="bg-white border border-gray-100 rounded-xl p-5 hover:border-fuchsia-200 hover:shadow-md transition-all">
                <div class="flex items-center justify-between mb-4">
                  <div class="w-10 h-10 bg-linear-to-br from-fuchsia-500 to-violet-600 rounded-lg flex items-center justify-center">
                    <svg class="w-5 h-5 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"/></svg>
                  </div>
                  <span class="text-xs text-fuchsia-600 font-medium">In Progress</span>
                </div>
                <h3 class="text-gray-800 font-medium mb-1">Current Module</h3>
                <p class="text-gray-500 text-sm mb-3">React Fundamentals</p>
                <div class="h-1.5 bg-gray-100 rounded-full overflow-hidden">
                  <div class="h-full w-[67%] bg-linear-to-r from-fuchsia-500 to-violet-600 rounded-full"></div>
                </div>
              </div>
              
              <!-- AI Mentor Card -->
              <div class="bg-white border border-gray-100 rounded-xl p-5 hover:border-violet-200 hover:shadow-md transition-all">
                <div class="flex items-center justify-between mb-4">
                  <div class="w-10 h-10 bg-violet-600 rounded-lg flex items-center justify-center">
                    <svg class="w-5 h-5 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"/></svg>
                  </div>
                  <div class="flex items-center gap-1">
                    <span class="w-1.5 h-1.5 bg-violet-500 rounded-full"></span>
                    <span class="text-xs text-violet-600">Online</span>
                  </div>
                </div>
                <h3 class="text-gray-800 font-medium mb-1">DOT Mentor</h3>
                <p class="text-gray-500 text-sm mb-3">"How can I help you today?"</p>
                <div class="flex gap-2">
                  <button class="flex-1 py-2 bg-violet-600 rounded-lg text-white text-sm font-medium flex items-center justify-center gap-1.5 hover:bg-violet-700 transition-colors">
                    <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11a7 7 0 01-7 7m0 0a7 7 0 01-7-7m7 7v4m0 0H8m4 0h4m-4-8a3 3 0 01-3-3V5a3 3 0 116 0v6a3 3 0 01-3 3z"/></svg>
                    Voice
                  </button>
                  <button class="flex-1 py-2 bg-white border border-gray-200 rounded-lg text-gray-600 text-sm font-medium hover:border-violet-200 transition-colors">Chat</button>
                </div>
              </div>
              
              <!-- Progress Card -->
              <div class="bg-white border border-gray-100 rounded-xl p-5 hover:border-fuchsia-200 hover:shadow-md transition-all">
                <div class="flex items-center justify-between mb-4">
                  <div class="w-10 h-10 bg-fuchsia-500 rounded-lg flex items-center justify-center">
                    <svg class="w-5 h-5 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"/></svg>
                  </div>
                  <span class="text-xs text-fuchsia-600 font-medium">This Week</span>
                </div>
                <h3 class="text-gray-800 font-medium mb-1">Your Progress</h3>
                <div class="text-3xl font-semibold bg-linear-to-r from-fuchsia-500 to-violet-600 bg-clip-text text-transparent mb-1">78%</div>
                <p class="text-gray-500 text-sm">12 modules completed</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="relative py-16 sm:py-20 md:py-24 px-4 sm:px-6 bg-white">
      <div class="max-w-6xl mx-auto">
        
        <!-- Section Header -->
        <div class="text-center mb-10 sm:mb-16">
          <div class="inline-flex items-center gap-2 px-4 py-2 bg-linear-to-r from-fuchsia-50 to-violet-50 border border-fuchsia-200/50 rounded-full mb-6">
            <span class="w-2 h-2 bg-fuchsia-500 rounded-full"></span>
            <span class="text-sm text-fuchsia-700 font-medium">Built for students who want real progress</span>
          </div>
          <h2 class="text-2xl sm:text-3xl md:text-4xl font-bold text-gray-900 mb-4">Tools that make learning feel easy</h2>
          <p class="text-lg text-gray-500 max-w-2xl mx-auto">
            Notes, mentor, tracks, quizzes — everything organized in one place so you can focus on building skills.
          </p>
        </div>

        <!-- Features Grid - 2 rows of 3 -->
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 sm:gap-6">
          
          <!-- AI-Enhanced Notes -->
          <div class="group bg-gray-50 hover:bg-white border border-gray-100 hover:border-fuchsia-200 rounded-2xl p-6 sm:p-8 hover:shadow-xl transition-all duration-300">
            <div class="w-12 sm:w-14 h-12 sm:h-14 rounded-xl bg-fuchsia-100 flex items-center justify-center mb-4 sm:mb-6 group-hover:scale-110 transition-transform">
              <svg class="w-6 sm:w-7 h-6 sm:h-7 text-fuchsia-600" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"/></svg>
            </div>
            <h3 class="text-lg sm:text-xl font-bold text-gray-900 mb-2 sm:mb-3">AI-Enhanced Notes</h3>
            <p class="text-gray-500 leading-relaxed">Take notes, save to modules, and let AI summarize or expand your content instantly.</p>
          </div>

          <!-- Smart Questionnaire -->
          <div class="group bg-gray-50 hover:bg-white border border-gray-100 hover:border-violet-200 rounded-2xl p-8 hover:shadow-xl transition-all duration-300">
            <div class="w-14 h-14 rounded-xl bg-violet-100 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
              <svg class="w-7 h-7 text-violet-600" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"/></svg>
            </div>
            <h3 class="text-xl font-bold text-gray-900 mb-3">Smart Questionnaire</h3>
            <p class="text-gray-500 leading-relaxed">Answer personalized questions and get AI-powered course recommendations tailored to you.</p>
          </div>

          <!-- DOT Mentor -->
          <div class="group bg-gray-50 hover:bg-white border border-gray-100 hover:border-blue-200 rounded-2xl p-8 hover:shadow-xl transition-all duration-300">
            <div class="w-14 h-14 rounded-xl bg-blue-100 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
              <svg class="w-7 h-7 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11a7 7 0 01-7 7m0 0a7 7 0 01-7-7m7 7v4m0 0H8m4 0h4m-4-8a3 3 0 01-3-3V5a3 3 0 116 0v6a3 3 0 01-3 3z"/></svg>
            </div>
            <h3 class="text-xl font-bold text-gray-900 mb-3">DOT Mentor</h3>
            <p class="text-gray-500 leading-relaxed">Your AI companion for voice and chat support. Ask anything, anytime. Never feel stuck again.</p>
          </div>

          <!-- Module-Based Courses -->
          <div class="group bg-gray-50 hover:bg-white border border-gray-100 hover:border-fuchsia-200 rounded-2xl p-8 hover:shadow-xl transition-all duration-300">
            <div class="w-14 h-14 rounded-xl bg-fuchsia-100 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
              <svg class="w-7 h-7 text-fuchsia-600" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"/></svg>
            </div>
            <h3 class="text-xl font-bold text-gray-900 mb-3">Module-Based Courses</h3>
            <p class="text-gray-500 leading-relaxed">Learn through structured modules with both voice and text explanations. Your pace, your style.</p>
          </div>

          <!-- Learning Tracks -->
          <div class="group bg-gray-50 hover:bg-white border border-gray-100 hover:border-emerald-200 rounded-2xl p-8 hover:shadow-xl transition-all duration-300">
            <div class="w-14 h-14 rounded-xl bg-emerald-100 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
              <svg class="w-7 h-7 text-emerald-600" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 5a1 1 0 011-1h14a1 1 0 011 1v2a1 1 0 01-1 1H5a1 1 0 01-1-1V5zM4 13a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H5a1 1 0 01-1-1v-6zM16 13a1 1 0 011-1h2a1 1 0 011 1v6a1 1 0 01-1 1h-2a1 1 0 01-1-1v-6z"/></svg>
            </div>
            <h3 class="text-xl font-bold text-gray-900 mb-3">Learning Tracks</h3>
            <p class="text-gray-500 leading-relaxed">Follow tree-shaped paths. See Django → React and every step visualized clearly.</p>
          </div>

          <!-- Smart Quizzes -->
          <div class="group bg-gray-50 hover:bg-white border border-gray-100 hover:border-amber-200 rounded-2xl p-8 hover:shadow-xl transition-all duration-300">
            <div class="w-14 h-14 rounded-xl bg-amber-100 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
              <svg class="w-7 h-7 text-amber-600" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
            </div>
            <h3 class="text-xl font-bold text-gray-900 mb-3">Smart Quizzes</h3>
            <p class="text-gray-500 leading-relaxed">Test your knowledge with adaptive quizzes after each module. Track your growth in real-time.</p>
          </div>

        </div>
      </div>
    </section>

    <!-- Learning Tracks Section -->
    <section class="relative py-16 sm:py-20 md:py-24 px-4 sm:px-6">
      <div class="max-w-6xl mx-auto">
        <div class="grid lg:grid-cols-2 gap-8 sm:gap-12 lg:gap-16 items-center">
          <div>
            <p class="text-sm text-gray-500 uppercase tracking-wide mb-3">Learning Tracks</p>
            <h2 class="text-2xl sm:text-3xl md:text-4xl font-semibold text-gray-900 mb-4">
              Visualize your path to mastery
            </h2>
            <p class="text-gray-500 mb-8 leading-relaxed">
              Our tree-structured courses show you exactly what to learn and when. See how skills connect and build upon each other.
            </p>
            <div class="space-y-3">
              <div class="flex items-center gap-3">
                <svg class="w-5 h-5 text-fuchsia-500" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/></svg>
                <span class="text-gray-600">Clear skill progression</span>
              </div>
              <div class="flex items-center gap-3">
                <svg class="w-5 h-5 text-fuchsia-500" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/></svg>
                <span class="text-gray-600">Multiple paths to same goal</span>
              </div>
              <div class="flex items-center gap-3">
                <svg class="w-5 h-5 text-fuchsia-500" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/></svg>
                <span class="text-gray-600">Track your position</span>
              </div>
            </div>
          </div>

          <!-- Tree Visualization -->
          <div class="relative mt-8 lg:mt-0">
            <div class="bg-white border border-gray-200 rounded-2xl p-4 sm:p-6 md:p-8 shadow-sm overflow-x-auto">
              <div class="flex flex-col items-center">
                <div class="w-24 h-12 bg-linear-to-r from-fuchsia-500 to-violet-600 rounded-lg flex items-center justify-center text-white text-sm font-medium">
                  Full Stack
                </div>
                <div class="w-px h-8 bg-fuchsia-200"></div>
                <div class="w-48 h-px bg-gray-200"></div>
                <div class="flex gap-12 sm:gap-16 md:gap-24 -mt-px">
                  <div class="flex flex-col items-center">
                    <div class="w-px h-8 bg-gray-200"></div>
                    <div class="w-20 h-10 bg-fuchsia-500 rounded-lg flex items-center justify-center text-white text-xs font-medium">
                      Frontend
                    </div>
                    <div class="w-px h-6 bg-fuchsia-200"></div>
                    <div class="flex gap-2">
                      <div class="px-3 py-1.5 bg-fuchsia-50 border border-fuchsia-200 rounded text-fuchsia-600 text-xs font-medium">React</div>
                      <div class="px-3 py-1.5 bg-fuchsia-50 border border-fuchsia-200 rounded text-fuchsia-600 text-xs font-medium">Vue</div>
                    </div>
                  </div>
                  <div class="flex flex-col items-center">
                    <div class="w-px h-8 bg-gray-200"></div>
                    <div class="w-20 h-10 bg-violet-600 rounded-lg flex items-center justify-center text-white text-xs font-medium">
                      Backend
                    </div>
                    <div class="w-px h-6 bg-violet-200"></div>
                    <div class="flex gap-2">
                      <div class="px-3 py-1.5 bg-violet-50 border border-violet-200 rounded text-violet-600 text-xs font-medium">Django</div>
                      <div class="px-3 py-1.5 bg-violet-50 border border-violet-200 rounded text-violet-600 text-xs font-medium">Node</div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Roles Section -->
    <section id="roles" class="relative py-16 sm:py-20 md:py-24 px-4 sm:px-6 bg-white">
      <div class="max-w-6xl mx-auto">
        <!-- Header like Features section -->
        <div class="text-center mb-10 sm:mb-16">
          <div class="inline-flex items-center gap-2 px-4 py-2 bg-linear-to-r from-fuchsia-50 to-violet-50 border border-fuchsia-200/50 rounded-full mb-6">
            <span class="w-2 h-2 bg-fuchsia-500 rounded-full"></span>
            <span class="text-sm text-fuchsia-700 font-medium">Two paths, one platform</span>
          </div>
          <h2 class="text-2xl sm:text-3xl md:text-4xl font-bold text-gray-900 mb-4">Choose your role</h2>
          <p class="text-lg text-gray-500 max-w-2xl mx-auto">
            Whether you want to learn new skills or share your expertise — DOT has you covered.
          </p>
        </div>

        <!-- Simple Minimalistic Cards -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 sm:gap-8 max-w-4xl mx-auto">
          
          <!-- Learner Card -->
          <div class="group bg-gray-50 hover:bg-white border border-gray-100 hover:border-fuchsia-200 rounded-2xl p-8 hover:shadow-xl transition-all duration-300">
            <div class="w-14 h-14 rounded-xl bg-fuchsia-100 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
              <svg class="w-7 h-7 text-fuchsia-600" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M4.26 10.147a60.436 60.436 0 00-.491 6.347A48.627 48.627 0 0112 20.904a48.627 48.627 0 018.232-4.41 60.46 60.46 0 00-.491-6.347m-15.482 0a50.57 50.57 0 00-2.658-.813A59.905 59.905 0 0112 3.493a59.902 59.902 0 0110.399 5.84c-.896.248-1.783.52-2.658.814m-15.482 0A50.697 50.697 0 0112 13.489a50.702 50.702 0 017.74-3.342M6.75 15a.75.75 0 100-1.5.75.75 0 000 1.5zm0 0v-3.675A55.378 55.378 0 0112 8.443m-7.007 11.55A5.981 5.981 0 006.75 15.75v-1.5"/></svg>
            </div>
            <h3 class="text-xl font-bold text-gray-900 mb-3">Learner</h3>
            <p class="text-gray-500 leading-relaxed">Take personalized courses, interact with AI mentor, and track your progress toward mastery.</p>
          </div>

          <!-- Editor Card -->
          <div class="group bg-gray-50 hover:bg-white border border-gray-100 hover:border-violet-200 rounded-2xl p-8 hover:shadow-xl transition-all duration-300">
            <div class="w-14 h-14 rounded-xl bg-violet-100 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
              <svg class="w-7 h-7 text-violet-600" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M16.862 4.487l1.687-1.688a1.875 1.875 0 112.652 2.652L10.582 16.07a4.5 4.5 0 01-1.897 1.13L6 18l.8-2.685a4.5 4.5 0 011.13-1.897l8.932-8.931zm0 0L19.5 7.125M18 14v4.75A2.25 2.25 0 0115.75 21H5.25A2.25 2.25 0 013 18.75V8.25A2.25 2.25 0 015.25 6H10"/></svg>
            </div>
            <h3 class="text-xl font-bold text-gray-900 mb-3">Editor</h3>
            <p class="text-gray-500 leading-relaxed">Create and manage courses, add modules, and build learning paths for your students.</p>
          </div>

        </div>
      </div>
    </section>

    <!-- Pricing Section -->
    <section id="pricing" class="relative py-16 sm:py-20 md:py-24 px-4 sm:px-6">
      <div class="max-w-6xl mx-auto">
        <div class="text-center mb-12">
          <div class="inline-flex items-center gap-2 px-4 py-2 bg-linear-to-r from-fuchsia-50 to-violet-50 border border-fuchsia-200/50 rounded-full mb-6">
            <span class="w-2 h-2 bg-fuchsia-500 rounded-full"></span>
            <span class="text-sm text-fuchsia-700 font-medium">Simple and transparent</span>
          </div>
          <h2 class="text-2xl sm:text-3xl md:text-4xl font-bold text-gray-900 mb-4">
            Choose your plan
          </h2>
          <p class="text-lg text-gray-500 max-w-2xl mx-auto mb-8">
            Start free. Upgrade when you're ready.
          </p>

          <!-- Billing Toggle -->
          <div class="inline-flex bg-gray-100 rounded-lg p-1">
            <button @click="billingCycle = 'monthly'" :class="['px-5 py-2 rounded-md text-sm font-medium transition-all', billingCycle === 'monthly' ? 'bg-white text-gray-900 shadow-sm' : 'text-gray-500']">Monthly</button>
            <button @click="billingCycle = 'yearly'" :class="['px-5 py-2 rounded-md text-sm font-medium transition-all', billingCycle === 'yearly' ? 'bg-white text-gray-900 shadow-sm' : 'text-gray-500']">
              Yearly <span class="text-xs text-gray-400">-17%</span>
            </button>
          </div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-5 max-w-5xl mx-auto">
          <div v-for="(plan, index) in plans" :key="index" :class="['relative rounded-xl p-6 transition-all', plan.highlighted ? 'bg-linear-to-br from-fuchsia-500 to-violet-600 text-white ring-2 ring-fuchsia-500 shadow-lg' : 'bg-white border border-gray-200 hover:border-fuchsia-200']">
            <div v-if="plan.highlighted" class="absolute -top-3 left-1/2 -translate-x-1/2">
              <span class="px-3 py-1 bg-violet-500 rounded-full text-xs font-medium text-white">Popular</span>
            </div>
            <div class="mb-5">
              <h3 :class="['text-lg font-semibold mb-1', plan.highlighted ? 'text-white' : 'text-gray-800']">{{ plan.name }}</h3>
              <p :class="['text-sm', plan.highlighted ? 'text-fuchsia-100' : 'text-gray-500']">{{ plan.description }}</p>
            </div>
            <div class="mb-6">
              <span :class="['text-4xl font-semibold', plan.highlighted ? 'text-white' : 'text-gray-800']">${{ billingCycle === 'monthly' ? plan.monthlyPrice : Math.round(plan.yearlyPrice / 12) }}</span>
              <span :class="['text-sm', plan.highlighted ? 'text-fuchsia-100' : 'text-gray-500']">/month</span>
            </div>
            <ul class="space-y-3 mb-6">
              <li v-for="(feature, fIndex) in plan.features" :key="fIndex" :class="['flex items-center gap-2 text-sm', plan.highlighted ? 'text-fuchsia-100' : 'text-gray-600']">
                <svg :class="['w-4 h-4', plan.highlighted ? 'text-fuchsia-200' : 'text-fuchsia-500']" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/></svg>
                {{ feature }}
              </li>
            </ul>
            <button :class="['w-full py-3 rounded-lg text-sm font-medium transition-all', plan.highlighted ? 'bg-white text-fuchsia-600 hover:bg-fuchsia-50' : 'bg-linear-to-r from-fuchsia-500 to-violet-600 text-white hover:opacity-90']">
              Get Started
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="relative py-16 sm:py-20 md:py-24 px-4 sm:px-6 bg-fuchsia-50">
      <div class="max-w-3xl mx-auto text-center">
        <h2 class="text-2xl sm:text-3xl md:text-4xl font-semibold text-gray-800 mb-4">Ready to start learning?</h2>
        <p class="text-gray-600 mb-8 max-w-xl mx-auto">Join thousands of learners who've discovered the joy of learning with AI.</p>
        <a href="#pricing" class="inline-flex items-center gap-2 px-6 py-3 bg-linear-to-r from-fuchsia-500 to-violet-600 text-white font-medium rounded-lg hover:opacity-90 transition-opacity shadow-md">
          Start Learning Free
          <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/></svg>
        </a>
      </div>
    </section>

    <!-- Footer -->
    <footer class="relative py-8 sm:py-10 px-4 sm:px-6 border-t border-gray-100">
      <div class="max-w-6xl mx-auto">
        <div class="flex flex-col md:flex-row items-center justify-between gap-4 text-center md:text-left">
          <div class="flex items-center">
            <img src="./assets/images/logo 2.png" alt="DOT APP" class="h-8 sm:h-10 w-auto" />
          </div>
          <div class="flex items-center gap-6 text-sm text-gray-500">
            <a href="#" class="hover:text-gray-900 transition-colors">Privacy</a>
            <a href="#" class="hover:text-gray-900 transition-colors">Terms</a>
            <a href="#" class="hover:text-gray-900 transition-colors">Contact</a>
          </div>
          <p class="text-sm text-gray-400">© 2024 DOT. All rights reserved.</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<style>
@keyframes blob {
  0%, 100% { transform: translate(0, 0) scale(1); }
  25% { transform: translate(20px, -30px) scale(1.1); }
  50% { transform: translate(-20px, 20px) scale(0.9); }
  75% { transform: translate(30px, 10px) scale(1.05); }
}
.animate-blob { animation: blob 20s ease-in-out infinite; }
.animation-delay-2000 { animation-delay: 2s; }
.animation-delay-4000 { animation-delay: 4s; }
</style>
