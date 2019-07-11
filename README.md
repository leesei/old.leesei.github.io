# leesei.github.io

This is a technical blog for me to organize my knowledge.  
I was previously using [Gists](https://gist.github.com/) and ~~[My Gists](https://www.mygists.info/)~~ (now down) for tags support.  
But then I discovered [Hexo](http://hexo.io/) which can do much more, and can be edited OFFLINE with my favorite editor.  
So I switched to Hexo and uses Github pages for hosting.

## Usage

```sh
# assuming node, npm and hexo-cli are properly installed
git clone https://github.com/leesei/leesei.github.io
# install dependencies
cd leesei.github.io; npm install
# fetch theme
git clone --branch leesei.github.io https://github.com/leesei/hexo-theme-freemind.git themes/freemind

# local serve
hexo server

# generate staic site with hexo-console-optimize 
# not working for 3.0
# hexo optimize
hexo generate
hexo deploy
```
