## Eventful

Largest collection of events around the world
Allows use of its data, after a license agreement.

Any use of the Eventful API requires a valid, current application key. Keys should not be shared between applications, but a single user may have any number of keys.

## Authentication
To query for data in the api, application key must be generated. Please visit the following link to generate the document.

[Generate API Key Here](http://api.eventful.com/keys)

Each API method accepts a set of authentication parameters in addition to its stated arguments:
* app_key string (app_key)
    _required_ Application key as provided by Eventful
* oauth_fieldsstring
    _optional or required depending on specific API call_ OAuth parameters (token,signature,etc).


## Authorization
  For querying the data, only app_key is required, Authorization is needed if we want to access user specific data.

## API Endpoints

All Eventful API methods are available for use via the REST XML, JSON, or YAML interfaces.
  + XML
      http://api.eventful.com/rest/events/search?location=San+Diego&app_key=<you_app_key>
  + JSON
      http://api.eventful.com/json/events/search?&location=San+Diego&app_key=<you_app_key>
  + YAML
      http://api.eventful.com/yaml/events/search?&location=San+Diego&app_key=<you_app_key>

## Searching

Searching on Eventful can be as simple as What, Where, and When. We can also search specific details, and exclude unwanted data.

we search through events, venues, performers, demands, calendar, groups, and users.

**Basics**
  * What ('q' or 'keywords'): used to search by any aspect of an event that isn't part of the category, location or time
      Example:
      http://api.eventful.com/json/events/search?keywords="NY"&app_key=XzzC7JS7sQZgR7DF
                                                 ^  
      http://api.eventful.com/json/events/search?q="NY"&app_key=XzzC7JS7sQZgR7DF
                                                 ^
  * Where ('l' or 'location'): search by city, region, postal code (ZIP), country, street address, or venue.
      Example:
      http://api.eventful.com/json/events/search?location="11217"&app_key=XzzC7JS7sQZgR7DF
                                                 ^
      http://api.eventful.com/json/events/search?l="11217"&app_key=XzzC7JS7sQZgR7DF
                                                 ^
      It's often used in concert with the 'within' and 'units' parameters to do a radius search.
      http://api.eventful.com/json/events/search?q=music&l=92103&within=10&units=miles

  * When ('t'): The 'when' argument, also called 't', is used to search within a specific time frame.
                The default is "Future"
                other human-readable time formats are supported
                keywords like "Past", "This Weekend", "Friday", "Next month", and "Next 30 days" also supported
      Examples
      http://api.eventful.com/json/events/search?q=music&l=San+Diego&t=This+Weekend
      http://api.eventful.com/json/events/search?q=music&l=San+Diego&t=9+December+2006
                                                     ^

  * Category ('c'): used to search within a category.

      http://api.eventful.com/json/events/search?q=hiphop&l=San+Diego&t=This+Weekend&c=music
                                                                     ^

## Search domains

'What' search term will be matched against a set of search domains.
  For example, "music" search for events will search the title, description, and tags for the term "music".

  To search against a specific domain, add the domain to each search term, separated by a colon (:).

  For example: title:Cats tag:musical
      http://api.eventful.com/json/events/search?q=title:music+tag:jazz&app_key=XzzC7JS7sQZgR7DF

Most attributes are searchable by domain. Here's a partial list:

  + title - matches words in the event title.
  + description - matches words in the event description.
  + tag - matches any tag. For instance, tag:music will find events with the Music tag, but not the "musical" or "Rock Music" tag.
  + owner - matches the owner of the event (venue, etc), usually the user who created the event. For instance, owner:chris_radcliff will find events owned by the user chris_radcliff.
  + going - matches any user marked as "I'm going" to the event. For instance, going:chris_radcliff will find events attended by the user chris_radcliff.
  + prop_name_value - matches a user-defined property/value combination. For instance, prop_name_value:agelimit=21 will find events with the 'agelimit' property set to '21'. (See /events/properties/add for more information about properties.)


**AND and OR**
What term:
  In the What argument, search terms are joined with AND by default, which means that each result must match all of the terms.

  _AND_ or _OR_ can be specified using *&&* or *||* to join the terms.

Where Term:
  In the Where argument, the entire string is considered a quoted search term unless separated by && or ||.

  tag:music tag:jazz
  tag:music && tag:jazz
  title:cats || title:wicked
  Where: Dallas || Houston

**Grouping and quoting**

A quoted search term (like "jazz music") can be used wherever a single-word term is used. If specifying a search domain, be sure to put the domain outside of the quotes (like tag:"Kansas City Royals").
Examples:
    "jazz music"
    title:"Jonathan Coulton" || performer:"Jonathan Coulton"

Search terms can also be grouped together with parentheses, which is most useful when joining those groups with AND or OR.
  Example: (title:Cats || title:Wicked) && tag:musical


**Excluding search terms**

It's also possible to narrow a search by excluding results that match a search term.

tag:music -tag:musical
tag:animals || dogs || (cats && -tag:musical)





------

## Significant Data

  * Search events
      * Categories : important to identify keywords to look for

      * usable endpoints
          /events/search
          /events/get
          /events/tags/list
          /events/going/list
          /events/properties/list


          /venues/get
          /venues/search
          /venues/tags/list

          /performers/get
          /performers/search
          /performers/events/list
          /performers/xids/list

          /tags/list

          /demands/search
          /demands/get


          /categories/list

      * Important elements of result
        /events/search
            id- string
            url - string
            title - string
            description -  string

            Venue
            Region
            Postal code
            created by
            event start time
            event end time


            tags -- get


            Calendar Count
            comment_count
            Performers
            <going count>



        * /venue/search
