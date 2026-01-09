ChaosApp Discord Bot
====================

This Bot is currently in public beta. Please let me know if you have any
problems (either on Discord or via an issue here) and I will try to address 
them quickly. 

To install, use this link:
https://discord.com/oauth2/authorize?client_id=1444195507567071313&permissions=277025490944&integration_type=0&scope=bot+applications.commands

Basic Usage
-----------

1. ``/f`` The slash command to obtain a fractal from the Bot library
2. ``/fract`` The slash command to compute a new fractal
3. Use ``!info`` to get detailed information on the last fractal displayed. 

Note that both of these slash commands are subject to
constraints on the server's current computational burden and may be
delayed or fail depending on the current load. This is particularly the
case for ``/fract``, which can be time consuming. 

If an image receives a positive reaction (i.e. via an emoji response)
then that image will be more likely to be displayed in a subsequent 
``/f`` command.

Arguments to ``/fract``
-----------------------

Without any arguments, ``/fract`` generates a random fractal with random
colors using it's own algorithm. You can specify additional arguments to 
the ``/fract`` slash command to arbitrarily compute a fractal. 
You can specify the coordinates of the image to be computed using 

- -x0 \<left edge\>
- -x1 \<right edge\>
- -y0 \<bottom edge\>
- -y1 \<top edge\>

Color specifications
--------------------

You may specify colors in three different ways:

- CSS4 colors with no spaces, i.e. ``-color aliceblue``, 
- RGB colors with numbers between 0 and 1, e.g. ``-color "(0.5,0.2,0.9)"``,
- and HTML colors, e.g. ``-color "#FFA023"``.

Different fractal types handle colors differently, as explained below. 

Strange attractors
------------------

Strange attractor fractals are built upon the mapping

$$x \rightarrow a_1 + a_2 x + a_3 x^2 + a_4 x y + a_5 y + a_6 y^2$$

$$y \rightarrow b_1 + b_2 x + b_3 x^2 + b_4 x y + b_5 y + b_6 y^2$$

To compute a random strange attractor fractal, use ``-sta``. To 
select a particular strange attractor, use ``-st`` followed by the
12 numerical values, ``<a1> <a2> ... <a6> <b1> ... <b6>``.

Two color arguments are used (any subsequent color specifications
are ignored). Random colors will be chosen if they are not provided. 

Lyapunov fractals
-----------------

To compute a random Lyapunov fractal, use ``-lyapa``. To select 
a particular pattern, use ``-lyap <integer>``, where the user
specifies the decimal integer for which the binary representation
gives the pattern plus a ``1`` prefix. For example, 

- 5 (decimal), 101 (binary), AB (pattern)
- 18 (decimal), 10010 (binary), AABA (pattern)
- 49 (decimal), 110001 (binary), BAAAB (pattern)

Three color arguments are used (any subsequent color specifications
are ignored). Random colors will be chosen if they are not provided.

Escape-Time fractals
--------------------

To generate a random escape-time fractal, use ``-etfa``. To 
select a particular escape time fractal, you can use the
``-ftype`` argument. 

Terms of Service
-----------------

Last updated: 1/8/26

1. Acceptance of Terms:
By adding or using the ChaosApp Discord bot ("the Bot"), you agree to these
Terms of Service ("Terms"). If you do not agree, do not use the Bot.

2. Description of Service:
The Bot provides functionality within Discord servers and direct messages.
Features may change or be discontinued at any time without notice.

3. Eligibility:
You must comply with Discord’s Terms of Service and Community Guidelines to
use the Bot. The Bot is not intended for use by individuals under the age
required by Discord’s own policies.

4. Acceptable Use:
You agree not to

  - Use the Bot for illegal, abusive, or malicious purposes
  - Attempt to exploit, disrupt, or reverse engineer the Bot
  - Use the Bot to violate Discord’s Terms of Service or applicable laws

5. Data and Privacy:
The Bot's collection and use of data are governed by the Privacy Policy
(see below). By using the Bot, you consent to the data practices described
therein.

6. Availability and Reliability:
The Bot is provided on an "as-is" and "as-available" basis. No guarantees are
made regarding uptime, performance, or accuracy.

7. Termination:
Access to the Bot may be suspended or terminated at any time, with or
without notice, for any reason, including violation of these Terms.

8. Limitation of Liability
To the maximum extent permitted by law, the Bot's operator shall not be
liable for any indirect, incidental, or consequential damages arising from
use of the Bot.

9. Changes to These Terms:
These Terms may be updated periodically. Continued use of the Bot after
changes constitutes acceptance of the revised Terms.

10. Contact:
For questions or concerns regarding these Terms, create an issue on this GitHub repository. 

Privacy Policy
==============

Last updated: 1/8/26

1. Information Collected:
The Bot may collect and process the following information:

  - Discord user IDs, server IDs, and channel IDs
  - Message content only when required for functionality (e.g., commands, moderation)
  - Configuration data specific to a server or user

The Bot does not intentionally collect personal information 
outside of what Discord provides via its API.

2. How Information is Used:
Collected data is used solely to:

  - Provide and maintain the Bot’s functionality
  - Respond to user commands
  - Store user or server preferences
  - Ensure compliance with Discord policies

3. Data Storage and Retention:
   
  - Data is stored only as long as necessary for the Bot’s operation
  - Temporary data may be processed in memory and not persisted
  - Users may request deletion of stored data where applicable

4. Data Sharing:
The Bot does not sell, rent, or share collected data with third
parties, except when required by law or necessary to operate infrastructure.

5. User Rights:
Users may request information about stored data, request deletion
of stored data associated with their Discord user ID, or remove the Bot
from a server to stop further data collection.

6. Security: Reasonable technical measures are used to protect
stored data. However, no system can be guaranteed to be completely secure.

8. Children's Privacy
The Bot does not knowingly collect data from individuals under the
age required by Discord’s Terms of Service.

9. Changes to This Policy
This Privacy Policy may be updated periodically. Continued use of the
Bot constitutes acceptance of the revised policy.

11. Contact
For privacy-related questions or requests, create an issue on this GitHub repository. 
