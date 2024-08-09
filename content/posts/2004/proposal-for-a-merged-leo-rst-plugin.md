---
title: 'Proposal for a Merged Leo RST Plugin'
date: Thu, 08 Jul 2004 17:05:00 +0000
draft: false
tags: ['Uncategorised']
---

Posted today to the Leo Developer’s forum.

### Context

I have used the RST2 plugin for a couple of days translating a lab sheet for a programming exercise and think I have gotten a feel for how it works, and perhaps how it should work.

Tracking back through the forums it seems clear that the original rst plugin (developed by Josef Dalcolmo) was intended only to produce reST documents. All the nodes of an `@rst` tree would become an reST document with the headlines becoming different levels of heading.

The idea was extended by Stephen Zatz who developed a version that could produce code documentation. He added support for embedded `@file-noindent` nodes, introduced the `@rst` node for documentation (which have to contain the @ignore directive) and extracted any leo code nodes into reST preformatted code blocks with syntax colouring. This is the rst2 plugin which is enabled in preference to rst plugin in current versions of Leo 4.2. I think Edward tidied up the code and wrote the documentation that appears on the Leo website.

Unfortunately there are incompatibilities between rst and rst2 and inconsistencies between rst2 and leo that means

1.  rst2 can’t be used in the way originally planned,  
    ie to simply creation of reST documents.
    
2.  rst2 is too difficult to use for it’s stated purpose
    
3.  because of the need to create an `@rst` node for  
    reST documentation nodes,
    
4.  the need to put the `@ignored` directive in all `@rst`  
    nodes which itslef requires that `@file-nosent` nodes  
    have to  
    be used rather than `@file` or even the new `@file-thin`  
    nodes
    
5.  which itself implies that neither reST documentation, nor  
    normal leo code documentation can appear in body text.
    

### Proposal

Having played with the system I think that the incompatibilites can be removed if the usual leo interpretation of `@file` nodes are used instead of having a distinction between `@rst` and code nodes.

This is what I mean. reStructuredText (reST) is a text-only form of documentation that uses layout conventions, familiar to email users, to give the impression of typeset documentation without the need for tags. There has long been a clamour in the leo community (although not for a while now) for some form of rich text in documentation nodes. Let us propose that (at least for documentation nodes in `@rst` trees) reST becomes our rich text documentation format. \[It will do no harm if it occasionally slips into documentation nodes, and hence into tangled code, because it’s designed to work in text-only views!\]

Thus, instead of having a separate `@rst` node, I propose that the rst plugin simple assumes that within an `@rst` filename tree, text introduced with the `@` directive is valid reST text and the normal leo rules for `@file` nodes otherwise apply. That is

*   body text is code by default
    
*   body text is documentation if introduced by the `@` directive
    
*   body text can be a mixture of code and documentation when the  
    `@` and `@c` directives are use.
    

Here are the advantages as I see them

1.  The new plugin will immediately allow @rst to be used for  
    it’s original purpose. In effect, all body text in an `@rst`  
    could be assumed to be documentation.
    
2.  When a `@file` tree appears in an `@rst` tree, the rst plugin  
    assumes that it is now a code documentation tool. We simply  
    pass  
    documentation text to reST and wrap code in code blocks  
    (as now). Presumably the `@language` directive could guide the  
    syntax colouring feature.
    
3.  `@file` trees within a documented `@rst` tree would be  
    transparent. They could be cloned and reused in other non-rst  
    contexts without change.
    
4.  All the advantages of reST as a “rich-text” documentation  
    format immediately, and transparently, become available to leo.  
    Improving the readability of leo documentation nodes and the  
    readability of embedded documentation in files with sentinals.
    

The only disadvantage (perhaps not trivial) is that new-style  
Leo+reST code documentation would be incompatible with existing documentation written for rst2. The `@rst` documentation node would perhaps have to be maintained for backwards compatibility. But I have the feeling that rst plugin working has described above is actually quite natural and is certainly more “leo-nic”.

The price is increased complexity in the rst plugin code which now  
has to look inside code nodes to distinguish documentation and code sections, but presumably that code is available within the leo APIs.

### Refinements

The above proposal provides a merger of current rst and rst2 functionality. aving tried reST+Leo for code documentation there are a couple of additions that I would propose.

*   Rst2 deletes @others when it appears in code. I would prefer  
    it to put in a place holder. Perhaps `[…]`. This indicates  
    to the reader that the following code sections fill in the  
    ommited details.
    
*   Use of line numbering, the labelling (or not) of  
    **code** sections in the generated reST documentation,  
    and syntax colouring should perhaps be configuration options.
    
*   It would be nice if > could become hyperlinks.  
    Thus::
    
    def aFunction():  
    <>  
    :  
    <>  
    return "Hello There"
    
    would be “typeset”::
    
    def aFunction():  
    `<<aFunction body>>`\_  
    :  
    .. \_`<<aFunction body>>`  
    return "Hello There"
    

### Comments Welcome

I’d appreciate any comments that you have on this proposal, particularly from the authors of the rst/rst2 plugins.

As to implementation, I’m willing to have a go, but only if no-one more competent wants to take on the challenge.