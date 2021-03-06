---
name: Stack Exchange
x-slug: stack-exchange
description: After someone asks a question, members of the community propose answers.
  Others vote on those answers. Very quickly, the answers with the most votes rise
  to the top. You dont have to read through a lot of discussion to find the best answer.    Like
  to...
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
x-kinRank: "8"
x-alexaRank: "126"
tags: General Data
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/apis.md
specificationVersion: "0.14"
apis:
- name: Stack Exchange - Get Answers
  x-api-slug: answers-get
  description: "Returns all the undeleted answers in the system.\n \nThe sorts accepted
    by this method operate on the follow fields of the answer object:\n - activity
    - last_activity_date\n - creation - creation_date\n - votes - score\n  activity
    is the default sort.\n \n It is possible to create moderately complex queries
    using sort, min, max, fromdate, and todate.\n \nThis method returns a list of
    answers."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/answers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/answers-get-openapi.md
- name: Stack Exchange - Get Answer Comments
  x-api-slug: answersidscomments-get
  description: "Gets the comments on a set of answers.\n \nIf you know that you have
    an answer id and need the comments, use this method. If you know you have a question
    id, use /questions/{id}/comments. If you are unsure, use /posts/{id}/comments.\n
    \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
    look for answer_id on answer objects.\n \nThe sorts accepted by this method operate
    on the follow fields of the comment object:\n - creation - creation_date\n - votes
    - score\n  creation is the default sort.\n \n It is possible to create moderately
    complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns
    a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/answersidscomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/answersidscomments-get-openapi.md
- name: Stack Exchange - Get Comments
  x-api-slug: comments-get
  description: "Gets all the comments on the site.\n \nIf you're filtering for interesting
    comments (by score, creation date, etc.) make use of the sort paramter with appropriate
    min and max values.\n \nIf you're looking to query conversations between users,
    instead use the /users/{ids}/mentioned and /users/{ids}/comments/{toid} methods.\n
    \nThe sorts accepted by this method operate on the follow fields of the comment
    object:\n - creation - creation_date\n - votes - score\n  creation is the default
    sort.\n \n It is possible to create moderately complex queries using sort, min,
    max, fromdate, and todate.\n \nThis method returns a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/comments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/comments-get-openapi.md
- name: Stack Exchange - Get Posts
  x-api-slug: posts-get
  description: "Fetches all posts (questions and answers) on the site.\n \nIn many
    ways this method is the union of /questions and /answers, returning both sets
    of data albeit only the common fields.\n \nMost applications should use the question
    or answer specific methods, but /posts is available for those rare cases where
    any activity is of intereset. Examples of such queries would be: \"all posts on
    Jan. 1st 2011\" or \"top 10 posts by score of all time\".\n \nThe sorts accepted
    by this method operate on the follow fields of the post object:\n - activity -
    last_activity_date\n - creation - creation_date\n - votes - score\n  activity
    is the default sort.\n \n It is possible to create moderately complex queries
    using sort, min, max, fromdate, and todate.\n \nThis method returns a list of
    posts."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/posts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/posts-get-openapi.md
- name: Stack Exchange - Get Post Comments
  x-api-slug: postsidscomments-get
  description: "Gets the comments on the posts identified in ids, regardless of the
    type of the posts.\n \nThis method is meant for cases when you are unsure of the
    type of the post id provided. Generally, this would be due to obtaining the post
    id directly from a user.\n \n{ids} can contain up to 100 semicolon delimited ids,
    to find ids programatically look for post_id, answer_id, or question_id on post,
    answer, and question objects respectively.\n \nThe sorts accepted by this method
    operate on the follow fields of the comment object:\n - creation - creation_date\n
    - votes - score\n  creation is the default sort.\n \n It is possible to create
    moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
    method returns a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/postsidscomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/postsidscomments-get-openapi.md
- name: Stack Exchange - Get Post Revisions
  x-api-slug: postsidsrevisions-get
  description: "Returns edit revisions for the posts identified in ids.\n \n{ids}
    can contain up to 100 semicolon delimited ids, to find ids programatically look
    for post_id, answer_id, or question_id on post, answer, and question objects respectively.\n
    \nThis method returns a list of revisions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/postsidsrevisions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/postsidsrevisions-get-openapi.md
