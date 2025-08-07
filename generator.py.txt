def generate_readme(project_name, language, license_type, description, include_badges=True):
    badges = []
    if include_badges:
        badges.append(f"![License](https://img.shields.io/badge/license-{license_type}-blue)")
        badges.append(f"![Language](https://img.shields.io/badge/language-{language}-yellow)")

    badge_line = "\n".join(badges) if badges else ""

    readme = f"""# {project_name}

{badge_line}

## 📝 Description
{description}

## 🚀 Installation
```bash
# clone the repo
$ git clone https://github.com/yourusername/{project_name.lower().replace(' ', '-')}.git
$ cd {project_name.lower().replace(' ', '-')}
```

## 📦 Usage
```bash
# run your app
$ python main.py
```

## 📄 License
This project is licensed under the {license_type} license.
"""
    return readme
