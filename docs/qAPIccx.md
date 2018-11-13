# query API for [ccMixter]

The Query API is how you get data from a ccHost site installation. This information can used as widgets in a blog or other web page, a feed or raw data for programmatic manipulation.

!!! note
    
    [Query string](https://en.wikipedia.org/wiki/Query_string) [attribute-value pairs](https://en.wikipedia.org/wiki/Attribute%E2%80%93value_pair) are often indicated with **strongly emphasized** attributes and *normally emphasized* values.

## Parameter Passing
No matter what the calling context, the information in the results and how they are formatted are controlled by setting up parameters and values using the URL query parameter syntax:

> **name**=*value*&**another_name**=*another_value*

For example, to return uploads that have been tagged with either foo or bar you would say:

> **tags**=*foo+bar*&**type**=*any*

To see the results in a RSS feed format, you would add the *rss* value as a **format** (f for short) parameter:

> **tags**=*foo+bar*&**type**=*any*&**f**=*rss*

Unlike the RSS format which has a pre-defined output format, the HTML format can be further controlled by specifying a **template** (**t** for short) to be used. For example, to embed the same results into a web page with links and attribution:

> **tags**=*foo*+*bar*&**type**=*any*&**format**=*html*&**t**=*links_by*

See the [parameter reference](#param_ref) for a detailed explanation of what parameters are available.

## Calling Context
The Query API can invoked from several contexts:

- Remotely via a URL
- Directly from PHP in a ccHost installation
- Embedded in a template in a ccHost installation
- Embedded into a topic using ccHost formatting
- Embedded into ccHost navigation tabs

### URL Remote invocation
The base URL for the Query API is `http://example.com/api/query`, where *example.com* is the base of the ccHost site installation. Parameters and values are passed URL query parameters. In the following example the **user** (**u** for short) is used to limit the results to uploads by a specific uploader:

> http://ccmixter.org/api/query?**tags**=*hip_hop*&**sort**=*name*&**u**=*teru*
> http://ccmixter.org/api/query?**f**=*rss*&**datasource**=*topics*&**type**=*review*&**u**=*victor*

This type of query request can be used anywhere an URL is used, however only certain formats make sense in some URL contexts. For example, when typing in an URL in your browser, only the f=page is useful. When embedding into a blog use **f**=*html* or if used in the SRC parameter of a `<script>` then **f**=*docwrite* should be used.

### Directly from PHP
Developers that write extensions to ccHost use the URL query syntax to call the CCQuery object:

> require_once('cchost_lib/cc-query.php');  
> $query = new CCQuery();  
> $args = $query->ProcessAdminArgs('tags=hip_hop&sort=name&user=teru');  
> $query->Query($args);

In order to facilitate using query parameters passed to a URL other than api/query, either via GET or POST:

> require_once('cchost_lib/cc-query.php');  
> $query = new CCQuery();  
> $args = $query->**ProcessUriArgs**();  
> $query->Query($args);

Instead of outputting the results into the page directly, the results can be returned as a PHP array by using **f**=*php*. The following is an example of using a **dataview** to retrieve the upload_ids of all uploads by *teru* tagged as *hip_hop*:

> require_once('cchost_lib/cc-query.php');  
> $query = new CCQuery();  
> $args = $query->ProcessAdminArgs('tags=hip_hop&u=teru&**dataview=ids&b=php**');  
> $results = $query->Query($args);  
> foreach( $results[0] as $row )  
> {  
>     $id = $row['upload_id'];  
>     //...  
> }

The `$results` variable now contains an array that contains the results.

### Embedded in a template in a ccHost installation
Template developers use the URL query sytax but in a more concise way:

> %query('tags=hip_hop&t=links_by_ul&limit=5')%

### Embedded into a topic using ccHost formatting
Queries can be embedded into topic content posts in a ccHost site using the following syntax:

> [query=template=mplayer&playlist=340][/query]

### Embedded into ccHost navigation tabs
ccHost site admins can embed queries into the navigation tabs by selecting 'Query' for the tab type and entering the query. Format is always *page*.

## Concepts and Definitions
### Formats
Every query must have a **format** parameter (or **f** for short).

The **f** parameter determines how the final data is returned. There are several categories:

| Category | Format Values
|:-|:-
| HTML | page, html
| Feeds/XML | atom, rss, xspf, xml
| Javascript | js, json, docwrite
| Plain text | csv, textfile
| Special | m3u, ids, count

The default **format** is *page* which will embed the results into a full HTML page based on the current skin of the ccHost installation. For HTML without the full page use **format**=*html*.

### Templates
For the HTML **formats** *page* and *html* there are many different specialized templates that return the requested in specific HTML snippets.

See the [Templates Appendix](#templates) for details.

### Data Views
For non HTML queries a **dataview** is used to return rows of data. The **dataview** acts as a column selector while the other query parameters (such as **tags** and **user**) determine which rows to return and **sort** will determine the order.

See the [Dataview Appendix](#dataviews) section for a list of **dataview** values in the system.

### Specifying Parameters
Use parameters to select which records, how many of them and in which order.

For example in order to return the 10 latest uploads that are tagged as *sample* with an Attribution license we use the follow query:

> [**limit**=*10*&**tags**=*sample*&**lic**=*by*](http://ccmixter.org/api/query?limit=10&tags=sample&lic=by)

## Usage Cookbook
### Combining Parameters That Make Sense
When queries for a set of uploads it might be helpful to group the parameters so the results are not too limited. For example you probably never want to combine the following parameters: **collab**, **ids**, **playlist**, **remixes**, **remixesof**, and **sources** because they each return a very small set of records.

But things get interesting when you refine the results with some set parameters like **lic**, **reccby**, **remixmax**, **remixmin**, **reqtags**, **score**, **sinceu**, **sinced**, **tags**, or **user**.

Suppose that you know of a playlist (986) and you want to know which songs are available under an Attribution license:

> **f**=*html*&**t**=*links*&**playlist**=*986*&**lic**=*by*

You want to know of a cappellas by calendargirl that have been remixed less than 5 times...

> **f**=*html*&**t**=*links*&**user**=*calendargirl*&**tags**=*acappella*&**remixmax**=*5*

### Example Queries
The lastest 15 uploads sorted by user's full name
: `f=html&t=links_by&limit=15&chop=0&sort=fullname`

The latest 15 modified uploads
: `f=html&t=links_by&limit=15&chop=0&sort=last_edit`

Playlists created in the last 3 weeks that have at least 3 items
: `t=playlist_2_browse&since=3 weeks ago&minitems=3`

Playlists created by user 'teru' sorted alphabetically
: `t=playlist_2_browse&u=teru&sort=name&ord=asc`

Uploads sorted by number of playlists they are included in
: `t=playlist_2_uploads&sort=num_playlists&ord=desc`

Uploads by user 'teru' ordered by times included in playlists
: `t=playlist_2_uploads&sort=num_playlists&ord=desc&u=teru`

Raw header information about a playlier
: `f=html&t=playlist_2_info&ids=1651`

Link to the latest 5 topics on the page 'Featured Samples'
: `f=html&t=topic_page_links&limit=5&page=featured-samples`

Avatar for the user 'mcjackinthebox'
: `f=html&t=avatar&u=mcjackinthebox`

XML formatted search results for 'anthony' in user table.
: `f=xml&t=search_users&limit=5&search_type=any&search=anthony`

Yahoo! Easy Listener Flash(tm) plugin with uploads that are tagged 'remix' and either 'ambient' or 'chill'
: `f=html&t=easy_listener&limit=10&reqtags=remix&tags=ambient+chill&type=any`

Count of uploads during the month of July 2006
: `sinced=July 2006&befored=Aug 2006&f=count`

Highest recommended uploads from 3 weeks ago
: `sinced=3 weeks ago&befored=2 weeks ago&sort=num_scores`

XML with basic user info of the last 3 registered users
: `dataview=user_basic&limit=3&f=xml`

## Appendix A: Parameter Reference {: #param_ref }

| Parameter | Short Form | Description
|:-|:-|:-
| beforeu || Unix time.
| befored || Date string (see php's [strtodate](http://us.php.net/strtotime)).
| chop || Several of the embedding HTML templates will "chop" long names to this value.
| collab || Return files belonging to a given collaboration project. Value is a numeric id of the project.
| datasource || Set to topics with **format**=*rss* to get topics related feeds. (See type parameter.)
| dataview || (See [Data View section](#dataviews))
| format | f | (See [Formats section](#formats))
| ids || Comma-separated numeric ids.
| lic || (See [License Values](#license))
| limit || (See [limit](#limit))
| match || Template specific, for example `t=review_upload&match=%upload_id%` and `t=topic_thread&match=%thread_id%`
| nosort || Used with param **ids** to honor the order of ids passed in.
| offset || Combine with **limit** to page through results.
| paging || Used with **format**s *page* and *html* to include prev/next buttons. Valid values are *on* and *off*. The default for page is on, for *html* is *off*.
| playlist || Return records belonging to a specific playlist. Value is the numeric playlist id.
| rand || Set to *1* to return records in a random order.
| reccby || Return records ecommended by a user at the site. Value is the login name of the user.
| remixes || Request for remixes of a given upload id.
| remixesof || Request for remixes of a given user (value is login name).
| remixmax || Uploads that have been remixed no more than *remixmax* times.
| remixmin || Uploads that have been rmeixed no less than *remixmin* times.
| reqtags || These tags must be included in upload.
| reviewee || Review topics authored by reviewee.
| score || Uploads that have at least score number of ratings.
| search | s | Search for text words or a phrase.
| search_type || Valid values are *match* for an exact phrase, *any* for matches of any of the terms, *all* for matches of all of the terms.
| sinceu || Unix time.
| sinced || Date string (see php's [strtodate](http://us.php.net/strtotime)).
| sort || (See [Valid Sorts](#sorts))
| ord || Order of score. Valid values are *ASC* and *DESC*.
| sources || Sources of a given remix.
| tags || Return uploads with the tags (separated by '+'). For multiple tags set the type parameter to either all to see records with *all* tags or *any* to see records that have any of the tags.
| template | t | (See [Templates Appendix](#templates))
| thread || Used with forum related templates to specify the topics associated with a given thread.
| title || Used with **format**=*page* and some feed formats to display a title at the top of the page or XML file.
| type || When data source is *uploads* this is a modifier for the tags parameter. When data source is *topics* this restricts the returning records to topics of that type (e.g. *forum*, *review*, *artist_qa*, etc.) The exact types available are site specific.
| user | u | Return records that were uploaded by a certain user. Value is the login name.

### limit {: #limit }
This will tell the QAPI to return "no more than" a certain number of records. Valid values are:

numeric value
: A paging system can simulated by setting a limit, combined with **offset**.

page
: This tells the QAPI to return no more than the number of records shown on a typical page listing. This is the default value for **f**=*page*. This is assigned by the site's administrator, typically in the 10-15 range, and can not be surpassed in URL context.

feed
: This tells the QAPI to return no more than the number of records in a feed listing. This is the default value for any of the feed category of formats (*rss*, *atom*, etc.). This is assigned by the site's administrator, typically in the 15-20 range, and can not be surpassed in URL context.

query
: This tells the QAPI to return no more than the number of records in a feed listing. This is the default value for any of the non feed or page category of formats (*html*, *csv*, etc.). This is assigned by the site's administrator, typically in the 100-200 range, and can not be surpassed in URL context.

default
: This tells the QAPI to use whatever is the admin assigned value for the current context and format. This is the same as leaving out the limit parameter.

## Appendix B: License Values {: #license }

by
: Attribution

nc
: NonCommercial

sa
: Share-Alike

nod
: NoDerives

byncsa
: NonCommercial ShareAlike

byncnd
: NonCommercial NoDerives

s
: Sampling

splus
: Sampling+

ncsplus
: NonCommercial Sampling+

pd
: Public Domain

## Appendix C: Data Views {: #dataviews }
The following is a list of Data Views.

In order to peek into a Data View use he following query:

> **f**=*csv*&**limit**=*1*&**dataview**=*NAME_OF_DATA_VIEW*

replacing *NAME_OF_DATA_VIEW* with one of the following names:

content_page_blog
: Blog Content Page
: datasource - topics

count
: 

count_pool_items
: datasource - pool_items

count_ratings
: datasource - ratings

count_tags
: datasource - tags

count_topics
: datasource - topics

default
: datasource - uploads

files
: 

ids
: 

info
: Deep info for upload details

info_avatar
: Deep info (no remixes, user avatar)

links
: datasource - uploads

links_by
: 

links_by_chop
: 

links_by_dl
: 

links_by_pool
: Used by upload listing for Samples are From
: datasource - pool_item

links_dl
: 

links_extra
: 

links_short
: 

list_narrow
: datasource - uploads

passthru
: Pass Thru (noop)

playlist_detail
: Playlist details

datasource - cart

playlist_line
: 

playlist_reorder
: 

playlists
: Playlist line info

datasource - cart

pool_item
: datasource - pool_item

pool_item_history_list
: Used by upload histogram

datasource - pool_item

pool_item_list
: Pool Item Listing

datasource - pool_item

pool_item_search
: datasource - pool_item

required_args - match

pool_item_search_gen
: datasource - pool_item

required_args - match

remixes_of
: 

rss_20
: For RSS 2.0 Feed

rss_20_topics
: For RSS 2.0 Topic Feed

datasource - topics

search_remix
: required_args - match

search_remix_artist
: required_args - match

search_remix_gen
: required_args - match

search_remix_gen_artist
: required_args - match

search_remix_gen_title
: required_args - match

search_remix_title
: required_args - match

tag_alias
: Return tag aliases

datasource - tag_alias

require_arg - search

tag_cat
: Basic tag categories

datasource - tag_cat

tags
: Basic tags

datasource - tags

tags_with_cat
: Tags that only have categories

datasource - tags

topic_info
: Simple Topic Info

datasource - topics

topics
: Generic Topics

datasource - topics

upload_column
: 

upload_description
: Upload Description

datasource - uploads

upload_extra
: 

upload_histogram
: All the information needed for upload history

upload_list_wide
: Multiple upload listing (wide)

datasource - uploads

upload_menu
: 

upload_owner
: Upload name, id with owner name, id

upload_page
: All the information needed for uploads page

user_basic
: Basic user info for data mining
: datasource - user

## Appendix D: Sort values {: #sorts }
Valid sort requests depends on the data source:

| Data Source | Value | Description
|:-|:-|:-
| users | fullname | Aritst display name
|| date | Registration date
|| user | Artist login name
|| user_remixes | Number of remixes
|| remixed | Number of times remixed
|| uploads | Number of uploads
|| userscore | Artists average rating
|| user_num_scores | Number of ratings
|| user_reviews | Reviews left by artist
|| user_reviewed | Reviews left for artist
|| posts | Forum topics by artist
| uploads | Same as user +
|| name | Upload name
|| lic | Upload license
|| date | Upload date
|| last_edit | Upload last edited
|| remixes | Upload's remixes
|| sources | Upload's sources
|| num_scores | Number of ratings
|| num_playlists | Number of playlists
|| id | Internal upload id
|| local_remixes | Upload's local remixes
|| pool_remixes | Upload's remote remixes
|| local_sources | Upload's local sources
|| pool_sources | Upload's sample pool sources
|| rank | Upload Rank
|| score | Upload's ratings
| topics | name | Topic name
|| date | Topic date
|| type | Topic type
|| left | Topic tree
| collab | Same as user +
|| name | Collaboration name
|| date | Collaboration creation date
|| user | Collaboration owner (instead of every artist)
| pool_items | name | Pool item name
|| user | Pool item artist

## Appendix E: HTML Templates {: #templates }
The templates are grouped by specifc usage scenarios they where designed for.

### Formats
Designed for blogs and other off-site pages

big_contact
: Big Contact Flash Player

links
: Links to upload page

links_ul
: Links to upload page (UL)

links_by
: Links to upload page with attribution

links_by_dl_ul
: Links to upload page with attribution and download links (UL)

links_stream
: Links to upload page with attribution and stream links

links_dl
: Links to upload page with download links

links_by_ul
: Links to uploads with attribution (UL)

links_by_lic
: Links with license, attribution)

med
: Medium verbose (license, attribution, download link, tags, description)

links_by_dl_names
: Named download links (good for Y! Music player)

easy_listener
: Y!(tm) Easy Listener Player

### Topic Formats
Designed for blogs and other off-site pages (topics)

topic_page_links
: Content topic links (set page=content_page_name)
: **required_args** page

topic_dump
: Content topic links (set type=topic_type)
: **datasource** topics
: **required_args** type

news
: New blurbs (set type=news)
: **datasource** topics
: **required_args** type

topic_links_next
: Next-prev Content topic links(set page=content_page_name,topic=topic_name)
: **required_args** page

topic
: Single topic [ids = topic]
: **required_args** ids

upload_description
: Single upload descrption [ids = upload_id]
: **required_args** ids

topic_reply
: Topic text for reply form [ids = topic]
: **required_args** ids

### Object Embeddings
Object/Flash embeddings

mplayer-button
: Fabricio Zuardi's Button Player - Requires Flash

mplayer
: Fabricio Zuardi's Music Player - Requires Flash

mplayerbig
: Fabricio Zuardi's Music Player BIG - Requires Flash

yahoo_black
: Fabricio Zuardi's Player - (Yahoo Repl.)

### Page
Designed to be used within the main site

upload_page_narrow
: Single upload page (narrow)
: require_args ids

upload_page_wide
: Single upload page (wide)

### Search Results
Used by site search feature

search_forums
: For forums search results (set type=forum)
: **example** type=forum&t=search_forums&limit=30&search_type=any&s=charlie+rose
: **datasource** topics
: **required_args** type, search

search_playlists
: For playlist search results
: **example** limit=30&search_type=any&search=charlie+rose
: **datasource** cart
: **required_args** search

search_pool_items
: For pool items search results (set type=pools)
: **example** type=pools&t=search_pool_items&limit=30&search_type=any&s=rooster
: **datasource** pool_items
: **required_args** type, search

search_reviews
: For reviews search results (set type=review)
: **example** type=review&t=search_reviews&limit=30&search_type=any&s=charlie+rose
: **datasource** topics
: **required_args** type, search

search_uploads
: For upload search results
: **example** t=search_uploads&limit=30&search_type=any&s=charlie+rose
: **valid_args** search, search_type
: **required_args** search

search_users
: For user search results
: **example** t=search_users&limit=30&search_type=any&search=charlie+rose
: **datasource** users
: **required_args** search

### Ajax
Designed to be used in response to ajax requests

reviewers_recent
: 7 most recent reviewers (for menu)
: **datasource** topics

collab_thread
: Collab style topic thread (set match=collab_id)
: **example** t=collab_thread&f=html&type=collab&upload=123
: **datasource** topics
: **valid_args** type,match
: **required_args** match

pools_list
: Display remix searchable pools
: **datasource** pools

info
: Info popup for upload

collab_users
: List collab users (embedded in collab page)
: **datasource** collab_users
: **valid_args** collab

collab_files
: List files in collaboration
: **valid_args** ids, collab

playlist_2_uploads
: List playlist lines (Headless playlist with style) 
: **example** t=playlist_2_uploads&sort=num_playlists&ord=desc

playable_list
: Listing with Play All/in Window

playlist_2_head
: Playlist head (set ids=playlist_id)
: **required_args** ids

playlist_2_info
: Playlist head alt (set ids=playlist_id)
: **required_args** ids

playlist_2_nostyle
: Playlist head and listing (no styles)
: **required_args** playlist

playlist_2_popup_window
: Playlist in a popop window
: **required_args** playlist

playlists_links
: Playlist links
: **datasource** cart

ajax_menu
: Return a menu for an upload
: **valid_args** ids

playlist_2_show_one
: Show a playlist (with styles)
: **required_args** playlist

avatar
: User avatar
: **datasource** user
: **require_args** user

upload_menu
: upload_menu
: **required_args** ids

remix_pool_checks
: used by pool remix search
: **datasource** pool_items
: **dataview_param** ok

remix_checks
: used by remix search
: **dataview_param** ok

## licensing
**Some rights reserved: [CC BY-NC 3.0 US](http://creativecommons.org/licenses/by-nc/3.0/us/).** Includes significant content from [Query API 2.0 (beta)](http://ccmixter.org/query-api) on ccMixter with modifications, including the following:

- Added some punctuation.
- Changed some formatting.
- Converted HTML to Markdown-style text.
- Converted tables under “Example Queries”, “Appendix B: License Values”, and “Appendix C: Data Views” to definition lists.
- Extracted nested table under “Appendix A: Parameter Reference” and converted it into a definition list.
- Removed title “Query API 2.0 (beta)”.

[ccMixter]: http://ccmixter.org/view/media/home