- name: Stack Exchange - Get Questions
  x-api-slug: questions-get
  description: "Gets all the questions on the site.\n \nThis method allows you make
    fairly flexible queries across the entire corpus of questions on a site. For example,
    getting all questions asked in the the week of Jan 1st 2011 with scores of 10
    or more is a single query with parameters sort=votes&min=10&fromdate=1293840000&todate=1294444800.\n
    \nTo constrain questions returned to those with a set of tags, use the tagged
    parameter with a semi-colon delimited list of tags. This is an and contraint,
    passing tagged=c;java will return only those questions with both tags. As such,
    passing more than 5 tags will always return zero results.\n \nThe sorts accepted
    by this method operate on the follow fields of the question object:\n - activity
    - last_activity_date\n - creation - creation_date\n - votes - score\n - hot -
    by the formula ordering the hot tab Does not accept min or max\n - week - by the
    formula ordering the week tab Does not accept min or max\n - month - by the formula
    ordering the month tab Does not accept min or max\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/questions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/questions-get-openapi.md
- name: Stack Exchange - Get Questions No Answers
  x-api-slug: questionsnoanswers-get
  description: "Returns questions which have received no answers.\n \nCompare with
    /questions/unanswered which mearly returns questions that the sites consider insufficiently
    well answered.\n \nThis method corresponds roughly with the this site tab.\n \nTo
    constrain questions returned to those with a set of tags, use the tagged parameter
    with a semi-colon delimited list of tags. This is an and contraint, passing tagged=c;java
    will return only those questions with both tags. As such, passing more than 5
    tags will always return zero results.\n \nThe sorts accepted by this method operate
    on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/questionsnoanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/questionsnoanswers-get-openapi.md
- name: Stack Exchange - Get Questions
  x-api-slug: questionsids-get
  description: "Returns the questions identified in {ids}.\n \nThis is most useful
    for fetching fresh data when maintaining a cache of question ids, or polling for
    changes.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids
    programatically look for question_id on question objects.\n \nThe sorts accepted
    by this method operate on the follow fields of the question object:\n - activity
    - last_activity_date\n - creation - creation_date\n - votes - score\n  activity
    is the default sort.\n \n It is possible to create moderately complex queries
    using sort, min, max, fromdate, and todate.\n \nThis method returns a list of
    questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/questionsids-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/questionsids-get-openapi.md
- name: Stack Exchange - Get Question Linked
  x-api-slug: questionsidslinked-get
  description: "Gets questions which link to those questions identified in {ids}.\n
    \nThis method only considers questions that are linked within a site, and will
    never return questions from another Stack Exchange site.\n \nA question is considered
    \"linked\" when it explicitly includes a hyperlink to another question, there
    are no other heuristics.\n \n{ids} can contain up to 100 semicolon delimited ids,
    to find ids programatically look for question_id on question objects.\n \nThe
    sorts accepted by this method operate on the follow fields of the question object:\n
    - activity - last_activity_date\n - creation - creation_date\n - votes - score\n
    - rank - a priority sort by site applies, subject to change at any time Does not
    accept min or max\n  activity is the default sort.\n \n It is possible to create
    moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
    method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/questionsidslinked-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/questionsidslinked-get-openapi.md
- name: Stack Exchange - Get Question Related
  x-api-slug: questionsidsrelated-get
  description: "Returns questions that the site considers related to those identified
    in {ids}.\n \nThe algorithm for determining if questions are related is not documented,
    and subject to change at any time. Futhermore, these values are very heavily cached,
    and may not update immediately after a question has been editted. It is also not
    guaranteed that a question will be considered related to any number (even non-zero)
    of questions, and a consumer should be able to handle a variable number of returned
    questions.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids
    programatically look for question_id on question objects.\n \nThe sorts accepted
    by this method operate on the follow fields of the question object:\n - activity
    - last_activity_date\n - creation - creation_date\n - votes - score\n - rank -
    a priority sort by site applies, subject to change at any time Does not accept
    min or max\n  activity is the default sort.\n \n It is possible to create moderately
    complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns
    a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/questionsidsrelated-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/questionsidsrelated-get-openapi.md
