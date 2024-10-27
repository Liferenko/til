## VScode global search RegEx

Yess, vscode mentioned :D I needed to use it within a team. With vim ext of course :)

Anyway... There was a case when I needed to find globally all defmodules with `.Address` in it.
I'd say copilot helped here faster and better than my own decade-ago knowledges about regex :) 

`defmodule\s+[\w\.]*\.Address[\w\.]*`
