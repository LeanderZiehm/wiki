# VIM

# Modes:
- ## Normal Mode
<Esc>       enter normal mode
gv          reselect last selection
o           create new empty line
J           join lines with adding space
gJ          join lines without space
r           replace char
R           replace multible chars till hit <ESC>
I           insert at start of line. like ^
A           instert at end of line. like $
a           instert after cursor 
/           search forward
?           serch backward
gh          ? select mode
Ctrl o      go backwards (best after gf)
Ctrl i      go forwards



- ## Visaul Mode
u           lowercase selection
U           UPPERCASE SELECTION
c           delete section and enter insert mode


- ## Command Mode:
:           enter command mode
:s@FIND@REPLACE@gc      Find and replace in line and confirm
:%s@FIND@REPLACE@gc     Find and replace in file and confirm
:put _

## Other Modes:
insert mode
replace mode
select mode (works like visual mode but similar to gui behavior)


# Cool Motions
viW

vit
vi'
A           Go to End of line in insert mode
I           Go to Start of line in insert mode
gJ          Join Line
tile tilde  Go back to last location
Ctlr o      Go Back
Ctrl i      Go forward

# Helpful Resources
[vim-cheat-sheet](https://vim.rtorr.com/)



# Related Topics:
[nvim](nvim)
