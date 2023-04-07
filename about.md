---
# https://vitepress.dev/reference/default-theme-home-page
layout: doc
nocomment: true
title: ""
---

<script setup>
import { onMounted, ref } from 'vue'

const isFromBeiyanyunyi = ref(false)
onMounted(()=>{
    const { referrer } = document
    isFromBeiyanyunyi.value = referrer.search("penclub.club") !== -1 ||  referrer.search("beiyanyunyi.github.io") !== -1
})
</script>

这里是马良姐姐
---


