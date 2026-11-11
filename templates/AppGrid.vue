<script setup>
import {useWindowsStore} from '@/stores/windows'
import { onMounted } from 'vue';

const windowsStore = useWindowsStore()

const gridHeight = ref("")

const openWindow = (windowId) => {
    const payload = {
        windowState: "open",
        windowId: windowId
    }
    windowsStore.setWindowState(payload)
}

const openGithub = () => {
    window.open("https://github.com/DonChiaQE");
}

// Icons with an externalUrl are shortcuts that link out; all others open a window.
// An empty externalUrl means the link is not set yet, so nothing happens.
const activateIcon = (item) => {
    if (item.externalUrl !== undefined) {
        if (item.externalUrl) {
            window.open(item.externalUrl, "_blank", "noopener");
        }
        return
    }
    openWindow(item.windowId)
}


const getImagePath = (iconImage) => {
    const path = `../assets/win95Icons/${iconImage}`;
    const modules = import.meta.glob("../assets/win95Icons/*", { eager: true });
    const mod = modules[path]
    return mod.default;
};

onMounted(() => {
    let gridH = windowsStore.getFullscreenWindowHeight
    gridHeight.value = gridH.substring(0, gridH.length - 2) - 60 + "px"
})
</script>

<template>
    <nav class="grid-container" :style="{ height: gridHeight }">
    <li v-for="window in windowsStore.windows" :key="window.key">
      <button
        class="icon"
        v-if="window.showInAppGrid != false"
        @touchstart="activateIcon(window)"
        @dblclick="activateIcon(window)"
      >
      <img class="icon-image" :src=getImagePath(window.iconImage) :alt="window.altText" />
        <div class="border-box">
          <p class="icon-text">
            {{ window.displayName }}
          </p>
        </div>
      </button>
    </li>
  </nav>
</template>