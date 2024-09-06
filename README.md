# fabric

Patterns for the https://github.com/danielmiessler/fabric AI tool.

Review the pattern for fabric options such as temperature.

```shell
$ cat input.txt | fabric --pattern explain_cookies --temperature=.2 --presencepenalty=.2 --stream
```

## explain_cookies

Input is:
- `.raw` file that is the raw data of the request and/or response.
- `.har` (HTTP Archive file)

```shell
$ cat request.raw | fabric --pattern explain_cookies --temperature=.2 --presencepenalty=.2 --stream

$ cat example.har | fabric --pattern explain_cookies --temperature=.2 --presencepenalty=.2 --stream

```

## create_persona

Creates a fictitious persona for use in registering accounts on targets. Input isn't required, but
recommended to at least give a city and an interest related to the target. Any amount of personal
information will inform the bot.

```shell
$ echo "St. Louis, MO, USA, travel junkie" | fabric --pattern create_persona --stream

- Name: Jordan Mitchell
- Gender: Male
- Date of Birth: March 15, 1990
- Billing Address:
  - 4782 Cedar Lane
  - St. Louis, MO 63101
  - USA
- Shipping Address:
  - Same as billing address
- Phone Number: +1 (314) 555-9721
- Email: jordan.mitchell@travellermail.com
- Password: 8!GhT3x@4Pz
- Username: wanderlust90
- Payment Card Information:
  - Card Type: Visa
  - Card Number: 4111 1111 1111 1234
  - Expiration Date: 12/25
  - CCV: 456
- Security Questions:
  - What is your favorite book? The Alchemist
  - What was the name of your first pet? Max
  - What is your mother's maiden name? Thompson
- City of Birth: Kansas City, MO, USA
- Places Lived:
  - Kansas City, MO, USA (1990-2012)
  - Chicago, IL, USA (2012-2018)
  - St. Louis, MO, USA (2018-Present)
- Education:
  - Bachelor of Arts in Communications, University of Missouri, 2012
- Job:
  - Title: Travel Blogger
  - Company: Explore More Inc.
  - Work Location: St. Louis, MO
- Personal Interests:
  - Traveling
  - Photography
  - Hiking
  - Trying new cuisines
- Personal Bio: Hey there! I'm Jordan, a total travel junkie who's been bitten by the wanderlust bug big time. I live for hitting the road, snapping epic photos, and discovering hidden gems around the world. When I'm not exploring, I'm usually planning my next big adventure or sharing stories from my travels.
- Tag Line: Adventure awaits, let's find it!
- Avatars:
  - ![Avatar 1](https://i.pravatar.cc/150?img=52)
  - ![Avatar 2](https://i.pravatar.cc/150?img=33)
  - ![Avatar 3](https://i.pravatar.cc/150?img=15)

```