- name: Stack Exchange - Get Revisions
  x-api-slug: revisionsids-get
  description: "Returns edit revisions identified by ids in {ids}.\n \n{ids} can contain
    up to 20 semicolon delimited ids, to find ids programatically look for revision_guid
    on revision objects. Note that unlike most other id types in the API, revision_guid
    is a string.\n \nThis method returns a list of revisions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/revisionsids-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/revisionsids-get-openapi.md
- name: Stack Exchange - Search
  x-api-slug: search-get
  description: "Searches a site for any questions which fit the given criteria.\n
    \nThis method is intentionally quite limited. For more general searching, you
    should use a proper internet search engine restricted to the domain of the site
    in question.\n \nAt least one of tagged or intitle must be set on this method.
    nottagged is only used if tagged is also set, for performance reasons.\n \ntagged
    and nottagged are semi-colon delimited list of tags. At least 1 tag in tagged
    will be on each returned question if it is passed, making it the OR equivalent
    of the AND version of tagged on /questions.\n \nThe sorts accepted by this method
    operate on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n - relevance - matches the relevance
    tab on the site itself Does not accept min or max\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/search-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/search-get-openapi.md
- name: Stack Exchange - Advanced Search
  x-api-slug: searchadvanced-get
  description: "Searches a site for any questions which fit the given criteria.\n
    \nSearch criteria are expressed using the following parameters:\n  - q - a free
    form text parameter, will match all question properties based on an undocumented
    algorithm.\n - accepted - true to return only questions with accepted answers,
    false to return only those without. Omit to elide constraint.\n - answers - the
    minimum number of answers returned questions must have.\n - body - text which
    must appear in returned questions' bodies.\n - closed - true to return only closed
    questions, false to return only open ones. Omit to elide constraint.\n - migrated
    - true to return only questions migrated away from a site, false to return only
    those not. Omit to elide constraint.\n - notice - true to return only questions
    with post notices, false to return only those without. Omit to elide constraint.\n
    - nottagged - a semicolon delimited list of tags, none of which will be present
    on returned questions.\n - tagged - a semicolon delimited list of tags, of which
    at least one will be present on all returned questions.\n - title - text which
    must appear in returned questions' titles.\n - user - the id of the user who must
    own the questions returned.\n - url - a url which must be contained in a post,
    may include a wildcard.\n - views - the minimum number of views returned questions
    must have.\n - wiki - true to return only community wiki questions, false to return
    only non-community wiki ones. Omit to elide constraint.\n  \nAt least one additional
    parameter must be set if nottagged is set, for performance reasons.\n \nThe sorts
    accepted by this method operate on the follow fields of the question object:\n
    - activity - last_activity_date\n - creation - creation_date\n - votes - score\n
    - relevance - matches the relevance tab on the site itself Does not accept min
    or max\n  activity is the default sort.\n \n It is possible to create moderately
    complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns
    a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/searchadvanced-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/searchadvanced-get-openapi.md
- name: Stack Exchange - Get Similar
  x-api-slug: similar-get
  description: "Returns questions which are similar to a hypothetical one based on
    a title and tag combination.\n \nThis method is roughly equivalent to a site's
    related questions suggestion on the ask page.\n \nThis method is useful for correlating
    data outside of a Stack Exchange site with similar content within one.\n \nNote
    that title must always be passed as a parameter. tagged and nottagged are optional,
    semi-colon delimited lists of tags.\n \nIf tagged is passed it is treated as a
    preference, there is no guarantee that questions returned will have any of those
    tags. nottagged is treated as a requirement, no questions will be returned with
    those tags.\n \nThe sorts accepted by this method operate on the follow fields
    of the question object:\n - activity - last_activity_date\n - creation - creation_date\n
    - votes - score\n - relevance - order by \"how similar\" the questions are, most
    likely candidate first with a descending order Does not accept min or max\n  activity
    is the default sort.\n \n It is possible to create moderately complex queries
    using sort, min, max, fromdate, and todate.\n \nThis method returns a list of
    questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/similar-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/similar-get-openapi.md
