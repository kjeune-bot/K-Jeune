/* =================================================================ative
   DESIGN SYSTEM & VARIABLES
   =================================================================== */
:root {
  /* Color Palette */
  --color-primary: #1e3a8a;      /* Deep Slate Blue */
  --color-secondary: #0d9488;    /* Teal Accent */
  --color-background: #f8fafc;   /* Off-white Background */
  --color-surface: #ffffff;      /* Card / Container White */
  --color-text: #1e293b;         /* Dark Charcoal Body Text */
  --color-muted: #64748b;        /* Muted Grey Text */

  /* Spacing System (Multiples of 8px) */
  --space-xs: 8px;
  --space-sm: 16px;
  --space-md: 24px;
  --space-lg: 32px;
  --space-xl: 48px;
  --space-xxl: 64px;

  /* Typography */
  --font-heading: 'Poppins', sans-serif;
  --font-body: 'Inter', sans-serif;
}

/* =================================================================
   BASE STYLES & RESET (Type Selectors)
   =================================================================== */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: var(--font-body);
  background-color: var(--color-background);
  color: var(--color-text);
  line-height: 1.6;
}

h1, h2, h3, h4, h5, h6 {
  font-family: var(--font-heading);
  color: var(--color-primary);
  margin-bottom: var(--space-sm);
}

p {
  margin-bottom: var(--space-sm);
}

a {
  color: var(--color-secondary);
  text-decoration: none;
  transition: color 0.2s ease;
}

a:hover {
  color: var(--color-primary);
  text-decoration: underline;
}

/* =================================================================
   LAYOUT & CLASS SELECTORS
   =================================================================== */
.site-header {
  background-color: var(--color-surface);
  border-bottom: 1px solid #e2e8f0;
  padding: var(--space-md) var(--space-lg);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-list {
  list-style: none;
  display: flex;
  gap: var(--space-md);
}

.main-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: var(--space-xl) var(--space-md);
}

/* Flexbox / Grid Multi-column Section */
.card-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: var(--space-md);
  margin-top: var(--space-lg);
}

.card {
  background-color: var(--color-surface);
  padding: var(--space-lg);
  border-radius: 8px;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05), 0 2px 4px -1px rgba(0, 0, 0, 0.03);
  transition: transform 0.2s ease;
}

.card:hover {
  transform: translateY(-4px);
}

.site-footer {
  background-color: var(--color-primary);
  color: var(--color-surface);
  text-align: center;
  padding: var(--space-lg);
  margin-top: var(--space-xxl);
}

/* =================================================================
   ID SELECTOR
   =================================================================== */
#hero-banner {
  background: linear-gradient(135deg, var(--color-primary), var(--color-secondary));
  color: var(--color-surface);
  padding: var(--space-xxl) var(--space-lg);
  border-radius: 12px;
  text-align: center;
  margin-bottom: var(--space-xl);
}

#hero-banner h1 {
  color: var(--color-surface);
  font-size: 2.25rem;
}

/* =================================================================
   RESPONSIVENESS (@MEDIA QUERIES)
   =================================================================== */

/* Tablet View (768px and up) */
@media (min-width: 768px) {
  .card-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  #hero-banner h1 {
    font-size: 2.75rem;
  }
  
  .main-container {
    padding: var(--space-xxl) var(--space-lg);
  }
}

/* Desktop View (1200px and up) */
@media (min-width: 1200px) {
  .card-grid {
    grid-template-columns: repeat(3, 1fr);
  }

  #hero-banner {
    padding: 80px var(--space-xxl);
  }

  #hero-banner h1 {
    font-size: 3.25rem;
  }
}
