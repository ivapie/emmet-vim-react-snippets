# emmet-vim-react-snippets

##What it will looks like:
![emmet-vim-react-snippets](https://raw.githubusercontent.com/duteng/emmet-vim-react-snippets/master/emmet-vim-react-snippets.gif)

##How to config:
###1.Using [Vundle](https://github.com/gmarik/Vundle.vim) to install the following plugins:
```
Plugin 'vim-scripts/Emmet.vim'
Plugin 'vim-scripts/WebAPI.vim'
```

###2.Next you need to add this to your ~/.vimrc:
```
let g:user_emmet_settings = webapi#json#decode(
\  join(readfile(expand('~/.snippets.json')), "\n"))
```

###3.Edit your ~/.snippets.json as following:
```
{
    "javascript": {
        "snippets": {
            "rcc": "var React = require('react');\nvar ${cursor} = React.createClass({\n\trender: function() {\n\t\treturn (\n\t\n\t\t);\n\t}\n});",

            "pt": "propTypes: {\n\t${cursor}\n},",
            "gdp": "getDefaultProps: function() {\n\treturn {\n\t${cursor}\n\t};\n},",
            "gis": "getInitialState: function() {\n\treturn {\n\t${cursor}\n\t};\n},",

            "cdm": "componentDidMount: function() { \n\t${cursor} \n},",
            "cwm": "componentWillMount: function() {\n\t${cursor}\n},",
            "cdup": "componentDidUpdate: function(prevProps, prevState) {\n\t${cursor}\n},",
            "crw": "componentWillReceiveProps: function(nextProps) {\n\t${cursor}\n},",
            "cwun": "componentWillUnmount: function() {\n\t${cursor}\n},",
            "cwu": "componentWillUpdate: function(nextProps, nextState) {\n\t${cursor}\n},",
            "sst": "setState({\n\t${cursor}\n});"
        }
    },
    "jsx": {
        "snippets": {
            "extends": "javascript"
        }
    }
}
```
###4.Done, enjoy!


