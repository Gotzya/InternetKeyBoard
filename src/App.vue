<template>
  <div class="container">
    <div class="keyboard">
      <div class="row">
        <button class="key" v-bind:class="{ active: keys['q'] }" @mousedown="activateKey('q')" @mouseup="deactivateKey('q')"></button>
        <button class="key" v-bind:class="{ active: keys['w'] }" @mousedown="activateKey('w')" @mouseup="deactivateKey('w')"></button>
        <button class="key" v-bind:class="{ active: keys['e'] }" @mousedown="activateKey('e')" @mouseup="deactivateKey('e')"></button>
        <button class="key" v-bind:class="{ active: keys['r'] }" @mousedown="activateKey('r')" @mouseup="deactivateKey('r')"></button>
        <button class="key" v-bind:class="{ active: keys['t'] }" @mousedown="activateKey('t')" @mouseup="deactivateKey('t')"></button>
        <button class="key" v-bind:class="{ active: keys['y'] }" @mousedown="activateKey('y')" @mouseup="deactivateKey('y')"></button>
        <button class="key" v-bind:class="{ active: keys['u'] }" @mousedown="activateKey('u')" @mouseup="deactivateKey('u')"></button>
        <button class="key" v-bind:class="{ active: keys['i'] }" @mousedown="activateKey('i')" @mouseup="deactivateKey('i')"></button>
        <button class="key" v-bind:class="{ active: keys['o'] }" @mousedown="activateKey('o')" @mouseup="deactivateKey('o')"></button>
        <button class="key" v-bind:class="{ active: keys['p'] }" @mousedown="activateKey('p')" @mouseup="deactivateKey('p')"></button>
        <button class="key" v-bind:class="{ active: keys['['] }" @mousedown="activateKey('[')" @mouseup="deactivateKey('[')"></button>
        <button class="key" v-bind:class="{ active: keys[']'] }" @mousedown="activateKey(']')" @mouseup="deactivateKey(']')"></button>
      </div>
      <div class="row">
        <button class="key" v-bind:class="{ active: keys['a'] }" @mousedown="activateKey('a')" @mouseup="deactivateKey('a')"></button>
        <button class="key" v-bind:class="{ active: keys['s'] }" @mousedown="activateKey('s')" @mouseup="deactivateKey('s')"></button>
        <button class="key" v-bind:class="{ active: keys['d'] }" @mousedown="activateKey('d')" @mouseup="deactivateKey('d')"></button>
        <button style = "color: rgb(190, 190, 190); bottom: 1px; center;" class="key" v-bind:class="{ active: keys['f'] }" @mousedown="activateKey('f')" @mouseup="deactivateKey('f')"></button>
        <button class="key" v-bind:class="{ active: keys['g'] }" @mousedown="activateKey('g')" @mouseup="deactivateKey('g')"></button>
        <button class="key" v-bind:class="{ active: keys['h'] }" @mousedown="activateKey('h')" @mouseup="deactivateKey('h')"></button>
        <button style = "color: rgb(190, 190, 190); bottom: 1px;" class="key" v-bind:class="{ active: keys['j'] }" @mousedown="activateKey('j')" @mouseup="deactivateKey('j')"></button>
        <button class="key" v-bind:class="{ active: keys['k'] }" @mousedown="activateKey('k')" @mouseup="deactivateKey('k')"></button>
        <button class="key" v-bind:class="{ active: keys['l'] }" @mousedown="activateKey('l')" @mouseup="deactivateKey('l')"></button>
        <button class="key" v-bind:class="{ active: keys[';'] }" @mousedown="activateKey(';')" @mouseup="deactivateKey(';')"></button>
        <button class="key" v-bind:class="{ active: keys['\''] }" @mousedown="activateKey('\'')" @mouseup="deactivateKey('\'')"></button>
      </div>
      <div class="row">
        <button class="key" v-bind:class="{ active: keys['z'] }" @mousedown="activateKey('z')" @mouseup="deactivateKey('z')"></button>
        <button class="key" v-bind:class="{ active: keys['x'] }" @mousedown="activateKey('x')" @mouseup="deactivateKey('x')"></button>
        <button class="key" v-bind:class="{ active: keys['c'] }" @mousedown="activateKey('c')" @mouseup="deactivateKey('c')"></button>
        <button class="key" v-bind:class="{ active: keys['v'] }" @mousedown="activateKey('v')" @mouseup="deactivateKey('v')"></button>
        <button class="key" v-bind:class="{ active: keys['b'] }" @mousedown="activateKey('b')" @mouseup="deactivateKey('b')"></button>
        <button class="key" v-bind:class="{ active: keys['n'] }" @mousedown="activateKey('n')" @mouseup="deactivateKey('n')"></button>
        <button class="key" v-bind:class="{ active: keys['m'] }" @mousedown="activateKey('m')" @mouseup="deactivateKey('m')"></button>
        <button class="key" v-bind:class="{ active: keys[','] }" @mousedown="activateKey(',')" @mouseup="deactivateKey(',')"></button>
        <button class="key" v-bind:class="{ active: keys['.'] }" @mousedown="activateKey('.')" @mouseup="deactivateKey('.')"></button>
        <button class="key" v-bind:class="{ active: keys['/'] }" @mousedown="activateKey('/')" @mouseup="deactivateKey('/')"></button>
      </div>
      <div class="space">
        <button style="width: 400px;" class="key" v-bind:class="{ active: keys[' '] }" @mousedown="activateKey(' ')" @mouseup="deactivateKey(' ')"></button>
      </div>
    </div>
  </div>
    <h1 style = "position: fixed; bottom: -1%; right: 0%; padding: 4px; font-size: 20px; color: rgb(100, 100, 100);">N.N.</h1>
</template>

<style>
.container {
  display: flex;
  align-items: center;
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.keyboard {
  display: flex;
  flex-direction: column;
  align-items: inherit;
}

.row {
  display: flex;
}

.key {
  display: flex;
  width: 50px;
  height: 50px;
  margin: 4px;
  border: 2px solid #333;
  color: #333;
  font-size: 18px;
  cursor: pointer;
  padding: 20px;
  font-size: 18px;
  border: none;
  background-color: #333;
  border-radius: 6px;
  color: rgb(190, 190, 190);
  animation: fadeOut 200ms;

}

@keyframes fadeIn {
  0% { background-color: #333; }
  100% { background-color: rgb(73, 73, 73); }
}

@keyframes fadeOut {
  0% { background-color: rgb(73, 73, 73); }
  100% { background-color: #333; }
}

.key.active {
  background-color: rgb(73, 73, 73);
  animation: fadeIn 30ms;
}
</style>

<script>

export default {
  name: 'App',
  data() {
    return {
      keys: {}
    }
  },
  mounted() {
    document.addEventListener('keydown', this.handleKeyDown)
    document.addEventListener('keyup', this.handleKeyUp)
  },
  beforeDestroy() {
    document.removeEventListener('keydown', this.handleKeyDown)
    document.removeEventListener('keyup', this.handleKeyUp)
  },
  methods: {
    activateKey(key) {
      this.keys[key] = true
    },
    deactivateKey(key) {
      this.keys[key] = false
    },
    handleKeyDown(event) {
      this.activateKey(event.key.toLowerCase())
    },
    handleKeyUp(event) {
      this.deactivateKey(event.key.toLowerCase())
    }
  }
}
</script>
