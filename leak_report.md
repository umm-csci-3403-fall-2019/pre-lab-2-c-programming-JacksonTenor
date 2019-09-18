# Leak report

The leaking memory is allocated as the return value of strip. This gets passed to is\_clean, which never frees it. By adding free(cleaned) before the return statement in that function,the leak is taken care of.
