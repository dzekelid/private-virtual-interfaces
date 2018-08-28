---
swagger: "2.0"
x-collection-name: AWS Direct Connect
x-complete: 0
info:
  title: AWS Direct Connect API Describe Virtual Interfaces
  version: 1.0.0
  description: Displays all virtual interfaces for an AWS account.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AllocatePrivateVirtualInterface:
    get:
      summary: Allocate Private Virtual Interface
      description: Provisions a private virtual interface to be owned by a different
        customer.
      operationId: allocatePrivateVirtualInterface
      x-api-path-slug: actionallocateprivatevirtualinterface-get
      parameters:
      - in: query
        name: connectionId
        description: The connection ID on which the private virtual interface is provisioned
        type: string
      - in: query
        name: newPrivateVirtualInterfaceAllocation
        description: Detailed information for the private virtual interface to be
          provisioned
        type: string
      - in: query
        name: ownerAccount
        description: The AWS account that will own the new private virtual interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
  /?Action=AllocatePublicVirtualInterface:
    get:
      summary: Allocate Public Virtual Interface
      description: Provisions a public virtual interface to be owned by a different
        customer.
      operationId: allocatePublicVirtualInterface
      x-api-path-slug: actionallocatepublicvirtualinterface-get
      parameters:
      - in: query
        name: connectionId
        description: The connection ID on which the public virtual interface is provisioned
        type: string
      - in: query
        name: newPublicVirtualInterfaceAllocation
        description: Detailed information for the public virtual interface to be provisioned
        type: string
      - in: query
        name: ownerAccount
        description: The AWS account that will own the new public virtual interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
  /?Action=ConfirmPrivateVirtualInterface:
    get:
      summary: Confirm Private Virtual Interface
      description: Accept ownership of a private virtual interface created by another
        customer.
      operationId: confirmPrivateVirtualInterface
      x-api-path-slug: actionconfirmprivatevirtualinterface-get
      parameters:
      - in: query
        name: virtualGatewayId
        description: ID of the virtual private gateway that will be attached to the
          virtual interface
        type: string
      - in: query
        name: virtualInterfaceId
        description: ID of the virtual interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
  /?Action=ConfirmPublicVirtualInterface:
    get:
      summary: Confirm Public Virtual Interface
      description: Accept ownership of a public virtual interface created by another
        customer.
      operationId: confirmPublicVirtualInterface
      x-api-path-slug: actionconfirmpublicvirtualinterface-get
      parameters:
      - in: query
        name: virtualInterfaceId
        description: ID of the virtual interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
  /?Action=CreatePrivateVirtualInterface:
    get:
      summary: Create Private Virtual Interface
      description: Creates a new private virtual interface.
      operationId: createPrivateVirtualInterface
      x-api-path-slug: actioncreateprivatevirtualinterface-get
      parameters:
      - in: query
        name: connectionId
        description: ID of the connection
        type: string
      - in: query
        name: newPrivateVirtualInterface
        description: Detailed information for the private virtual interface to be
          created
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
  /?Action=CreatePublicVirtualInterface:
    get:
      summary: Create Public Virtual Interface
      description: Creates a new public virtual interface.
      operationId: createPublicVirtualInterface
      x-api-path-slug: actioncreatepublicvirtualinterface-get
      parameters:
      - in: query
        name: connectionId
        description: ID of the connection
        type: string
      - in: query
        name: newPublicVirtualInterface
        description: Detailed information for the public virtual interface to be created
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
  /?Action=DescribeVirtualInterfaces:
    get:
      summary: Describe Virtual Interfaces
      description: Displays all virtual interfaces for an AWS account.
      operationId: describeVirtualInterfaces
      x-api-path-slug: actiondescribevirtualinterfaces-get
      parameters:
      - in: query
        name: connectionId
        description: ID of the connection
        type: string
      - in: query
        name: virtualInterfaceId
        description: ID of the virtual interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
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