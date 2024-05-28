<script>
import NavBar from '@/components/NavBar.vue'
import Footer from '@/components/Footer.vue'

export default{
  components:{
    NavBar,
    Footer
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      const section = document.querySelector('.about');
      const nav = document.querySelector('.nav');

      if (section && nav) {
        if (window.scrollY >= section.offsetTop - 300) {
          nav.style.display = 'flex';
        } else {
          nav.style.display = 'none';
        }
      }
    }
  }
}

</script>

<template>
  <div class="page">
    <NavBar class="nav" />
  <img class="image" src="@/assets/download.png">
  <main>
    <div class="home">
      <img data-aos="fade-down" data-aos-duration="2000" src="data:image/png;base64,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">
      <h1 data-aos="fade-down" data-aos-duration="2000">Hl <span>Services</span></h1>
      <a data-aos="fade-down" data-aos-duration="2000" class="btn">JOIN SERVER</a>
    </div>
    <div class="about" id="about">
      <div class="cont">
        <div class="left" data-aos="fade-right" data-aos-duration="2000">
          <h1 class="start">Server Idea</h1>
          <h3>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae eum architecto voluptatum magnam vel tempora saepe doloremque et, doloribus aliquid autem quia in, perspiciatis id sit optio a ad voluptas.</h3>
          <a class="btn">See More</a>
        </div>
        <div class="right" data-aos="fade-right" data-aos-duration="2000">
          

          <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="303.71" height="525.42" viewBox="0 0 303.71 525.42"><path d="m42.49,524.23c0,.66.53,1.19,1.19,1.19h258.84c.66,0,1.19-.53,1.19-1.19s-.53-1.19-1.19-1.19H43.68c-.66,0-1.19.53-1.19,1.19Z" fill="#484565"/><path d="m178.61.33s-21.91-5.31-35.17,26.77c-11.05,26.74-18.89,41.02-9.92,50.72,3.21,3.47,7.79,5.34,12.51,5.5l50.5,1.66s18.54-48.62,7.27-66.2C192.53,1.19,178.61.33,178.61.33Z" fill="#2f2e41"/><polygon points="189.07 80.94 164.78 88.93 164.78 53.96 186.82 53.96 189.07 80.94" fill="#f6a6a9"/><polygon points="170.43 504.69 147.67 504.69 134.48 383.11 169.65 383.11 170.43 504.69" fill="#f6a6a9"/><path d="m125.51,524.23c-2.39,0-4.52-.06-6.13-.21-6.05-.55-11.81-5.01-14.71-7.62-1.3-1.17-1.72-3.04-1.04-4.65h0c.49-1.16,1.46-2.02,2.66-2.36l15.97-4.56,25.86-17.45.29.52c.11.19,2.65,4.77,3.5,7.86.32,1.18.24,2.16-.25,2.91-.34.53-.81.83-1.2,1,.47.49,1.94,1.48,6.45,2.2,6.6,1.05,7.98-5.79,8.04-6.08l.04-.23.2-.13c3.14-2.02,5.07-2.94,5.74-2.75.42.12,1.11.33,2.98,18.95.19.58,1.5,4.87.61,8.96-.97,4.46-20.44,2.92-24.34,2.57-.11.01-14.69,1.05-24.68,1.05v.02h.01Z" fill="#2f2e41"/><polygon points="221.83 504.69 199.08 504.69 185.88 383.11 221.05 383.11 221.83 504.69" fill="#f6a6a9"/><path d="m176.92,524.23c-2.39,0-4.52-.06-6.13-.21-6.05-.55-11.81-5.01-14.71-7.62-1.3-1.17-1.72-3.04-1.04-4.65h0c.49-1.16,1.46-2.02,2.66-2.36l15.97-4.56,25.86-17.45.29.52c.11.19,2.65,4.77,3.5,7.86.32,1.18.24,2.16-.25,2.91-.34.53-.81.83-1.2,1,.47.49,1.94,1.48,6.45,2.2,6.6,1.05,7.98-5.79,8.04-6.08l.04-.23.2-.13c3.14-2.02,5.07-2.94,5.74-2.75.42.12,1.11.33,2.98,18.95.19.58,1.5,4.87.61,8.96-.97,4.46-20.44,2.92-24.34,2.57-.11.01-14.69,1.05-24.68,1.05v.02h.01Z" fill="#2f2e41"/><polygon points="228.38 206.07 117.82 206.07 157.56 75.28 201.64 75.28 228.38 206.07" fill="#dddedf"/><path id="uuid-91f12725-4651-4192-855e-1b1e45ba96a1-112-46-91-103-33" d="m114.81,279.46c-1.32,8.01-6.66,13.76-11.93,12.83-5.27-.93-8.48-8.17-7.16-16.18.48-3.21,1.75-6.24,3.7-8.85l6.02-33.87,16.39,3.43-7.68,33.02c1.01,3.12,1.24,6.42.67,9.62h0s0,0,0,0Z" fill="#f6a6a9"/><path d="m164.52,75.3s-27.46-.72-30.35,6.5c-2.89,7.23-36.85,179.21-36.85,179.21h22.4s44.8-185.71,44.8-185.71Z" fill="#dddedf"/><circle cx="170.35" cy="38.01" r="24.21" fill="#f6a6a9"/><path d="m174.15,8.32s-31.08,46.23-25.85,75.07l-18.08-11.33s12.73-58.38,31.7-62.91l12.23-.84h0s0,.01,0,.01Z" fill="#2f2e41"/><path d="m205.4,206.07h-72.55l-39.7,162.93c-.73,6.88,3.63,13.3,10.32,15.09,21.78,5.83,74.04,14.1,153.15-8.92,7.61-2.21,11.93-10.24,9.54-17.8l-60.76-151.29h0s0-.01,0-.01Z" fill="#2f2e41"/><path d="m107.55,98.48l-.5-.5-.5.5c-24.33-24.31-63.76-24.28-88.07.05-24.31,24.34-24.8,64.26-.47,88.57h0l89.1,89.01,89.04-89.12h0c24.31-24.34,23.8-64.26-.52-88.57-24.33-24.31-63.76-24.28-88.07.05h0s0,0,0,0Z" fill="#8e82ff"/><path d="m173.35,87.52l20.1-10.31c9.19-3.4,19.44-2.26,27.66,3.09,25,16.26,74.28,52.11,53.1,69.83-27.91,23.36-65.64-18.07-65.64-18.07l-35.22-44.54h0Z" fill="#dddedf"/><path id="uuid-8411e106-0120-401a-9ba4-6dca08ef376d-113-47-92-104-34" d="m172.91,105.14c-6.99-4.12-10.42-11.18-7.65-15.77,2.77-4.58,10.68-4.95,17.68-.83,2.82,1.61,5.19,3.89,6.91,6.65l29.4,17.86-9.12,14.04-28.02-19.1c-3.28-.19-6.44-1.17-9.21-2.86h.01Z" fill="#f6a6a9"/><polygon points="192.89 121.33 201.25 101.36 242.1 114.88 223.83 145.29 192.89 121.33" fill="#dddedf"/></svg>        </div>
      </div>
      <div class="cont" id="c1">
        <div class="left" data-aos="fade-left" data-aos-duration="2000">
          <h1 class="start" data-aos="fade-right">Server Idea</h1>
          <h3 data-aos="fade-right">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas, perferendis nulla at accusantium veniam dignissimos laudantium eius quam, unde praesentium enim nam perspiciatis molestias? Facere quis laborum itaque fuga perferendis?</h3>
          <a class="btn">See More</a>
        </div>
        <div class="right" data-aos="fade-right" data-aos-duration="2000">
          

          <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="303.71" height="525.42" viewBox="0 0 303.71 525.42"><path d="m42.49,524.23c0,.66.53,1.19,1.19,1.19h258.84c.66,0,1.19-.53,1.19-1.19s-.53-1.19-1.19-1.19H43.68c-.66,0-1.19.53-1.19,1.19Z" fill="#484565"/><path d="m178.61.33s-21.91-5.31-35.17,26.77c-11.05,26.74-18.89,41.02-9.92,50.72,3.21,3.47,7.79,5.34,12.51,5.5l50.5,1.66s18.54-48.62,7.27-66.2C192.53,1.19,178.61.33,178.61.33Z" fill="#2f2e41"/><polygon points="189.07 80.94 164.78 88.93 164.78 53.96 186.82 53.96 189.07 80.94" fill="#f6a6a9"/><polygon points="170.43 504.69 147.67 504.69 134.48 383.11 169.65 383.11 170.43 504.69" fill="#f6a6a9"/><path d="m125.51,524.23c-2.39,0-4.52-.06-6.13-.21-6.05-.55-11.81-5.01-14.71-7.62-1.3-1.17-1.72-3.04-1.04-4.65h0c.49-1.16,1.46-2.02,2.66-2.36l15.97-4.56,25.86-17.45.29.52c.11.19,2.65,4.77,3.5,7.86.32,1.18.24,2.16-.25,2.91-.34.53-.81.83-1.2,1,.47.49,1.94,1.48,6.45,2.2,6.6,1.05,7.98-5.79,8.04-6.08l.04-.23.2-.13c3.14-2.02,5.07-2.94,5.74-2.75.42.12,1.11.33,2.98,18.95.19.58,1.5,4.87.61,8.96-.97,4.46-20.44,2.92-24.34,2.57-.11.01-14.69,1.05-24.68,1.05v.02h.01Z" fill="#2f2e41"/><polygon points="221.83 504.69 199.08 504.69 185.88 383.11 221.05 383.11 221.83 504.69" fill="#f6a6a9"/><path d="m176.92,524.23c-2.39,0-4.52-.06-6.13-.21-6.05-.55-11.81-5.01-14.71-7.62-1.3-1.17-1.72-3.04-1.04-4.65h0c.49-1.16,1.46-2.02,2.66-2.36l15.97-4.56,25.86-17.45.29.52c.11.19,2.65,4.77,3.5,7.86.32,1.18.24,2.16-.25,2.91-.34.53-.81.83-1.2,1,.47.49,1.94,1.48,6.45,2.2,6.6,1.05,7.98-5.79,8.04-6.08l.04-.23.2-.13c3.14-2.02,5.07-2.94,5.74-2.75.42.12,1.11.33,2.98,18.95.19.58,1.5,4.87.61,8.96-.97,4.46-20.44,2.92-24.34,2.57-.11.01-14.69,1.05-24.68,1.05v.02h.01Z" fill="#2f2e41"/><polygon points="228.38 206.07 117.82 206.07 157.56 75.28 201.64 75.28 228.38 206.07" fill="#dddedf"/><path id="uuid-91f12725-4651-4192-855e-1b1e45ba96a1-112-46-91-103-33" d="m114.81,279.46c-1.32,8.01-6.66,13.76-11.93,12.83-5.27-.93-8.48-8.17-7.16-16.18.48-3.21,1.75-6.24,3.7-8.85l6.02-33.87,16.39,3.43-7.68,33.02c1.01,3.12,1.24,6.42.67,9.62h0s0,0,0,0Z" fill="#f6a6a9"/><path d="m164.52,75.3s-27.46-.72-30.35,6.5c-2.89,7.23-36.85,179.21-36.85,179.21h22.4s44.8-185.71,44.8-185.71Z" fill="#dddedf"/><circle cx="170.35" cy="38.01" r="24.21" fill="#f6a6a9"/><path d="m174.15,8.32s-31.08,46.23-25.85,75.07l-18.08-11.33s12.73-58.38,31.7-62.91l12.23-.84h0s0,.01,0,.01Z" fill="#2f2e41"/><path d="m205.4,206.07h-72.55l-39.7,162.93c-.73,6.88,3.63,13.3,10.32,15.09,21.78,5.83,74.04,14.1,153.15-8.92,7.61-2.21,11.93-10.24,9.54-17.8l-60.76-151.29h0s0-.01,0-.01Z" fill="#2f2e41"/><path d="m107.55,98.48l-.5-.5-.5.5c-24.33-24.31-63.76-24.28-88.07.05-24.31,24.34-24.8,64.26-.47,88.57h0l89.1,89.01,89.04-89.12h0c24.31-24.34,23.8-64.26-.52-88.57-24.33-24.31-63.76-24.28-88.07.05h0s0,0,0,0Z" fill="#8e82ff"/><path d="m173.35,87.52l20.1-10.31c9.19-3.4,19.44-2.26,27.66,3.09,25,16.26,74.28,52.11,53.1,69.83-27.91,23.36-65.64-18.07-65.64-18.07l-35.22-44.54h0Z" fill="#dddedf"/><path id="uuid-8411e106-0120-401a-9ba4-6dca08ef376d-113-47-92-104-34" d="m172.91,105.14c-6.99-4.12-10.42-11.18-7.65-15.77,2.77-4.58,10.68-4.95,17.68-.83,2.82,1.61,5.19,3.89,6.91,6.65l29.4,17.86-9.12,14.04-28.02-19.1c-3.28-.19-6.44-1.17-9.21-2.86h.01Z" fill="#f6a6a9"/><polygon points="192.89 121.33 201.25 101.36 242.1 114.88 223.83 145.29 192.89 121.33" fill="#dddedf"/></svg>        </div>
      </div>
      <div class="cont">
        <div class="left" data-aos="fade-right" data-aos-duration="2000">
          <h1 class="start">Server Idea</h1>
          <h3>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Tempore ad tempora perferendis? Dolorum magnam eos pariatur rerum saepe doloremque cum voluptate nisi. Tenetur ad corrupti quae quibusdam quis alias eveniet!</h3>
          <a class="btn">See More</a>
        </div>
        <div class="right" data-aos="fade-left" data-aos-duration="2000">
          

          <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="303.71" height="525.42" viewBox="0 0 303.71 525.42"><path d="m42.49,524.23c0,.66.53,1.19,1.19,1.19h258.84c.66,0,1.19-.53,1.19-1.19s-.53-1.19-1.19-1.19H43.68c-.66,0-1.19.53-1.19,1.19Z" fill="#484565"/><path d="m178.61.33s-21.91-5.31-35.17,26.77c-11.05,26.74-18.89,41.02-9.92,50.72,3.21,3.47,7.79,5.34,12.51,5.5l50.5,1.66s18.54-48.62,7.27-66.2C192.53,1.19,178.61.33,178.61.33Z" fill="#2f2e41"/><polygon points="189.07 80.94 164.78 88.93 164.78 53.96 186.82 53.96 189.07 80.94" fill="#f6a6a9"/><polygon points="170.43 504.69 147.67 504.69 134.48 383.11 169.65 383.11 170.43 504.69" fill="#f6a6a9"/><path d="m125.51,524.23c-2.39,0-4.52-.06-6.13-.21-6.05-.55-11.81-5.01-14.71-7.62-1.3-1.17-1.72-3.04-1.04-4.65h0c.49-1.16,1.46-2.02,2.66-2.36l15.97-4.56,25.86-17.45.29.52c.11.19,2.65,4.77,3.5,7.86.32,1.18.24,2.16-.25,2.91-.34.53-.81.83-1.2,1,.47.49,1.94,1.48,6.45,2.2,6.6,1.05,7.98-5.79,8.04-6.08l.04-.23.2-.13c3.14-2.02,5.07-2.94,5.74-2.75.42.12,1.11.33,2.98,18.95.19.58,1.5,4.87.61,8.96-.97,4.46-20.44,2.92-24.34,2.57-.11.01-14.69,1.05-24.68,1.05v.02h.01Z" fill="#2f2e41"/><polygon points="221.83 504.69 199.08 504.69 185.88 383.11 221.05 383.11 221.83 504.69" fill="#f6a6a9"/><path d="m176.92,524.23c-2.39,0-4.52-.06-6.13-.21-6.05-.55-11.81-5.01-14.71-7.62-1.3-1.17-1.72-3.04-1.04-4.65h0c.49-1.16,1.46-2.02,2.66-2.36l15.97-4.56,25.86-17.45.29.52c.11.19,2.65,4.77,3.5,7.86.32,1.18.24,2.16-.25,2.91-.34.53-.81.83-1.2,1,.47.49,1.94,1.48,6.45,2.2,6.6,1.05,7.98-5.79,8.04-6.08l.04-.23.2-.13c3.14-2.02,5.07-2.94,5.74-2.75.42.12,1.11.33,2.98,18.95.19.58,1.5,4.87.61,8.96-.97,4.46-20.44,2.92-24.34,2.57-.11.01-14.69,1.05-24.68,1.05v.02h.01Z" fill="#2f2e41"/><polygon points="228.38 206.07 117.82 206.07 157.56 75.28 201.64 75.28 228.38 206.07" fill="#dddedf"/><path id="uuid-91f12725-4651-4192-855e-1b1e45ba96a1-112-46-91-103-33" d="m114.81,279.46c-1.32,8.01-6.66,13.76-11.93,12.83-5.27-.93-8.48-8.17-7.16-16.18.48-3.21,1.75-6.24,3.7-8.85l6.02-33.87,16.39,3.43-7.68,33.02c1.01,3.12,1.24,6.42.67,9.62h0s0,0,0,0Z" fill="#f6a6a9"/><path d="m164.52,75.3s-27.46-.72-30.35,6.5c-2.89,7.23-36.85,179.21-36.85,179.21h22.4s44.8-185.71,44.8-185.71Z" fill="#dddedf"/><circle cx="170.35" cy="38.01" r="24.21" fill="#f6a6a9"/><path d="m174.15,8.32s-31.08,46.23-25.85,75.07l-18.08-11.33s12.73-58.38,31.7-62.91l12.23-.84h0s0,.01,0,.01Z" fill="#2f2e41"/><path d="m205.4,206.07h-72.55l-39.7,162.93c-.73,6.88,3.63,13.3,10.32,15.09,21.78,5.83,74.04,14.1,153.15-8.92,7.61-2.21,11.93-10.24,9.54-17.8l-60.76-151.29h0s0-.01,0-.01Z" fill="#2f2e41"/><path d="m107.55,98.48l-.5-.5-.5.5c-24.33-24.31-63.76-24.28-88.07.05-24.31,24.34-24.8,64.26-.47,88.57h0l89.1,89.01,89.04-89.12h0c24.31-24.34,23.8-64.26-.52-88.57-24.33-24.31-63.76-24.28-88.07.05h0s0,0,0,0Z" fill="#8e82ff"/><path d="m173.35,87.52l20.1-10.31c9.19-3.4,19.44-2.26,27.66,3.09,25,16.26,74.28,52.11,53.1,69.83-27.91,23.36-65.64-18.07-65.64-18.07l-35.22-44.54h0Z" fill="#dddedf"/><path id="uuid-8411e106-0120-401a-9ba4-6dca08ef376d-113-47-92-104-34" d="m172.91,105.14c-6.99-4.12-10.42-11.18-7.65-15.77,2.77-4.58,10.68-4.95,17.68-.83,2.82,1.61,5.19,3.89,6.91,6.65l29.4,17.86-9.12,14.04-28.02-19.1c-3.28-.19-6.44-1.17-9.21-2.86h.01Z" fill="#f6a6a9"/><polygon points="192.89 121.33 201.25 101.36 242.1 114.88 223.83 145.29 192.89 121.33" fill="#dddedf"/></svg>        </div>
      </div>
    </div>
    <div class="feedbacks">
      <h1>Feedbacks</h1>
      <div class="cont">
        <div data-aos="fade-right" data-aos-duration="1500" class="cont1">
                    <div class="top">
                        <div class="left">
                            <img src="https://cdn.discordapp.com/avatars/1156271094894968902/5f766c95df9f7d6ee1410518f1208e3f.png?size=1024" alt="lamsa feedbacks">
                        <p>kg.r</p>
                        </div>
                        <div class="right">
                            <p>✨✨✨✨✨</p>
                        </div>
                    </div>
                    <h3>يبوي اقسم بالله فنان و تصاميم جامده و فرعون القوه مواقع توب توب</h3>
                    </div>
                    <div data-aos="fade-right" data-aos-duration="1500" class="cont1">
                    <div class="top">
                        <div class="left">
                            <img src="https://cdn.discordapp.com/avatars/1156271094894968902/5f766c95df9f7d6ee1410518f1208e3f.png?size=1024" alt="lamsa feedbacks">
                        <p>naseer1319</p>
                        </div>
                        <div class="right">
                            <p>✨✨✨✨✨</p>
                        </div>
                    </div>
                    <h3>فنااااااان ماشاء الله مواقعه مرة قوية والجودة عالية مرة انصحكم فيه بدون تفكير</h3>
                    </div>
                    <div data-aos="fade-right" data-aos-duration="1500" class="cont1">
                    <div class="top">
                        <div class="left">
                            <img src="https://cdn.discordapp.com/avatars/1156271094894968902/5f766c95df9f7d6ee1410518f1208e3f.png?size=1024" alt="lamsa feedbacks">
                        <p>3we6</p>
                        </div>
                        <div class="right">
                            <p>✨✨✨✨✨</p>
                        </div>
                    </div>
                    <h3>ما عندي شي اقولوا غير انهم ملوك البرمجة</h3>
                    </div>
      </div>
    </div>
    <div class="developers" id="developers">
    <h1 class="frist">Our <span> Team</span></h1>
    <div class="dev-card" data-aos="fade-left">
      <img style="width:200px;" src="https://cdn.discordapp.com/avatars/1156271094894968902/5f766c95df9f7d6ee1410518f1208e3f.png?size=1024" alt="developer-profile">
      <div class="right">
        <h2>Fr3oN</h2>
        <h3>Html, Css, Js, VueJs, Vuex, JSON, Api, NodeJs, ExpressJs</h3>
        <h4>HL Services <span> ,Coder</span></h4>
      </div>
      <a class="btn">My Portfolio</a>
    </div>
    <div class="dev-card" data-aos="fade-up">
      <img style="width:200px;" src="https://cdn.discordapp.com/avatars/1156271094894968902/5f766c95df9f7d6ee1410518f1208e3f.png?size=1024" alt="developer-profile">
      <div class="right">
        <h2>Fr3oN</h2>
        <h3>Html, Css, Js, VueJs, Vuex, JSON, Api, NodeJs, ExpressJs</h3>
        <h4>HL Services <span> ,Coder</span></h4>
      </div>
      <a class="btn">My Portfolio</a>
    </div>
    <div class="dev-card" data-aos="fade-right">
      <img style="width:200px;" src="https://cdn.discordapp.com/avatars/1156271094894968902/5f766c95df9f7d6ee1410518f1208e3f.png?size=1024" alt="developer-profile">
      <div class="right">
        <h2>Fr3oN</h2>
        <h3>Html, Css, Js, VueJs, Vuex, JSON, Api, NodeJs, ExpressJs</h3>
        <h4>HL Services <span> ,Coder</span></h4>
      </div>
      <a class="btn">My Portfolio</a>
    </div>
  </div>
  </main>
  <Footer />
  </div>
