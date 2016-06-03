

To find the available printers, at a terminal type

```lpstat -p -d```

Then to pick one as the default lpd printer, type at the terminal

```lpoptions -d <printer_name>```

You can copy and paste the <printer> from the list given by lpstat -p -d

Then type 

<pre><code>lpq</pre></code>

to see if the printer you selected is now the default.
