<template>
  <div class="bg-slate-900 text-slate-100 min-h-screen font-sans">
    
    <section id="about" class="min-h-screen flex flex-col justify-center items-center px-4 max-w-4xl mx-auto pt-20">
      <div class="flex flex-col md:flex-row items-center gap-6 md:gap-12 animate-fade-in">
        <div class="w-48 h-48 md:w-56 md:h-56 rounded-2xl overflow-hidden shadow-2xl border-2 border-emerald-500/30 flex-shrink-0 bg-slate-800">
            <img src="/images/profile.jpg" alt="Ratipong Pomhan" class="w-full h-full object-cover" />
        </div>

        <div class="space-y-4 text-center md:text-left">
          <div class="space-y-1">
            <h1 class="text-4xl md:text-5xl font-extrabold text-white tracking-tight">
              Ratipong Pomhan
            </h1>
            <p class="text-xl font-semibold text-emerald-400 font-mono">Full Stack Developer</p>
          </div>
          
          <p class="text-slate-400 text-base md:text-lg leading-relaxed max-w-2xl">
            Experienced Full Stack Developer specializing in enterprise-level software. I have a proven track record in developing and maintaining legacy systems using <span class="text-white font-medium">C#, ASP.NET WebForms</span>, and <span class="text-white font-medium">SQL Server</span>, alongside experience in building data-driven reports and interactive dashboards. Possesses strong analytical, problem-solving skills, and the capability to handle complex, real-world backend architectures.
          </p>

          <div class="flex flex-wrap gap-3 justify-center md:justify-start pt-2">
            <a href="#portfolio" class="bg-emerald-500 hover:bg-emerald-600 text-slate-950 font-bold py-2.5 px-6 rounded-xl transition-all shadow-lg shadow-emerald-500/10">
              View My Work
            </a>
            <a href="#contact" class="bg-slate-800 hover:bg-slate-700 text-white font-medium py-2.5 px-6 rounded-xl border border-slate-700 transition-all">
              Get In Touch
            </a>
          </div>
        </div>
      </div>
    </section>
    
    <section id="skills" class="py-24 bg-slate-950 border-y border-slate-800/50">
      <div class="max-w-4xl mx-auto px-4">
        <div class="text-center space-y-2 mb-16">
          <h2 class="text-3xl font-bold text-white tracking-tight">Technical Skills</h2>
        </div>

        <div class="space-y-12">
          
          <div class="space-y-4">
            <h3 class="font-bold text-emerald-400 flex items-center gap-2 text-xl font-mono uppercase tracking-wider">
              <span class="flex h-2 w-2 relative">
                <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
                <span class="relative inline-flex rounded-full h-2 w-2 bg-emerald-500"></span>
              </span>
              Using Now
            </h3>
            
            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-3">
              <div class="bg-slate-900 border border-slate-800 p-2.5 md:p-3 rounded-xl flex items-center space-x-3 hover:border-slate-700 transition-colors">
                <Icon name="simple-icons:csharp" class="w-6 h-6 text-indigo-400 flex-shrink-0" />
                <span class="text-sm font-medium text-slate-200">C#</span>
              </div>
              <div class="bg-slate-900 border border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-slate-700 transition-colors">
                <Icon name="simple-icons:dotnet" class="w-6 h-6 text-blue-400 flex-shrink-0" />
                <span class="text-sm font-medium text-slate-200">ASP.NET</span>
              </div>
              <div class="bg-slate-900 border border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-slate-700 transition-colors">
                <Icon name="simple-icons:microsoftsqlserver" class="w-6 h-6 text-red-400 flex-shrink-0" />
                <span class="text-sm font-medium text-slate-200">SQL Server</span>
              </div>
              <div class="bg-slate-900 border border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-slate-700 transition-colors">
                <Icon name="simple-icons:oracle" class="w-6 h-6 text-red-500 flex-shrink-0" />
                <span class="text-sm font-medium text-slate-200">Oracle</span>
              </div>
              <div class="bg-slate-900 border border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-slate-700 transition-colors">
                <Icon name="simple-icons:javascript" class="w-6 h-6 text-yellow-400 flex-shrink-0" />
                <span class="text-sm font-medium text-slate-200">JavaScript</span>
              </div>
              <div class="bg-slate-900 border border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-slate-700 transition-colors">
                <Icon name="simple-icons:typescript" class="w-6 h-6 text-blue-500 flex-shrink-0" />
                <span class="text-sm font-medium text-slate-200">TypeScript</span>
              </div>
              <div class="bg-slate-900 border border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-slate-700 transition-colors">
                <Icon name="simple-icons:html5" class="w-6 h-6 text-orange-500 flex-shrink-0" />
                <span class="text-sm font-medium text-slate-200">HTML5</span>
              </div>
              <div class="bg-slate-900 border border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-slate-700 transition-colors">
                <Icon name="simple-icons:css3" class="w-6 h-6 text-blue-400 flex-shrink-0" />
                <span class="text-sm font-medium text-slate-200">CSS3</span>
              </div>
              <div class="bg-slate-900 border border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-slate-700 transition-colors">
                <Icon name="simple-icons:bootstrap" class="w-6 h-6 text-purple-500 flex-shrink-0" />
                <span class="text-sm font-medium text-slate-200">Bootstrap</span>
              </div>
              <div class="bg-slate-900 border border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-slate-700 transition-colors">
                <Icon name="simple-icons:git" class="w-6 h-6 text-orange-600 flex-shrink-0" />
                <span class="text-sm font-medium text-slate-200">Git</span>
              </div>
              <div class="bg-slate-900 border border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-slate-700 transition-colors">
                <Icon name="simple-icons:figma" class="w-6 h-6 text-rose-400 flex-shrink-0" />
                <span class="text-sm font-medium text-slate-200">Figma</span>
              </div>
            </div>
          </div>

          <div class="space-y-4">
            <h3 class="font-bold text-amber-400 flex items-center gap-2 text-xl font-mono uppercase tracking-wider">
              <Icon name="mdi:book-open-page-variant" class="w-5 h-5 animate-pulse" />
              Learning
            </h3>
            
            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-3">
              <div class="bg-slate-900/40 border border-dashed border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-amber-500/30 transition-colors group">
                <Icon name="simple-icons:react" class="w-6 h-6 text-sky-400 flex-shrink-0 grayscale group-hover:grayscale-0 transition-all" />
                <span class="text-sm font-medium text-slate-400 group-hover:text-slate-200 transition-colors">React</span>
              </div>
              <div class="bg-slate-900/40 border border-dashed border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-amber-500/30 transition-colors group">
                <Icon name="simple-icons:nodedotjs" class="w-6 h-6 text-green-500 flex-shrink-0 grayscale group-hover:grayscale-0 transition-all" />
                <span class="text-sm font-medium text-slate-400 group-hover:text-slate-200 transition-colors">Node.js</span>
              </div>
              <div class="bg-slate-900/40 border border-dashed border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-amber-500/30 transition-colors group">
                <Icon name="simple-icons:vuedotjs" class="w-6 h-6 text-green-500 flex-shrink-0 grayscale group-hover:grayscale-0 transition-all" />
                <span class="text-sm font-medium text-slate-400 group-hover:text-slate-200 transition-colors">Vue.js</span>
              </div>
              <div class="bg-slate-900/40 border border-dashed border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-amber-500/30 transition-colors group">
                <Icon name="simple-icons:nuxtdotjs" class="w-6 h-6 text-emerald-500 flex-shrink-0 grayscale group-hover:grayscale-0 transition-all" />
                <span class="text-sm font-medium text-slate-400 group-hover:text-slate-200 transition-colors">Nuxt.js</span>
              </div>
              <div class="bg-slate-900/40 border border-dashed border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-amber-500/30 transition-colors group">
                <Icon name="simple-icons:tailwindcss" class="w-6 h-6 text-cyan-400 flex-shrink-0 grayscale group-hover:grayscale-0 transition-all" />
                <span class="text-sm font-medium text-slate-400 group-hover:text-slate-200 transition-colors">Tailwind CSS</span>
              </div>
              <div class="bg-slate-900/40 border border-dashed border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-amber-500/30 transition-colors group">
                <Icon name="simple-icons:firebase" class="w-6 h-6 text-amber-500 flex-shrink-0 grayscale group-hover:grayscale-0 transition-all" />
                <span class="text-sm font-medium text-slate-400 group-hover:text-slate-200 transition-colors">Firebase</span>
              </div>
            </div>
          </div>

          <div class="space-y-4">
            <h3 class="font-bold text-sky-400 flex items-center gap-2 text-xl font-mono uppercase tracking-wider">
              <Icon name="mdi:star-circle-outline" class="w-5 h-5 text-sky-400" />
              Other Skills
            </h3>
            
            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-3">             
              <div class="bg-slate-900 border border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-slate-700 transition-colors">
                <Icon name="simple-icons:adobeillustrator" class="w-6 h-6 text-orange-500 flex-shrink-0" />
                <span class="text-sm font-medium text-slate-200">Illustrator</span>
              </div>
              <div class="bg-slate-900 border border-slate-800 p-3 rounded-xl flex items-center space-x-3 hover:border-slate-700 transition-colors">
                <Icon name="simple-icons:adobephotoshop" class="w-6 h-6 text-sky-600 flex-shrink-0" />
                <span class="text-sm font-medium text-slate-200">Photoshop</span>
              </div>
            </div>
          </div>

        </div>
      </div>
    </section>

    <section id="portfolio" class="py-24 max-w-4xl mx-auto px-4">
      <div class="text-center space-y-2 mb-12">
        <h2 class="text-3xl font-bold text-white tracking-tight">Featured Projects</h2>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <div class="bg-slate-900 rounded-2xl border border-slate-800 overflow-hidden hover:border-emerald-500/30 transition-all group">
          <div class="p-6 space-y-4">
            <div class="flex justify-between items-start">
              <span class="text-xs font-mono px-2.5 py-1 bg-emerald-500/10 text-emerald-400 rounded-md">Current Project</span>
              <div class="flex items-center space-x-2 text-slate-400">
                <Icon name="mdi:github" class="w-5 h-5 hover:text-white cursor-pointer" />
              </div>
            </div>
            <h3 class="text-xl font-bold text-white group-hover:text-emerald-400 transition-colors">Personal Web Portfolio</h3>
            <div class="flex flex-wrap gap-1.5 pt-2">
              <span class="text-xs bg-slate-800 text-slate-300 px-2.5 py-1 rounded-md font-mono">Nuxt 4</span>
              <span class="text-xs bg-slate-800 text-slate-300 px-2.5 py-1 rounded-md font-mono">Vue 3</span>
              <span class="text-xs bg-slate-800 text-slate-300 px-2.5 py-1 rounded-md font-mono">TailwindCSS</span>
            </div>
          </div>
        </div>

        <div class="bg-slate-900/40 rounded-2xl border border-dashed border-slate-800 flex flex-col items-center justify-center p-8 text-center text-slate-500">
          <Icon name="mdi:plus-circle-outline" class="w-8 h-8 mb-2 text-slate-600" />
          <p class="text-sm">กำลังเตรียมโปรเจ็คถัดไป...</p>
        </div>
      </div>
    </section>

    <section id="experience" class="py-24 bg-slate-950 border-t border-slate-800/50">
      <div class="max-w-3xl mx-auto px-4">
        <div class="text-center space-y-2 mb-16">
          <h2 class="text-3xl font-bold text-white tracking-tight">Work Experience</h2>
        </div>

        <div class="relative border-l border-slate-800 ml-4 md:ml-40 space-y-12">
          
          <div class="relative pl-6 md:pl-8 group">
            <div class="absolute -left-[9px] top-1.5 w-4 h-4 rounded-full bg-slate-950 border-2 border-emerald-400 group-hover:bg-emerald-400 transition-colors z-10"></div>
            
            <div class="md:absolute md:-left-44 md:top-1 md:w-36 md:text-right text-[11px] md:text-sm font-mono text-emerald-400 mb-3 md:mb-0 whitespace-nowrap inline-flex items-center bg-emerald-500/10 md:bg-transparent px-2.5 py-1 md:p-0 rounded-full md:rounded-none border border-emerald-500/20 md:border-none">
              Jan 2025 - Jan 2026
            </div>

            <div class="space-y-2">
              <h3 class="text-xl font-bold text-white">Full Stack Developer</h3>
              <div class="text-sm font-medium text-slate-300">
                Nimblesoft <span class="text-slate-500 font-normal">| 184/83 Forum Tower, 17th Floor, Ratchadaphisek Road, Huai Khwang, Bangkok 10310</span>
              </div>
              <ul class="list-disc pl-4 text-sm text-slate-400 space-y-1.5 pt-2">
                <li>Develop and maintain enterprise-level web applications using C#, ASP.NET WebForms, and SQL Server.</li>
                <li>Design and implement interactive charts and enterprise dashboards.</li>
                <li>Create and modify highly optimized SQL statements and complex stored procedures.</li>
                <li>Collaborate with quality assurance testers to resolve production issues and ensure system reliability.</li>
              </ul>
            </div>
          </div>

          <div class="relative pl-6 md:pl-8 group">
            <div class="absolute -left-[9px] top-1.5 w-4 h-4 rounded-full bg-slate-950 border-2 border-slate-700 group-hover:border-emerald-400 transition-colors z-10"></div>
            
            <div class="md:absolute md:-left-44 md:top-1 md:w-36 md:text-right text-[11px] md:text-sm font-mono text-slate-500 mb-3 md:mb-0 group-hover:text-emerald-400 transition-colors whitespace-nowrap inline-flex items-center bg-slate-800 md:bg-transparent px-2.5 py-1 md:p-0 rounded-full md:rounded-none border border-slate-800 md:border-none">
              Apr 2023 - Jun 2023
            </div>

            <div class="space-y-2">
              <h3 class="text-xl font-bold text-slate-300 group-hover:text-white transition-colors">QA Tester</h3>
              <div class="text-sm font-medium text-slate-400">
                Drago Venture Company Limited
              </div>
              <ul class="list-disc pl-4 text-sm text-slate-400 space-y-1.5 pt-2">
                <li>Test and verify web application interfaces for functional precision and UX/UI accuracy.</li>
              </ul>
            </div>
          </div>

        </div>

        <div class="mt-24 pt-12 border-t border-slate-900 space-y-8">
          <div class="text-center space-y-1">
            <h3 class="text-2xl font-bold text-white">Education</h3>
          </div>
          
          <div class="bg-slate-900/50 border border-slate-800 p-6 rounded-2xl flex flex-col sm:flex-row justify-between gap-4">
            <div class="space-y-1">
              <h4 class="font-bold text-white text-lg">Bachelor's Degree in Information Technology</h4>
              <p class="text-sm text-slate-300">Udon Thani Rajabhat University</p>
              <p class="text-xs text-slate-500">Faculty of Science</p>
            </div>
            <div class="sm:text-right space-y-1 flex-shrink-0">
              <span class="inline-block text-xs font-mono font-bold bg-emerald-500/10 text-emerald-400 px-2.5 py-1 rounded-md">GPA: 3.07</span>
              <p class="text-xs text-slate-500 font-mono">Class of 2018 - 2023</p>
            </div>
          </div>
        </div>

      </div>
    </section>

  </div>
</template>