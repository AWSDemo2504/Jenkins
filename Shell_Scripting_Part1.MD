(1)#!/bin/bash
MY_SHELL="bash"
echo "I like the ${MY_SHELL} shell."

(2)#!/bin/bash

for COLOR in red green blue
do
  echo "COLOR: $COLOR"
done

(3)#!/bin/bash

COLORS="red green blue"

for COLOR in $COLORS
do
  echo "COLOR: $COLOR"
done

(4)#!/bin/bash

MY_SHELL="csh"

if [ "$MY_SHELL" = "bash" ]
then
  echo "You seem to like the bash shell."
else
  echo "You don't seem to like the bash shell."
fi

(5)#!/bin/bash

HOST="google.com"

ping -c 1 $HOST

if [ "$?" -eq "0" ]
then
  echo "$HOST reachable."
else
  echo "$HOST unreachable."
fi

(6)#!/bin/bash

HOST="google.com"

ping -c 1 $HOST

if [ "$?" -ne "0" ]
then
  echo "$HOST unreachable."
fi

(7)#!/bin/bash

HOST="google.com"

ping -c 1 $HOST && echo "$HOST reachable."

(8)#!/bin/bash

HOST="google.com"

ping -c 1 $HOST

if [ "$?" -ne "0" ]
then
  echo "$HOST unreachable."
  exit 1
fi

exit 0