(1)#!/bin/bash

function hello() {
    echo "Hello!"
}

hello

(2)#!/bin/bash

function hello() {
    for NAME in $@
    do
        echo "Hello $NAME"
    done
}

(3)#!/bin/bash

my_function() {
    echo "$GLOBAL_VAR"
}

# The value of GLOBAL_VAR is NOT available to my_function since GLOBAL_VAR was defined after my_function was called.
my_function
GLOBAL_VAR=1

(4)#!/bin/bash -x

TEST_VAR="test"
echo "$TEST_VAR"

(5)#!/bin/bash

DEBUG=false
$DEBUG || echo "Debug mode OFF."

(6)#!/bin/bash -x

PS4='+ $BASH_SOURCE : $LINENO : '

TEST_VAR="test"
echo "$TEST_VAR"

(7)#!/bin/bash

case "$1" in
    start)
        /usr/sbin/sshd
        ;;
    stop)
        kill $(cat /var/run/sshd.pid)
        ;;
    *)
        echo "Usage: $0 start|stop" ; exit 1
        ;;
esac

sleep 30s

(8)#!/bin/bash

while [ "$CORRECT" != "Y" ]
do
  read -p "Enter your name: " NAME
  read -p "Is ${NAME} correct? " CORRECT
done

(9)#!/bin/bash

while [ "$CORRECT" != "y" ]
do
  read -p "Enter your name: " NAME
  read -p "Is ${NAME} correct? " CORRECT
done

sleep 30s