- name: Stack Exchange - Get Tags
  x-api-slug: tags-get
  description: "Returns the tags found on a site.\n \nThe inname parameter lets a
    consumer filter down to tags that contain a certain substring. For example, inname=own
    would return both \"download\" and \"owner\" amongst others.\n \nThis method returns
    a list of tags.\n \nThe sorts accepted by this method operate on the follow fields
    of the tag object:\n - popular - count\n - activity - the creation_date of the
    last question asked with the tag\n - name - name\n  popular is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/tags-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/tags-get-openapi.md
- name: Stack Exchange - Get Tags Requred
  x-api-slug: tagsrequired-get
  description: "Returns the tags found on a site that fulfill required tag constraints
    on questions.\n \nThe inname parameter lets a consumer filter down to tags that
    contain a certain substring. For example, inname=own would return both \"download\"
    and \"owner\" amongst others.\n \nThis method returns a list of tags.\n \nThe
    sorts accepted by this method operate on the follow fields of the tag object:\n
    - popular - count\n - activity - the creation_date of the last question asked
    with the tag\n - name - name\n  popular is the default sort.\n \n It is possible
    to create moderately complex queries using sort, min, max, fromdate, and todate."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/tagsrequired-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/tagsrequired-get-openapi.md
- name: Stack Exchange - Get Tags Synonyms
  x-api-slug: tagssynonyms-get
  description: "Returns all tag synonyms found a site.\n \nWhen searching for synonyms
    of specific tags, it is better to use /tags/{tags}/synonyms over this method.\n
    \nThe sorts accepted by this method operate on the follow fields of the tag_synonym
    object:\n - creation - creation_date\n - applied - applied_count\n - activity
    - last_applied_date\n  creation is the default sort.\n \n It is possible to create
    moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
    method returns a list of tag_synonyms."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/tagssynonyms-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/tagssynonyms-get-openapi.md
- name: Stack Exchange - Get Tags Info
  x-api-slug: tagstagsinfo-get
  description: "Returns tag objects representing the tags in {tags} found on the site.\n
    \nThis method diverges from the standard naming patterns to avoid to conflicting
    with existing methods, due to the free form nature of tag names.\n \nThis method
    returns a list of tags.\n \nThe sorts accepted by this method operate on the follow
    fields of the tag object:\n - popular - count\n - activity - the creation_date
    of the last question asked with the tag\n - name - name\n  popular is the default
    sort.\n \n It is possible to create moderately complex queries using sort, min,
    max, fromdate, and todate."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/tagstagsinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/tagstagsinfo-get-openapi.md
- name: Stack Exchange - Get Tags Synonyms
  x-api-slug: tagstagssynonyms-get
  description: "Gets all the synonyms that point to the tags identified in {tags}.
    If you're looking to discover all the tag synonyms on a site, use the /tags/synonyms
    methods instead of call this method on all tags.\n \n{tags} can contain up to
    20 individual tags per request.\n \nThe sorts accepted by this method operate
    on the follow fields of the tag_synonym object:\n - creation - creation_date\n
    - applied - applied_count\n - activity - last_applied_date\n  creation is the
    default sort.\n \n It is possible to create moderately complex queries using sort,
    min, max, fromdate, and todate.\n \nThis method returns a list of tag synonyms."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/tagstagssynonyms-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/tagstagssynonyms-get-openapi.md
- name: Stack Exchange - Get Users
  x-api-slug: users-get
  description: "Returns all users on a site.\n \nThis method returns a list of users.\n
    \nThe sorts accepted by this method operate on the follow fields of the user object:\n
    - reputation - reputation\n - creation - creation_date\n - name - display_name\n
    - modified - last_modified_date\n  reputation is the default sort.\n \n It is
    possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThe inname parameter lets consumers filter the results down to
    just those users with a certain substring in their display name. For example,
    inname=kevin will return all users with both users named simply \"Kevin\" or those
    with Kevin as one of (or part of) their names; such as \"Kevin Montrose\"."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/users-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/users-get-openapi.md
