fis-preprocessor-extlang
========================

支持使用Smarty script, style 插件的JavaScript的语言扩展

    {%script%}
        require('./a.js');
        __inline('./b.js');
        var a = __uri('./c.js');
        //blabla
    {%/script%}
    
    {%style%}
    @import url(./a.css?__inline);
    {%/style%}

使用
====

    //install
    npm install -g fis-preprocessor-extlang


    //config
    vi <project>/fis-conf.js

    fis.merge.config({
        modules: {
            preprocessor: {
                tpl: "extlang"
            }
        },
        ....
    });
