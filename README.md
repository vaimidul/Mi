from pathlib import Path
from zipfile import ZipFile

# Create directory and HTML file
base_path = Path("/mnt/data/mostafigur_website")
base_path.mkdir(parents=True, exist_ok=True)

html_content = """<!DOCTYPE html>
<html>
<head>
  <title>Mostafigur Rahman - Learning Zone</title>
  <meta charset="UTF-8">
  <style>
    body { font-family: sans-serif; padding: 20px; max-width: 800px; margin: auto; background: #f4f4f4; }
    h1 { color: #333; }
    nav a { margin: 0 10px; text-decoration: none; color: #0073aa; }
    section { background: white; padding: 20px; margin-top: 20px; border-radius: 8px; }
  </style>
</head>
<body>
  <h1>📘 Welcome to Mostafigur Rahman’s Learning Zone</h1>
  <nav>
    <a href="#about">About</a> |
    <a href="#subjects">Subjects</a> |
    <a href="#blog">Blog</a> |
    <a href="#contact">Contact</a>
  </nav>

  <section id="about">
    <h2>About Me</h2>
    <p>আমি মোস্তাফিগুর রহমান। আমি একজন লেখাপড়ার আগ্রহী ব্যক্তি। আমার লক্ষ্য হলো ছাত্রছাত্রীদের সহজ ভাষায় শেখানো।</p>
  </section>

  <section id="subjects">
    <h2>Subjects</h2>
    <ul>
      <li><strong>বাংলা:</strong> বাক্য গঠন, অনুচ্ছেদ, প্রবাদ</li>
      <li><strong>গণিত:</strong> মৌলিক গণনা, সূত্র</li>
      <li><strong>ইংরেজি:</strong> Vocabulary, Translation Practice</li>
    </ul>
  </section>

  <section id="blog">
    <h2>Study Blog</h2>
    <p>নতুন লেখাগুলো:</p>
    <ul>
      <li>৫টি সহজ ইংরেজি বাক্য প্রতিদিনের ব্যবহারের জন্য</li>
      <li>ছোটদের জন্য ১০টি সহজ গণিতের কৌশল</li>
      <li>পরীক্ষার প্রস্তুতির টিপস</li>
    </ul>
  </section>

  <section id="contact">
    <h2>Contact Me</h2>
    <p>📧 Email: mostafigur@email.com</p>
    <p>📱 ফোন: 01XXXXXXXXX</p>
  </section>
</body>
</html>
"""

html_file = base_path / "index.html"
html_file.write_text(html_content, encoding='utf-8')

# Create ZIP file
zip_path = "/mnt/data/mostafigur_website.zip"
with ZipFile(zip_path, 'w') as zipf:
    zipf.write(html_file, arcname="index.html")

zip_path

 Mi
