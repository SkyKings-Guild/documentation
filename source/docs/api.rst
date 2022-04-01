API
=============

We have a public API that allows you to access public data that we store.

The API's base URL is ``https://skykings.net/api/``.

.. warn::

    The API is very unstable right now, and will be subject to many changes in the near future.

Authorization
--------------

All endpoints require an ``Authorization`` header containing a valid API key.

Example:
``Authorization: abcdefghijklmnopqrstuvwxyz``

You can obtain an API key by opening a ticket at https://skykings.net/discord.

Ratelimiting
-------------

All endpoints have a ratelimit of 60 requests per minute.

Developers are expected to implement proper ratelimit handling with the headers the API returns:

- ``X-RateLimit-Limit`` - The amount of requests you can make

- ``X-RateLimit-Remaining`` The amount of requests you have left

- ``X-RateLimit-Reset`` The timestamp in UTC when the ratelimit resets

- ``Retry-After`` - Seconds until the ratelimit resets

Violating the ratelimit will result in a 429 response.

Repeated violations of the ratelimit are logged and an API ban may be issued for your IP.
Your API key will also be invalidated.

Errors
-------

When an error occurs, the response will be a JSON object with ``success`` set to ``false`` and a ``reason`` field
detailing what went wrong.

.. code-block:: json

    {
        "success": false,
        "reason": "The endpoint requested does not exist"
    }


Endpoints
----------

``uuid?id=<id>``
    Returns the UUID of the user with the given ID.

    Parameters:
        - ``id``: The user's Discord ID

    Returns:
        .. code-block:: js

            {
                "uuid": "uuid", // User's Minecraft UUID, non dashed
                "success": true,
            }

``id?uuid=<uuid>``
    Returns the ID of the user with the given UUID.

    Parameters:
        - ``uuid``: The user's Minecraft UUID

    Returns:
        .. code-block:: js

            {
                "id": "1234567890", // Player's Discord ID
                "success": true,
            }

``scammer?id=<id>&type=<type>``
    Returns scammer entries for a player or user.

    Parameters:
        - ``id``: The user's Discord ID or Minecraft UUID, depending on the ``type`` parameter.
        - ``type``: The scammer type to return. Can be ``user`` for a Discord user or ``player`` for a Minecraft player.

    Returns:
        .. code-block:: js

            {
                "data":[
                    {
                        "reason": "Scammed 350k by Fake Basket of Seeds Trade.", // Entry reason
                        "type": 1, // Entry type, 1 for scammer, 2 for IRL trader
                        "user": "user" // Either a Discord user ID or a Minecraft UUID, non dashed
                    }
                ],
                "success": true
            }
