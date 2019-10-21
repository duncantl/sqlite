
If, when you run make after configure, you get a message about aclocal-1.15 being missing,
e.g.,
```
CDPATH="${ZSH_VERSION+.}:" && cd . && /bin/sh /Users/duncan/Projects/SQLite/sqlite-autoconf-3290000/missing aclocal-1.15 
/Users/duncan/Projects/SQLite/sqlite-autoconf-3290000/missing: line 81: aclocal-1.15: command not found
WARNING: 'aclocal-1.15' is missing on your system.
         You should only need it if you modified 'acinclude.m4' or
         'configure.ac' or m4 files included by 'configure.ac'.
         The 'aclocal' program is part of the GNU Automake package:
         <http://www.gnu.org/software/automake>
         It also requires GNU Autoconf, GNU m4 and Perl in order to run:
         <http://www.gnu.org/software/autoconf>
         <http://www.gnu.org/software/m4/>
         <http://www.perl.org/>
make: *** [aclocal.m4] Error 127
```
run the command
```
autoreconf -f -i
```
See
https://stackoverflow.com/questions/33278928/how-to-overcome-aclocal-1-15-is-missing-on-your-system-warning
for the solution and explanation related to git and timestamps.

