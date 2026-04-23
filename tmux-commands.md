<h2>TMUX COMMANDS</h2>

<p><strong>Start tmux</strong></p>
<pre><code>tmux</code></pre>

<p><strong>Create a named session</strong></p>
<pre><code>tmux new -s name</code></pre>

<p><strong>List all sessions</strong></p>
<pre><code>tmux ls</code></pre>

<p><strong>Attach to a session</strong></p>
<pre><code>tmux attach -t name</code></pre>

<p><strong>Detach from current session</strong></p>
<pre><code>tmux detach</code></pre>

<p><strong>Kill a specific session</strong></p>
<pre><code>tmux kill-session -t name</code></pre>

<p><strong>Kill all sessions (stop tmux server)</strong></p>
<pre><code>tmux kill-server</code></pre>

<p><strong>Rename a session</strong></p>
<pre><code>tmux rename-session -t old_name new_name</code></pre>

<p><strong>Start a session and run a command</strong></p>
<pre><code>tmux new -s name 'command'</code></pre>

<p><strong>Attach to last session</strong></p>
<pre><code>tmux attach</code></pre>

<h2>ADVANCED TMUX COMMANDS</h2>

<p><strong>Attach to session (or create if not exists)</strong></p>
<pre><code>tmux new -A -s name</code></pre>

<p><strong>Run command in a new detached session</strong></p>
<pre><code>tmux new -d -s name 'command'</code></pre>

<p><strong>Send command to a session (automation)</strong></p>
<pre><code>tmux send-keys -t name 'php artisan serve' C-m</code></pre>

<p><strong>Split window and run command</strong></p>
<pre><code>tmux split-window -h 'npm run dev'</code></pre>

<p><strong>Create new window with command</strong></p>
<pre><code>tmux new-window -n backend 'php artisan serve'</code></pre>

<p><strong>Rename window from CLI</strong></p>
<pre><code>tmux rename-window -t 1 backend</code></pre>

<p><strong>Move window to another index</strong></p>
<pre><code>tmux move-window -s 3 -t 1</code></pre>

<p><strong>Swap panes</strong></p>
<pre><code>tmux swap-pane -s 1 -t 2</code></pre>

<p><strong>Resize panes (fine control)</strong></p>
<pre><code>tmux resize-pane -L 10
tmux resize-pane -R 10
tmux resize-pane -U 5
tmux resize-pane -D 5</code></pre>

<p><strong>List windows and panes</strong></p>
<pre><code>tmux list-windows
tmux list-panes</code></pre>

<p><strong>Capture pane output (logs)</strong></p>
<pre><code>tmux capture-pane -p > output.txt</code></pre>

<p><strong>Kill all panes except current</strong></p>
<pre><code>tmux kill-pane -a</code></pre>

<p><strong>Kill all windows except current</strong></p>
<pre><code>tmux kill-window -a</code></pre>

<p><strong>Reload config without restart</strong></p>
<pre><code>tmux source-file ~/.tmux.conf</code></pre>

<p><strong>Show all key bindings</strong></p>
<pre><code>tmux list-keys</code></pre>

<p><strong>Display tmux environment info</strong></p>
<pre><code>tmux info</code></pre>
