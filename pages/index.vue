<template>
<div class="bg-white">
  <div class="max-w-2xl mx-auto py-16 px-4 sm:py-24 sm:px-6 lg:max-w-7xl lg:px-8">
    <h2 class="text-2xl font-extrabold tracking-tight text-gray-900">Optimizing image loading using sprites</h2>

    <div class="mt-6 grid grid-cols-1 gap-y-10 gap-x-6 sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8">
      
      <div 
        v-for="(image,index) in images"
        :key="index"
        class="group relative"
      >
        <div class="w-full min-h-80 bg-gray-200 aspect-w-1 aspect-h-1 rounded-md overflow-hidden group-hover:opacity-75">
          <div :class="`${image.class} w-full h-full mx-auto`"></div>
        </div>
        <div class="mt-4 flex justify-between">
          <div>
            <h3 class="text-sm text-gray-700">
              <a :href="image.link" target="_blank">
                {{image.credit}}
              </a>
            </h3>
          </div>
        </div>
      </div>

    </div>
  </div>
</div>

</template>

<script>
export default {
  data(){
    return {
      images:[
        {
          class: 'cartoon',
          credit: 'Cartoon icons created by wanicon - Flaticon',
          link: 'https://www.flaticon.com/free-icons/cartoon'
        },
        {
          class: 'chick',
          credit: 'Cartoon icons created by surang - Flaticon',
          link: 'https://www.flaticon.com/free-icons/cartoon'
        },
        {
          class: 'comic_book',
          credit: 'Cartoon icons created by Freepik - Flaticon',
          link: 'https://www.flaticon.com/free-icons/cartoon'
        },
        {
          class: 'leonardo',
          credit: 'Cute icons created by Smashicons - Flaticon',
          link: 'https://www.flaticon.com/free-icons/cute'
        },
        {
          class: 'mushrooms',
          credit: 'Mushroom icons created by Rabbixcons - Flaticon',
          link: 'https://www.flaticon.com/free-icons/mushroom'
        },
      ]
    }
  }
}
</script>

<style>
.cartoon, .chick, .comic_book, .leonardo , .mushrooms {
  background: url('//res.cloudinary.com/hackit-africa/image/sprite/w_280,c_fit/nis-cartoons.png') no-repeat;
}
.cartoon { background-position: 0px 0px; width: 280px; height: 280px; }
.chick { background-position: 0px -280px; width: 280px; height: 280px; }
.comic_book { background-position: 0px -560px; width: 280px; height: 280px; }
.leonardo { background-position: 0px -840px; width: 280px; height: 280px; }
.mushrooms { background-position: 0px -1120px; width: 280px; height: 280px; }

</style>
