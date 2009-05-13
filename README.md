Ginatra
=======

This project  is to make a  clone of gitweb in  Ruby and Sinatra. It  serves git
repositories out  of a specified  directory at the moment,  but i have  plans to
make  it function  just  as gitweb  does, including  leeching  config files  and
suchlike.

Installation
------------

You should be using Git 1.6.3 or later just to be sure that it all works:

    $ git --version
    git version 1.6.3

You'll need a few gems just to serve git repositories:

    (sudo) gem install sinatra grit coderay

To run the test suite, you also need:

    (sudo) gem install rspec webrat rack-test cucumber 
    
Then clone this repository:

    git clone git://github.com/lenary/ginatra.git
    
You'll  also need  to  (`--bare`) clone  `atmos/hancock-client`  into the  repos
directory and call it test: (don't ask, it was just a repo i chose at random)

    cd repos && git clone --bare git://github.com/atmos/hancock-client.git test.git
    
Usage
-----
        
If you're just using it in development, use the following to run Ginatra:

    ruby ginatra.rb
    
There are issues running sinatra on passenger. We discourage Ginatra's use on passenger until we can make it stable.

To clone repositories so that Ginatra  can see them, clone the repositories into
`./repos/` - they will be served  automatically. Use the `--bare` switch to both
save space and  make sure Ginatra can  read them. If you rename  them, make sure
the directory ends in `.git`. For Example:

    cd repos
    git clone --bare git://github.com/lenary/ginatra.git
    git clone --bare git://github.com/mojombo/grit.git fun.git

Authors & Thanks
----------------

**Authors:**

- Samuel Elliott (lenary)

**Thanks**

- tekkub - For help with Grit
- schacon - For help with Grit
- cirwin - For moral support and design help
- irc://irc.freenode.net/git - for any other problems I had
- Picol Project (http://picol.org) - for the icons
- sr - For help with a large sinatra error

Screenshots
-----------

![Ginatra Index](http://lenary-uploads.appspot.com/img/i?id=ag5sZW5hcnktdXBsb2Fkc3IMCxIFSW1hZ2UYuRcM&w=500&h=500 "Ginatra Index")

**Index**

![Ginatra Log](http://lenary-uploads.appspot.com/img/i?id=ag5sZW5hcnktdXBsb2Fkc3IMCxIFSW1hZ2UYuhcM&w=500&h=500 "Ginatra Log")

**Log**

![Ginatra Commit](http://lenary-uploads.appspot.com/img/i?id=ag5sZW5hcnktdXBsb2Fkc3IMCxIFSW1hZ2UYuxcM&w=500&h=500 "Ginatra Commit")

**Commit**

![Ginatra Tree](http://lenary-uploads.appspot.com/img/i?id=ag5sZW5hcnktdXBsb2Fkc3IMCxIFSW1hZ2UYuxcM&w=500&h=500 "Ginatra Tree")

**Tree**

Licence
-------

The MIT License

Copyright (c) 2009 Samuel Elliott

Permission is hereby granted, free of charge,  to any person obtaining a copy of
this software  and associated documentation  files (the "Software"), to  deal in
the Software  without restriction,  including without  limitation the  rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to  whom the Software is furnished to do so,
subject to the following conditions:

The above copyright  notice and this permission notice shall  be included in all
copies or substantial portions of the Software.

THE  SOFTWARE IS  PROVIDED "AS  IS", WITHOUT  WARRANTY OF  ANY KIND,  EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR  PURPOSE AND NONINFRINGEMENT. IN NO EVENT  SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE  LIABLE FOR ANY CLAIM, DAMAGES OR  OTHER LIABILITY, WHETHER
IN  AN ACTION  OF  CONTRACT, TORT  OR  OTHERWISE,  ARISING FROM,  OUT  OF OR  IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.