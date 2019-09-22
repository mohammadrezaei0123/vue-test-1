<template>

</template>

<script>
export default {
    mounted(){
        window.addEventListener('resize',this.resize)
    },
    beforeDestroy(){
        
    },
    methods:{
        resize () {
            console.log('object')
        let windowW=window.innerWidth
        const baseSize=1140
        let baseP=18
        if(baseSize-200<windowW){
            baseP=14
        document.querySelectorAll('p').forEach(v=>v.style.fontSize=baseP+"px")
        document.querySelectorAll('div').forEach(v=>v.style.fontSize=baseP+"px")
        document.querySelectorAll('button').forEach(v=>v.style.fontSize=baseP+"px")
        
        document.querySelectorAll('h6').forEach(v=>v.style.fontSize=(baseP+1)+"px")
        document.querySelectorAll('h5').forEach(v=>v.style.fontSize=(baseP+2)+"px")
        document.querySelectorAll('h4').forEach(v=>v.style.fontSize=(baseP+3)+"px")
        document.querySelectorAll('h3').forEach(v=>v.style.fontSize=(baseP+4)+"px")
        document.querySelectorAll('h2').forEach(v=>v.style.fontSize=(baseP+5)+"px")
        document.querySelectorAll('h1').forEach(v=>v.style.fontSize=(baseP+6)+"px")
        }else if(baseSize-300<windowW){
            baseP=13
        document.querySelectorAll('p').forEach(v=>v.style.fontSize=baseP+"px")
        document.querySelectorAll('div').forEach(v=>v.style.fontSize=baseP+"px")
        document.querySelectorAll('button').forEach(v=>v.style.fontSize=baseP+"px")
        
        document.querySelectorAll('h6').forEach(v=>v.style.fontSize=(baseP+1)+"px")
        document.querySelectorAll('h5').forEach(v=>v.style.fontSize=(baseP+2)+"px")
        document.querySelectorAll('h4').forEach(v=>v.style.fontSize=(baseP+3)+"px")
        document.querySelectorAll('h3').forEach(v=>v.style.fontSize=(baseP+4)+"px")
        document.querySelectorAll('h2').forEach(v=>v.style.fontSize=(baseP+5)+"px")
        document.querySelectorAll('h1').forEach(v=>v.style.fontSize=(baseP+6)+"px")
        }else if(baseSize-400<windowW){
            baseP=12
        document.querySelectorAll('p').forEach(v=>v.style.fontSize=baseP+"px")
        document.querySelectorAll('div').forEach(v=>v.style.fontSize=baseP+"px")
        document.querySelectorAll('button').forEach(v=>v.style.fontSize=baseP+"px")
        
        document.querySelectorAll('h6').forEach(v=>v.style.fontSize=(baseP+1)+"px")
        document.querySelectorAll('h5').forEach(v=>v.style.fontSize=(baseP+2)+"px")
        document.querySelectorAll('h4').forEach(v=>v.style.fontSize=(baseP+3)+"px")
        document.querySelectorAll('h3').forEach(v=>v.style.fontSize=(baseP+4)+"px")
        document.querySelectorAll('h2').forEach(v=>v.style.fontSize=(baseP+5)+"px")
        document.querySelectorAll('h1').forEach(v=>v.style.fontSize=(baseP+6)+"px")
        }
        }
    }
};
</script>

// <style lang="scss">
//     *{
//         // font-size: 24px;
//         color: rgb(5, 90, 10);
//     }
    
//     h1{

// font-size: 19px;
//     }
//     h2{

// font-size: 18px;
//     }
//     h3{

// font-size: 17px;
//     }
//     h4{

// font-size: 16px;
//     }
//     h5{

// font-size: 15px;
//     }
//     h6{

// font-size: 14px;
//     }
//   p,div,button{
// font-size: 13px;
//   }
// @media only screen and (min-width: 540px) {
//     *{
//         // font-size: 24px;
//         color: rgb(36, 26, 13);
//     }
    
//     h1{

// font-size: 20px;
//     }
//     h2{

// font-size: 19px;
//     }
//     h3{

// font-size: 18px;
//     }
//     h4{

// font-size: 17px;
//     }
//     h5{

// font-size: 16px;
//     }
//     h6{

// font-size: 15px;
//     }
//   p,div,button{
// font-size: 14px;
//   }

// //     h1{

// //     }
// //     h2{

// //     }
// //     h3{

// //     }
// //     h4{

// //     }
// //     h5{

// //     }
// //     h6{

// //     }
// //   p,div,button{

// //   }
// }
// @media only screen and (min-width: 720px) {
//   *{
//         // font-size: 24px;
//         color: rgb(225, 156, 65);
//     }
    
//     h1{

// font-size: 21px;
//     }
//     h2{

// font-size: 20px;
//     }
//     h3{

// font-size: 19px;
//     }
//     h4{

// font-size: 18px;
//     }
//     h5{

// font-size: 17px;
//     }
//     h6{

// font-size: 16px;
//     }
//   p,div,button{
// font-size: 15px;
//   }
// }
// @media only screen and (min-width: 960px) {
//  *{
//         // font-size: 24px;
//         color: rgb(201, 225, 65);
//     }
    
//     h1{

// font-size: 22px;
//     }
//     h2{

// font-size: 21px;
//     }
//     h3{

// font-size: 20px;
//     }
//     h4{

// font-size: 19px;
//     }
//     h5{

// font-size: 18px;
//     }
//     h6{

// font-size: 17px;
//     }
//   p,div,button{
// font-size: 16px;
//   }
// }
// @media only screen and (min-width: 1140px) {
//   *{
//         font-size: 30px;
//         color: aqua;
//     }
//     h1{

// font-size: 23px;
//     }
//     h2{

// font-size: 22px;
//     }
//     h3{

// font-size: 21px;
//     }
//     h4{

// font-size: 20px;
//     }
//     h5{

// font-size: 19px;
//     }
//     h6{

// font-size: 18px;
//     }
//   p,div,button{
// font-size: 17px;
//   }
// }
// </style>