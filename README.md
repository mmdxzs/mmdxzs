- 👋 Hi, I’m @mmdxzs
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
mmdxzs/mmdxzs is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<!DOCTYPE html>
<html>

<head>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no"> 
    <meta name="language" content="zh-CN">
    <meta name="title" content="爱心代码">
    <meta name="describe" content="欢迎点赞分享 ">

    <title>💗 我爱你 💗</title>
     <link rel="stylesheet" href="./style/main.css">
    <style type="text/css">
        body {
            margin: 0;
            height: 100vh;
            overflow: hidden;
            background: rgb(4, 4, 22);

         #contents {
            color: pink;
            font-size: 2em;
            text-align: center;
            width: 100%;
            height: 100px;
            text-transform: none;
        }

        .type_words{position:fixed;top:50%;left:50%;transform:translate(-50%,-50%);width:180px;height:180px;color:#f1dadb;padding:20px;text-transform:lowercase;}
    </style>
</head>

<body onclick="bodyPlayMusic()">
     <a href="https://mp.weixin.qq.com/s/oxLqXBcLCT8ij67DjkW2kw" class="hide_buttom"
  style="position: fixed;top: 10%;right: 10px;width: 35px;height: 35px;z-index: 999;background: #696969;border-radius: 50%;padding: 1.0px;text-align: center;color: #ddd;text-decoration: none;   clear: both; line-height: 35px; 	margin:auto;   font-size: 13px;">制作</a>
  <a href="https://mp.weixin.qq.com/s/KA3nFLUB5W8f1BIyd_g0cg" class="hide_buttom"
  style="position: fixed;top: 4%;right: 10px;width: 35px;height: 35px;z-index: 998;background: #696969;border-radius: 50%;padding: 1.0px;text-align: center;color: #ddd;text-decoration: none;   clear: both; line-height: 35px; 	margin:auto;   font-size: 13px;">更多</a>
          <a href="https://pan.quark.cn/s/3344d23e48a8" class="hide_buttom"
  style="position: fixed;top: 16%;right: 10px;width: 35px;height: 35px;z-index: 997;background: #696969;border-radius: 50%;padding: 1.0px;text-align: center;color: #ddd;text-decoration: none;   clear: both; line-height: 35px; 	margin:auto;   font-size: 13px;">源码</a>
  <a href="https://shop1619956412.v.weidian.com/?userid=1619956412&spider_token=2720" class="hide_buttom"
  style="position: fixed;top: 22%;right: 10px;width: 35px;height: 35px;z-index: 996;background: #696969;border-radius: 50%;padding: 1.0px;text-align: center;color: #ddd;text-decoration: none;   clear: both; line-height: 35px; 	margin:auto;   font-size: 13px;">红包</a>


    <div class="type_words" id="contents">给你的爱心</div>
    <canvas id="pinkboard" width="1707" height="868"></canvas>
    <canvas id="heart" width="1000" height="600"></canvas>

    <audio id="audio" src="https://music.163.com/song/media/outer/url?id=27130317.mp3" preload="auto"
        loop="loop"></audio>
    <script>
        var shouci = true;
        console.log(shouci);
        function bodyPlayMusic() {
            if (shouci) {
                shouci = false;
                audio.play();
                console.log(shouci);
            }
        };
    </script>
    <script src="./js/lxheart.js"></script>
    <script src="./js/filltext.js"></script>
    <script>
        var texts = ['亲爱的', '生日快乐', '❤️'];

        var params = new URLSearchParams(window.location.search);
        var text = params.get('text');
        var word = params.get('word');
        if (text) {
            texts = text.split(',')
        }
        document.getElementById('contents').innerHTML = word || 'xxx, 生日快乐';

        renderLxHeart(document.getElementById('heart'), '#ec9bad');
        fillText(document.getElementById('pinkboard'), texts)
    </script>
</body>

</html>
