# emmet-vim-react-snippets

##Requirements

###Using Vundle to install the following plugins:
```
Plugin 'vim-scripts/Emmet.vim'
Plugin 'vim-scripts/WebAPI.vim'
```

###Next you need to add this to your ~/.vimrc:
```
let g:user_emmet_settings = webapi#json#decode(
\  join(readfile(expand('~/.snippets.json')), "\n"))
```

###Edit your ~/.snippets.json as following:
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



