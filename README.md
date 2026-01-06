# Flick Landing Page

A beautiful, modern landing page and waitlist signup for the Flick app - the revolutionary lighter tracking, trading, and collecting application.

## 🚀 Features

- **Modern Design**: Clean, gradient-based design with smooth animations
- **Responsive Layout**: Fully responsive for all devices (mobile, tablet, desktop)
- **Waitlist Form**: Capture user interest with an email signup form
- **Feature Showcase**: Highlights all key app features
- **How It Works**: Simple 3-step explanation
- **Animated Elements**: Smooth scroll animations and interactive components
- **Phone Mockup**: Visual preview of the app interface
- **Success Modal**: User-friendly confirmation after signup

## 📁 Structure

```
landing-page/
├── index.html          # Main HTML structure
├── styles.css          # All styling and animations
├── script.js           # Interactive functionality
└── README.md          # This file
```

## 🎨 Design Elements

- **Color Scheme**: Gradient purples and blues (#667eea, #764ba2)
- **Typography**: Inter font family
- **Icons**: Emoji-based icons for modern, friendly feel
- **Animations**: Floating phone mockup, counter animations, scroll effects
- **Layout**: Grid-based responsive design

## 🔧 Customization

### Changing Colors

Edit the CSS variables in `styles.css`:

```css
:root {
    --primary-color: #667eea;    /* Main brand color */
    --primary-dark: #5568d3;      /* Darker shade */
    --primary-light: #764ba2;     /* Lighter shade */
    --gradient-1: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

### Adding Backend Integration

Replace the form submission in `script.js`:

```javascript
document.getElementById('waitlistForm').addEventListener('submit', async function(e) {
    e.preventDefault();
    
    const formData = {
        name: document.getElementById('name').value,
        email: document.getElementById('email').value,
        phone: document.getElementById('phone').value
    };
    
    try {
        const response = await fetch('YOUR_API_ENDPOINT', {
            method: 'POST',
            headers: { 'Content-Type': 'application/json' },
            body: JSON.stringify(formData)
        });
        
        if (response.ok) {
            document.getElementById('successModal').style.display = 'block';
            document.getElementById('waitlistForm').reset();
        }
    } catch (error) {
        console.error('Error:', error);
    }
});
```

## 📊 Analytics

Add Google Analytics or other tracking:

```html
<!-- Add to <head> in index.html -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🚢 Deployment

### Option 1: Static Hosting (Recommended)

**Netlify:**
1. Push to GitHub
2. Import project to Netlify
3. Deploy automatically

**Vercel:**
1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` in the landing-page directory
3. Follow prompts

**GitHub Pages:**
1. Push to GitHub repository
2. Go to Settings > Pages
3. Select main branch and deploy

### Option 2: Traditional Web Hosting

Simply upload all files to your web server's public directory.

## 📝 Todo List

- [ ] Integrate with backend API for form submissions
- [ ] Add email validation
- [ ] Implement CAPTCHA for spam protection
- [ ] Add social media sharing buttons
- [ ] Create FAQ section
- [ ] Add testimonials section
- [ ] Implement dark mode toggle
- [ ] Add multi-language support
- [ ] Optimize images and assets
- [ ] Add PWA capabilities

## 🔒 Privacy & Legal

Don't forget to:
- Add a Privacy Policy page
- Add Terms of Service page
- Implement GDPR compliance (if needed)
- Add cookie consent banner
- Link to privacy policy in footer

## 📧 Contact

For questions or support, contact: [Your Contact Info]

## 📄 License

© 2025 Flick by Good Monkeys LLC. All rights reserved.

---

**Built with ❤️ for the Flick community**


