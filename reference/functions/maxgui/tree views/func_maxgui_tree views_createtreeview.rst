.. _func_maxgui_tree views_createtreeview:

==============
CreateTreeView
==============

CreateTreeView - 

Description
===========

.. code-block:: blitzmax

    CreateTreeView:TGadget(x,y,w,h,group:TGadget,style=0)

Create a TreeView gadget.

A TreeView provides a view of an expandable list of nodes populated with the
#AddTreeViewNode command. TreeView nodes can themselves contain nodes providing
a flexible method of displaying a hierachy of information.

[ @{Event ID} | @Description
* EVENT_GADGETSELECT | The user has selected a node.
* EVENT_GADGETACTION | The user has double-clicked a node.
* EVENT_GADGETOPEN | The user has expanded a node to reveal its child nodes.
* EVENT_GADGETCLOSE | The user has collapsed a node to hide its child nodes.
* EVENT_GADGETMENU | The user has right-cliked somewhere in the TreeView.
]

Each event will have the containing TreeView gadget as the event source and the concerned
node gadget in the EventExtra field of the #TEvent.

See Also: #AddTreeViewNode, #InsertTreeViewNode, #ModifyTreeViewNode, #TreeViewRoot,
#SelectedTreeViewNode and #CountTreeViewNodes, #SelectTreeViewNode, #ExpandTreeViewNode,
#CollapseTreeViewNode and #FreeTreeViewNode.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' createtreeview.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget=CreateWindow("My Window",50,50,240,240)
    Local treeview:TGadget=CreateTreeView(0,0,200,200,window)
    
    SetGadgetLayout treeview,2,2,2,2
    
    Local root:TGadget=TreeViewRoot(treeview)
    
    Local help:TGadget=AddTreeViewNode("Help",root)
    AddTreeViewNode "topic 1",help
    AddTreeViewNode "topic 2",help
    AddTreeViewNode "topic 3",help
    
    Local projects:TGadget=AddTreeViewNode("Projects",root)
    AddTreeViewNode "project 1",projects
    AddTreeViewNode("project 2",projects)
    AddTreeViewNode("project 3 is a big waste of time",projects)
    
    While WaitEvent()
        Print CurrentEvent.ToString()
        Select EventID()
            Case EVENT_WINDOWCLOSE
                End
        End Select
    Wend

See Also
========



