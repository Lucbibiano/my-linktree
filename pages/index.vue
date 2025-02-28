<template>
  <ProfileInfo
    title="Lucas Bibiano"
    subtitle="@lucasbibiano"
    headline="Technology | TechLead | Developer"
    :photo="photoProfile"
  />
  <p class="text-gray-600 text-center text-sm max-w-sm mx-auto">
    Apaixonado por tecnologia e inovação. Atualmente, atuo como Tech Lead,
    ajudando a construir soluções inteligentes.
  </p>
  <div
    class="max-w-xs mx-auto bg-white/70 backdrop-blur-lg border border-gray-200 rounded-2xl shadow-xl p-6 space-y-3 mt-3 pt-0"
  >
    <ButtonAction
      link="https://www.linkedin.com/in/lucasbibiano/"
      text="Linkedin"
      :icon="linkedinIcon"
    />
    <ButtonAction
      link="https://github.com/Lucbibiano/"
      text="GitHub"
      :icon="githubIcon"
    />
    <ButtonAction
      link="https://www.instagram.com/lubibiano/"
      text="Instagram"
      :icon="instagramIcon"
    />
  </div>

  <a
    href="mailto:lucassouzasb@gmail.com"
    class="block text-center text-blue-500 font-semibold hover:underline mt-4"
  >
    📩 Entre em contato por e-mail!
  </a>
</template>

<script>
import linkedinIcon from "./../assets/images/linkedin.png";
import githubIcon from "./../assets/images/github.png";
import instagramIcon from "./../assets/images/instagram.png";
import photoProfile from "./../assets/images/photo.jpeg";

export default {
  data() {
    return {
      linkedinIcon,
      githubIcon,
      instagramIcon,
      photoProfile,
    };
  },
};
</script>
