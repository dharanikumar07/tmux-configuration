# Tmux Keybindings (Option + Ctrl Space Setup)

<h2>Table of Contents</h2>
<ul>
  <li><a href="#tmux-commands">Tmux Commands</a></li>
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
  <li><a href="#command-11">Tmux File Configuration Commands</a></li>
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

<h2 id="tmux-commands">Tmux Commands</h2>
<table>
  <tr>
    <th>Command</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><code>tmux</code></td>
    <td>Start a new tmux session</td>
  </tr>
  <tr>
    <td><code>tmux new -s name</code></td>
    <td>Create a new named session</td>
  </tr>
  <tr>
    <td><code>tmux ls</code></td>
    <td>List all sessions</td>
  </tr>
  <tr>
    <td><code>tmux attach -t name</code></td>
    <td>Attach to a session</td>
  </tr>
  <tr>
    <td><code>tmux kill-session -t name</code></td>
    <td>Kill a session</td>
  </tr>
  <tr>
    <td><code>tmux detach</code></td>
    <td>Detach from current session</td>
  </tr>
</table>

---

<h2 id="command-11">Tmux configuration files command to write</h2>
<ul>
  <li><pre><code> nano ~/.tmux.conf </code></pre>
</li>
  <li><pre><code> tmux source-file ~/.tmux.conf </code></pre>
</li>
</ul>

---

<h2 id="command-12">Iterm Setup</h2>
<ul>
  <li>Go to iTerm2 → Settings → Profiles → Keys → set Left Option Key = Esc+ (this makes Option behave like Meta for tmux shortcuts).</li>
  <li>In the same tab, click Key Bindings → + → press Ctrl + Space → set Action = Send Hex Code → enter 0x00 (this prevents ^@ and makes it work properly with tmux).</li>
</ul>

---

<p><strong>Note:</strong></p>
<ul>
  <li>Option keys are fast but may not work over SSH</li>
  <li>Ctrl + Space works everywhere (SSH-safe)</li>
  <li>This setup gives both speed and reliability</li>
</ul>
