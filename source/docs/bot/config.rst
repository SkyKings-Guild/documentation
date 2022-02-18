Configuration
==============

This page outlines the various configuration settings you can set on the bot.

- :ref:`General Config`
- :ref:`Verification Config`
- :ref:`Guilds`
- :ref:`SkyBlock Events`


.. _General Config:

General Configuration
**********************

These settings are edited with the ``/configuration edit`` command.

You can reset a setting to its default value by leaving the value blank.

.. list-table:: General
   :header-rows: 1

   * - Key
     - Description
     - Value
     - Example
   * - ``TRIGGERS``
     - Enables or disables the bot's autoresponse. (ez, etc.)
     - Boolean
     - ``yes``, ``true``, ``off``
   * - ``NOTIFY``
     - Sets the channel bot notifications (scammer alerts) should be sent to.
     - Text Channel
     - ``#scammers``, ``1234567890``, ``scammers``
   * - ``STATUS``
     - The channel that Hypixel status updates should be sent to.
     - Text Channel
     - ``#status``, ``1234567890``, ``status``
   * - ``STATUS_PING``
     - The role that is pinged for a Hypixel status update. ``STATUS`` must be set.
     - Role
     - ``@Status``, ``1234567890``, ``Status``
   * - ``GIVEAWAYS``
     - The role that should be able to run giveaways.
     - Role
     - ``@Giveaway Runner``, ``1234567890``, ``Giveaway Runner``
   * - ``SCAMMER_ACTION``
     - The action that should be taken when a scammer joins.
     - ``Kick``, ``Ban``, Role
     - ``kick``, ``ban``, ``@Scammer``, ``1234567890``
   * - ``TRADER_ACTION``
     - The action that should be taken when an IRL trader joins.
     - ``Kick``, ``Ban``, Role
     - ``kick``, ``ban``, ``@IRL Trader``, ``1234567890``
   * - ``NEWS``
     - The channel that Hypixel news from the forums should be sent to.
     - Text Channel
     - ``#news``, ``1234567890``, ``news``
   * - ``STATUS_PING``
     - The role that is pinged for a Hypixel news forum post. ``NEWS`` must be set.
     - Role
     - ``@News``, ``1234567890``, ``News``
   * - ``PATCHNOTES``
     - The channel that SkyBlock patchnotes from the forums should be sent to.
     - Text Channel
     - ``#patchnotes``, ``1234567890``, ``patchnotes``
   * - ``PATCHNOTES_PING``
     - The role that is pinged for a SkyBlock patchnote forum post. ``PATCHNOTES`` must be set.
     - Role
     - ``@SB Updates``, ``1234567890``, ``SB Updates``
   * - ``SKYBLOCK_DATE``
     - The channel the current Hypixel SkyBlock date should be shown on. Requires the ``manage_channels`` permission.
     - Voice Channel
     - ``#Date``, ``1234567890``, ``Date``
   * - ``EVENTS_CHANNEL``
     - The channel that Hypixel SkyBlock events should be sent to. More configuration is in the :ref:`SkyBlock Events` category.
     - Text Channel
     - ``#events``, ``1234567890``, ``events``
   * - ``GLOBAL_EVENT_CHANNEL``
     - The channel that global events run by SkyKings should be sent to.
     - Text Channel
     - ``#events``, ``1234567890``, ``events``
   * - ``FETCHUR``
     - The channel that daily SkyBlock fetchur items should be sent to.
     - Text Channel
     - ``#fetchur``, ``1234567890``, ``fetchur``
   * - ``FETCHUR_PING``
     - The role that is pinged for a new fetchur item. ``FETCHUR`` must be set.
     - Role
     - ``@Fetchur Ping``, ``1234567890``, ``Fetchur Ping``
     

.. _Verification Config:

Verification Configuration
**********************

These settings are edited with the ``/configuration edit`` command. They depend on the ``VERIFICATION`` setting being enabled.

You can reset a setting to its default value by leaving the value blank.

.. list-table:: Verification
   :header-rows: 1

   * - Key
     - Description
     - Value
     - Example
   * - ``VERIFICATION``
     - Whether or not verification settings are enabled. 
     - Boolean
     - ``yes``, ``true``, ``off``
   * - ``NICK``
     - Determines a verified player's nickname. Supports variables ``name``, ``rank``, ``network_level`` and ``cata_level``.
     - String
     - ``[{rank}] {name}``, ``{name}``
   * - ``VERIFIED``
     - The role given to verified members.
     - Role
     - ``@Verified``, ``1234567890``, ``Verified``
   * - ``VIP``
     - The role given to players with VIP on Hypixel.
     - Role
     - ``@VIP``, ``1234567890``, ``VIP``
   * - ``VIP+``
     - The role given to players with VIP+ on Hypixel.
     - Role
     - ``@VIP+``, ``1234567890``, ``VIP+``
   * - ``MVP``
     - The role given to players with MVP on Hypixel.
     - Role
     - ``@MVP``, ``1234567890``, ``MVP``
   * - ``MVP+``
     - The role given to players with MVP+ on Hypixel.
     - Role
     - ``@MVP+``, ``1234567890``, ``MVP+``
   * - ``MVP++``
     - The role given to players with MVP++ on Hypixel.
     - Role
     - ``@MVP++``, ``1234567890``, ``MVP++``
   * - ``YOUTUBE``
     - The role given to players with YouTube rank on Hypixel.
     - Role
     - ``@YT``, ``1234567890``, ``YT``
   * - ``STAFF``
     - The role given to Hypixel staff members.
     - Role
     - ``@Hypixel Staff``, ``1234567890``, ``Hypixel Staff``

