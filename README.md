# Your Fellowship workbench

This is your repo for the 12 weeks of the Applied AI Training and Fellowship at Redmond AI Academy. Everything you build lives here. It is your workbench while you learn, and your portfolio when you are done. Anyone can see it, so work the way you would want a future colleague to read it.

This starter is provided for Fellows' use. The company and tickets in it are fictional.

## First-time setup

You do this once. If a step fails, do not guess. Paste the error to your mentor.

**1. Create your repo from the template.** On the template page, click **Use this template**, then **Create a new repository**. Owner: your own GitHub account. Name: `fellowship-<your-github-username>`. Visibility: **Public**. Never commit your `.env` file; it is already git-ignored.

**2. Clone it into a dedicated folder** (not your Desktop, not your Documents, not your home folder). Copy the clone URL from your new repo and run:

```
git clone https://github.com/<your-username>/fellowship-<your-username>.git
cd fellowship-<your-username>
```

**3. Make a virtual environment and install the packages.**

Mac / Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Windows PowerShell:

```powershell
py -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

If PowerShell refuses to run the activate script, run `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned` once, then try again. Your prompt should now start with `(.venv)`.

**4. Add your API key.** Get a free Gemini API key at https://aistudio.google.com/apikey (use your personal Gmail). Then copy the example file and paste the key after the `=` sign. Save the file as UTF-8.

Mac / Linux: `cp .env.example .env`
Windows PowerShell: `Copy-Item .env.example .env`

Open `.env` in VS Code and fill in `GEMINI_API_KEY=`. Free-tier requests may be used by Google to improve its products, so never send real customer or personal data. Our tickets are synthetic.

**5. Check your setup.**

```
python week00/check_setup.py
```

You want no FAIL lines. A WARN about `.env` is fine until you have a key. To make one tiny real call to Gemini and see the delay: `python week00/check_setup.py --ping`. To run the setup tests: `python -m pytest week00`.

On Mac you may need `python3` instead of `python` outside the virtual environment. Inside `.venv`, `python` always works. A yellow `DeprecationWarning` from `google-genai` is harmless.

## How each week works

1. **Branch.** Start each week on its own branch: `git switch -c week01`.
2. **Build.** Small steps. Run the tests often.
3. **Commit.** Commit when something works, with a message that says what and why. Commits are your undo button.
4. **Push and open a pull request** into your own `main`: `git push -u origin week01`, then click the link GitHub prints. Fill in the PR template honestly. Add your mentor (`@ravick`) as reviewer.
5. **Review.** Your mentor comments. You answer, change, push again. A review is a conversation, not a mark.
6. **Merge** when your mentor says so. Then start the next week from an updated `main`.

## House rules

- **You must be able to explain every line you submit.** A mentor can point at any line and ask "why?". AI help is welcome. Code you cannot explain is not.
- **Synthetic data only.** Never put real customer data, personal data or secrets in this repo.
- **Never commit `.env`.** If you ever do, tell your mentor straight away. We rotate the key and learn from it together.
- **Read before you approve.** When your coding assistant wants to run a command, read it. If you do not understand it, say no and ask.
- **Open only this folder** in your editor and assistant.
- **Say what the AI wrote and what you wrote.** In the PR, in `AI_LOG.md`, out loud. It is a skill.

## Where things are

| Folder | What it is |
|---|---|
| `week00/` | Setup checker and its tests |
| `week01/triage/` | This week's build: Ticket Triage. Start with its `README.md` |
| `articulation/` | The Articulation Track: your written and recorded homework, week by week |
| `ABOUT_ME.md` | Your "Where are you now?" self-check. Fill it in and commit it |
| `AGENTS.md` | Rules your AI coding assistant follows in this repo |

## Articulation homework

Each week has a short speaking-and-writing task. It goes in `articulation/` as `weekNN-<topic>.md`, in the same pull request as your build, or a small one of its own. Recordings are not committed. Share them privately with your mentor. `articulation/README.md` explains how.

## Questions

fellowship@hybr.com · hybr.com/fellowship

---

© 2026 Cloud Assert Technologies India Private Limited. Redmond AI Academy is a programme of Cloud Assert.
