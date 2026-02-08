KDE Plasma is using a file search application called balooctl6




# Troubleshooting

Close Plasma settings app,

Disable baloo
balooctl6 disable
check if it’s not running
balooctl6 status
you should get
Baloo is currently disabled. To enable, please run balooctl enable

Purge the index
rm -rf ~/.local/share/baloo
balooctl6 purge

Check the content of ~/.config/baloofilerc, in the line
folders[$e]=$HOME/,/mnt/989A18F59A18D19C/Books/,/mnt/989A18F59A18D19C/Courses/
remove any duplicated or unwanted entries

Enable baloo two times
balooctl6 enable
balooctl6 enable