- name: Stack Exchange - Get User Moderators
  x-api-slug: usersmoderators-get
  description: "Gets those users on a site who can exercise moderation powers.\n \nNote,
    employees of Stack Exchange Inc. will be returned if they have been granted moderation
    powers on a site even if they have never been appointed or elected explicitly.
    This method checks abilities, not the manner in which they were obtained.\n \nThe
    sorts accepted by this method operate on the follow fields of the user object:\n
    - reputation - reputation\n - creation - creation_date\n - name - display_name\n
    - modified - last_modified_date\n  reputation is the default sort.\n \n It is
    possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of users."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersmoderators-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersmoderators-get-openapi.md
- name: Stack Exchange - Get Users Moderators Elected
  x-api-slug: usersmoderatorselected-get
  description: "Returns those users on a site who both have moderator powers, and
    were actually elected.\n \nThis method excludes Stack Exchange Inc. employees,
    unless they were actually elected moderators on a site (which can only have happened
    prior to their employment).\n \nThe sorts accepted by this method operate on the
    follow fields of the user object:\n - reputation - reputation\n - creation - creation_date\n
    - name - display_name\n - modified - last_modified_date\n  reputation is the default
    sort.\n \n It is possible to create moderately complex queries using sort, min,
    max, fromdate, and todate.\n \nThis method returns a list of users."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersmoderatorselected-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersmoderatorselected-get-openapi.md
- name: Stack Exchange - Get User
  x-api-slug: usersids-get
  description: "Gets the users identified in ids in {ids}.\n \nTypically this method
    will be called to fetch user profiles when you have obtained user ids from some
    other source, such as /questions.\n \n{ids} can contain up to 100 semicolon delimited
    ids, to find ids programatically look for user_id on user or shallow_user objects.\n
    \nThe sorts accepted by this method operate on the follow fields of the user object:\n
    - reputation - reputation\n - creation - creation_date\n - name - display_name\n
    - modified - last_modified_date\n  reputation is the default sort.\n \n It is
    possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of users."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersids-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersids-get-openapi.md
- name: Stack Exchange - Get User Answers
  x-api-slug: usersidsanswers-get
  description: "Returns the answers the users in {ids} have posted.\n \n{ids} can
    contain up to 100 semicolon delimited ids, to find ids programatically look for
    user_id on user or shallow_user objects.\n \nThe sorts accepted by this method
    operate on the follow fields of the answer object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of answers."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsanswers-get-openapi.md
- name: Stack Exchange - Get User Badges
  x-api-slug: usersidsbadges-get
  description: "Get the badges the users in {ids} have earned.\n \nBadge sorts are
    a tad complicated. For the purposes of sorting (and min/max) tag_based is considered
    to be greater than named.\n \nThis means that you can get a list of all tag based
    badges a user has by passing min=tag_based, and conversely all the named badges
    by passing max=named, with sort=type.\n \nFor ranks, bronze is greater than silver
    which is greater than gold. Along with sort=rank, set max=gold for just gold badges,
    max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank
    is the default sort.\n \n{ids} can contain up to 100 semicolon delimited ids,
    to find ids programatically look for user_id on user or shallow_user objects.\n
    \nThis method returns a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsbadges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsbadges-get-openapi.md
- name: Stack Exchange - Get User Comments
  x-api-slug: usersidscomments-get
  description: "Get the comments posted by users in {ids}.\n \n{ids} can contain up
    to 100 semicolon delimited ids, to find ids programatically look for user_id on
    user or shallow_user objects.\n \nThe sorts accepted by this method operate on
    the follow fields of the comment object:\n - creation - creation_date\n - votes
    - score\n  creation is the default sort.\n \n It is possible to create moderately
    complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns
    a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidscomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidscomments-get-openapi.md
