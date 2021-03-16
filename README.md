# An Analysis of "Scorched Earth and Chemical Weapons Attacks in Darfur"

## Introduction

#### Brief Overview

This web map outlines specific instances of human rights violations that occurred during 2016 in the Jebel Marra region of Darfur, Sudan. Though the Sudanese government engaged in military action in the region to put down a rebellion, there have been numerous instances documented that show that the government carried out attacks against the civilian population of Jebel Marra. This web map displays specific locations where these human rights violations occurred, and shows visual evidence of villages that were burned and where chemical attacks happened.

To view the platform itself, follow the link here: http://darfurconflict2016.amnesty.org/report/7


#### Goal of the project

The primary goal of this project is to show the public specific documentation of human rights violations and combine this documentation into one platform. The website itself also gives details of the project's goals when the "About the Platform'' button is clicked:

```"The goal of this collaboration and the platform itself is to render visible the developments and scale of ongoing human rights violations in a remote and inaccessible part of Sudan"```

Overall, the project is aimed to drive awareness of these attacks, the human rights violations that occurred, and detail how some of these attacks happened with eye-witness accounts.

#### Major Functions

The platform has three major functions:

1) To give an overview of the attacks that occured by plotting the location of the attacks
2) To visually display villages that were clearly damaged/destroyed as a result of an attack through satellite imagery (before and after photos), as well as eye-witness testimony of the attacks
3) To display locations in which chemical weapons were used, as well as eye witness accounts of the chemical attacks, and photos of the injuries that occured as to provide evidence of the use of chemical weapons.

#### Web Elements

One of the primary elements used on this platform is a leaflet web map that is centered on the Jebel Mara region of Darfur. Depending on which button is pressed, the web map changes size to accommodate other elements on the screen. The map displays various markers of where the attacks occured, and most of the markers have a pop-up text box once clicked by the user.

The left most side of the page primarily consists of drop down buttons, text boxes and other buttons. When a button is clicked, it displays additional text to provide more context about the subject. For example, when the dropdown button "Burned Villages" is pressed, it displays a text box that outlines when these villages began getting attacked and how these villages were often burned in the process. There are also three other standard buttons that users can press to get additional information. This includes the bottom for "Link to the Report", "Take Action", and "About the Platform". Pressing "Link to the Report" will take the user to another site where they can download a report of the atrocities that occured, whereas "Take Action" and "About the Platform" will open up in-page text pop-ups that provide additional information about the project and how people can take action.

There are also icons on the bottom left of the screen that allow people to share the platform on either Twitter or Facebook.

#### Audience

The audience for this project appears to be members of the general public, members of the various governments, and people who are looking to be educated about injustices throughout the world.

Since these attacks occured in highly dangerous and unstable regions of Sudan, it can be challenging to fully investigate the claims about the attacks. However, through the use of satellite imagery, it can be difficult to hide clear destruction. Before and after satellite images shown on this page help to provide evidence for the claims made, as getting additional documentation (photos of burned villages, bodies, residue of chemical weapons) is unfeasible to get since the area is so dangerous. It would be difficult to get a team of outsiders into the region without putting their lives at risk.

I think another important audience are people who want to make a greater contribution to hold people accountable for events such as this. When a user clicks the "Take Action" button, they are directed to sign up for the "Amnesty Decoders" project, which is a group of volunteers who helps Amnesty International do their research. Here is how Amnesty International describes the project:

```"Amnesty Decoders is an innovative platform for volunteers around the world to use their computers or phones to help our researchers sift through pictures information and documents"```

Source:https://decoders.amnesty.org/


#### Authors and their affiliations

The primary authors of this project are Amnesty International and SITU Research.

Amnesty international is an organization that fights against human rights abuses across the world, and helps raise awareness of abuses, who was affected by them, and who caused them.

According to the platform page, SITU Research "is an interdisciplinary practice working in design, visualization and spatial analysis" (background information on SITU research can be found by clicking on the "About the Platform Button"). Based on the description given, it appears that SITU Research's main work on this project was to design the interactive platform, while Amnesty International gathered the data for the platform.

#### Data Collection Date

