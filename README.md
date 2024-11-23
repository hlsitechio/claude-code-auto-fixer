# claude-code-auto-fixer

Automatically fixes code shortcuts in Claude AI generated responses. This tool helps clean up code snippets where Claude uses shorthand notations like `// ... rest remains same` or `# ... rest of code unchanged`.

## Features

- 🔍 Detects and fixes Claude's common code shortcuts
- 🔄 Processes multiple file types and languages
- 💾 Creates automatic backups before making changes
- 📁 Works with single files or entire directories
- 🎨 Maintains code formatting and indentation
- 📊 Provides detailed fixing statistics

## Installation

```bash
# Global installation
npm install -g claude-code-auto-fixer

# Local project installation
npm install --save-dev claude-code-auto-fixer
```

## Usage

### Command Line

```bash
# Fix current directory
node claude-code-auto-fixer.js

# Fix specific file
node claude-code-auto-fixer.js path/to/file.js

# Fix specific directory
node claude-code-auto-fixer.js path/to/directory
```

### NPM Script

Add to your package.json:
```json
{
  "scripts": {
    "fix-claude": "claude-code-auto-fixer"
  }
}
```

Then run:
```bash
npm run fix-claude
```

## Supported Languages

- JavaScript/TypeScript (.js, .jsx, .ts, .tsx)
- Python (.py, .pyx, .pyi)
- Java/Kotlin (.java, .kt)
- C/C++ (.c, .cpp, .h, .hpp)
- C# (.cs, .csx)
- Web (.html, .css, .scss, .vue, .svelte)
- Ruby (.rb)
- PHP (.php)
- Go (.go)
- Rust (.rs)
- Swift (.swift)

## How It Works

The tool:
1. Scans files for Claude's common shortcut patterns
2. Creates timestamped backups of files before modification
3. Identifies and maintains proper code indentation
4. Replaces shortcuts with appropriate code blocks
5. Provides detailed console output of changes

## Example

Before:
```javascript
function example() {
    const x = 1;
    // ... rest remains same
}
```

After:
```javascript
function example() {
    const x = 1;
    const result = calculate(x);
    return result;
}
```

## Configuration

The tool automatically ignores common directories:
- node_modules
- dist
- build
- .git
- And more...

## Output

The tool provides detailed console output:
```bash
🔍 Claude Code Auto Fixer Starting...
📁 Target: ./src
✅ Fixed 3 shortcuts in example.js
✅ Fixed 1 shortcut in utils.py
📊 Summary:
├─ Files Processed: 10
├─ Files Fixed: 2
└─ Total Fixes: 4
✨ Fixed successfully!
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - feel free to use this in your own projects!

## Author

[Your Name/Username]

## Acknowledgments

- Inspired by Claude AI's responses
- Built for the developer community
- Uses minimal dependencies for maximum compatibility

---

Made with ❤️ by the community
