## 🚀 Ways to Contribute

You can contribute to OpenUtility in several ways:
* **Add a New Web Utility / Site**: Build a client-side tool or list a relevant web utility in the directory.
* **Fix Bugs & Improve Code**: Optimize client-side JavaScript execution, fix layout issues, or improve dark mode compatibility.
* **Enhance UX/UI**: Improve design responsiveness, accessibility (a11y), or Lucide icon pairings.
* **Improve Documentation**: Enhance README setup guides, document tool APIs, or clarify code comments.

---

## 🛠️ Adding a New Web Tool

All internal utilities in OpenUtility must adhere to these core rules:
1. **Client-Side First**: Tools must execute purely in the browser (HTML5 Canvas, Web APIs, JS) without sending user data to external servers.
2. **Zero-Fluff & Lightweight**: Focus on speed, minimal UI overhead, and instant usability.
3. **Responsive & Theme-Aware**: Ensure new elements support both Light and Dark themes via Tailwind CSS classes.

### Step-by-Step Guide

1. **Fork the Repository**
   Click the **Fork** button at the top right of this repository to create your copy.

2. **Clone your Fork locally**
   ```bash
   git clone [https://github.com/YOUR-USERNAME/OpenUtility.git](https://github.com/YOUR-USERNAME/OpenUtility.git)
   cd OpenUtility

 * Create a Feature Branch
   git checkout -b feature/add-new-tool

 * Add Your Tool Card to index.html
   Add your card inside the #tools-grid container:
   <div class="tool-card group p-6 rounded-2xl bg-slate-50 dark:bg-slate-900/40 border border-slate-200 dark:border-slate-800 hover:border-blue-500/50 transition-all duration-300 flex flex-col justify-between shadow-sm dark:shadow-none" 
     data-category="utility" 
     data-title="your tool keywords search terms">
    <div>
        <div class="p-3 bg-white dark:bg-slate-800 text-blue-500 rounded-xl w-fit mb-4 border border-slate-200 dark:border-slate-700">
            <i data-lucide="wrench" class="w-6 h-6"></i>
        </div>
        <h4 class="text-lg font-bold text-slate-900 dark:text-white mb-2">Tool Name</h4>
        <p class="text-xs text-slate-600 dark:text-slate-400 leading-relaxed mb-4">
            Short description of what the utility does.
        </p>
    </div>
    <button onclick="openModal('your-tool-modal')" class="inline-flex items-center gap-1.5 text-xs font-semibold text-blue-600 dark:text-blue-400 hover:text-blue-500 pt-4 border-t border-slate-200 dark:border-slate-800/60 w-full text-left">
        Launch Tool <i data-lucide="arrow-right" class="w-3.5 h-3.5"></i>
    </button>
</div>

 * Create Modal & JS Logic
   * Add your modal HTML structure near the other modals.
   * Add pure client-side JavaScript inside the main <script> tag.
   * Call lucide.createIcons() if dynamically appending icons.
 * Test Your Changes
   * Open index.html in your browser.
   * Test light/dark mode toggling.
   * Test mobile responsiveness and verify search/filter functionality works with your card's data-title and data-category.
📬 Submitting a Pull Request (PR)
 * Commit Your Changes
   git add .
git commit -m "feat: add [Tool Name] utility"

 * Push to Your Fork
   git push origin feature/add-new-tool

 * Open a Pull Request
   * Go to the original OpenUtility repository on GitHub.
   * Click Compare & pull request.
   * Provide a clear title and description of your tool or fix.
📜 Code of Conduct
 * Be respectful and inclusive toward all community members.
 * Accept constructive feedback gracefully.
 * Focus on what is best for the overall user community.
💬 Need Help?
If you have questions or feature suggestions prior to coding, feel free to open a GitHub Issue or reach out via our Discord server!
