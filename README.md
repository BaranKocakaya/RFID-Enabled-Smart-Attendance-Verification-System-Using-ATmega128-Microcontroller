mkdir rfid-attendance-site
cd rfid-attendance-site

git init

# PDF dosyanı klasöre kopyala
cp /path/to/RFID_PROJECT.pdf .

# index.html oluştur
 cat > index.html <<'HTML'
<!doctype html>
<html>
<head>
  <meta charset="utf-8">
  <title>RFID-Based Smart Attendance System</title>
</head>
<body>
  <h1>RFID-Based Smart Attendance System</h1>
  <p>This page hosts the project documentation for the RFID-Based Smart Attendance System.</p>

  <p><a href="RFID_PROJECT.pdf" target="_blank">
     Click here to view or download the full project PDF
  </a></p>

  <embed src="RFID_PROJECT.pdf" type="application/pdf" width="100%" height="850px" />
</body>
</html>
HTML

git add .
git commit -m "Upload RFID attendance project site and PDF"
git remote add origin https://github.com/BaranKocakaya/BaranKocakaya.github.io.git
git branch -M main
git push -u origin main
