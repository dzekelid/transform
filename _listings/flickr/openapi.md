---
swagger: "2.0"
x-collection-name: Flickr
x-complete: 1
info:
  title: Flickr
  description: explore-upload-and-organize-photos-on-flickr
  version: 1.0.0
host: api.flickr.com
basePath: /services/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/?method=flickr.photos.transform.rotate:
    post:
      summary: Photos Transform Rotate
      description: Rotate a photo.
      operationId: postRestMethodFlickr.photos.transform.rotate
      x-api-path-slug: restmethodflickr-photos-transform-rotate-post
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: degrees
        description: The amount of degrees by which to rotate the photo (clockwise)
          from its current orientation
      - in: query
        name: format
        description: Response format
      - in: query
        name: photo_id
        description: The id of the photo to rotate
      responses:
        200:
          description: OK
      tags:
      - Photos
      - Transform
      - Rotate
---