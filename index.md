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
        <!--自动尝试播放（带静音处理）-->
        window.onload = function() {
            const player = document.getElementById('music-player');
            player.muted = true; <!--静音状态允许自动播放-->
            
            player.play()
                .then(() => {
                    player.style.display = 'block';
                    player.muted = false; <!--取消静音-->
                    document.querySelector('.play-tip').style.display = 'none';
                })
                .catch(error => {
                    console.log('静音自动播放失败:', error);
                });
        }
    </script>
