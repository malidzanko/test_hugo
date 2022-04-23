+++
author = []
categories = []
date = 2016-08-09T17:22:44Z
description = ""
draft = true
image = ""
tags = []
title = "Fix horrid blue dir colours in bash"

+++
\`\`\`

echo "LS_COLORS=\\$LS_COLORS:'di=0;35:' ; export LS_COLORS" &gt;&gt; \~/.bashrc

\`\`\`

To fix the *dir* colour in the bash prompt, not just the LS output, set this in *.bashrc*:

\`if \[ "$color_prompt" = yes \]; then  

\#PS1='${debian_chroot:+($debian_chroot)}\\\[\\033\[01;32m\\\]\\u@\\h\\\[\\033\[00m\\\]:\\\[\\033\[01;34\\\[\\033\[00m\\\]\\$'\`

\**\`PS1='${debian_chroot:+($debian_chroot)}\\\[\\033\[01;35m\\\]\\u\\\[\\033\[01;31m\\\]@\\\[\\033\[01;32m\\\]\\h\\\[\\033\[00m\\\]:\\\[\\033\[01;35m\\\]\\w\\\[\\033\[00m\\\]\\$\`**

\`else\`

\` PS1='${debian_chroot:+($debian_chroot)}\\\[\\033\[01;35m\\\]\\u\\\[\\033\[01;31m\\\]@\\\[\\033\[01;32m\\\]\\h\\\[\\033\[00m\\\]:\\\[\\033\[01;35m\\\]\\w\\\[\\033\[00m\\\]\\$ \`

\`fi\`

\` unset color_prompt force_color_prompt\`