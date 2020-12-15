# fix_story
Ошибки, которые часто встречаются c Python и как их решать


# Установка pillow
Ошибка:

```
      During handling of the above exception, another exception occurred:

      Traceback (most recent call last):
        File "<string>", line 1, in <module>
        File "/private/var/folders/43/m0xllqv95ys08ld5pnrw0znw0000gn/T/pip-req-build-3y3g32rd/setup.py", line 814, in <module>
          raise RequiredDependencyException(msg)
      __main__.RequiredDependencyException:

      The headers or library files could not be found for zlib,
      a required dependency when compiling Pillow from source.

      Please see the install instructions at:
         https://pillow.readthedocs.io/en/latest/installation.html
```

Решение:

`pkg-config zlib --libs`
`export PKG_CONFIG_PATH=$PKG_CONFIG_PATH:/usr/local/Cellar/zlib/1.2.11/lib/pkgconfig/`

# Установка psycopg2-binary

Ошибка:

```
      psycopg/pqpath.c:214:17: warning: implicit conversion from enumeration type 'ConnStatusType' to different enumeration type 'ExecStatusType' [-Wenum-conversion]
                      PQstatus(conn->pgconn) : PQresultStatus(*pgres)));
                      ^~~~~~~~~~~~~~~~~~~~~~
      psycopg/pqpath.c:1871:11: warning: code will never be executed [-Wunreachable-code]
          ret = 1;
                ^
      psycopg/pqpath.c:1990:17: warning: implicit conversion from enumeration type 'ConnStatusType' to different enumeration type 'ExecStatusType' [-Wenum-conversion]
                      PQstatus(curs->conn->pgconn) : PQresultStatus(curs->pgres)));
                      ^~~~~~~~~~~~~~~~~~~~~~~~~~~~
      3 warnings generated.
      clang -Wno-unused-result -Wsign-compare -Wunreachable-code -fno-common -dynamic -DNDEBUG -g -fwrapv -O3 -Wall -I/usr/local/include -isysroot /Library/Developer/CommandLineTools/SDKs/MacOSX10.15.sdk -I/Library/Developer/CommandLineTools/SDKs/MacOSX10.15.sdk/usr/include -I/Library/Developer/CommandLineTools/SDKs/MacOSX10.15.sdk/System/Library/Frameworks/Tk.framework/Versions/8.5/Headers -DPSYCOPG_DEFAULT_PYDATETIME=1 -DPSYCOPG_VERSION=2.7.6.1 (dt dec pq3 ext lo64) -DPG_VERSION_NUM=130001 -DHAVE_LO64=1 -I/usr/local/include -I/usr/local/opt/openssl@1.1/include -I/usr/local/opt/sqlite/include -I/Users/p141592/Library/Caches/pypoetry/virtualenvs/backend-UcZQt5nT-py3.9/include -I/usr/local/Cellar/python@3.9/3.9.1/Frameworks/Python.framework/Versions/3.9/include/python3.9 -I. -I/usr/local/include -I/usr/local/include/postgresql/server -c psycopg/psycopgmodule.c -o build/temp.macosx-10.15-x86_64-3.9/psycopg/psycopgmodule.o
      psycopg/psycopgmodule.c:689:18: error: incomplete definition of type 'struct _is'
          while (interp->next)
                 ~~~~~~^
      /usr/local/Cellar/python@3.9/3.9.1/Frameworks/Python.framework/Versions/3.9/include/python3.9/pystate.h:17:8: note: forward declaration of 'struct _is'
      struct _is;
             ^
      psycopg/psycopgmodule.c:690:24: error: incomplete definition of type 'struct _is'
              interp = interp->next;
                       ~~~~~~^
      /usr/local/Cellar/python@3.9/3.9.1/Frameworks/Python.framework/Versions/3.9/include/python3.9/pystate.h:17:8: note: forward declaration of 'struct _is'
      struct _is;
             ^
      2 errors generated.
      error: command '/usr/bin/clang' failed with exit code 1
      ----------------------------------------
  ERROR: Command errored out with exit status 1: /Users/p141592/Library/Caches/pypoetry/virtualenvs/backend-UcZQt5nT-py3.9/bin/python -u -c 'import sys, setuptools, tokenize; sys.argv[0] = '"'"'/private/var/folders/43/m0xllqv95ys08ld5pnrw0znw0000gn/T/pip-req-build-2skz03l7/setup.py'"'"'; __file__='"'"'/private/var/folders/43/m0xllqv95ys08ld5pnrw0znw0000gn/T/pip-req-build-2skz03l7/setup.py'"'"';f=getattr(tokenize, '"'"'open'"'"', open)(__file__);code=f.read().replace('"'"'\r\n'"'"', '"'"'\n'"'"');f.close();exec(compile(code, __file__, '"'"'exec'"'"'))' install --record /private/var/folders/43/m0xllqv95ys08ld5pnrw0znw0000gn/T/pip-record-hjom9muh/install-record.txt --single-version-externally-managed --compile --install-headers /Users/p141592/Library/Caches/pypoetry/virtualenvs/backend-UcZQt5nT-py3.9/include/site/python3.9/psycopg2-binary Check the logs for full command output.
  WARNING: You are using pip version 20.3.1; however, version 20.3.3 is available.
  You should consider upgrading via the '/Users/p141592/Library/Caches/pypoetry/virtualenvs/backend-UcZQt5nT-py3.9/bin/python -m pip install --upgrade pip' command.

```

Решение:

```

```

