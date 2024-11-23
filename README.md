# claude-code-auto-fixer

🔧 A tool that automatically fixes code shortcuts in Claude AI generated responses. It replaces patterns like `// ... rest remains same` or `# ... rest of code unchanged` with the appropriate code blocks.

## 🚀 Installation

### NPM Package (Recommended)
```bash
# Global installation
npm install -g claude-code-auto-fixer

# Local project installation
npm install --save-dev claude-code-auto-fixer
```

### From Source
```bash
# Clone the repository
git clone https://github.com/your-username/claude-code-auto-fixer.git
cd claude-code-auto-fixer
npm install
```

## 💻 Usage

### Using NPM Package

```bash
# If installed globally
claude-fix ./your-directory

# Using npx
npx claude-code-auto-fixer ./your-directory

# If installed locally, add to your package.json scripts:
{
  "scripts": {
    "fix-claude": "claude-fix"
  }
}

# Then run:
npm run fix-claude
```

### Using in Your Code

```javascript
// CommonJS
const ClaudeCodeAutoFixer = require('claude-code-auto-fixer');

// ES Modules
import ClaudeCodeAutoFixer from 'claude-code-auto-fixer';

// Use the fixer
const fixer = new ClaudeCodeAutoFixer();
await fixer.fix('./src');
```

### Command Line Options
```bash
claude-fix [directory]     # Fix directory (default: current)
claude-fix file.js        # Fix single file
```

## 🌟 Features

- 🤖 Specifically designed for Claude AI code responses
- 🔄 Preserves code structure and indentation
- 💾 Creates automatic timestamped backups
- 📂 Process single files or entire directories
- 🎨 Multiple language support
- 📦 Automatic npm script integration

## 🔍 Examples

### Before:
```javascript
function calculateTotal() {
    const subtotal = getSubtotal();
    // ... rest remains same
}
```

### After:
```javascript
function calculateTotal() {
    const subtotal = getSubtotal();
    const tax = subtotal * 0.2;
    return subtotal + tax;
}
```

## 🗃️ Supported File Types

### Programming Languages
- JavaScript/TypeScript (.js, .jsx, .ts, .tsx)
- Python (.py, .pyx, .pyi)
- Java/Kotlin (.java, .kt)
- C/C++ (.c, .cpp, .h, .hpp)
- C# (.cs)
- Ruby (.rb)
- PHP (.php)
- Go (.go)
- Rust (.rs)
- Swift (.swift)

### Web Technologies
- HTML (.html)
- CSS/SCSS (.css, .scss)
- Vue (.vue)
- Svelte (.svelte)

## 📋 Requirements

- Node.js (version 12 or higher)
- npm or yarn

## 🔒 Safety Features

- Creates timestamped backups before modifying files
- Skips common build and dependency directories
- Preserves original file structure
- Maintains code indentation

## ⚙️ Integration Examples

### With VS Code Tasks
```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "Fix Claude Code",
      "type": "shell",
      "command": "claude-fix",
      "args": ["${workspaceFolder}"]
    }
  ]
}
```

### With Git Hooks (using husky)
```json
{
  "husky": {
    "hooks": {
      "pre-commit": "claude-fix ./src"
    }
  }
}
```

### With GitHub Actions
```yaml
name: Fix Claude Code
on: [push]
jobs:
  fix-code:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: actions/setup-node@v2
      - run: npm install -g claude-code-auto-fixer
      - run: claude-fix ./src
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🐛 Troubleshooting

### Common Issues

1. **Global Command Not Found**
   ```bash
   npm install -g claude-code-auto-fixer
   ```

2. **Permission Issues**
   ```bash
   sudo npm install -g claude-code-auto-fixer
   ```

3. **Package Not Found**
   ```bash
   # Check your npm configuration
   npm config list
   # Make sure you're using the correct registry
   npm config set registry https://registry.npmjs.org/
   ```

## 📞 Support

If you have any questions or run into issues, please:

1. Check the [issues page](https://github.com/your-username/claude-code-auto-fixer/issues)
2. Open a new issue if needed

---

Made with 🔧 by [Your Name]

[GitHub Repository](https://github.com/your-username/claude-code-auto-fixer) | 
[NPM Package](https://www.npmjs.com/package/claude-code-auto-fixer)
