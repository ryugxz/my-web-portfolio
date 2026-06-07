<template>
  <div class="bg-slate-900 text-slate-100 min-h-screen">
    
    <section id="about" class="min-h-screen flex flex-col justify-center items-center px-4 max-w-5xl mx-auto pt-16">
      <div class="flex flex-col md:flex-row items-center gap-10 md:gap-16 animate-fade-in w-full">
        
        <div class="relative group flex-shrink-0">
          <div class="absolute -inset-1 rounded-2xl bg-gradient-to-r from-emerald-500 to-teal-500 opacity-30 blur group-hover:opacity-50 transition duration-300"></div>
          <div class="w-48 h-48 md:w-56 md:h-56 rounded-2xl overflow-hidden shadow-2xl border border-emerald-500/20 relative bg-slate-800">
            <img src="/images/profile.jpg" alt="Ratipong Pomhan" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" />
          </div>
        </div>

        <div class="space-y-6 text-center md:text-left flex-1">
          <div class="space-y-2">
            <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-emerald-500/10 border border-emerald-500/20 text-emerald-400 text-xs font-mono tracking-wider uppercase mb-1">
              <span class="w-1.5 h-1.5 rounded-full bg-emerald-400 animate-pulse"></span>
              Available for Opportunities
            </div>
            <h1 class="text-3xl md:text-5xl font-extrabold text-white tracking-tight leading-tight">
              Building Business Solutions
              <span class="block bg-gradient-to-r from-emerald-400 to-teal-400 bg-clip-text text-transparent">Through Modern Web Development</span>
            </h1>
            <p class="text-slate-400 text-sm md:text-base leading-relaxed max-w-2xl">
              Full Stack Developer specializing in <span class="text-emerald-400">C#, ASP.NET, SQL Server</span> and Modern Frontend Technologies.
            </p>
            <div class="text-emerald-400 font-mono">
              Ratipong Pomhan
            </div>
          </div>
          <div class="flex flex-wrap gap-2">
            <!-- <span>🇹🇭 Chonburi, Thailand</span> -->
            <!-- <span>•</span> -->
            <span>Open to Work</span>
            <span>•</span>
            <span>Frontend / Full Stack</span>
          </div>
          
          <!-- <p class="text-slate-400 text-sm md:text-base leading-relaxed max-w-2xl">
            I'm a Web Developer with experience in enterprise software maintenance and web application development. My primary expertise is 
            <span class="text-slate-200 font-semibold underline decoration-emerald-500/40">C#, ASP.NET WebForms</span>, and <span class="text-slate-200 font-semibold underline decoration-emerald-500/40">SQL Server</span>
            , and I am currently expanding my skillset into modern frontend development with React. I enjoy solving business problems through software,
            improving system performance, and building user-friendly web experiences.
          </p> -->

          <div class="grid grid-cols-2 gap-4 max-w-sm pt-2">
            <div class="bg-slate-950/30 border border-slate-800/60 p-3 rounded-xl font-mono text-center md:text-left">
              <div class="text-xl font-bold text-white">1+ Year</div>
              <div class="text-xs text-slate-500">Enterprise Exp.</div>
            </div>
            <div class="bg-slate-950/30 border border-slate-800/60 p-3 rounded-xl font-mono text-center md:text-left">
              <div class="text-xl font-bold text-white">3+ Core</div>
              <div class="text-xs text-slate-500">Live Apps</div>
            </div>
          </div>

          <div class="flex flex-wrap gap-3 justify-center md:justify-start pt-2">
            <a href="#portfolio" class="bg-emerald-500 hover:bg-emerald-600 text-slate-950 font-bold py-2.5 px-6 rounded-xl transition-all shadow-lg shadow-emerald-500/10 hover:shadow-emerald-500/20 active:scale-95 text-sm">
              View My Projects
            </a>
            <a href="#contact" class="bg-slate-800 hover:bg-slate-700 text-white font-medium py-2.5 px-6 rounded-xl border border-slate-700 transition-all text-sm active:scale-95">
              Get In Touch
            </a>
            <div class="flex flex-wrap gap-3">
              <a
                href="/resume/ratipong-pomhan-cv-th.pdf" target="_blank" class="inline-flex items-center justify-center gap-2 bg-slate-800 hover:bg-slate-700 text-white font-medium py-2.5 px-6 rounded-xl border border-slate-700 transition-all text-sm active:scale-95">
                <Icon name="mdi:eye" class="w-5 h-5 text-emerald-400" />
                View CV
              </a>
              <a
                href="/resume/ratipong-pomhan-cv-th.pdf"
                download="Ratipong-Pomhan-CV.pdf"
                class="inline-flex items-center justify-center gap-2 bg-slate-800 hover:bg-slate-700 text-white font-medium py-2.5 px-6 rounded-xl border border-slate-700 transition-all text-sm active:scale-95">
                <Icon name="mdi:file-pdf-box" class="w-5 h-5 text-red-400" />
                Download CV
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>
    
    <section id="skills" class="py-24 bg-slate-950 border-y border-slate-800/50">
      <div class="max-w-4xl mx-auto px-4">
        <div class="text-center space-y-2 mb-16">
          <h2 class="text-2xl md:text-3xl font-bold text-white tracking-tight">Technical Skills</h2>
          <p class="text-slate-400 text-xs md:text-sm">คลังทักษะและการเรียนรู้ทางด้านเทคโนโลยีเครื่องมือต่างๆ ของผม</p>
        </div>

        <div class="space-y-14">
          
          <div class="space-y-4">
            <h3 class="font-bold text-emerald-400 flex items-center gap-2 text-base font-mono uppercase tracking-wider">
              <span class="flex h-2 w-2 relative"><span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span><span class="relative inline-flex rounded-full h-2 w-2 bg-emerald-500"></span></span>
              Using Now
            </h3>
            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-3">
              <SkillIcon v-for="skill in currentSkills" :key="skill.name" :name="skill.name" :icon="skill.icon" :color="skill.color" />
            </div>
          </div>

          <div class="space-y-4">
            <h3 class="font-bold text-amber-400 flex items-center gap-2 text-base font-mono uppercase tracking-wider">
              <Icon name="mdi:book-open-page-variant" class="w-4 h-4 animate-pulse" />
              Learning
            </h3>
            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-3">
              <SkillIcon v-for="skill in learningSkills" :key="skill.name" :name="skill.name" :icon="skill.icon" :color="skill.color" :is-learning="true" />
            </div>
          </div>

          <div class="space-y-4">
            <h3 class="font-bold text-sky-400 flex items-center gap-2 text-base font-mono uppercase tracking-wider">
              <Icon name="mdi:star-circle-outline" class="w-4 h-4 text-sky-400" />
              Other Skills
            </h3>
            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-3">              
              <SkillIcon v-for="skill in otherSkills" :key="skill.name" :name="skill.name" :icon="skill.icon" :color="skill.color" />
            </div>
          </div>

        </div>
      </div>
    </section>

    <section id="portfolio" class="py-24 max-w-4xl mx-auto px-4">
      <div class="text-center space-y-2 mb-14">
        <h2 class="text-2xl md:text-3xl font-bold text-white tracking-tight">Featured Projects</h2>
        <p class="text-slate-400 text-xs md:text-sm">รวมผลงานการพัฒนาแอปพลิเคชันระบบจัดการและการันตีผลงานบน Git</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <ProjectCard
          v-for="(project, index) in projects"
          :key="index"
          :project="project"
        />
      </div>
    </section>

    <section id="experience" class="py-24 bg-slate-950 border-t border-slate-800/50">
      <div class="max-w-3xl mx-auto px-4">
        <div class="text-center space-y-2 mb-16">
          <h2 class="text-2xl md:text-3xl font-bold text-white tracking-tight">Work Experience</h2>
          <p class="text-slate-400 text-xs md:text-sm">ประวัติและเส้นทางการทำงานในสายงานพัฒนาซอฟต์แวร์ที่ผ่านมา</p>
        </div>

        <div class="relative border-l border-slate-800 ml-4 md:ml-40 space-y-12">
          
          <div class="relative pl-6 md:pl-8 group">
            <div class="absolute -left-[9px] top-1.5 w-4 h-4 rounded-full bg-slate-950 border-2 border-emerald-400 group-hover:bg-emerald-400 transition-colors z-10"></div>
            <div class="md:absolute md:-left-44 md:top-1 md:w-36 md:text-right text-[11px] md:text-sm font-mono text-emerald-400 mb-3 md:mb-0 whitespace-nowrap inline-flex items-center bg-emerald-500/10 md:bg-transparent px-2.5 py-1 md:p-0 rounded-full md:rounded-none border border-emerald-500/20 md:border-none font-bold">
              Jan 2025 - Jan 2026
            </div>

            <div class="space-y-2">
              <h3 class="text-lg font-bold text-white group-hover:text-emerald-400 transition-colors">Full Stack Developer</h3>
              <div class="text-xs md:text-sm font-medium text-slate-300">
                Nimblesoft <span class="text-slate-500 font-normal">| 184/83 Forum Tower, 17th Floor, Ratchadaphisek Road, Huai Khwang, Bangkok 10310</span>
              </div>
              <ul class="list-disc pl-4 text-xs md:text-sm text-slate-400 space-y-2 pt-2">
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
              <h3 class="text-lg font-bold text-slate-300 group-hover:text-white transition-colors">QA Tester</h3>
              <div class="text-xs md:text-sm font-medium text-slate-400">
                Drago Venture Company Limited
              </div>
              <ul class="list-disc pl-4 text-xs md:text-sm text-slate-400 space-y-2 pt-2">
                <li>Test and verify web application interfaces for functional precision and UX/UI accuracy.</li>
              </ul>
            </div>
          </div>

        </div>

        <div class="mt-24 pt-12 border-t border-slate-900 space-y-8">
          <div class="text-center space-y-1">
            <h3 class="text-xl md:text-2xl font-bold text-white">Education</h3>
          </div>
          
          <div class="bg-slate-900/40 border border-slate-800/80 p-6 rounded-2xl flex flex-col sm:flex-row justify-between gap-4 hover:border-slate-700 transition-colors">
            <div class="space-y-1">
              <h4 class="font-bold text-white text-base md:text-lg">Bachelor's Degree in Information Technology</h4>
              <p class="text-sm text-slate-300">Udon Thani Rajabhat University</p>
              <p class="text-xs text-slate-500 font-mono">Faculty of Science</p>
            </div>
            <div class="sm:text-right space-y-2 flex-shrink-0">
              <span class="inline-block text-xs font-mono font-bold bg-emerald-500/10 text-emerald-400 px-2.5 py-1 rounded-md border border-emerald-500/10">GPA: 3.07</span>
              <p class="text-xs text-slate-500 font-mono">Class of 2018 - 2023</p>
            </div>
          </div>
        </div>

      </div>
    </section>

  </div>
