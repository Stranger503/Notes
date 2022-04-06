fmt - text file formatter

gq/gw - in visual or normal mode

or better - gwip is much easier than visual and gq/gw.
or even better - !fmt %

for more - :h gq, :h gw, :h fo (format options), :h fp (format program), :h
fo-table.


why gq/gw produce same results?

gw = use Vim's internal formatter.
gq = use external format program (ex:par).
If there's no program it's fallback to Vim's internal formatter
