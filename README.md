# A LaTeX resume template

`resume.cls` is a document class that adds name and address information to the
head of the document and provides resume section and subsection environments
(`rSection` and `rSubsection`).  The address separator format, the
`rSubsection` heading format, and the skip sizes defined in `resume.cls` can be
customized.

### License

Please see LICENSE file.

---

## Editing in VS Code

### Required tools

- [VS Code](https://code.visualstudio.com/) with [LaTeX Workshop by James Yu](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop).

Install the tools for your OS:

| OS | LaTeX and Perl |
| --- | --- |
| Windows | [MiKTeX](https://miktex.org/download) + [Strawberry Perl](https://strawberryperl.com/) (64-bit MSI). Check for updates in MiKTeX Console. |
| macOS | [MacTeX](https://tug.org/mactex/mactex-download.html) (full distribution). Use the system Perl; if unavailable, install [Perl](https://www.perl.org/get.html). |
| Linux | [TeX Live](https://tug.org/texlive/), `latexmk`, and `perl` through your distribution's package manager. |

Restart VS Code after installation.

### Workflow

1. Open the project folder in VS Code.
2. Edit `resume.tex` or the section files in `sections/`, then save all changes.
3. Open the Command Palette and select **LaTeX Workshop: Build LaTeX project**. If using MiKTeX, accept any required package installations.
4. From the same palette, select **LaTeX Workshop: View LaTeX PDF file**.

In MiKTeX's package installation dialog, uncheck **Always show this dialog** before clicking **Install** to install missing packages automatically without repeated prompts.

Open the Command Palette with **Ctrl + Shift + P** on Windows/Linux or **Cmd + Shift + P** on macOS.

Alternatively, compile from the project root in the terminal:

```sh
latexmk -pdf -interaction=nonstopmode -synctex=1 resume.tex
```

A successful build updates `resume.pdf` automatically. Review the PDF before committing it with the source files. Build artifacts are excluded by `.gitignore`.
