<template>
  <div class="bg-gray-50 min-h-screen py-10 px-5">
    <!-- Container utama -->
    <div class="max-w-4xl mx-auto bg-white shadow-lg rounded-lg overflow-hidden p-8">
      
      <!-- Header (Nama dan Job Title) -->
      <header class="text-center border-b pb-8 mb-8">
        <h1 class="text-4xl font-bold text-gray-800">{{ name }}</h1>
        <p class="text-xl text-gray-600">{{ jobTitle }}</p>
        <d class="text-xl text-gray-600">{{ emailNoTelephone}}</d>
      </header>

      <!-- Konten satu kolom -->
      <div class="grid grid-cols-1 gap-8">
         <!-- About Me -->
         <section>
          <h2 class="text-2xl font-semibold text-gray-700 border-b pb-2 mb-6">About Me</h2>
          <p class="text-gray-600">{{ about }}</p>
        </section>

         <!-- Education -->
         <section>
          <h2 class="text-2xl font-semibold text-gray-700 border-b pb-2 mb-6">Education</h2>
          <ul class="space-y-4">
            <li v-for="(edu, index) in education" :key="index" class="flex items-start">
              <div class="ml-3">
                <strong class="text-lg font-medium text-gray-800">{{ edu.degree }}</strong> 
                <span class="block text-gray-600">{{ edu.field }}</span>
                <span class="block text-gray-500">{{ edu.institution }} ({{ edu.year }})</span>
              </div>
            </li>
          </ul>
        </section>

        <!-- Experience -->
        <section>
          <h2 class="text-2xl font-semibold text-gray-700 border-b pb-2 mb-6">Job Experience</h2>
          <ul class="space-y-8">
            <li v-for="(job, index) in experience" :key="index">
              <div>
                <strong class="text-lg font-medium text-gray-800">{{ job.title }}</strong> 
                <span class="block text-gray-600">{{ job.company }} ({{ job.year }})</span>
                <p class="text-gray-600 mt-2">{{ job.description }}</p>
              </div>
            </li>
          </ul>
        </section>

        <!-- Experience -->
        <section>
          <h2 class="text-2xl font-semibold text-gray-700 border-b pb-2 mb-6">Project Experience</h2>
          <ul class="space-y-8">
            <li v-for="(project) in project" key:="project">
              <div>
                <strong class="text-lg font-medium text-gray-800">{{ project.title }}</strong> 
                <span class="block text-gray-600">{{ project.work }} ({{ project.year }})</span>
                <p class="text-gray-600 mt-2">{{ project.description }}</p>
              </div>
            </li>
          </ul>
        </section>

        <!-- Skills -->
        <section>
          <h2 class="text-2xl font-semibold text-gray-700 border-b pb-2 mb-6">Skills</h2>
          <ul class="flex flex-wrap gap-4">
            <li v-for="(skill, index) in skills" :key="index" class="text-gray-600 bg-gray-200 px-4 py-2 rounded-lg">
              {{ skill }}
            </li>
          </ul>
        </section>
      </div>
    </div>
  </div>
</template>


<script lang="ts">
export default {
  data() {
    return {
      name: 'Azizah Nur Istiqomah',
      jobTitle: 'Data Analyst',
      emailNoTelephone: 'azizahnuristiqomah456@gmail.com | +62-882-0065-43100',
      about: 'Saya adalah seorang mahasiswi program studi Teknologi Informasi, Universitas Brawijaya. Saya memiliki pengalaman dalam membuat project project di perkuliahan yang akan menjadi penunjang skill saya untuk karir di masa depan. Tujuan karir masa depan saya adalah menjadi Data Analyst, karena Data Analyst mencakup bidang keahlian yang ingin saya tekuni dan saat ini lebih berfokus pada skill skill yang di butuhkan untuk menjadi Data Analyst.',
      experience: [
        {
          title: 'Posisi 1',
          company: 'PT. Lampung Cerdas',
          year: '2023',
          description: 'Saya bekerja freelance sebagai Digital Marketing di perusahaan ini. Saya mempromosikan jasa pendidikan kepada pengguna, mengelola database pengguna, dan juga menjalin komunikasi dengan pengguna melalui konsultasi pengguna dan mengarahkan langsung tentang prosedur apa yang harus dilakukan pengguna.'
        },
      ],

      project: [
        {
          title: 'Project 1',
          work: 'Kalkulator ',
          year: '2024',
          description: 'Project ini adalah kalkulator sederhana yang dapat melakukan perhitungan seperti pemjumlahan, pengurangan, perkalian dan pembagian. Project kalkulator sederhana ini dibuat menggunakan bahasa pemrograman Python.'
        },
        {
          title: 'Project 2',
          work: 'Contact Form',
          year: '2024',
          description: 'Project ini adalah form untuk mengumpulakan database, yang dimana di dalamnya dapat memasukan data nama, gender, email, kelas, yang nantinya data yang dimasukan akan masuk dalam basis data.'
        },
        {
          title: 'Project 3',
          work: 'Slider App',
          year: '2024',
          description: 'Ini adalah project sederhana yang dibuat menggunakan Java Script yang dapat menampilkan berapa banyak kita menekan di laman tersebut, dapat merubah warna dan menampilkan gambar yang dapat di geser horizontal.'
        },
        {
          title: 'Project 4',
          work: 'UI/UX Aplikasi Kuliner Halal Pallate',
          year: '2023',
          description: 'Ini adalah project tampilan aplikasi kuliner yang mana di dalamnya terdapat fitur untuk memesan makanan, terdapat maps di dalamnya untuk melihat dimana saja restoran berada, terdapat fitur untuk mereview restoran dan makanan yang pernah kita kunjungi melalui platform aplikasi ini.'
        },
        {
          title: 'Project 5',
          work: 'UI/UX Aplikasi Transportasi umum',
          year: '2023',
          description: 'Ini adalah project tampilan aplikasi untuk memesan transportasi umum seperti ojek online, taxi online dan juga melihat jadwal dan rute bus.'
        },
      ],
      
      education: [
        {
          degree: 'Diploma 3',
          field: 'Teknologi Informasi',
          institution: 'Universitas Brawijaya',
          year: '2026'
        },
        {
          degree: 'SMA',
          field: 'Matematika Ilmu Pengetahuan Alam',
          institution: 'MAN 1 Karanganom Klaten',
          year: '2023'
        },
      ],
      skills: [
        'Microsoft Excel',
        'Microsoft Word',
        'Microsoft Power Point',
        'Java Script',
        'Data Analysis',
        'Python',
        'SQL',
        'Figma',
        'Java'
      ]
    };
  }
};
</script>

