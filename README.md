# ABOUT
This project is a replication of the printf function in c

_printf() function takes 2 arguments: a character pointer to a string: format, \
and a 'variable arguments list': arg_list. _printf() loops through the format \
string searching for a conversion specifier, which is indicated with the '%' \
symbol. If found, the match_specifier() function loops through an array of \
structs (contianing character and function pairs) to find the specifier \
function that is matched with the given conversion specifier from the format \
string, and then returns a pointer to that paired function. _printf() uses the \
pointer to that specifier function to call the specifier function on the next \
queued argument from the arg_list. Each specifier function writes a character \
one at a time as determined from the value in arg_list. In the buffer branch \
and in the 'release: v0.1', our code writes the characters from the format \
string and the associated specifiers to the buffer, and in the 'no-buffer' \
branch, our code is instead written to standard output one at a time.
