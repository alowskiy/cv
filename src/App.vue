<script>
export default {
  data(){
    return{
main: 'content',
introd: 'cl_intro',
intro: 'Hello, i am Nikita. Frontend developer. Im looking for job, freelance. My portfolio here. Here is not full list ',
href: '/src/assets/images.jpg',
img:'img',
skills: ['JavaScript', 'Figma','Git', 'Html', 'CSS', 'Vue 3'],
Educ: ['HtmlAcademy', 'Mentoring by Dmitry Trepachev' ,'Youtube','Other computer science courses'],
lg: ['Russian-native', 'English-B1'],
name: 'cl_name',
IsVis: false,
links: ['https://alowskiy.github.io/plants/', 'https://alowskiy.github.io/library/', 'https://alowskiy.github.io/shelter/'],
port: ['Plants', 'Library', 'Shelter'],
pf: 'cl_pf',
lins: 'cl_link',
cnt: ['Telegram', 'Mail'],
cnts: ['https://t.me/alowski', 'mailto:alowskiynikita@gmail.com'],
c_l:'cont_l',
cont:'in_bl'


    }
  }
}

</script>

<template>
  <div :class="main">
     <div :class="img"></div>
     <h1 :class="name">Nikita Alows</h1>
    <div :class="introd">
      <p>{{ intro }}</p>
   
      <div :class="cont">
        <div :class="pf">
       
       <a v-for="(web,index) in port" :href="links[index]" :class="lins">{{web + ' '}}</a>
       </div>
       <div :class="c_l">
      <a  :class="lins" v-for="(lin, i) in cnt" :href="cnts[i]">{{ lin }}<br></a>
      </div>
      </div>
      
    
    </div>
   <div>
    <h3 >Skills</h3>
    <ul>
      <li v-for="skill in skills">{{ skill }}</li>
    </ul>
   </div>
     <div>
    <h3 >Education</h3>
    <ul>
      <li v-for="edu in Educ">{{ edu }}</li>
    </ul>
   </div>
      <div>
    <h3 >Languages</h3>
    <ul>
      <li v-for="lan in lg">{{ lan }}</li>
    </ul>
   </div>
<div>


</div>
  </div>

</template>
<style>

  @import url('https://fonts.googleapis.com/css2?family=Varela+Round&display=swap');
</style>

<style>
body{
  margin: 0;
  padding: 0;
  padding-bottom: 10px;
  padding-top: 10px;
  font-family: 'Varela Round', sans-serif;
  background: #000;
}
.content{
  
  width: 99%;
  max-width: 1440px ;
  height: 95vh;
  margin-left: auto;
  margin-right: auto;
  display: grid;
    grid-template-columns: 25% 28% 28%  1fr ;
    padding-top: 10px;
    padding-left: 10px;
     background: linear-gradient(149deg, rgba(24,187,156,1) 0%, rgba(106,57,175,1) 42%, rgba(187,24,148,1) 72%, rgba(115,53,134,1) 100%);
    animation: gradient 25s infinite linear;
    background-size: 400%;
    color: rgb(241, 243, 245);
    
    
}
.img{
  background: url(/src/images.jpg);
  background-repeat: no-repeat;
  max-width:220px;
  min-height: 150px;
}
ul{
  list-style: none;
  width: fit-content;
    margin-left: auto;
  padding: 0;
  margin-right: auto;
}
.cl_intro{
  grid-column: 1/1;
}

.cl_name{
  margin-top: auto;
  margin-bottom: auto;
}
h3{
  font-size: 22px;
  width: fit-content;
  letter-spacing: 7px;
  margin-left: auto;
  margin-right: auto;
}
li{
 letter-spacing: 5px;
}
@keyframes gradient {
    0% {
        background-position: 80% 0%;
    }
    10% {
        background-position: 20% 100%;
    }
    50% {
        background-position: 50% 0%;
    }
    100% {
        background-position: 80% 0%;
    }
}
@media (max-width:1028px) {
  body{
overflow-x: hidden;
  }
  .content{
    font-size: 13px !important;
   
    
  }
  h3{
     font-size: 13px !important;
     letter-spacing: 3px;
  }
}
@media (max-width:708px) {
 body{
  padding: 0;
 }
  .content{
    display: flex;
    flex-direction: column;
    align-items: center;
      height: fit-content;
      padding: 0;
  }
  h1{
    margin: 0 !important;
  }
  .img{
 
    height: 260px;
    width: 240px;
    border-radius: 10px;
   
  }
  .cl_intro{
    width: 55%;
  }

}
.cl_pf{
 width: 55px;
}
.cl_link{
  color: wheat;
  text-decoration: none;
}

h1{
  letter-spacing: 10px;
}
.cont_l{
  width: 100px;


}
.in_bl{
  display: flex;
  gap: 50%;
}
</style>
