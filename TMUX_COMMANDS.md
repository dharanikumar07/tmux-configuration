<h2>TMUX COMMANDS</h2>
<a href="./README.md">← Back to shortcuts</a>
<h3>Table of Contents</h3>
<ul>
  <li><a href="#cmd-1">Start tmux</a></li>
  <li><a href="#cmd-2">Create Session</a></li>
  <li><a href="#cmd-3">List Sessions</a></li>
  <li><a href="#cmd-4">Attach Session</a></li>
  <li><a href="#cmd-5">Kill Session</a></li>
  <li><a href="#cmd-6">Detach Session</a></li>
  <li><a href="#cmd-7">Auto Attach/Create</a></li>
  <li><a href="#cmd-8">Run Detached Command</a></li>
  <li><a href="#cmd-9">Send Keys</a></li>
  <li><a href="#cmd-10">Split Window + Command</a></li>
  <li><a href="#cmd-11">New Window + Command</a></li>
  <li><a href="#cmd-12">Rename Window</a></li>
  <li><a href="#cmd-13">Move Window</a></li>
  <li><a href="#cmd-14">Swap Panes</a></li>
  <li><a href="#cmd-15">Resize Panes</a></li>
  <li><a href="#cmd-16">List Windows/Panes</a></li>
  <li><a href="#cmd-17">Capture Output</a></li>
  <li><a href="#cmd-18">Kill Other Panes</a></li>
  <li><a href="#cmd-19">Kill Other Windows</a></li>
  <li><a href="#cmd-20">Reload Config</a></li>
  <li><a href="#cmd-21">List Keys</a></li>
  <li><a href="#cmd-22">Tmux Info</a></li>
</ul>

<hr>

<p id="cmd-1"><strong>Start tmux</strong></p>
<p>Starts a new tmux session.<br>If no session exists, it creates one automatically.</p>
<pre><code>tmux</code></pre>
<hr>

<p id="cmd-2"><strong>Create a named session</strong></p>
<p>Creates a new session with a custom name.<br>Useful to organize projects separately.</p>
<pre><code>tmux new -s name</code></pre>
<p><strong>Example:</strong></p>
<pre><code>tmux new -s backend</code></pre>
<hr>

<p id="cmd-3"><strong>List all sessions</strong></p>
<p>Shows all running tmux sessions.<br>Helps you see active workspaces.</p>
<pre><code>tmux ls</code></pre>
<hr>

<p id="cmd-4"><strong>Attach to a session</strong></p>
<p>Reconnects to an existing session.<br>Used when you detached earlier.</p>
<pre><code>tmux attach -t name</code></pre>
<p><strong>Example:</strong></p>
<pre><code>tmux attach -t backend</code></pre>
<hr>

<p id="cmd-5"><strong>Kill a session</strong></p>
<p>Stops and removes a specific session.<br>Closes all windows and panes inside it.</p>
<pre><code>tmux kill-session -t name</code></pre>
<p><strong>Example:</strong></p>
<pre><code>tmux kill-session -t backend</code></pre>
<hr>

<p id="cmd-6"><strong>Detach from current session</strong></p>
<p>Leaves the session but keeps it running.<br>You can reattach later without losing work.</p>
<pre><code>tmux detach</code></pre>
<hr>

<p id="cmd-7"><strong>Attach or create session</strong></p>
<p>Attaches if session exists, otherwise creates it.<br>Best for quick start workflows.</p>
<pre><code>tmux new -A -s name</code></pre>
<p><strong>Example:</strong></p>
<pre><code>tmux new -A -s dev</code></pre>
<hr>

<p id="cmd-8"><strong>Run command in detached session</strong></p>
<p>Starts a session in background and runs a command.<br>No terminal is attached.</p>
<pre><code>tmux new -d -s name 'command'</code></pre>
<p><strong>Example:</strong></p>
<pre><code>tmux new -d -s server 'php artisan serve'</code></pre>
<hr>