</template>

<script setup>

useHead({
  htmlAttrs: {
    class: 'scroll-smooth',
    style: 'scroll-padding-top: 4rem;'
  },
  link: [
    { 
      rel: 'icon', 
      type: 'image/png',
      href: 'images/code-circle-stroke-rounded.png'
    }
  ]
})

const currentSkills = [
  { name: 'C#', icon: 'simple-icons:csharp', color: 'text-indigo-400' },
  { name: 'ASP.NET', icon: 'simple-icons:dotnet', color: 'text-blue-400' },
  { name: 'SQL Server', icon: 'simple-icons:microsoftsqlserver', color: 'text-red-400' },
  { name: 'Oracle', icon: 'simple-icons:oracle', color: 'text-red-500' },
  { name: 'JavaScript', icon: 'simple-icons:javascript', color: 'text-yellow-400' },
  { name: 'TypeScript', icon: 'simple-icons:typescript', color: 'text-blue-500' },
  { name: 'HTML5', icon: 'simple-icons:html5', color: 'text-orange-500' },
  { name: 'CSS3', icon: 'simple-icons:css3', color: 'text-blue-400' },
  { name: 'Bootstrap', icon: 'simple-icons:bootstrap', color: 'text-purple-500' },
  { name: 'Git', icon: 'simple-icons:git', color: 'text-orange-600' },
  { name: 'Figma', icon: 'simple-icons:figma', color: 'text-rose-400' },
];