- name: Stack Exchange - Get User Favorites
  x-api-slug: usersidsfavorites-get
  description: "Get the questions that users in {ids} have favorited.\n \nThis method
    is effectively a view onto a user's favorites tab.\n \n{ids} can contain up to
    100 semicolon delimited ids, to find ids programatically look for user_id on user
    or shallow_user objects.\n \nThe sorts accepted by this method operate on the
    follow fields of the question object:\n - activity - last_activity_date\n - creation
    - creation_date\n - votes - score\n - added - when the user favorited the question\n
    \ activity is the default sort.\n \n It is possible to create moderately complex
    queries using sort, min, max, fromdate, and todate.\n \nThis method returns a
    list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsfavorites-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsfavorites-get-openapi.md
- name: Stack Exchange - Get User Mentioned
  x-api-slug: usersidsmentioned-get
  description: "Gets all the comments that the users in {ids} were mentioned in.\n
    \nNote, to count as a mention the comment must be considered to be \"in reply
    to\" a user. Most importantly, this means that a comment can only be in reply
    to a single user.\n \n{ids} can contain up to 100 semicolon delimited ids, to
    find ids programatically look for user_id on user or shallow_user objects.\n \nThe
    sorts accepted by this method operate on the follow fields of the comment object:\n
    - creation - creation_date\n - votes - score\n  It is possible to create moderately
    complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns
    a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsmentioned-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsmentioned-get-openapi.md
- name: Stack Exchange - Get User Questions
  x-api-slug: usersidsquestions-get
  description: "Gets the questions asked by the users in {ids}.\n \n{ids} can contain
    up to 100 semicolon delimited ids, to find ids programatically look for user_id
    on user or shallow_user objects.\n \nThe sorts accepted by this method operate
    on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsquestions-get-openapi.md
- name: Stack Exchange - Get User Questions Featured
  x-api-slug: usersidsquestionsfeatured-get
  description: "Gets the questions on which the users in {ids} have active bounties.\n
    \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
    look for user_id on user or shallow_user objects.\n \nThe sorts accepted by this
    method operate on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsquestionsfeatured-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsquestionsfeatured-get-openapi.md
- name: Stack Exchange - Get User Questions No Answers
  x-api-slug: usersidsquestionsnoanswers-get
  description: "Gets the questions asked by the users in {ids} which have no answers.\n
    \nQuestions returns by this method actually have zero undeleted answers. It is
    completely disjoint /users/{ids}/questions/unanswered and /users/{ids}/questions/unaccepted,
    which only return questions with at least one answer, subject to other contraints.\n
    \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
    look for user_id on user or shallow_user objects.\n \nThe sorts accepted by this
    method operate on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsquestionsnoanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsquestionsnoanswers-get-openapi.md
- name: Stack Exchange - Get User Questions Unnacepted
  x-api-slug: usersidsquestionsunaccepted-get
  description: "Gets the questions asked by the users in {ids} which have at least
    one answer, but no accepted answer.\n \nQuestions returned by this method have
    answers, but the owner has not opted to accept any of them.\n \n{ids} can contain
    up to 100 semicolon delimited ids, to find ids programatically look for user_id
    on user or shallow_user objects.\n \nThe sorts accepted by this method operate
    on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsquestionsunaccepted-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsquestionsunaccepted-get-openapi.md
- name: Stack Exchange - Get User Questions Unanswered
  x-api-slug: usersidsquestionsunanswered-get
  description: "Gets the questions asked by the users in {ids} which the site consideres
    unanswered, while still having at least one answer posted.\n \nThese rules are
    subject to change, but currently any question without at least one upvoted or
    accepted answer is considered unanswered.\n \nTo get the set of questions that
    a user probably considers unanswered, the returned questions should be unioned
    with those returned by /users/{id}/questions/no-answers. These methods are distinct
    so that truly unanswered (that is, zero posted answers) questions can be easily
    separated from mearly poorly or inadequately answered ones.\n \n{ids} can contain
    up to 100 semicolon delimited ids, to find ids programatically look for user_id
    on user or shallow_user objects.\n \nThe sorts accepted by this method operate
    on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsquestionsunanswered-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsquestionsunanswered-get-openapi.md
