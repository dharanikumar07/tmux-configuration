# Tmux Keybindings (Option Key Setup)

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
</ul>

---

<h2 id="command-1">New Window</h2>
<p>Creates a new tmux window.</p>
<pre><code>Option + c</code></pre>

---

<h2 id="command-2">Next Window</h2>
<p>Switch to the next window.</p>
<pre><code>Option + ]</code></pre>

---

<h2 id="command-3">Previous Window</h2>
<p>Switch to the previous window.</p>
<pre><code>Option + [</code></pre>

---

<h2 id="command-4">Jump to Window</h2>
<p>Directly jump to a specific window by number.</p>
<pre><code>Option + 0 / 1 / 2</code></pre>

---

<h2 id="command-5">Rename Window</h2>
<p>Rename the current window.</p>
<pre><code>Option + ,</code></pre>

---

<h2 id="command-6">Split Vertical</h2>
<p>Split the pane vertically.</p>
<pre><code>Option + v</code></pre>

---

<h2 id="command-7">Split Horizontal</h2>
<p>Split the pane horizontally.</p>
<pre><code>Option + h</code></pre>

---

<h2 id="command-8">Move Between Panes</h2>
<p>Navigate between panes.</p>
<pre><code>Option + Arrow Keys</code></pre>

---

<h2 id="command-9">Kill Pane</h2>
<p>Close the current pane.</p>
<pre><code>Option + d</code></pre>

---

<h2 id="command-10">Kill Window</h2>
<p>Close the current window.</p>
<pre><code>Option + w</code></pre>

---

<h2 id="command-11">Tmux Configuration</h2>
<p>Add the following to your <code>~/.tmux.conf</code> file:</p>

<pre><code># --- Option Key (Meta) Bindings ---

# New window
bind -n M-c new-window

# Next / Previous window
bind -n M-] next-window
bind -n M-[ previous-window

# Jump windows
bind -n M-0 select-window -t 0
bind -n M-1 select-window -t 1
bind -n M-2 select-window -t 2

# Rename window
bind -n M-, command-prompt -I "#W" "rename-window '%%'"

# Split panes
bind -n M-v split-window -h
bind -n M-h split-window -v

# Pane navigation
bind -n M-Left select-pane -L
bind -n M-Right select-pane -R
bind -n M-Up select-pane -U
bind -n M-Down select-pane -D

# Kill pane
bind -n M-d kill-pane

# Kill window
bind -n M-w kill-window
</code></pre>

---

<h2 id="command-12">iTerm Setup</h2>
<p>Configure Option key to work as Meta:</p>

<pre><code>iTerm2 → Settings → Profiles → Keys

Left Option Key = Esc+
Right Option Key = Esc+ (optional)
</code></pre>

<p>This ensures Option key sends Meta (M-) to tmux.</p>