const learningSkills = [
  { name: 'React', icon: 'simple-icons:react', color: 'text-sky-400' },
  { name: 'Node.js', icon: 'simple-icons:nodedotjs', color: 'text-green-500' },
  { name: 'Vue.js', icon: 'simple-icons:vuedotjs', color: 'text-green-500' },
  { name: 'Nuxt.js', icon: 'simple-icons:nuxtdotjs', color: 'text-emerald-500' },
  { name: 'Tailwind CSS', icon: 'simple-icons:tailwindcss', color: 'text-cyan-400' },
  { name: 'Firebase', icon: 'simple-icons:firebase', color: 'text-amber-500' },
];

const otherSkills = [
  { name: 'Illustrator', icon: 'simple-icons:adobeillustrator', color: 'text-orange-500' },
  { name: 'Photoshop', icon: 'simple-icons:adobephotoshop', color: 'text-sky-600' },
];

const projects = [
  {
    title: 'Personal Web Portfolio',
    image: '/images/myportfolio.png',
    description: 'เว็บไซต์รวบรวมผลงานและประวัติส่วนตัว ที่พัฒนาด้วย Nuxt และ TailwindCSS',
    tag: 'Current',
    tagClass: 'bg-emerald-500/10 text-emerald-400 border-emerald-500/10',
    vercelUrl: 'https://my-web-portfolio-ruby.vercel.app/',
    githubUrl: 'https://github.com/ryugxz/my-web-portfolio',
    techStack: ['Nuxt', 'Vue', 'TailwindCSS']
  },
  {
    title: 'Web-Swoosh',
    image: '/images/swoosh.png',
    description: 'เว็บแอปพลิเคชัน ของสโมสรฟุตบอล Swoosh จากเกม EA FC ในโหมด Clubs ที่พัฒนาด้วย React และ Vite เพื่อฝึกทักษะการพัฒนาเว็บด้วยเทคโนโลยีสมัยใหม่',
    tag: 'React Project',
    tagClass: 'bg-sky-500/10 text-sky-400 border-sky-500/10',
    vercelUrl: 'https://web-swoosh.vercel.app/',
    githubUrl: 'https://github.com/ryugxz/web-swoosh',
    techStack: ['React', 'JavaScript', 'Vite']
  },
  {
    title: 'Web-EAFC-Clubs-Leagues',
    image: '/images/eafcclubs.png',
    description: 'แพลตฟอร์มจัดการแมตช์ ประมวลผลคะแนน และสถิติลีกอีสปอร์ตสำหรับสโมสรเกม EA FC ในโหมด Clubs เพื่อออกแบบระบบจัดเก็บชุดข้อมูลให้เป็นระเบียบ',
    tag: 'Gaming Web',
    tagClass: 'bg-yellow-500/10 text-yellow-500 border-yellow-500/10',
    vercelUrl: 'https://web-eafc-clubs-leagues.vercel.app/',
    githubUrl: 'https://github.com/ryugxz/web-eafc-clubs-leagues',
    techStack: ['React', 'JavaScript']
  }
]

useSeoMeta({
  title: 'Ratipong Pomhan | Full Stack Developer',

  description:
    'Full Stack Developer specializing in ASP.NET, C#, SQL Server, React, Nuxt.js and modern web technologies.',

  keywords:
    'Ratipong Pomhan, Full Stack Developer, ASP.NET Developer, C#, SQL Server, React Developer, Nuxt Developer, Portfolio',

  ogTitle:
    'Ratipong Pomhan Portfolio',

  ogDescription:
    'Full Stack Developer Portfolio',

  ogType:
    'website',
    
  author:
    'Ratipong Pomhan'
})
</script>