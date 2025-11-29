# Contributing to Quran Video Creator

First off, thank you for considering contributing to Quran Video Creator! It's people like you that make this tool better for the Muslim community worldwide.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Setup](#development-setup)
- [Style Guidelines](#style-guidelines)
- [Commit Messages](#commit-messages)
- [Pull Request Process](#pull-request-process)

## Code of Conduct

This project adheres to Islamic values of respect, kindness, and brotherhood/sisterhood. By participating, you are expected to uphold this standard. Please:

- Be respectful and considerate in all communications
- Welcome newcomers and help them learn
- Accept constructive criticism gracefully
- Focus on what is best for the community
- Show empathy towards other community members

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates. When creating a bug report, include:

- **Clear title and description**
- **Steps to reproduce** the problem
- **Expected behavior** vs **actual behavior**
- **Screenshots** if applicable
- **Environment details**: OS, Python version, installed packages
- **Log files** if available

**Example:**
```
Title: Video export fails with FFmpeg error on Windows 11

Description:
When trying to export a video with the midnight_forest preset,
the program crashes with an FFmpeg codec error.

Steps to reproduce:
1. Select language: English
2. Select preset: midnight_forest
3. Enter verse: 1:1
4. Click export

Expected: Video should be created successfully
Actual: Program crashes with error "FFmpeg codec not found"

Environment:
- OS: Windows 11
- Python: 3.10.5
- FFmpeg: 5.1.2
```

### Suggesting Enhancements

Enhancement suggestions are welcome! Please provide:

- **Clear use case**: Why is this needed?
- **Detailed description**: What should it do?
- **Mockups or examples**: Visual aids help
- **Alternatives considered**: Other approaches you thought about

### Code Contributions

1. **Find an issue** to work on, or create a new one
2. **Comment on the issue** to let others know you're working on it
3. **Fork the repository** and create a branch
4. **Make your changes** following our style guidelines
5. **Test thoroughly** before submitting
6. **Submit a pull request** with a clear description

## Development Setup

### 1. Fork and Clone

```bash
git clone https://github.com/YOUR-USERNAME/quran-video-creator.git
cd quran-video-creator
```

### 2. Create Virtual Environment

```bash
# Create virtual environment
python -m venv venv

# Activate it
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up Environment Variables

```bash
# Copy example env file
cp .env.example .env

# Edit .env and add your API keys (optional for testing)
```

### 5. Create a Branch

```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/bug-description
```

## Style Guidelines

### Python Code Style

We follow **PEP 8** with some project-specific conventions:

1. **Indentation**: 4 spaces (no tabs)
2. **Line length**: Maximum 100 characters
3. **Naming conventions**:
   - Classes: `PascalCase` (e.g., `VideoCreator`)
   - Functions/methods: `snake_case` (e.g., `create_video`)
   - Constants: `UPPER_SNAKE_CASE` (e.g., `MAX_DURATION`)
   - Private methods: `_leading_underscore` (e.g., `_internal_method`)

4. **Type hints**: Use them for function parameters and returns
   ```python
   def create_video(verse: str, language: str) -> bool:
       """Create a Quran video."""
       pass
   ```

5. **Docstrings**: Use Google-style docstrings
   ```python
   def complex_function(param1: str, param2: int) -> Dict[str, Any]:
       """
       Brief description of what the function does.

       Args:
           param1: Description of param1
           param2: Description of param2

       Returns:
           Dictionary containing the results

       Raises:
           ValueError: If param2 is negative
       """
       pass
   ```

6. **Comments**:
   - Write self-documenting code
   - Use comments for complex logic
   - Explain *why*, not *what*

### Code Organization

- Keep functions focused and small (< 50 lines ideally)
- Group related functions into classes
- Separate concerns (video processing, API calls, UI, etc.)
- Use meaningful variable names

### Testing

Before submitting:

1. **Test your changes** with multiple scenarios
2. **Check edge cases** (empty inputs, invalid data, etc.)
3. **Verify on multiple platforms** if possible
4. **Check logs** for errors or warnings

## Commit Messages

Write clear, descriptive commit messages:

### Format

```
<type>: <subject>

<body>

<footer>
```

### Types

- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code restructuring without behavior change
- `perf`: Performance improvements
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

### Examples

**Good:**
```
feat: Add support for Indonesian translation

Implemented Indonesian language support with Dr. Quraish Shihab's
translation. Updated language selection menu and added proper RTL
support detection.

Closes #42
```

**Bad:**
```
fixed stuff
```

### Subject Line Rules

- Use imperative mood ("Add feature" not "Added feature")
- Don't capitalize first letter
- No period at the end
- Keep under 50 characters

## Pull Request Process

### Before Submitting

- [ ] Code follows style guidelines
- [ ] Self-review completed
- [ ] Comments added for complex code
- [ ] No console logs or debug code left in
- [ ] Tested on your local machine
- [ ] Updated documentation if needed
- [ ] No merge conflicts with main branch

### PR Description Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing
Describe how you tested these changes

## Screenshots (if applicable)
Add screenshots for visual changes

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-reviewed
- [ ] Commented complex code
- [ ] Documentation updated
- [ ] No console logs left
- [ ] Tested locally
```

### Review Process

1. **Automated checks** must pass (if configured)
2. **Code review** by maintainers
3. **Address feedback** promptly and professionally
4. **Approval required** before merging
5. **Squash commits** may be requested for cleaner history

## Priority Areas for Contribution

We especially welcome contributions in these areas:

1. **Translations**: Adding more language support
2. **Visual Presets**: New background themes
3. **Performance**: Optimization improvements
4. **Documentation**: Tutorials, guides, examples
5. **Testing**: Automated tests and test coverage
6. **Accessibility**: Making the tool easier to use
7. **Platform Support**: Better Windows/macOS/Linux compatibility

## Questions?

- Open an issue with the `question` label
- Start a discussion in GitHub Discussions
- Be patient - maintainers are volunteers

## Recognition

Contributors will be:
- Listed in the project README
- Credited in release notes
- Given our sincere gratitude and duas

---

**JazakAllahu Khayran** for contributing to this project. May Allah reward your efforts in helping spread the message of the Quran!
