import typer
from readmegen.generator import generate_readme
from rich.console import Console

app = typer.Typer()
console = Console()

@app.command()
def create(
    project: str = typer.Option(..., help="Project name"),
    lang: str = typer.Option("python", help="Programming language (python, nodejs, rust, etc.)"),
    license: str = typer.Option("MIT", help="License type (MIT, GPL, Apache, etc.)"),
    description: str = typer.Option("A cool project.", help="Short project description"),
    badges: bool = typer.Option(True, help="Include standard badges (e.g., license, language)")
):
    """Generate a README.md file based on your inputs"""
    readme_content = generate_readme(
        project_name=project,
        language=lang,
        license_type=license,
        description=description,
        include_badges=badges
    )

    with open("README.md", "w") as f:
        f.write(readme_content)

    console.print(f"[bold green]README.md generated for [cyan]{project}[/cyan] successfully![/bold green]")

if __name__ == "__main__":
    app()
