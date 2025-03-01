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
  <div class="text-center mt-6">
    <div class="flex justify-center mt-6">
      <button
        @click="openModal"
        class="flex items-center rounded-2xl bg-gray-100 px-6 py-4 text-lg font-medium shadow-md hover:shadow-lg transition ease-in-out duration-150 border border-gray-300 cursor-pointer"
      >
        Ver Tecnologias
      </button>
    </div>
    <TechModal :isOpen="isModalOpen" :closeModal="closeModal" />
  </div>
  <a
    href="mailto:lucassouzasb@gmail.com"
    class="block text-center text-blue-500 font-semibold hover:underline mt-4"
  >
    📩 Entre em contato por e-mail!
  </a>
</template>

<script>
import { ref } from "vue";
import TechModal from "./../components/TechModal.vue";
import linkedinIcon from "./../assets/images/linkedin.png";
import githubIcon from "./../assets/images/github.png";
import instagramIcon from "./../assets/images/instagram.png";
import photoProfile from "./../assets/images/photo.jpeg";

export default {
  components: {
    TechModal,
  },
  setup() {
    const isModalOpen = ref(false);

    const openModal = () => {
      isModalOpen.value = true;
    };

    const closeModal = () => {
      isModalOpen.value = false;
    };

    return {
      isModalOpen,
      openModal,
      closeModal,
      linkedinIcon,
      githubIcon,
      instagramIcon,
      photoProfile,
    };
  },
};
</script>
