# AutoCheck V2

AutoCheck is a Windows tool that checks your system’s health and stability by running diagnostics and stress tests.

It does **not** change anything on your computer — it only reads data and tests performance.

---

## What you need

* Windows 10 or 11
* Internet connection
* About 5–10 minutes

---

## Step 1 — Install Python (this also installs pip)

AutoCheck needs Python, and **pip comes with Python** (pip is just what installs the required packages).

1. Go to: https://www.python.org/downloads/

2. Click **Download Python 3.12**

3. Open the installer

4. **IMPORTANT — check this box:**

   Add Python to PATH

5. Click **Install Now**

---

## Step 2 — Make sure Python and pip work

1. Press the Windows key
2. Type `cmd` and open Command Prompt

Now type:

```bash
py -3.12 --version
```

You should see something like:

```
Python 3.12.x
```

---

Now check pip:

```bash
pip --version
```

You should see something like:

```
pip 23.x from ...
```

---

### If pip does NOT work

Try this instead:

```bash
py -3.12 -m pip --version
```

If that works, you’re good — just use `py -3.12 -m pip` instead of `pip`.

---

## Step 3 — Download AutoCheck

1. Download the project from GitHub
2. Right-click the file → click **Extract All**
3. Open the extracted folder

---

## Step 4 — Open Command Prompt in the folder

Inside the AutoCheck folder:

1. Click the address bar at the top
2. Type:

```
cmd
```

3. Press Enter

A black window will open — this is where you run commands.

---

## Step 5 — Install required packages

Now type:

```bash
pip install -r requirements.txt
```

Press Enter and wait.

---

### If that fails, use this instead:

```bash
py -3.12 -m pip install -r requirements.txt
```

This does the exact same thing, just more reliable.

---

## Step 6 — Run AutoCheck

Still in the same window, type:

```bash
py -3.12 main.py soft
```

---

## Modes

### Light check (recommended first run)

```bash
py -3.12 main.py soft
```

### Balanced test

```bash
py -3.12 main.py med --full
```

### Heavy stress test

```bash
py -3.12 main.py hard --full
```

### Monitor only (no stress)

```bash
py -3.12 main.py monitor
```

---

## Where results go

* `logs/` → detailed data
* `reports/` → summaries

---

## GPU testing (optional)

If you want GPU stress testing:

```bash
py -3.12 -m pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```

---

## Common issues

### "pip is not recognized"

Use:

```bash
py -3.12 -m pip install -r requirements.txt
```

---

### "py is not recognized"

Python was not installed correctly. Reinstall and make sure **Add to PATH** is checked.

---

### Nothing happens / errors

Make sure:

* You are inside the AutoCheck folder
* You installed requirements
* You are using Python 3.12

---

## First time?

Run this:

```bash
py -3.12 main.py soft
```

---

## License

MIT
