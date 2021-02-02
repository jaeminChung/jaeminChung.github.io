1.  Using org-mode to write about computer programming <http://clubctrl.com/org/prog/source.html>
2.  How to install emacs snapshot on Ubuntu <https://askubuntu.com/questions/297170/how-to-install-emacs-24-3-on-ubuntu>
    
        sudo apt-add-repository ppa:ubuntu-elisp/ppa
        sudo apt-get update
        sudo apt-get install emacs-snapshot emacs-snapshot-el
3.  How to fix emacs segmentation fault error in elementary os
    -   edit emacs.desktop file
    
        Exec=env XLIB_SKIP_ARGB_VISUALS=1 emacs %F