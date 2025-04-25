<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>VVVNNN - Mạng xã hội</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f0f2f5;
    }
    .navbar {
      background-color: #1877f2;
      padding: 10px;
      color: white;
      font-size: 20px;
      font-weight: bold;
    }
    .post-area {
      background: white;
      margin: 20px auto;
      padding: 15px;
      border-radius: 10px;
      width: 90%;
      max-width: 500px;
    }
    .post-area input {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .post-button {
      margin-top: 10px;
      background-color: #1877f2;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 5px;
      cursor: pointer;
    }
    .feed {
      margin: 20px auto;
      width: 90%;
      max-width: 500px;
    }
    .feed .post {
      background: white;
      padding: 15px;
      margin-bottom: 15px;
      border-radius: 10px;
    }
  </style>
</head>
<body>

<div class="navbar">VVVNNN</div>

<div class="post-area">
  <h3>Bạn đang nghĩ gì?</h3>
  <input type="text" id="postContent" placeholder="Viết gì đó...">
  <button class="post-button" onclick="addPost()">Đăng bài</button>
</div>

<div class="feed" id="feed">
  <!-- Các bài đăng sẽ hiện ở đây -->
</div>

<script>
function addPost() {
  var content = document.getElementById('postContent').value;
  if (content.trim() !== '') {
    var feed = document.getElementById('feed');
    var post = document.createElement('div');
    post.className = 'post';
    post.innerHTML = `<p>${content}</p>`;
    feed.prepend(post);
    document.getElementById('postContent').value = '';
  }
}
</script>

</body>
</html>