It is not clear specifically when the data was collected, though we can assume most of the data was collected at various points in 2016 since this is the date in which the report the platform was based on was published. Additionally, it looks as though Amnesty International collected data between January and September of 2016, potentially indicating that there could have been further attacks that occurred outside this time window (source: pg. 4-5 of the Amnesty International report: https://www.amnesty.org/en/documents/afr54/4877/2016/en/).

#### Data Sources

The data sources for this project appear to be individuals who witnessed the attacks first hand and were interviewed by Amnesty International. Additionally, satellite imagery was also a source for confirming the destruction of villages in the region, as the satellite images showed clear signs of burned areas and rubble where the villages were located.

Additionally, Amnesty International sought outside advice to help verify claims that chemical weapons were used. While it cannot be confirmed with complete confidence that chemical weapons were used (since this would require investigators to travel to the region to conduct their analysis), the experts they consulted deemed that the pictures of injuries and symptoms of survivors "strongly suggest that chemical weapons agents were used in the attacks" (source: pg. 5 of the Amnesty International report: https://www.amnesty.org/en/documents/afr54/4877/2016/en/).

## Systematic Architecture

#### Client:

- This web app appears to use a variety of stylesheets, though Bootstrap appears to be the primary front-end framework used for this site.
- Leaflet.js is one of the other major frameworks used. While Bootstrap might be useful for general front-end work, Leaflet.js is the backbone for creating the map functionality on the page.

Additional services used:
- JQuery
- Bing.js
- facebook-jssdk
- AWS

#### Server

- Some of the images come from AWS, while others are stored in local files on the browser

#### Data

- It appears that much of the data has already been loaded onto the client side. But some of the data also appears to be coming from AWS since certain icon images are linked under AWS file names.
- Additionally, it looks as though the actual marker location itself was hardcoded into the Leaflet map object itself, as there are no geoJSON or other spatial data files to be found.
- I wasn't able to find any obvious open connections to databases, which further reinforces my belief that most of the data is just being loaded directly onto the clients browser as opposed to making any calls to geodatabases when the user interacts with the site.


Major functions:

- There is a Google Analytics function which is presumably used to track how users interact with the site. By including this function, Amnesty International and SITU are able to measure the performance of the site and measure what they might need to improve on.


## UI/UX Critique

While this project is somewhat responsive in the sense that it can be resized to fit larger or smaller browser sizes, it is not completely responsive. In fact, it cannot work on mobile devices at all. When I attempted to view the platform on my phone, I received a message that simply said "this platform, a collaboration between SITU Research and Amnesty International, is optimized for desktop viewing." Even though it might be optimized for desktop viewing, I think this might be a major turn off for many users, since many people use their phones as their primary means of browsing the internet. Amnesty International has limited opportunities to get users to become engaged in their platform, and many people who are unable to view it on their phone will likely forget to visit the platform on their computer.

Despite this limitation, I do think that the rest of the design works well. I think they made the perfect choice in making the basemap satellite imagery, as this is the clearest possible picture for someone to see the aftermath of the attacks on the villages. The thematic layer of the map displays the locations of the various attacks that occured in the Jebel Marra region. Depending on what dropdown button is pressed on the left side of the page, the types of markers on the map change to reflect the dropdown button. For example, the "Overview" button lists points of all the recorded attacks along with their dates. The "Burned Villages'' button leads to only villages that have been verified through satellite imagery to have been burned show up as markers on the map. The same thing goes for the "Chemical Weapons” button, in which markers of locations where chemical weapons attacks occured.

## Pros and Cons of this Project

#### Pros

- This project found ways to document and verify human rights violations without directly sending people into the dangerous region in which they occured.
- The evidence presented for the attacks was visual, which can easily show the damage that occured.In addition to high quality before and after satellite images, there are also many images taken by villagers that show the damage on the ground.
- While the photos of the chemical attacks might be gruesome, the presence of them on the platform helps provide transparency over the claims since other experts outside of Amnesty International can review the evidence and offer their opinions.

#### Cons

- There does not appear to be any updates about the situation posted on the platform. Though this event occured in 2016, I am curious to know if any progress was made as a result of this platform. The way it is now, it seems like the platform was a one-off, so I'm not sure if the status of this issue. I think it would be good if they had a section within the platform where they detail any updates or any progress that has been made as a result of their advocacy efforts. While I applaud Amnesty International for documenting this issue, I'm not sure how much of a benefit the project will be if the findings were mentioned once but then never revisited.

## Further Critical Analysis

One notable thing that access to satellite imagery presents is an overwhelming sense of surveillance over the world. Despite the fact that there could be something going on in a remote/desolate area of the world, someone in a far away location can witness what happened in that remote area. In many ways, I think this idea can be scary. Everything we do can be watched by prying eyes, and we don't really get a say in the matter. The satellites are thousands of miles away from us, and there's not always much we can do to shield ourselves from this surveillance. Even for individuals, people can log onto Google Maps or Google Earth and survey quite a bit of some place. You want to know what your neighbors back yard looks like? Easy, just zoom in on their location and enable 3d buildings. You can get a pretty good sense of the location just from doing this. Is this always bad? No. But the issue is it can be difficult (or impossible) for people to opt out if they want to.

However, this surveillance also means that it can be easier to catch bad actors when atrocities are committed. As we've seen from the Amnesty International platform, satellite imagery provides evidence for things that would otherwise be difficult to prove. Better yet, the evidence is highly visual, which makes it easy for people of any background to see what has happened. Because of this, it is harder for human rights violators to deflect accusations, as the world is watching what they do. Even if they prevent people from accessing the locations in which they occur, they can still be caught. I think this is a very positive thing, and in this case I am glad that it is not so easy to shield against satellite imagery.

## References

The platform: http://darfurconflict2016.amnesty.org/report/7

The Amnesty International Report: https://www.amnesty.org/en/documents/afr54/4877/2016/en/

SITU Research: https://situ.nyc/research