</template>

<style scoped>
.feedbacks{
  margin-top:100px;
  width:100%;
  display:flex;
  flex-direction:column;
  align-items:center;
}

.feedbacks h1,.developers h1{
  color:var(--text);
  font-size:50px;
}

.page{
  overflow:hidden;
}

.nav{
  display:none;
}

.image{
  position:fixed;
  top:18%;
  left:18%;
}

main{
  position:relative;
  width:100%;
  min-height:100vh; 
}

.home{
  width:100%;
  display:flex;
  justify-content:center;
  align-items:center;
  flex-direction:column;
  gap:20px;
}

.about{
  width:100%;
  margin-top:250px;
}

.feedbacks .cont{
  margin-top:100px;
  width:100%;
  display:flex;
  flex-direction:row;
  gap:80px;
  justify-content:center;
  flex-wrap:wrap;
}

.about .cont{
  display:flex;
  justify-content:center;
  align-items:center;
  gap:20%;
  padding:100px 0;
}

.cont .left{
  width:30%;
  text-align:start;
  display:flex;
  align-items:start;
  flex-direction:column;
  gap:20px;
}

.cont .right{
  width:40%;
}

.about .right svg{
  width:500px;
  margin-left:100px;
}

.home img{
  width:25%;
  margin-top:200px;
  border-radius:25%;
}