- name: Stack Exchange - Get User Reputation
  x-api-slug: usersidsreputation-get
  description: "Gets a subset of the reputation changes for users in {ids}.\n \nReputation
    changes are intentionally scrubbed of some data to make it difficult to correlate
    votes on particular posts with user reputation changes. That being said, this
    method returns enough data for reasonable display of reputation trends.\n \n{ids}
    can contain up to 100 semicolon delimited ids, to find ids programatically look
    for user_id on user or shallow_user objects.\n \nThis method returns a list of
    reputation objects."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsreputation-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidsreputation-get-openapi.md
- name: Stack Exchange - Get User Tags
  x-api-slug: usersidstags-get
  description: "Returns the tags the users identified in {ids} have been active in.\n
    \nThis route corresponds roughly to user's stats tab, but does not include tag
    scores. A subset of tag scores are available (on a single user basis) in /users/{id}/top-answer-tags
    and /users/{id}/top-question-tags.\n \n{ids} can contain up to 100 semicolon delimited
    ids, to find ids programatically look for user_id on user or shallow_user objects.\n
    \nThe sorts accepted by this method operate on the follow fields of the tag object:\n
    - popular - count\n - activity - the creation_date of the last question asked
    with the tag\n - name - name\n  popular is the default sort.\n \n It is possible
    to create moderately complex queries using sort, min, max, fromdate, and todate.\n
    \nThis method returns a list of tags."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidstags-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidstags-get-openapi.md
- name: Stack Exchange - Get User Timeline
  x-api-slug: usersidstimeline-get
  description: "Returns a subset of the actions the users in {ids} have taken on the
    site.\n \nThis method returns users' posts, edits, and earned badges in the order
    they were accomplished. It is possible to filter to just a window of activity
    using the fromdate and todate parameters.\n \n{ids} can contain up to 100 semicolon
    delimited ids, to find ids programatically look for user_id on user or shallow_user
    objects.\n \nThis method returns a list of user timeline objects."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidstimeline-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidstimeline-get-openapi.md
- name: Stack Exchange - Get User Tags Top Questions
  x-api-slug: usersidtagstagstopquestions-get
  description: "Returns the top 30 questions a user has asked with the given tags.\n
    \n{id} can contain a single id, to find it programatically look for user_id on
    user or shallow_user objects. {tags} is limited to 5 tags, passing more will result
    in an error.\n \nThe sorts accepted by this method operate on the follow fields
    of the question object:\n - activity - last_activity_date\n - creation - creation_date\n
    - votes - score\n  activity is the default sort.\n \n It is possible to create
    moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
    method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidtagstagstopquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/stack-exchange/usersidtagstagstopquestions-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://square.api.gallery.streamdata.io
- type: x-api-stack
  url: http://stack.exchange.stack.network
- type: x-authentication
  url: https://api.stackexchange.com/docs/authentication
- type: x-base
  url: https://api.stackexchange.com/
- type: x-blog
  url: http://stackexchange.com/blogs
- type: x-blog-rss
  url: http://blog.stackoverflow.com/feed/
- type: x-crunchbase
  url: http://www.crunchbase.com/company/stack-exchange
- type: x-crunchbase
  url: https://crunchbase.com/organization/stack-exchange
- type: x-developer
  url: http://api.stackexchange.com/
- type: x-email
  url: legal@stackexchange.com
- type: x-email
  url: team@stackexchange.com
- type: x-email
  url: team+api@stackexchange.com
- type: x-error-codes
  url: https://api.stackexchange.com/docs/error-handling
- type: x-github
  url: https://github.com/StackExchange
- type: x-javascript-sdk
  url: https://api.stackexchange.com/docs/js-lib
- type: x-linkedin
  url: https://www.linkedin.com/company/stack-exchange
- type: x-privacy
  url: https://stackexchange.com/legal/privacy-policy
- type: x-rate-limits
  url: https://api.stackexchange.com/docs/throttle
- type: x-selfservice-registration
  url: https://stackapps.com/users/login?returnurl=/apps/oauth/register
- type: x-support
  url: https://stackexchange.com/about/contact
- type: x-terms-of-service
  url: http://stackexchange.com/legal/api-terms-of-use
- type: x-twitter
  url: https://twitter.com/StackExchange
- type: x-website
  url: http://stackexchange.com
- type: x-website
  url: https://stackexchange.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---