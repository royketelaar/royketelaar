<template>
  <main class="h-screen">
    <NuxtImg src="/background.jpg" alt="Background" class="background-image" />
    <!-- Content -->
    <div class="content">
      <!-- Avatar image using NuxtImg -->
      <NuxtImg src="/avatar.jpg" alt="Avatar" class="avatar" />
      <div class="text-content">
        <!-- Name -->
        <h1 class="title">Roy Ketelaar</h1>

        <!-- Job -->
        <h2 class="heading-large">Front-end Developer</h2>

        <!-- About me text -->
        <p v-for="(item, index) in aboutMeText" :key="index">
          {{ item.text }}
        </p>

        <div class="list-section">
          <h3 class="heading-small">Programming</h3>
          <ul>
            <li>JavaScript / TypeScript</li>
            <li>Nuxt.js</li>
            <li>Vue</li>
            <li>HTML/SCSS</li>
            <li>Playwright</li>
            <li>SEO</li>
            <li>Netlify</li>
          </ul>
        </div>

        <div class="list-section">
          <h3 class="heading-small">Design & Methodology</h3>
          <ul>
            <li>UI/UX Design</li>
            <li>Design Thinking</li>
            <li>SCRUM</li>
          </ul>
        </div>

        <!-- Actions -->
        <div class="actions">
          <a href="mailto:info@royketelaar.nl">
            <button class="button">Get in touch!</button>
          </a>

          <!-- Links to GitHub and LinkedIn using NuxtImg -->
          <a
            href="https://github.com/royketelaar/"
            target="_blank"
            rel="noopener noreferrer"
          >
            <!-- <NuxtImg
              src="/images/github.svg"
              alt="GitHub"
              class="icon"
              width="24"
              height="24"
            /> -->
            <Icon name="uil:github" class="icon" />
          </a>
          <a
            href="https://www.linkedin.com/in/roy-ketelaar-36821b6b/"
            target="_blank"
            rel="noopener noreferrer"
          >
            <Icon name="entypo-social:linkedin" class="icon" />
          </a>
        </div>
      </div>
    </div>
  </main>
</template>

<script lang="ts" setup>
// TODO: replace by Nuxt Content
const aboutMeText = [
  {
    text: 'Hi there, my name is Roy Ketelaar. I am a frontend developer with a background in web design.'
  },
  {
    text: 'I love learning new things, working with people and building applications that users find useful.'
  },
  {
    text: 'I enjoy the process of trial-and-error, optimizing, and creating a good user experience.'
  },
  {
    text: 'To make this happen, I think from a Design Thinking perspective, i.e. first understanding the user and putting yourself in their position before actually starting the work.'
  },
  {
    text: 'Outside of work, I like experiencing new things, traveling to cool places and maintaining an active lifestyle 🏋🏻🥾'
  }
]
</script>

<style lang="scss" scoped>
.background-image {
  @apply fixed w-screen h-screen object-cover;
}

.content {
  @apply relative rounded-2xl text-stone-950 bg-stone-50 bg-opacity-80 top-36 p-8 pt-48 mx-8 mb-64 md:px-16 md:pb-16 md:mx-16 lg:pt-16 xl:max-w-4xl xl:mx-auto;
}

.text-content {
  @apply lg:w-2/3 lg:pr-4;
}

.avatar {
  @apply absolute rounded-full w-56 h-56 transform -translate-x-1/2 -top-16 left-1/2 lg:top-0 lg:left-auto lg:right-0 lg:transform-none lg:w-64 lg:h-64 lg:m-8;
}

.title {
  @apply font-black text-4xl text-center mb-1 lg:text-left font-serif;
}

.heading-large {
  @apply text-xl text-center mb-6 lg:text-left;
}

.heading-small {
  @apply font-bold mb-1;
}

p {
  @apply text-stone-950 mb-4;
}

.list-section {
  @apply flex flex-col mb-4;
  ul {
    @apply list-disc list-inside;
  }
}

.actions {
  @apply flex items-center mt-12;
}

.button {
  @apply bg-red-900 text-white py-2 px-4 rounded-lg mr-4;
}

.icon {
  @apply mx-2 w-6 h-6;
}
</style>