.home h1{
  color:white;
  letter-spacing:6px;
  text-transform:uppercase;
}

.left h1{
  color:white;
  letter-spacing:6px;
  text-transform:uppercase;
  position:relative;
}

.left h1::before{
  content:'';
  width:10px;
  height:40px;
  background-color:var(--text);
  position:absolute;
  left:-10%;
}

.home h1 span{
  color:var(--text);
}

.left h3{
  color:var(--text);
}

.btn{
  padding:10px 30px;
  background-color:var(--text);
  border-radius:25px;
  cursor:pointer;
  color:black;
}

.home .icon{
  color:white;
  font-size:40px;
  margin-top:50px;
  animation: moveUp 2s ease-in-out infinite;
}

@keyframes moveUp{
  0% {
    transform: translateY(30px);
  }
  50% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(30px);
  }
}

#c1{
  display:flex;
  flex-direction:row-reverse;
}

.cont1{
    border-radius:8px;
    background-color:#17152b;
    width:400px;
    padding:5px 10px;
    height:250px;
    display:flex;
    flex-direction:column;
    border-top:4px solid var(--primary);
    border-bottom:4px solid var(--primary);
    color:var(--text);
}

.top{
    margin-top:15px;
    display:flex;
    justify-content:space-around;
    align-items:center;
}

