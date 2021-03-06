.. Generated automatically by doc/tools/makerst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the InputMap.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_InputMap:

InputMap
========

**Inherits:** :ref:`Object<class_Object>`

**Category:** Core

Brief Description
-----------------

Singleton that manages :ref:`InputEventAction<class_InputEventAction>`.

Methods
-------

+----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                       | :ref:`action_add_event<class_InputMap_action_add_event>` **(** :ref:`String<class_String>` action, :ref:`InputEvent<class_InputEvent>` event **)**     |
+----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                       | :ref:`action_erase_event<class_InputMap_action_erase_event>` **(** :ref:`String<class_String>` action, :ref:`InputEvent<class_InputEvent>` event **)** |
+----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                       | :ref:`action_erase_events<class_InputMap_action_erase_events>` **(** :ref:`String<class_String>` action **)**                                          |
+----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`    | :ref:`action_has_event<class_InputMap_action_has_event>` **(** :ref:`String<class_String>` action, :ref:`InputEvent<class_InputEvent>` event **)**     |
+----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                       | :ref:`action_set_deadzone<class_InputMap_action_set_deadzone>` **(** :ref:`String<class_String>` action, :ref:`float<class_float>` deadzone **)**      |
+----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                       | :ref:`add_action<class_InputMap_add_action>` **(** :ref:`String<class_String>` action, :ref:`float<class_float>` deadzone=0.5 **)**                    |
+----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                       | :ref:`erase_action<class_InputMap_erase_action>` **(** :ref:`String<class_String>` action **)**                                                        |
+----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`    | :ref:`event_is_action<class_InputMap_event_is_action>` **(** :ref:`InputEvent<class_InputEvent>` event, :ref:`String<class_String>` action **)** const |
+----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Array<class_Array>`  | :ref:`get_action_list<class_InputMap_get_action_list>` **(** :ref:`String<class_String>` action **)**                                                  |
+----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Array<class_Array>`  | :ref:`get_actions<class_InputMap_get_actions>` **(** **)**                                                                                             |
+----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`    | :ref:`has_action<class_InputMap_has_action>` **(** :ref:`String<class_String>` action **)** const                                                      |
+----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                       | :ref:`load_from_globals<class_InputMap_load_from_globals>` **(** **)**                                                                                 |
+----------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+

Description
-----------

Manages all :ref:`InputEventAction<class_InputEventAction>` which can be created/modified from the project settings menu ``Project > Project Settings > Input Map`` or in code with :ref:`add_action<class_InputMap_add_action>` and :ref:`action_add_event<class_InputMap_action_add_event>`. See :ref:`Node._input<class_Node__input>`.

Tutorials
---------

- `#inputmap <../tutorials/inputs/inputevent.html#inputmap>`_ in :doc:`../tutorials/inputs/inputevent`

Method Descriptions
-------------------

.. _class_InputMap_action_add_event:

- void **action_add_event** **(** :ref:`String<class_String>` action, :ref:`InputEvent<class_InputEvent>` event **)**

Adds an :ref:`InputEvent<class_InputEvent>` to an action. This :ref:`InputEvent<class_InputEvent>` will trigger the action.

.. _class_InputMap_action_erase_event:

- void **action_erase_event** **(** :ref:`String<class_String>` action, :ref:`InputEvent<class_InputEvent>` event **)**

Removes an :ref:`InputEvent<class_InputEvent>` from an action.

.. _class_InputMap_action_erase_events:

- void **action_erase_events** **(** :ref:`String<class_String>` action **)**

Removes all events from an action.

.. _class_InputMap_action_has_event:

- :ref:`bool<class_bool>` **action_has_event** **(** :ref:`String<class_String>` action, :ref:`InputEvent<class_InputEvent>` event **)**

Returns ``true`` if the action has the given :ref:`InputEvent<class_InputEvent>` associated with it.

.. _class_InputMap_action_set_deadzone:

- void **action_set_deadzone** **(** :ref:`String<class_String>` action, :ref:`float<class_float>` deadzone **)**

.. _class_InputMap_add_action:

- void **add_action** **(** :ref:`String<class_String>` action, :ref:`float<class_float>` deadzone=0.5 **)**

Adds an empty action to the ``InputMap`` with a configurable ``deadzone``.

An :ref:`InputEvent<class_InputEvent>` can then be added to this action with :ref:`action_add_event<class_InputMap_action_add_event>`.

.. _class_InputMap_erase_action:

- void **erase_action** **(** :ref:`String<class_String>` action **)**

Removes an action from the ``InputMap``.

.. _class_InputMap_event_is_action:

- :ref:`bool<class_bool>` **event_is_action** **(** :ref:`InputEvent<class_InputEvent>` event, :ref:`String<class_String>` action **)** const

Returns true if the given event is part of an existing action. This method ignores keyboard modifiers if the given :ref:`InputEvent<class_InputEvent>` is not pressed (for proper release detection). See :ref:`action_has_event<class_InputMap_action_has_event>` if you don't want this behavior.

.. _class_InputMap_get_action_list:

- :ref:`Array<class_Array>` **get_action_list** **(** :ref:`String<class_String>` action **)**

Returns an array of :ref:`InputEvent<class_InputEvent>`\ s associated with a given action.

.. _class_InputMap_get_actions:

- :ref:`Array<class_Array>` **get_actions** **(** **)**

Returns an array of all actions in the ``InputMap``.

.. _class_InputMap_has_action:

- :ref:`bool<class_bool>` **has_action** **(** :ref:`String<class_String>` action **)** const

Returns ``true`` if the ``InputMap`` has a registered action with the given name.

.. _class_InputMap_load_from_globals:

- void **load_from_globals** **(** **)**

Clears all :ref:`InputEventAction<class_InputEventAction>` in the ``InputMap`` and load it anew from :ref:`ProjectSettings<class_ProjectSettings>`.