<p id="cmd-9"><strong>Send command to session</strong></p>
<p>Sends keystrokes to a running session or pane.<br>Used for automation inside sessions.</p>
<pre><code>tmux send-keys -t name 'command' C-m</code></pre>
<p><strong>Example:</strong></p>
<pre><code>tmux send-keys -t backend 'npm run dev' C-m</code></pre>
<hr>

<p id="cmd-10"><strong>Split window + run command</strong></p>
<p>Splits current window and runs a command in new pane.<br>Only affects the current session/window.</p>
<pre><code>tmux split-window -h 'command'</code></pre>
<p><strong>Example:</strong></p>
<pre><code>tmux split-window -h 'npm run dev'</code></pre>
<hr>

<p id="cmd-11"><strong>New window + command</strong></p>
<p>Creates a new window and runs a command inside it.<br>Keeps processes separated.</p>
<pre><code>tmux new-window -n name 'command'</code></pre>
<p><strong>Example:</strong></p>
<pre><code>tmux new-window -n backend 'php artisan serve'</code></pre>
<hr>

<p id="cmd-12"><strong>Rename window</strong></p>
<p>Changes the name of a specific window.<br>Affects only that window in current session.</p>
<pre><code>tmux rename-window -t index name</code></pre>
<p><strong>Example:</strong></p>
<pre><code>tmux rename-window -t 1 api</code></pre>
<hr>

<p id="cmd-13"><strong>Move window</strong></p>
<p>Moves a window to a different position (index).<br>Helps reorder workflow in current session.</p>
<pre><code>tmux move-window -s src -t dest</code></pre>
<p><strong>Example:</strong></p>
<pre><code>tmux move-window -s 3 -t 1</code></pre>
<hr>

<p id="cmd-14"><strong>Swap panes</strong></p>
<p>Swaps positions of two panes.<br>Only affects the current window.</p>
<pre><code>tmux swap-pane -s src -t dest</code></pre>
<p><strong>Example:</strong></p>
<pre><code>tmux swap-pane -s 1 -t 2</code></pre>
<hr>

<p id="cmd-15"><strong>Resize panes</strong></p>
<p>Adjusts pane size in current window.<br>Moves pane borders by given number.</p>
<pre><code>tmux resize-pane -L 10
tmux resize-pane -R 10
tmux resize-pane -U 5
tmux resize-pane -D 5</code></pre>
<p><strong>Example:</strong></p>
<pre><code>tmux resize-pane -R 20</code></pre>
<hr>

<p id="cmd-16"><strong>List windows & panes</strong></p>
<p>Shows windows or panes in current session.<br>Useful for debugging layout.</p>
<pre><code>tmux list-windows
tmux list-panes</code></pre>
<hr>

<p id="cmd-17"><strong>Capture pane output</strong></p>
<p>Saves terminal output to a file.<br>Works only for current pane/session.</p>
<pre><code>tmux capture-pane -p > file</code></pre>
<p><strong>Example:</strong></p>
<pre><code>tmux capture-pane -p > logs.txt</code></pre>
<hr>

<p id="cmd-18"><strong>Kill other panes</strong></p>
<p>Closes all panes except the active one.<br>Only affects current window.</p>
<pre><code>tmux kill-pane -a</code></pre>
<hr>

<p id="cmd-19"><strong>Kill other windows</strong></p>
<p>Closes all windows in the current session except the active one.<br>Does NOT affect other sessions.</p>
<pre><code>tmux kill-window -a</code></pre>
<hr>

<p id="cmd-20"><strong>Reload config</strong></p>
<p>Reloads tmux config without restarting session.<br>Applies new settings instantly.</p>
<pre><code>tmux source-file ~/.tmux.conf</code></pre>
<hr>

<p id="cmd-21"><strong>List key bindings</strong></p>
<p>Displays all active tmux shortcuts.<br>Useful to debug key mappings.</p>
<pre><code>tmux list-keys</code></pre>
<hr>

<p id="cmd-22"><strong>Tmux info</strong></p>
<p>Shows internal tmux environment details.<br>Helpful for debugging issues.</p>
<pre><code>tmux info</code></pre>
<hr>