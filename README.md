Berikut adalah versi lengkap dari instruksi yang bisa langsung dimasukkan ke dalam satu file `README.md`. Semua langkah dan perintah telah digabungkan dalam satu dokumen yang terstruktur dengan baik untuk tampil di GitHub:

```markdown
# Set Up Docker for Birdy

Follow the steps below to set up Docker for the Birdy project.

### 1. Make a New Folder
```bash
mkdir bird
cd bird
```

### 2. Clone this Repository
```bash
git clone https://github.com/hamdansyaif/birdy.git
```

### 3. Open the Folder You Just Cloned
```bash
cd birdy
```

### 4. Create a File Named `Dockerfile` Without Any Extension
```bash
sudo nano Dockerfile
```

### 5. Type the Following Content in `Dockerfile`
```dockerfile
FROM node:16-alpine

WORKDIR /app
COPY package* .

RUN npm install

COPY . .

CMD ["npm", "start"]
```

### 6. Save the File
- Press `Ctrl + X`, then press `Y`, and hit `Enter` to save the file.

### 7. Build the Docker Image
```bash
docker build -t reactjs/birdy:1.0.0 .
```

### 8. Run the Docker Container
```bash
docker run -d -p 5000:5000 reactjs/birdy:1.0.0
```

### 9. Open the Application in Your Browser
Go to [http://localhost:5000](http://localhost:5000).
```

### Penjelasan Format:
- **Langkah-langkah dengan Markdown**: Saya menggunakan nomor untuk setiap langkah agar instruksi lebih terstruktur.
- **Kode dengan Highlight**: Setiap perintah yang harus diketik di terminal dimasukkan ke dalam blok kode dengan format `bash` untuk sintaks terminal, dan `dockerfile` untuk file Docker.
- **Link**: Menambahkan tautan yang bisa langsung diklik di bagian browser.

Dengan format ini, kamu akan mendapatkan instruksi yang rapi dan mudah dibaca ketika dilihat di GitHub. Silakan salin seluruh konten ini ke dalam file `README.md` di proyekmu.
