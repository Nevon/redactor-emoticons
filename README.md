#Redactor-emoticons

Redactor-emoticons is a plugin for the WYSIWYG editor [Redactor](http://imperavi.com/redactor/).

##Installation

Include redactor-emoticons.js in your markup:

    <script src="redactor-emoticons.js"></script>

Add the plugin to the `plugins` option and your emoticons to the `emoticons` option when you initialize Redactor:

    $('#redactor-editor').redactor({
        'plugins' : ['emoticons'],
        'emoticons' : {
            viewType: 'modal',
            items: [{
                'name': 'Happy',
                'src' : 'img/face-smile.png',
                'shortcode' : ':)'
            },
            {
                'name': 'Sad',
                'src' : 'img/face-sad.png',
                'shortcode' : ':('
            }],
            button: {
              addBefore: 'bold'
              separatorBefore: true
              separatorAfter: true
            }
        }
    });

`name` is simply used as an ALT-attribute.  
`src` is the URL to use to display the emoticon.  
`shortcode` - To quickly add an emoticon, type the corresponding shortcode, select it and press the emoticon button. Any selected text that matches a shortcode will be replaced with the corresponding image.  
`viewType` - Changes the UI for the emoticons. Default option is `modal`, also available is a `dropdown` view.
`button.addBefore`, `button.addAfter` – Set button before or after which emoticons button should be added
`button.separatorBefore`, `button.separatorAfter` – Set to add separator before and / or after emoticons button

##Usage

Click on the emoticon button to get a modal window with all your emoticons.

If you select a piece of text and press the emoticon button, any emoticons matching `shortcode` will be replaced with the appropriate image.

##Translation

The plugin only makes use of a single string, which is displayed as the modal window title as well as if you hover the emoticon button.

By default this string is "Insert emoticon". If you want to replace it, add `emoticons` to your translation array. Ex:

    var RELANG = {};
    RELANG['sv'] = {
        //Standard Redactor strings
        emoticons : 'Lägg till smiley'
    ]

##License

Copyright (c) 2013 Tommy Brunn (tommy.brunn@gmail.com)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
  
    
