# vim_pyclewn
Make pyclewn can be installed though vbundle

## Update to pyclewn 2.3

## How to use
### Out-of-the-box sample code 
put this code to ~/.vimrc between

    call vundle#begin()
    call vundle#end()

, it will auto detect python3, otherwise will use python

```vim
    if globpath( substitute($PATH, ':', ',', 'g'), 'python3' ) != '' " if you had install python3
        " ################ for python3 >= 3.4 ###############
        let $PYTHONPATH .= vundle#bundle_dir.'/vim_pyclewn/usr/lib64/python3.4/site-packages' " search path for module files
        let g:pyclewn_python = 'python3'    " python3 version must >= 3.4
    else
        " ################ for python2.7 ####################
        let $PYTHONPATH .= vundle#bundle_dir.'/vim_pyclewn/usr/lib64/python2.7/site-packages' " search path for module files
    endif
    Plugin 'clwu88/vim_pyclewn'         " Make pyclewn can be installed though vbundle
```

![screenshot_01](https://github.com/clwu88/vim_pyclewn/blob/master/screenshots/screenshot_01.png)

