

# Remove Files utilities #

Copyright (c) 2017-2018 G-Corp

__Version:__ 0.0.1

__Authors:__ Gregoire Lejeune ([`gregoire.lejeune@gmail.com`](mailto:gregoire.lejeune@gmail.com)).


### Usage ###
Remove :

```erlang

rfile:rm(
  "s3://my_bucket/my_dir/",
  #{aws => #{access_key_id => "ABCDEFGHIJKLMNOPQRST",
             secret_access_key => "ABCDEFGHIJKLMNOPQRSTUVWXYZ+1234567890---"},
    callback => fun(Action, Args, Response, Metadata) ->
                    io:format("~ts(~p) => ~p~n", [Action, Args, Response])
                end,
    metadata => {hello, world},
    recursive => true}).

```
Copy :

```erlang

rfile:cp(
  "file:///home/erlang/data/",
  "s3://my_bucket/my_data/",
  #{aws => #{access_key_id => "ABCDEFGHIJKLMNOPQRST",
             secret_access_key => "ABCDEFGHIJKLMNOPQRSTUVWXYZ+1234567890---"},
    callback => fun(Action, Args, Response, {UserId, UserName}) ->
                    io:format("~ts(~p) => ~p~n", [Action, Args, Response])
                end,
    metadata => {UserId, UserName},
    recursive => true}).

```
List:

```erlang

rfile:rm(
  "s3://my_bucket/my_dir/",
  #{aws => #{access_key_id => "ABCDEFGHIJKLMNOPQRST",
             secret_access_key => "ABCDEFGHIJKLMNOPQRSTUVWXYZ+1234567890---"},
    callback => fun(Action, Args, Response, undefined) ->
                    io:format("~ts(~p) => ~p~n", [Action, Args, Response])
                end}).

```


### Licence ###

Copyright (c) 2017-2018 G-Corp<br />

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
* Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
* The name of the author may not be used to endorse or promote products derived from this software without specific prior written permission.



THIS SOFTWARE IS PROVIDED BY THE AUTHOR ''AS IS'' AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.



## Modules ##


<table width="100%" border="0" summary="list of modules">
<tr><td><a href="https://github.com/G-Corp/rfile/blob/master/doc/rfile.md" class="module">rfile</a></td></tr>
<tr><td><a href="https://github.com/G-Corp/rfile/blob/master/doc/rfile_storage.md" class="module">rfile_storage</a></td></tr></table>

