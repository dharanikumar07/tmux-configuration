# Tmux Keybindings (Option + Ctrl Space Setup)

<h2>Table of Contents</h2>
<ul>
  <li><a href="#command-1">New Window</a></li>
  <li><a href="#command-2">Next Window</a></li>
  <li><a href="#command-3">Previous Window</a></li>
  <li><a href="#command-4">Jump to Window</a></li>
  <li><a href="#command-5">Rename Window</a></li>
  <li><a href="#command-6">Split Vertical</a></li>
  <li><a href="#command-7">Split Horizontal</a></li>
  <li><a href="#command-8">Move Between Panes</a></li>
  <li><a href="#command-9">Kill Pane</a></li>
  <li><a href="#command-10">Kill Window</a></li>
  <li><a href="#command-11">Configuration</a></li>
  <li><a href="#command-12">iTerm Setup</a></li>
  <li><a href="#command-13">Ctrl + Space (Prefix Mode)</a></li>
</ul>

---

<h2 id="command-1">New Window</h2>
<p>Creates a new tmux window.</p>
<pre><code>Option + c
Ctrl + Space → c</code></pre>

---

<h2 id="command-2">Next Window</h2>
<p>Switch to the next window.</p>
<pre><code>Option + ]
Ctrl + Space → n</code></pre>

---

<h2 id="command-3">Previous Window</h2>
<p>Switch to the previous window.</p>
<pre><code>Option + [
Ctrl + Space → p</code></pre>

---

<h2 id="command-4">Jump to Window</h2>
<p>Directly jump to a specific window by number.</p>
<pre><code>Option + 0 / 1 / 2
Ctrl + Space → 0 / 1 / 2</code></pre>

---

<h2 id="command-5">Rename Window</h2>
<p>Rename the current window.</p>
<pre><code>Option + ,
Ctrl + Space → ,</code></pre>

---

<h2 id="command-6">Split Vertical</h2>
<p>Split the pane vertically.</p>
<pre><code>Option + v
Ctrl + Space → v</code></pre>

---

<h2 id="command-7">Split Horizontal</h2>
<p>Split the pane horizontally.</p>
<pre><code>Option + h
Ctrl + Space → h</code></pre>

---

<h2 id="command-8">Move Between Panes</h2>
<p>Navigate between panes.</p>
<pre><code>Option + Arrow Keys
Ctrl + Space → Arrow Keys</code></pre>

---

<h2 id="command-9">Kill Pane</h2>
<p>Close the current pane.</p>
<pre><code>Option + d
Ctrl + Space → d</code></pre>

---

<h2 id="command-10">Kill Window</h2>
<p>Close the current window.</p>
<pre><code>Option + w
Ctrl + Space → w</code></pre>

---

<h2 id="command-11">Tmux Configuration</h2>
<p>Add the following to your <code>~/.tmux.conf</code> file:</p>

<pre><code># --- OPTION (NO PREFIX MODE) ---

bind -n M-c new-window
bind -n M-] next-window
bind -n M-[ previous-window

bind -n M-0 select-window -t 0
bind -n M-1 select-window -t 1
bind -n M-2 select-window -t 2

bind -n M-, command-prompt -I "#W" "rename-window '%%'"

bind -n M-v split-window -h
bind -n M-h split-window -v

bind -n M-Left select-pane -L
bind -n M-Right select-pane -R
bind -n M-Up select-pane -U
bind -n M-Down select-pane -D

bind -n M-d kill-pane
bind -n M-w kill-window


# --- PREFIX MODE (Ctrl + Space) ---

unbind C-b
set -g prefix C-Space
bind C-Space send-prefix

bind c new-window
bind n next-window
bind p previous-window

bind 0 select-window -t 0
bind 1 select-window -t 1
bind 2 select-window -t 2

bind , command-prompt -I "#W" "rename-window '%%'"

bind v split-window -h
bind h split-window -v

bind Left select-pane -L
bind Right select-pane -R
bind Up select-pane -U
bind Down select-pane -D

bind d kill-pane
bind w kill-window
</code></pre>

---

<h2 id="command-12">iTerm Setup</h2>
<p>Configure Option key and Ctrl + Space:</p>

<pre><code>iTerm2 → Settings → Profiles → Keys

Left Option Key = Esc+
Right Option Key = Esc+ (optional)
</code></pre>

<p>Add Ctrl + Space mapping:</p>

<pre><code>iTerm2 → Settings → Keys → Key Mappings → Add

Shortcut: Ctrl + Space
Action: Send Hex Code
Value: 0x00
</code></pre>

---

<h2 id="command-13">Ctrl + Space (Prefix Mode)</h2>
<p>Ctrl + Space acts as a prefix (like Ctrl + B by default).</p>

<pre><code>Ctrl + Space → c   (new window)
Ctrl + Space → n   (next window)
Ctrl + Space → p   (previous window)
Ctrl + Space → v   (split vertical)
Ctrl + Space → h   (split horizontal)
</code></pre>

<p><strong>Note:</strong></p>
<ul>
  <li>Option keys are fast but may not work over SSH</li>
  <li>Ctrl + Space works everywhere (SSH-safe)</li>
  <li>This setup gives both speed and reliability</li>
</ul>
