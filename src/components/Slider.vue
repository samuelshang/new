<template>
	<div class="banner">
        <ul class="clearfix">
            <li><img src="../assets/images/img_1.jpg" alt=""/>
            	<div class="text-box">
                	<h2>愿历尽千帆，归来仍少年</h2>
        
                </div>
            </li>
            <li><img src="../assets/images/img_2.jpg" alt=""/>
            	<div class="text-box">
                	<h2>乱我德邦者虽远比诛</h2>
                  
                </div>
            </li>
            <li><img src="../assets/images/img_3.jpg" alt=""/>
            	<div class="text-box">
                	<h2>愿历尽千帆，归来仍少年</h2>
                  
                </div>
            </li>
            <li><img src="../assets/images/img_1.jpg" alt=""/>
            	<div class="text-box">
                	<h2>一万个小时</h2>
                  
                </div>
            </li>
        </ul>
        <ol>
            <li class="active"></li>
            <li></li>
            <li></li>
            <li></li>
        </ol>
    </div>
</template>
<script>
	export default {
		mounted(){
			this.fnSlider();
		},
		watch:{
			// '$route':function(){
			// 	alert(1);
			// }
		},
		methods:{
			fnSlider(){
				$(function (){
					var mySwipe=new Swipe($('.banner')[0],{
						auto:2000,
						continuous:true,
						stopPropation:true,
						callback:function (index,element){
							$('.banner ol li').removeClass('active');
							$('.banner ol li').eq(index).addClass('active');
						}
					});
				});
			}
		}
	}
</script>