---
layout: vera
title: Frequently Asked Questions
---

<ul id='toc'>&nbsp;</ul>

## Why do I see so many different names: Vera, Mi Casa Verde, MCV, MiOS?

Vera is the name of the device being sold by Vera Control,
[previously known](http://getvera.com/news-posts/mi-casa-verde-is-now-vera-control-ltd/) as Mi Casa Verde and MCV.
MiOS is a development company for the same software engine that runs on Vera devices.
See [this post](http://forum.micasaverde.com/index.php/topic,3132.msg13469.html#msg13469) for some additional details.

## How can I check what version of the `vera` plugin I have?

You can run `ide.packages.vera.version` in the Local console.

## Debugging is not working because of an incorrect IP address. How do I fix that?

When you start debugging, the IDE may display the message with the server address: `Using 'x.x.x.x' as the debugger server address.` (You'll see the message if you are using `vera` plugin v0.12+).

If the address shown is not correct, or can't be reached from the Vera device, the debugging is not going to work.
To **set the correct address**, you can specify `debugger.hostname = 'correct.IPaddress.or.hostname'` in the [configuration](doc-configuration.html) file and restart the IDE.

## I had to reset the device and the debugging stopped working. What should I do?

If you reset all the files on the device, you probably removed one of the components that is needed for the debugging to work.
To reset the current configuration, which will restore the removed component, you can run the following command in the Local console:
`ide.packages.vera:SetSettings({regkey = ide.packages.vera:GetSettings().regkey})`.

## Where is the configuration file stored?

This is covered in the description of system [configuration](doc-configuration.html).