---
swagger: "2.0"
x-collection-name: OpenCorporates
x-complete: 0
info:
  title: OpenCorporates Companies Search
  description: nThis returns a collection of companies whose name matches the given
    search term (submitted as :q in the query parameters)
  termsOfService: https://opencorporates.com/info/licence
  version: v.04
host: api.opencorporates.com
basePath: v0.4/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /account_status:
    get:
      summary: Account Status
      description: nThis returns the status of your API Account (this information
        may also be retrieved at https://OpenCorporates
      operationId: account-status
      x-api-path-slug: account-status-get
      parameters:
      - in: query
        name: calls_remaining
        description: this has two subvalues - today and this_month
      - in: query
        name: expiry_date
        description: when the api_plan runs out
      - in: query
        name: plan
        description: the type of plan that you are on
      - in: query
        name: status
        description: status of the API account
      - in: query
        name: usage
        description: this has two subvalues - today and this_month
      responses:
        200:
          description: OK
      tags:
      - Businesses
      - Account
      - Status
  /officers/:id:
    get:
      summary: Officers  ID
      description: nThis returns information on a particular officer (a director or
        an agent for a company)
      operationId: officers--id
      x-api-path-slug: officersid-get
      parameters:
      - in: query
        name: address
        description: NEWthe given address of the officer, if known (only for users
          with API key)
      - in: query
        name: date_of_birth
        description: NEWthe date of birth of the officer, if known (only for users
          with API key)
      - in: query
        name: end_date
        description: this is date on which the officership ended
      - in: query
        name: position
        description: the position held (e
      - in: query
        name: start_date
        description: this is date on which the officership started
      - in: query
        name: uid
        description: the id given to the officer by the company registry
      responses:
        200:
          description: OK
      tags:
      - Businesses
      - Officers
  /companies/search:
    get:
      summary: Companies Search
      description: nThis returns a collection of companies whose name matches the
        given search term (submitted as :q in the query parameters)
      operationId: companies-search
      x-api-path-slug: companiessearch-get
      parameters:
      - in: query
        name: branch
        description: Filter by branch status (boolean)
      - in: query
        name: company_type
        description: The type of the company, as defined by the company register
      - in: query
        name: country_code
        description: NEWThe companies searched for can be restricted to a given country
          by passing a country_code query parameter
      - in: query
        name: created_since
        description: companies added to OpenCorporates after the given date
      - in: query
        name: current_status
        description: The current status of the company, as defined by the company
          register
      - in: query
        name: dissolution_date
        description: NEWas with all date fields, dissolution_date can be supplied
          either as a specific date or as a span of dates
      - in: query
        name: dissolved_before
        description: DeprecatedRestrict to companies with a dissolution_date before
          the given date
      - in: query
        name: dissolved_since
        description: DeprecatedRestrict to companies with a dissolution_date after
          the given date
      - in: query
        name: exclude_inactive
        description: DeprecatedRestrict to companies that are active/inactive
      - in: query
        name: fields
        description: NEWBy default when searching with a term (e
      - in: query
        name: inactive
        description: Filter by inactive status (boolean)
      - in: query
        name: incorporated_before
        description: DeprecatedRestrict to companies with an incorporation_date before
          the given date
      - in: query
        name: incorporated_since
        description: DeprecatedRestrict to companies with an incorporation_date after
          the given date
      - in: query
        name: incorporation_date
        description: NEWAs with all date fields, incorporation_date can be supplied
          either as a specific date or as a span of dates
      - in: query
        name: industry_codes
        description: NEWOne or more industry codes representing the industries the
          company operates in
      - in: query
        name: jurisdiction_code
        description: The companies searched for can be restricted to a given jurisdiction
          by passing a jurisdiction_code query parameter
      - in: query
        name: nonprofit
        description: NEWFilter by nonprofit company type (boolean)
      - in: query
        name: registered_address
        description: NEWThe companies searched for can be restricted by passing in
          an address or parts of an address
      responses:
        200:
          description: OK
      tags:
      - Businesses
      - Companies
      - Search
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---