*hier.txt*		For Vim version 7.3	   Last change: 2019 Aug 17
				    Copyright (c) 2019 Cheng Zeyi

Hier                                                                      *hier*

DESCRIPTION                    |hier-description|
USAGE                          |hier-usage|
CUSTOMIZATION                  |hier-customization|
INSTALLATION                   |hier-installation|

==============================================================================
DESCRIPTION                                                   *hier-description*

Highlight quickfix errors and location list entries in buffer. This plugin
is an enhanced version of Jan Christoph Ebersbach's orighinal vim-hier
(https://github.com/jceb/vim-hier) by providing a new command HierToggle and
the ability to echo message for the line under the cursor (referring
vim-markify: https://github.com/dhruvasagar/vim-markify).

Visit https://github.com/chengzeyi/hier.vim to get the latest version.

==============================================================================
USAGE                                                               *hier-usage*

The following commands are provided:
	:HierStart		" enable hier highlighting
	:HierStop		" disable hier highlighting
    :HierToggle     " toggle enable/disable hier highlighting
	:HierUpdate		" update error highlighting for current buffer
	:HierClear		" remove highlighting - it will be displayed
				" again when :HierUpdate is called

==============================================================================
CUSTOMIZATION                                               *hier-customization*

The highlight group can be customized by setting the following variables.
Setting a variable to the string "" will disable highlighting of that
group. Every type can be highlighted differently (error, warning, info):
	let g:hier_highlight_group_qf    = 'SpellBad'
	let g:hier_highlight_group_qfw   = 'SpellLocal'
	let g:hier_highlight_group_qfi   = 'SpellRare'

	let g:hier_highlight_group_loc   = 'SpellBad'
	let g:hier_highlight_group_locw  = 'SpellLocal'
	let g:hier_highlight_group_loci  = 'SpellRare'

Enable/disable highlighting highlighting by default:
	let g:hier_enabled               = 1

Enable echo message for the line under cursor:
    let g:hier_echo_current_messagee = 1

==============================================================================
INSTALLATION                                                 *hier-installation*

Use vim-plug or other plugin managers.

 vim:tw=78:ts=8:ft=help:norl:
