# The xSPECTARverse

## The Vision
The xSPECTARverse is a distributed, 3D modeled, virtual world build upon world-wide-web browser/server principles.

It is "distributed" in the world-wide-web sense of distributed. Different parts of the virtual world are owned and operated by different parties. They implement their own parts of the virtual world by running "Virtual Space" servers that they make available on the internet.

Users visit the virtual world through their xSPECTARverse "browser". This is software similar to a web browser that is downloaded and installed on the user's personal computer. It serves the role of "user agent" intermediating between the human user and the remotely hosted virtual spaces.

Each "virtual space" server can be though of as a multi-user scene of downloadable content. The browser is responsible for "rendering" the downloaded virtual environment and the the people within so as to be perceived by the human user. This will initially involve rendering on a traditional monitor, but it should be presumed that in the near future enhancements will allow rendering the virtual space to a head mounted display or other more immersive implementations.

### Technical Reasoning:
This multi-owner implementation model allows the extended virtual world to be built in parallel by anyone without unnecessary centralized gatekeepers. We will be shipping a developer kit that allows anyone to build their own building (exterior) for placement into the xSPECTARverse. While also developing their own unique (interior) activities to happen within.

These can initially be built and tested in a stand-alone fashion. Once they are ready for broader testing, they can be linked to the xSPECTARverse through a managed "doorway" allowing only pre-authorized people to visit. Finally, after user-experience testing, the building and its contents can be "dropped" into the expanding xSPECTAR city for seamless new user discovery.

A distributed design allows the extended xSPECTARverse to continue operating even if the xSPECTAR project becomes a financial failure. Our metaverse is intended to be eternal the way the world-wide-web is eternal. Individual virtual space servers may come and go, but the metaverse itself continues growing and adapting to user's interests and needs.

## User Experience:
The initial entry point to the extended xSPECTARverse will be the "xSPECTAR" hosted server. xSpectar is the arrival world for all new metaverse users. Its role is to be a friendly introduction to the xSPECTARverse. A way for new users to meet other people, for those newly formed groups to discover and experience collaborative activities together.

Unlike the traditional world-wide-web, the xSPECTARverse is designed as a multi-user experience for groups of humans interacting in ways they can't in the real-world. It is a tool for socializing and group activities. Today’s social media is the place you brag to your friends about what you did when they weren't around. The xSPECTARverse is where you gather your friends for real-time shared experiences and activities, even though you happen to be physically separated.

The xSPECTAR world is a curated experience aimed at showcasing the best, most engaging activities and experiences within the metaverse. Its aim is to encourage repeat visitors with a continually updating set of attractions.

Musical groups building an audience will want to perform in venues within xSPECTAR in order to attract the broadest audience.
Brands wishing prominence within the metaverse can build a large, attractive building which draws user into their custom experiences.
But within xSPECTAR's city and lands are many less obvious places waiting to be discovered. Think of them like a prohibition era "speakeasy". We don't advertise, but somehow people find us. 
As with real-world business, many metaverse activities will fail. Our approach allows them to be quickly replaced with new activities that happen withing the existing buildings. The xSPECTARverse is focused on innovation though experimentation and iteration.

## The Land:
The xSPECTAR world is modeled as a city and the land surrounding it. The city is merely an enabler to facilitate people meeting one another and then as a group to discover activities and entertainment to experience together. There are public areas to walk though. Street performers. Groups playing Frisbee and other outdoor games. These public areas are surrounded by buildings holding an unbounded number of other activities and entertainment opportunities.

Like the real-world, some buildings hold public experiences while others hold private experiences.
### Public Buildings
Stores, Pubs, Coffee Shops are all examples of public buildings that anyone can walk into. The activities inside will differ as will the user experiences. A pub might be intended as a gathering place for meeting people you don't already know. The activities might include group conversation, sing-alongs, and maybe dancing. While a store might be a more one-on-one experience between the customer and the store keeper aimed at driving digital goods sales.
### Private Buildings
A theater with ticketed admission is an example of an otherwise public building that has private entrance requirements.

There may be "private clubs" that are only open to select people. For example, there will be private areas only accessible by those who hold an xSPECTAR agent NFT.

Private houses and apartments are another example of specialty buildings. These are only for use by the owners and their invited guest. Once someone acquires their own private home withing xSPECTAR, that will become their future entry point into the metaverse. This avoids them entering among the new users and tourist having their first adventure.
### Outside the City
The surrounding landscape enables extended adventures inappropriate to a dense urban area. Just because the area is outside the city doesn't mean it must be inconvenient to travel to. Ours is a virtual space where people can "portal" to different areas directly without having to journey to them.

However, once arrived, the activity happening withing the landscape may require extensive wandering to complete. Activities like this might be considered "games" withing the greater xSPECTARverse. You can play a game in the verse, but the verse itself is not a game.

## Technical Reasoning:
The city and lands of xSPECTAR also serves as the launching point into the extended xSPECTARverse. Just because a building exists within the xSPECTAR's city doesn't imply that the activities that happen within are actually owned, operated or even hosted by xSPECTAR. The client/server model allows "doors" within xSPECTAR to lead to servers anywhere in the world.

This allows xSPECTAR users to discover activities, like gambling, that may not be allowed in all jurisdictions. A "doorway" within xSPECTAR can authenticate and authorize those legally allowed to gamble, then transfer them directly to a separate metaverse server hosted by licensed casino operators.

# Componenent Model
![ComponentModel](https://github.com/BobWay/xSPECTAR/assets/4283011/16adf8c0-766a-4666-8897-3947c7e192a8)

The xSPECTARverse is a distributed, 3D modeled, virtual world build upon world-wide-web browser/server principles.

Each metaverse user will run their own downloaded “xSPECTAR Browser” software. This application is analogous to a web browser, except instead of rendering HTML it renders 3D modeled multi-user environments.

Each 3D modeled environment is hosted on the internet by a “Virtual Space” server. This server is responsible for delivering the 3D models to the browser as “downloadable content”. As each virtual space will contain multiple user avatars, the server is also responsible for synchronizing model changes and user behavior across all connected browsers.

# Browser Notes

The xSpectar Browser connects to the Virtual Space server via some type of TCP connection. This might be HTTP, WebSocket or anything appropriate that might already exist in the Unreal Engine development kit. The only think important is that the browser be able to move easily from one server to another.

The Browser should keep a local cache of the downloaded models. This is primarily for efficiency of rendering and for returning quickly to previously visited places.

But a secondary REQUIREMENT is to allow the user access to the models in the case the user may want to modify the default models for his own local machine needs. I call this feature “hack-ability”. It should be possible for interested users to “mod” the models even if the process of modding is not user friendly.

# Server Notes

A virtual space server instance represents a single 3D modeled environment occupied by one or more users (via their avatars). It is possible to have several instances of the same environment running at the same time, each occupied by different people. Perhaps the room represents a billiard room appropriate for a single group of people. Each time a new group of people wishes to enter and play, their own personal room instances is created where their group can play in private. When the group leaves, the instance can simply be shut down.

Another use for instances is when there are many apartments based on a common model. As each owner enters, their personal apartment instance is launched and reset to the prior state it was in when they left.

## Doors

Each room (virtual space) can have multiple doors leading to spaces hosted by other server instances. These doors are similar to the double locked doors of connecting hotel rooms.

Upon “request to exit” the door must determine via the current room’s configuration, if the user is authorized to exit through that particular door. If not, that door is seen as “locked”. This feature allows an environment to contain “hidden doors” that are only revealed to those authorized to see them.

Next, the door must determine, from the destination room’s server, whether the user is authorized to enter the destination room. If not, the door remains “locked” and the user remains in the current environment. Entry authorization must always be performed in order to prevent unauthorized access via externally created doorways.

Technically, this “verify before exit” process prevents 404 “Not Found” type errors where the current environment is destroyed before it is determined that the destination exists and is accepting.

## Configuration

It is presumed that each Virtual Space will require some specific configuration based on its function. This may include rules about who is authorized to enter the room. For example, only the apartment’s owner may enter alone. Others are allowed only when the owner is present.

There may also be instantiation and hibernation rules which are intended to preserve the state of the room between uses. Of course in other cases, as with a hotel room, everything may return to its default state upon return.

The existence of doorways and their particular authorization rules should be specified through configuration.

It is important that doorways NOT be implemented at 3D model level. Models will likely be reused across different configurations. Connecting them directly will likely make it difficult to authenticate users and Authorize access dynamically.

## Dynamic State

While users are present and interacting with the virtual space, it is presumed that the models dynamic state will change and need to be synchronized across multiple browsers. This dynamic state should also be quickly accessible in the case that a new user enters the room and his browser needs to be updated from the initial configuration to the current state.

In some cases, the state of the environment may need to be preserved upon exit or room hibernation. This is the case for Owned Apartments and other locations with deliberately persistent state.

It is unclear to me how this is done using Unreal Engine tool kit, so I have represented that here as a database/storage icon.

# Multi-server Instance Model

This drawing represents the above component diagram instantiated as three users connected to a metaverse consisting of four virtual spaces connected by three doorways.

![Multi-ServerInstanceModel](https://github.com/BobWay/xSPECTAR/assets/4283011/4d092f71-6cd1-42fc-8fe3-dda5c8a5846b)

A requirement is to allow groups of people to move through a doorway together. Thus assuring that they all arrive in the destination environment together.

This can be done through multi-user authorization as the group approaches a doorway and “requests to exit”. Once group authorization is complete, each user’s browser should be redirected to the same destination server instance.

Note: This process must work the same whether the two room instances are running on the same server hardware, or separated on different machines scattered across the internet.

![Multi-ServerInstanceModel2](https://github.com/BobWay/xSPECTAR/assets/4283011/568ceac3-e55d-462a-884b-af4a2cf75e14)

# Target Audience
I’ll expand on this with details, but currently we see five separate classes of users who might be interested in the xSPECTARverse.

* Crypto Folks
  * Land Owners
  * NFT Owners
  * Token Holders 
These are the people who are currently funding the project. They are very important to our success, but they are not likely to be our initial “active daily user base”.

 
* Tourists - pre-users, look but don't touch
* Users - (Bring the Money) 
Regular people who work day jobs and bring their money with them to the metaverse are the “active daily users” that will sustain the metaverse as an economy. These users will be critical to our success.

But before people can become “active daily users” they must first discover the xSPECTARverse and become intrigued by it. These are the “tourists” interested in learning about the verse and perhaps peering into it via video without making the commitment of downloading software and actually visiting.

It is our job to make what the “tourists” see compelling enough for them to download the browser and actually make their first visit to the xSPECTARverse.

* Creative People
  * Attractions
  * Entertainers
  * Activity/Experience
  * Influencer
* Builders
  * Lease Buildings
  * In-verse Business - (sell in verse)
  * Brand Experiences - (sell in real-world)

Some people are going to be more compelled by the possibilities of the xSPECTARverse than others. These are the people who look at our metaverse platform and they see personal opportunity for themselves. These are the people who will attract the vast majority of our “active daily users”.

These people are analogous to those who made themselves influencers on instagram. Or those who started their own channels on YouTube. Or those who gained fame streaming themselves on Twitch.

These are our initial target audience.

* Advertisers - (Also bring some money)
  * Build experiences
  * Hire influencers
  * In-verse advertising

Advertisers will be quick to see the possibilities of the metaverse. But they are reliant on others to bring them a large audience. Advertisers are not likely to attract a large audience to the xSPECTARverse by themselves.

​

# What does success look like?

Success is a growing number of repeat users who bring a growing amount of money. 
This is most likely bootstrapped by:

1. Recruiting Creative People to the xSPECTARverse
 * Allowing them to perform and entertain
 * Allowing them to create fun activities and new experience
2. Having the users who discover those creative people in the xSPECTARverse
 * Bring their friends
 * Tell others about their experiences via social media
3. Allowing those entertained in the xSPECTARverse to pay those entertaining them directly.
 * With the growing profitability of creating and entertaining
 * Comes more creatives wanting build their own audience and profits
