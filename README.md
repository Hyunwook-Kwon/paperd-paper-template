# Paperd paper template

A small, complete LaTeX paper you can fork to start your own paper repository and write it together with co-authors in **Paperd**, a local LaTeX workspace with reviewed AI suggestions and tamper-evident history.

The example paper has sections in separate files, a table generated from a CSV file, a figure, and a bibliography. Replace it with your own paper; keep the folder layout.

```text
paper/main.tex          compile entry
paper/sections/*.tex    sections, pulled in with \input
paper/references.bib    bibliography
paper/csvrows.sty       tiny helper that turns refs/data/*.csv into table rows
refs/data/results.csv   data behind the results table
Images/                 figures
```

Paperd only manages `paper/`, `Images/` and `refs/`. Everything else in this repository (this README, a LICENSE, CI files) is left as it is when Paperd publishes.

## Start your paper

1. **Fork** this repository (or use **Use this template**). Make it private if your paper is not public yet.
2. Open **Paperd** → Home → **Open a paper repo…** → choose your fork (Paperd lists your repositories when the GitHub CLI `gh` is signed in) or paste its URL → **Open**.
   Paperd can also do the fork for you: Home → **Start from a template…** with `Hyunwook-Kwon/paperd-paper-template`.
3. Write, compile and review in Paperd. Every save is a revision in Paperd's local history.
4. **Publish** from Paperd (Share & sync → Publish) to push your revisions to the repository as commits. Paperd never force-pushes.

## Write together

1. Invite co-authors to your repository (GitHub → Settings → Collaborators, or Paperd → Share & sync).
2. Each co-author opens the same repository in their own Paperd: Home → **Open a paper repo…** → the repository URL.
3. To bring in someone else's work: Share & sync → **Fetch** → **Bring in as draft** → **Review merge**. Paperd shows a three-way merge; you choose for each conflict, then publish. Nothing from the repository changes your document until you approve the merge.

Commits made by Paperd carry a `Paperd-Revision:` trailer so every co-author's Paperd can match them to its own history. You can still edit the repository with plain git or on GitHub; Paperd imports those commits the same way.

## Compile without Paperd

```bash
cd paper && tectonic main.tex
```

The numbers and two of the bibliography entries in the example are illustrative.
