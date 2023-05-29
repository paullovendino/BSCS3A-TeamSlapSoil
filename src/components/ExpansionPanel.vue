<template>
  <div class="expansion-panel">
    <div class="panel-header" @click="togglePanel">
      <span class="title">{{ title }}</span>
      <span class="arrow-icon">{{ expanded ? '▼' : '►' }}</span>
    </div>
    <transition name="panel-transition">
      <div v-show="expanded" class="panel-content">
        <slot></slot>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  data() {
    return {
      expanded: false
    };
  },
  props: {
    title: {
      type: String,
      required: true
    }
  },
  methods: {
    togglePanel() {
      this.expanded = !this.expanded;
    }
  }
};
</script>

<style scoped>
.expansion-panel {
  border: 1px solid #ccc;
  border-radius: 4px;
  margin-bottom: 10px;
  min-width: 750px;
}

.panel-header {
  display: flex;
  align-items: center;
  padding: 10px;
  background-color: #f0f0f0;
  cursor: pointer;
}

.title {
  flex-grow: 1;
  font-weight: bold;
  color: black;
}

.arrow-icon {
  font-size: 14px;
  transition: transform 0.3s;
  color: black;
  width: 20px;
}

.panel-content {
  padding: 10px;
  border-top: 1px solid black;
  color: black;
  background: white;
}
.panel-content:hover{
    background: black;
    transition: ease .5s;
}

.panel-transition-enter-active,
.panel-transition-leave-active {
  transition: height 0.3s ease;
}

.panel-transition-enter,
.panel-transition-leave-to {
  height: 0;
  overflow: hidden;
}
</style>