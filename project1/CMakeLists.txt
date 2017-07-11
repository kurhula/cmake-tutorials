CMAKE_MINIMUM_REQUIRED(VERSION 2.6)

PROJECT(project1 C)

if( CMAKE_COMPILER_IS_GNUCC )
    #   gcc
    add_definitions( -ggdb -fsigned-char -freg-struct-return -Wall -W -Wshadow -Wstrict-prototypes -Wpointer-arith -Wcast-qual -Winline -Werror )
else( CMAKE_COMPILER_IS_GNUCC )
    #   non-gcc (intended for clang)
    add_definitions( -ggdb -fsigned-char -Wall -W -Wshadow -Wstrict-prototypes -Wpointer-arith -Wcast-qual -Winline -Werror )
endif( CMAKE_COMPILER_IS_GNUCC )

ADD_EXECUTABLE(simple main.c)