.left{
    display:flex;
    justify-content:space-around;
    align-items:center;
}

.top img{
    width:40px;
    margin-right:10px;
    border-radius:50%;
}

.cont1 h3{
    text-align:end;
    margin-top:60px;
    padding:5px 5px;
}

.developers{
  margin-top:200px;
  overflow:hidden;
  width:100%;
  display:flex;
  flex-direction:column;
  flex-wrap:wrap;
  justify-content:space-around;
  align-items:center;
}

.developers .dev-card{
  width:80%;
  display:flex;
  flex-direction:row;
  flex-wrap:wrap;
  justify-content:space-around;
  align-items:center;
  border-radius:8px;
  padding:15px 20px;
  background-color:#17152b;
  border-top:4px solid var(--primary);
  border-bottom:4px solid var(--primary);
  margin:4% 0;
}

.developers .dev-card .right{
  text-align:start;
}

.developers .dev-card h1{
  font-size:30px;
}

.dev-card img{
  border-radius:50%;
}

.dev-card h2{
  color:var(--text);
  font-size:30px;
}

.dev-card h3,.dev-card h4{
  color:var(--text);
  background-color:var(--background);
  padding:10px 20px;
  border-radius:8px;
  margin:10px 0;
}

@media (max-width:768px) {
  .dev-card{
    gap:30px;
  }

  .about .cont,.about #c1{
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
  }

  .about .cont .right,.about .cont .left,.about #c1 .right,.about .cont .left{
    width:90%;
  }

  .about .cont .left,.about #c1 .left{
    margin-left:30px;
  }

  .about .cont .right svg,.about #c1 .right svg{
    width:600px;
    margin-left:-100px;
    margin-top:80px;
  }

  .home img{
    width:600px;
  }
}
</style>
