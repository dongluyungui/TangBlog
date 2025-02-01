---
title: 糖芷企划
---
<div align="center"><!-- HTML <div> 标签包裹使得内容居中 -->
  <img src="img/TangZhiAll.png" alt="糖芷概念图"><!-- 引用img文件夹下的图片，并命名 -->
  <p class="image-caption">图1：糖芷概念图</p><!-- 文本给图片命名 -->
</div>


<audio id="music-player" controls loop>
        <source src="Audio/ShuiMu.mp3" type="audio/mpeg">
    </audio>
    
<script>
        <!-- 页面加载后尝试静音播放 -->
        window.onload = function() {
            const player = document.getElementById('music-player');
            
            <!-- 设置静音状态 -->
            player.muted = true;
            
            player.play().catch(() => {
                <!-- 静音播放失败时不提示 -->
            });
        }

        <!-- 用户交互处理函数 -->
        function handlePlay() {
            const player = document.getElementById('music-player');
            
            <!-- 解除静音并隐藏按钮 -->
            if(player.muted) {
                player.muted = false;
                document.getElementById('play-btn').style.display = 'none';
            } else {
                player.play().catch(() => {
                    alert('播放被阻止，请检查浏览器设置');
                });
            }
        }
    </script>
