---
layout: page
title: 朋友们
---

<script setup>
import {
  VPTeamPage,
  VPTeamPageTitle,
  VPTeamMembers
} from 'vitepress/theme'
import { h } from 'vue'

import friends, { webIcon } from './friends'

const members = [
    {
    name: '特菈',
    links: [
      {
        icon: "github",
        link: "https://github.com/Dustella"
      },{
      icon: webIcon,
      link: 'https://dustella.net',
    }],
    avatar: 'https://img-cdn.dustella.net/avtr.jpg',
    desc: '嘿嘿，这是我家某位',
  },
  ...friends.sort(()=> Math.random() - 0.5 )
]

const noScriptRender = { setup() { 
  return h("noscript",[ h(VPTeamMembers, { members }) ])
  } 
}
</script>

<VPTeamPage>
  <VPTeamPageTitle>
    <template #title>
      朋友们
    </template>
    <template #lead>
      欢迎扩列
    </template>
  </VPTeamPageTitle>

  <ClientOnly>
    <VPTeamMembers
      :members="members"
    />
  </ClientOnly>
</VPTeamPage>
