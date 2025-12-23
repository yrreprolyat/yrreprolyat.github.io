# yrreprolyat.com

Personal website — pure HTML and CSS, no frameworks.

## Local Development

Open `index.html` in your browser, or use a simple server:

```bash
python3 -m http.server 8000
# Then visit http://localhost:8000
```

## Deployment to GitHub Pages

### 1. Create Repository

Create a new repo named `yrreprolyat.github.io` (or any name with Pages enabled).

### 2. Push Code

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin git@github.com:yrreprolyat/yrreprolyat.github.io.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to repo **Settings** → **Pages**
2. Under "Source", select **Deploy from a branch**
3. Select **main** branch and **/ (root)** folder
4. Click **Save**

### 4. Configure Custom Domain

#### DNS Setup (at your domain registrar)

Add these DNS records for `yrreprolyat.com`:

**Option A: Apex domain (recommended)**
```
Type: A
Host: @
Value: 185.199.108.153

Type: A
Host: @
Value: 185.199.109.153

Type: A
Host: @
Value: 185.199.110.153

Type: A
Host: @
Value: 185.199.111.153
```

**Option B: Or use a CNAME for www**
```
Type: CNAME
Host: www
Value: yrreprolyat.github.io
```

#### GitHub Settings

1. In repo **Settings** → **Pages** → **Custom domain**
2. Enter `yrreprolyat.com`
3. Check **Enforce HTTPS** (after DNS propagates, ~24-48 hours)

### 5. Verify

After DNS propagates, your site will be live at:
- https://yrreprolyat.com
- https://yrreprolyat.github.io (redirects to custom domain)

## Customization

1. Replace placeholder content in `index.html`
2. Add your photo as `assets/photo.jpg`
3. Add company logos to `assets/` folder
4. Update social links with your profiles
5. Customize colors in `style.css` (CSS variables in `:root`)

## Structure

```
├── index.html      # Main page
├── style.css       # Styles (includes dark mode)
├── CNAME           # Custom domain config
├── README.md       # This file
└── assets/
    ├── photo.jpg   # Your profile photo
    └── *.png       # Company logos
```
