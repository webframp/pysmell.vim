Pysmell.vim (Bundle compatible)

# Installation Instructions 

To use PySmell omnicompletion from inside Vim, you have to have:

1. Python support in vim (`:echo has('python')`)
2. The pysmell package in the PYTHONPATH that Vim uses: `python import pysmell` should work.
3. Add `Bundle 'webframp/pysmell.vim'` to your `.vimrc` and then run `vim +BundleInstall +qall` or `:BundleInstall` inside Vim.
4. `:setlocal omnifunc=pysmell#Complete` Note: If you want to always use pysmell for
python, do: `autocmd FileType python setlocal omnifunc=pysmell#Complete`
5. [OPTIONAL] Select a matcher of your liking - look at pysmell.vim for
options. Eg: `:let g:pysmell_matcher='camel-case'`

You can then use ^X^O to invoke Vim's omnicompletion.

You can generate debugging information by doing:

    :let g:pysmell_debug=1
    :e PYSMELL_DEBUG

Debug information will be appended in that buffer, copy and paste it
into the report.
