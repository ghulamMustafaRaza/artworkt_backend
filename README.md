# NOTE
> API endpoint `https://shrouded-harbor-27936.herokuapp.com/app`

> Must user this header for authorization with all request <br/>
`Authorization: JWT eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI1ZDQ0NWE3ZTJjMDA0NDcxM2MwNzcwOTUiLCJpYXQiOjE1NjYyMDcwMTJ9.JuXaIx5XGQzbwek2JrCxI0K6aXv7UyNYiAW6teXlnqw`

for example : `https://shrouded-harbor-27936.herokuapp.com/app/store/products`
# Product

## Get a list of Sync Products
**GET** /store/products    
> Examples

**Response data:**
<pre>    {
        "code": 200,
        "result": [
            {
                "id": 79348721,
                "external_id": "e9460f6c67",
                "name": "API product",
                "variants": 2,
                "synced": 2
            }
        ],
        "extra": [],
        "paging": {
            "total": 1,
            "offset": 0,
            "limit": 20
        },
        "debug": []
    }</pre>

## Create a new Sync Product
**POST** /store/products    
> Examples

**Request body:**
<pre>    {
        "sync_product": {
            "name": "API product Bella",
            "thumbnail": "https://example.com/image.jpg"
        },
        "sync_variants": [
            {
                "retail_price": "21.00",
                "variant_id": 4011,
                "files": [
                    {
                        "url": "https://example.com/image.jpg"
                    },
                    {
                        "type": "back",
                        "url": "https://example.com/image.jpg"
                    }
                ]
            },
            {
                "retail_price": "21.00",
                "variant_id": 4012,
                "files": [
                    {
                        "url": "https://example.com/image.jpg"
                    },
                    {
                        "type": "back",
                        "url": "https://example.com/image.jpg"
                    }
                ]
            }
        ]
    }</pre>

**Response data:**
<pre>    {
        "code": 200,
        "result": {
            "id": 79348732,
            "external_id": "5bd9947c709b34",
            "name": "API product Bella",
            "variants": 2,
            "synced": 2
        },
        "extra": [],
        "debug": []
    }</pre>

## Get information about a single Sync Product and its Sync Variants
**GET** /store/products/
> Examples

**Response data:**
<pre>    {
        "code": 200,
        "result": {
            "sync_product": {
                "id": 79348721,
                "external_id": "e9460f6c67",
                "name": "API product",
                "variants": 2,
                "synced": 2
            },
            "sync_variants": [
                {
                    "id": 866914574,
                    "external_id": "5bd967595a1174",
                    "sync_product_id": 79348721,
                    "name": "API product",
                    "synced": true,
                    "variant_id": 4011,
                    "retail_price": "18.00",
                    "currency": "USD",
                    "product": {
                        "variant_id": 4011,
                        "product_id": 71,
                        "image": "https://s3.dev.printful.com/products/71/4012_1517927381.jpg",
                        "name": "Bella + Canvas 3001 Unisex Short Sleeve Jersey T-Shirt with Tear Away Label (White / S)"
                    },
                    "files": [
                        {
                            "id": 76564075,
                            "type": "default",
                            "hash": "7d6a2367c1e338750e68dc66b20cba1a",
                            "url": "https://picsum.photos/200/300",
                            "filename": "76564075.jpg",
                            "mime_type": "image/jpeg",
                            "size": 8245,
                            "width": 200,
                            "height": 300,
                            "dpi": null,
                            "status": "ok",
                            "created": 1539341673,
                            "thumbnail_url": "https://s3.dev.printful.com/files/7d6/7d6a2367c1e338750e68dc66b20cba1a_thumb.png",
                            "preview_url": "https://s3.dev.printful.com/files/7d6/7d6a2367c1e338750e68dc66b20cba1a_preview.png",
                            "visible": true
                        },
                        {
                            "id": 76564075,
                            "type": "back",
                            "hash": "7d6a2367c1e338750e68dc66b20cba1a",
                            "url": "https://picsum.photos/200/300",
                            "filename": "76564075.jpg",
                            "mime_type": "image/jpeg",
                            "size": 8245,
                            "width": 200,
                            "height": 300,
                            "dpi": null,
                            "status": "ok",
                            "created": 1539341673,
                            "thumbnail_url": "https://s3.dev.printful.com/files/7d6/7d6a2367c1e338750e68dc66b20cba1a_thumb.png",
                            "preview_url": "https://s3.dev.printful.com/files/7d6/7d6a2367c1e338750e68dc66b20cba1a_preview.png",
                            "visible": true
                        }
                    ],
                    "options": [
                        {
                            "id": "embroidery_type",
                            "value": "flat"
                        },
                        {
                            "id": "thread_colors",
                            "value": []
                        },
                        {
                            "id": "thread_colors_3d",
                            "value": []
                        },
                        {
                            "id": "thread_colors_chest_left",
                            "value": []
                        }
                    ]
                },
                {
                    "id": 866914580,
                    "external_id": "5bd96ea4a381f8",
                    "sync_product_id": 79348721,
                    "name": "API product",
                    "synced": true,
                    "variant_id": 4011,
                    "retail_price": "21.00",
                    "currency": "USD",
                    "product": {
                        "variant_id": 4011,
                        "product_id": 71,
                        "image": "https://s3.dev.printful.com/products/71/4012_1517927381.jpg",
                        "name": "Bella + Canvas 3001 Unisex Short Sleeve Jersey T-Shirt with Tear Away Label (White / S)"
                    },
                    "files": [
                        {
                            "id": 76564390,
                            "type": "default",
                            "hash": "77440392f60d2346a1bf690c1564d973",
                            "url": "https://i.etsystatic.com/17947654/r/il/3a0750/1565927694/il_570xN.1565927694_gfxu.jpg",
                            "filename": "il_570xN.1565927694_gfxu.jpg",
                            "mime_type": "image/jpeg",
                            "size": 70053,
                            "width": 570,
                            "height": 570,
                            "dpi": null,
                            "status": "ok",
                            "created": 1540982496,
                            "thumbnail_url": "https://s3.dev.printful.com/files/774/77440392f60d2346a1bf690c1564d973_thumb.png",
                            "preview_url": "https://s3.dev.printful.com/files/774/77440392f60d2346a1bf690c1564d973_preview.png",
                            "visible": true
                        },
                        {
                            "id": 76564159,
                            "type": "back",
                            "hash": "ebd559858e5703088de8900ce99c37d3",
                            "url": "https://picsum.photos/200/300?image=2",
                            "filename": "76564159.jpg",
                            "mime_type": "image/jpeg",
                            "size": 11246,
                            "width": 200,
                            "height": 300,
                            "dpi": null,
                            "status": "ok",
                            "created": 1540797879,
                            "thumbnail_url": "https://s3.dev.printful.com/files/ebd/ebd559858e5703088de8900ce99c37d3_thumb.png",
                            "preview_url": "https://s3.dev.printful.com/files/ebd/ebd559858e5703088de8900ce99c37d3_preview.png",
                            "visible": true
                        },
                        {
                            "id": 76564391,
                            "type": "preview",
                            "hash": "a0b4fa4e51f3feeee7a5f14260a257ea",
                            "url": null,
                            "filename": "mockup-fafde22d.png",
                            "mime_type": "image/png",
                            "size": 222824,
                            "width": 600,
                            "height": 600,
                            "dpi": 72,
                            "status": "ok",
                            "created": 1540982574,
                            "thumbnail_url": "https://s3.dev.printful.com/files/a0b/a0b4fa4e51f3feeee7a5f14260a257ea_thumb.png",
                            "preview_url": "https://s3.dev.printful.com/files/a0b/a0b4fa4e51f3feeee7a5f14260a257ea_preview.png",
                            "visible": false
                        }
                    ],
                    "options": [
                        {
                            "id": "embroidery_type",
                            "value": "flat"
                        },
                        {
                            "id": "thread_colors",
                            "value": []
                        },
                        {
                            "id": "thread_colors_3d",
                            "value": []
                        },
                        {
                            "id": "thread_colors_chest_left",
                            "value": []
                        }
                    ]
                }
            ]
        },
        "extra": [],
        "debug": []
    }</pre>

## Delete a Sync Product
**DELETE** /store/products/
> Examples


## Modify a Sync Product
**PUT** /store/products/
> Examples

**Request body:**
<pre>    {
        "sync_product": {
            "name": "API product new name",
            "thumbnail": "https://example.com/image.jpg"
        }
    }</pre>

**Response data:**
<pre>    {
        "code": 200,
        "result": {
            "id": 79348721,
            "external_id": "e9460f6c67",
            "name": "API product new name",
            "variants": 2,
            "synced": 2
        },
        "extra": [],
        "debug": []
    }</pre>

**Request body:**
<pre>    {
        "sync_product": {
            "name": "API product new name",
            "thumbnail": "https://example.com/image.jpg"
        },
        "sync_variants": [
            	{
                    "id": 866914574
                },
                {
                    "id": 866914580,
                    "retail_price": 21,
                    "files": [
                        {
                            "url": "https://example.com/image.jpg"
                        },
                        {
                            "type": "back",
                            "url": "https://example.com/image.jpg"
                        }
                    ]
                }
        ]
    }</pre>

**Response data:**
<pre>    {
        "code": 200,
        "result": {
            "id": 79348721,
            "external_id": "e9460f6c67",
            "name": "API product",
            "variants": 2,
            "synced": 2
        },
        "extra": [],
        "debug": []
    }</pre>

## Create a new Sync Variant
**POST** /store/products/
> Examples

**Request body:**
<pre>    {
        "external_id": "my-external-id",
        "retail_price": "19.00",
        "variant_id": 4011,
        "files": [
            {
                "type": "default",
                "url": "https://example.com/image.jpg"
            },
            {
                "type": "back",
                "url": "https://example.com/image.jpg"
            }
        ],
        "options": [
            {
                "id": "embroidery_type",
                "value": "flat"
            },
            {
                "id": "thread_colors",
                "value": []
            },
            {
                "id": "thread_colors_3d",
                "value": []
            },
            {
                "id": "thread_colors_chest_left",
                "value": []
            }
        ]
    }</pre>

**Response data:**
<pre>    {
        "code": 200,
        "result": {
            "id": 866914592,
            "external_id": "my-external-id",
            "sync_product_id": 79348732,
            "name": "API product Bella",
            "synced": true,
            "variant_id": 4011,
            "retail_price": "19.00",
            "currency": "USD",
            "product": {
                "variant_id": 4011,
                "product_id": 71,
                "image": "https://s3.dev.printful.com/products/71/4012_1517927381.jpg",
                "name": "Bella + Canvas 3001 Unisex Short Sleeve Jersey T-Shirt with Tear Away Label (White / S)"
            },
            "files": [
                {
                    "id": 76564159,
                    "type": "default",
                    "hash": "ebd559858e5703088de8900ce99c37d3",
                    "url": "https://example.com/image.jpg",
                    "filename": "76564159.jpg",
                    "mime_type": "image/jpeg",
                    "size": 11246,
                    "width": 200,
                    "height": 300,
                    "dpi": null,
                    "status": "ok",
                    "created": 1540797879,
                    "thumbnail_url": "https://s3.dev.printful.com/files/ebd/ebd559858e5703088de8900ce99c37d3_thumb.png",
                    "preview_url": "https://s3.dev.printful.com/files/ebd/ebd559858e5703088de8900ce99c37d3_preview.png",
                    "visible": true
                },
                {
                    "id": 76564159,
                    "type": "back",
                    "hash": "ebd559858e5703088de8900ce99c37d3",
                    "url": "https://example.com/image.jpg",
                    "filename": "76564159.jpg",
                    "mime_type": "image/jpeg",
                    "size": 11246,
                    "width": 200,
                    "height": 300,
                    "dpi": null,
                    "status": "ok",
                    "created": 1540797879,
                    "thumbnail_url": "https://s3.dev.printful.com/files/ebd/ebd559858e5703088de8900ce99c37d3_thumb.png",
                    "preview_url": "https://s3.dev.printful.com/files/ebd/ebd559858e5703088de8900ce99c37d3_preview.png",
                    "visible": true
                }
            ],
            "options": [
                {
                    "id": "embroidery_type",
                    "value": "flat"
                },
                {
                    "id": "thread_colors",
                    "value": []
                },
                {
                    "id": "thread_colors_3d",
                    "value": []
                },
                {
                    "id": "thread_colors_chest_left",
                    "value": []
                }
            ]
        },
        "extra": [],
        "debug": []
    }</pre>

## Get information about a single Sync Variant
**GET** /store/variants/
> Examples

**Response data:**
<pre>    {
        "code": 200,
        "result": {
            "sync_variant": {
                "id": 866914574,
                "external_id": "5bd967595a1174",
                "sync_product_id": 79348721,
                "name": "API product",
                "synced": true,
                "variant_id": 4011,
                "retail_price": "18.00",
                "currency": "USD",
                "product": {
                    "variant_id": 4011,
                    "product_id": 71,
                    "image": "https://s3.dev.printful.com/products/71/4012_1517927381.jpg",
                    "name": "Bella + Canvas 3001 Unisex Short Sleeve Jersey T-Shirt with Tear Away Label (White / S)"
                },
                "files": [
                    {
                        "id": 76564075,
                        "type": "default",
                        "hash": "7d6a2367c1e338750e68dc66b20cba1a",
                        "url": "https://picsum.photos/200/300",
                        "filename": "76564075.jpg",
                        "mime_type": "image/jpeg",
                        "size": 8245,
                        "width": 200,
                        "height": 300,
                        "dpi": null,
                        "status": "ok",
                        "created": 1539341673,
                        "thumbnail_url": "https://s3.dev.printful.com/files/7d6/7d6a2367c1e338750e68dc66b20cba1a_thumb.png",
                        "preview_url": "https://s3.dev.printful.com/files/7d6/7d6a2367c1e338750e68dc66b20cba1a_preview.png",
                        "visible": true
                    },
                    {
                        "id": 76564075,
                        "type": "back",
                        "hash": "7d6a2367c1e338750e68dc66b20cba1a",
                        "url": "https://picsum.photos/200/300",
                        "filename": "76564075.jpg",
                        "mime_type": "image/jpeg",
                        "size": 8245,
                        "width": 200,
                        "height": 300,
                        "dpi": null,
                        "status": "ok",
                        "created": 1539341673,
                        "thumbnail_url": "https://s3.dev.printful.com/files/7d6/7d6a2367c1e338750e68dc66b20cba1a_thumb.png",
                        "preview_url": "https://s3.dev.printful.com/files/7d6/7d6a2367c1e338750e68dc66b20cba1a_preview.png",
                        "visible": true
                    }
                ],
                "options": [
                    {
                        "id": "embroidery_type",
                        "value": "flat"
                    },
                    {
                        "id": "thread_colors",
                        "value": []
                    },
                    {
                        "id": "thread_colors_3d",
                        "value": []
                    },
                    {
                        "id": "thread_colors_chest_left",
                        "value": []
                    }
                ]
            },
            "sync_product": {
                "id": 79348721,
                "external_id": "e9460f6c67",
                "name": "API product",
                "variants": 1,
                "synced": 1
            }
        },
        "extra": [],
        "debug": []
    }</pre>

## Delete a Sync Variant
**DELETE** /store/variants/
> Examples


## Modify a Sync Variant
**PUT** /store/variants/
> Examples

**Request body:**
<pre>    {
        "retail_price": "29.00"
    }</pre>

**Response data:**
<pre>    {
        "code": 200,
        "result": {
            "id": 866914574,
            "external_id": "5bd967595a1174",
            "sync_product_id": 79348721,
            "name": "API product",
            "synced": true,
            "variant_id": 4011,
            "retail_price": "29.00",
            "currency": "",
            "product": {
                "variant_id": 4011,
                "product_id": 71,
                "image": "https://s3.dev.printful.com/products/71/4012_1517927381.jpg",
                "name": "Bella + Canvas 3001 Unisex Short Sleeve Jersey T-Shirt with Tear Away Label (White / S)"
            },
            "files": [
                {
                    "id": 76564075,
                    "type": "default",
                    "hash": "7d6a2367c1e338750e68dc66b20cba1a",
                    "url": "https://example.com/image.jpg",
                    "filename": "76564075.jpg",
                    "mime_type": "image/jpeg",
                    "size": 8245,
                    "width": 200,
                    "height": 300,
                    "dpi": null,
                    "status": "ok",
                    "created": 1539341673,
                    "thumbnail_url": "https://s3.dev.printful.com/files/7d6/7d6a2367c1e338750e68dc66b20cba1a_thumb.png",
                    "preview_url": "https://s3.dev.printful.com/files/7d6/7d6a2367c1e338750e68dc66b20cba1a_preview.png",
                    "visible": true
                },
                {
                    "id": 76564075,
                    "type": "back",
                    "hash": "7d6a2367c1e338750e68dc66b20cba1a",
                    "url": "https://example.com/image.jpg",
                    "filename": "76564075.jpg",
                    "mime_type": "image/jpeg",
                    "size": 8245,
                    "width": 200,
                    "height": 300,
                    "dpi": null,
                    "status": "ok",
                    "created": 1539341673,
                    "thumbnail_url": "https://s3.dev.printful.com/files/7d6/7d6a2367c1e338750e68dc66b20cba1a_thumb.png",
                    "preview_url": "https://s3.dev.printful.com/files/7d6/7d6a2367c1e338750e68dc66b20cba1a_preview.png",
                    "visible": true
                }
            ],
            "options": [
                {
                    "id": "embroidery_type",
                    "value": "flat"
                },
                {
                    "id": "thread_colors",
                    "value": []
                },
                {
                    "id": "thread_colors_3d",
                    "value": []
                },
                {
                    "id": "thread_colors_chest_left",
                    "value": []
                }
            ]
        },
        "extra": [],
        "debug": []
    }</pre>

**Request body:**
<pre>    {
        "files": [
            {
                "type": "default",
                "url": "https://example.com/image.jpg"
            }
        ]
    }</pre>

**Response data:**
<pre>    {
        "code": 200,
        "result": {
            "id": 866914574,
            "external_id": "5bd967595a1174",
            "sync_product_id": 79348721,
            "name": "API product",
            "synced": true,
            "variant_id": 4011,
            "retail_price": "29.00",
            "currency": "",
            "product": {
                "variant_id": 4011,
                "product_id": 71,
                "image": "https://s3.dev.printful.com/products/71/4012_1517927381.jpg",
                "name": "Bella + Canvas 3001 Unisex Short Sleeve Jersey T-Shirt with Tear Away Label (White / S)"
            },
            "files": [
                {
                    "id": 76564159,
                    "type": "default",
                    "hash": "ebd559858e5703088de8900ce99c37d3",
                    "url": "https://example.com/image.jpg",
                    "filename": "76564159.jpg",
                    "mime_type": "image/jpeg",
                    "size": 11246,
                    "width": 200,
                    "height": 300,
                    "dpi": null,
                    "status": "ok",
                    "created": 1540797879,
                    "thumbnail_url": "https://s3.dev.printful.com/files/ebd/ebd559858e5703088de8900ce99c37d3_thumb.png",
                    "preview_url": "https://s3.dev.printful.com/files/ebd/ebd559858e5703088de8900ce99c37d3_preview.png",
                    "visible": true
                }
            ],
            "options": [
                {
                    "id": "embroidery_type",
                    "value": "flat"
                },
                {
                    "id": "thread_colors",
                    "value": []
                },
                {
                    "id": "thread_colors_3d",
                    "value": []
                },
                {
                    "id": "thread_colors_chest_left",
                    "value": []
                }
            ]
        },
        "extra": [],
        "debug": []
    }</pre>

# Order

## Get list of orders
**undefined** /orders    
> Examples


## Create a new order
**undefined** /orders    
> Examples

**Request body:**
<pre>{
    "recipient": {
        "name": "John Doe",
        "address1": "19749 Dearborn St",
        "city": "Chatsworth",
        "state_code": "CA",
        "country_code": "US",
        "zip": "91311"
    },
    "items": [{
        "variant_id": 1,
        "quantity": 1,
        "files": [{
            "url": "http://example.com/files/posters/poster_1.jpg"
        }]
    }]
}</pre>

**Response data:**
<pre>{
    "code": 200,
    "result": {
        "id": 21510,
        "external_id": null,
        "status": "draft",
        "shipping": "STANDARD",
        "created": 1390825082,
        "updated": 1390825082,
        "recipient": {
            "name": "John Doe",
            "company": null,
            "address1": "19749 Dearborn St",
            "address2": null,
            "city": "Chatsworth",
            "state_code": "CA",
            "state_name": "California",
            "country_code": "US",
            "country_name": "United States",
            "zip": "91311",
            "phone": null,
            "email": null
        },
        "items": [{
            "id": 17621,
            "external_id": null,
            "variant_id": 1,
            "quantity": 1,
            "price": "13.00",
            "retail_price": null,
            "name": "Unframed Poster 18×24",
            "product": {
                "variant_id": 1,
                "product_id": 1,
                "image": "https://www.printful.com/storage/products/poster_18x24.jpg",
                "name": "Unframed Poster 18×24"
            },
            "files": [{
                "id": 11818,
                "type": "default",
                "hash": null,
                "url": "http://example.com/files/posters/poster_1.jpg",
                "filename": null,
                "mime_type": null,
                "size": 0,
                "width": null,
                "height": null,
                "dpi": null,
                "status": "waiting",
                "created": 1390823900,
                "thumbnail_url": null,
                "preview_url": null,
                "visible": true
            }],
            "options": []
        }],
        "costs": {
            "subtotal": "13.00",
            "discount": "0.00",
            "shipping": "7.95",
            "tax": "1.17",
            "total": "22.12"
        },
        "retail_costs": {
            "subtotal": null,
            "discount": null,
            "shipping": null,
            "tax": null,
            "total": null
        },
        "shipments": []
    }
}</pre>

**Request body:**
<pre>{
    "recipient": {
        "name": "John Doe",
        "address1": "19749 Dearborn St",
        "city": "Chatsworth",
        "state_code": "CA",
        "country_code": "US",
        "zip": "91311"
    },
    "items": [{
        "sync_variant_id": 1,
        "quantity": 1
    }]
}</pre>

**Response data:**
<pre>{
    "code": 200,
    "result": {
        "id": 11360229,
        "external_id": null,
        "store": 952434,
        "status": "draft",
        "error": null,
        "shipping": "PRINTFUL_FAST",
        "created": 1539584164,
        "updated": 1539584164,
        "recipient": {
            "name": "John Doe",
            "company": null,
            "address1": "19749 Dearborn St",
            "address2": null,
            "city": "Chatsworth",
            "state_code": "CA",
            "state_name": "California",
            "country_code": "US",
            "country_name": "United States",
            "zip": "91311",
            "phone": null,
            "email": null
        },
        "notes": null,
        "items": [
            {
                "id": 7253102,
                "external_id": null,
                "variant_id": 4011,
                "sync_variant_id": 866913817,
                "external_variant_id": "5bc04fbe956147",
                "quantity": 1,
                "price": "12.95",
                "retail_price": null,
                "name": "Short-Sleeve Unisex T-Shirt - S",
                "product": {
                    "variant_id": 4011,
                    "product_id": 71,
                    "image": "https://s3.dev.printful.com/products/71/4012_1517927381.jpg",
                    "name": "Bella + Canvas 3001 Unisex Short Sleeve Jersey T-Shirt with Tear Away Label (White / S)"
                },
                "files": [
                    {
                        "id": 76564071,
                        "type": "default",
                        "hash": "1c43709da13e3480049379d41e473ad9",
                        "url": null,
                        "filename": "printfile-23aeb205.png",
                        "mime_type": "image/png",
                        "size": 18660,
                        "width": 1800,
                        "height": 2400,
                        "dpi": 150,
                        "status": "ok",
                        "created": 1539329978,
                        "thumbnail_url": "https://s3.dev.printful.com/files/1c4/1c43709da13e3480049379d41e473ad9_thumb.png",
                        "preview_url": "https://s3.dev.printful.com/files/1c4/1c43709da13e3480049379d41e473ad9_preview.png",
                        "visible": false
                    },
                    {
                        "id": 76564072,
                        "type": "preview",
                        "hash": "2749bee4a392c4ee2f034c7246706329",
                        "url": null,
                        "filename": "mockup-6da92239.jpg",
                        "mime_type": "image/jpeg",
                        "size": 32944,
                        "width": 600,
                        "height": 600,
                        "dpi": 72,
                        "status": "ok",
                        "created": 1539329982,
                        "thumbnail_url": "https://s3.dev.printful.com/files/274/2749bee4a392c4ee2f034c7246706329_thumb.png",
                        "preview_url": "https://s3.dev.printful.com/files/274/2749bee4a392c4ee2f034c7246706329_preview.png",
                        "visible": false
                    }
                ],
                "options": [
                    {
                        "id": "embroidery_type",
                        "value": "flat"
                    },
                    {
                        "id": "thread_colors",
                        "value": []
                    },
                    {
                        "id": "thread_colors_3d",
                        "value": []
                    },
                    {
                        "id": "thread_colors_chest_left",
                        "value": []
                    }
                ],
                "sku": null,
                "discontinued": false,
                "out_of_stock": false
            }
        ],
        "is_sample": false,
        "needs_approval": false,
        "not_synced": false,
        "has_discontinued_items": false,
        "can_change_hold": true,
        "costs": {
            "currency": "USD",
            "subtotal": "12.95",
            "discount": "0.00",
            "shipping": "2.60",
            "digitization": "0.00",
            "additional_fee": "0.00",
            "fulfillment_fee": "0.00",
            "tax": "1.35",
            "vat": "0.00",
            "total": "16.90"
        },
        "retail_costs": {
            "currency": "USD",
            "subtotal": null,
            "discount": null,
            "shipping": null,
            "tax": null,
            "vat": null,
            "total": null
        },
        "shipments": [],
        "gift": null,
        "packing_slip": null,
        "dashboard_url": "https://www.printful.local/dashboard?order_id=11360229"
    },
    "extra": [],
    "debug": []
}</pre>

**Request body:**
<pre>{
    "recipient": {
        "name": "John Doe",
        "address1": "19749 Dearborn St",
        "city": "Chatsworth",
        "state_code": "CA",
        "country_code": "US",
        "zip": "91311"
    },
    "items": [{
        "external_variant_id": "5bc04fbe956148",
        "quantity": 1
    }]
}</pre>

**Response data:**
<pre>{
    "code": 200,
    "result": {
        "id": 11360229,
        "external_id": null,
        "store": 952434,
        "status": "draft",
        "error": null,
        "shipping": "PRINTFUL_FAST",
        "created": 1539584164,
        "updated": 1539584164,
        "recipient": {
            "name": "John Doe",
            "company": null,
            "address1": "19749 Dearborn St",
            "address2": null,
            "city": "Chatsworth",
            "state_code": "CA",
            "state_name": "California",
            "country_code": "US",
            "country_name": "United States",
            "zip": "91311",
            "phone": null,
            "email": null
        },
        "notes": null,
        "items": [
            {
                "id": 7253102,
                "external_id": null,
                "variant_id": 4011,
                "sync_variant_id": 866913817,
                "external_variant_id": "5bc04fbe956147",
                "quantity": 1,
                "price": "12.95",
                "retail_price": null,
                "name": "Short-Sleeve Unisex T-Shirt - S",
                "product": {
                    "variant_id": 4011,
                    "product_id": 71,
                    "image": "https://s3.dev.printful.com/products/71/4012_1517927381.jpg",
                    "name": "Bella + Canvas 3001 Unisex Short Sleeve Jersey T-Shirt with Tear Away Label (White / S)"
                },
                "files": [
                    {
                        "id": 76564071,
                        "type": "default",
                        "hash": "1c43709da13e3480049379d41e473ad9",
                        "url": null,
                        "filename": "printfile-23aeb205.png",
                        "mime_type": "image/png",
                        "size": 18660,
                        "width": 1800,
                        "height": 2400,
                        "dpi": 150,
                        "status": "ok",
                        "created": 1539329978,
                        "thumbnail_url": "https://s3.dev.printful.com/files/1c4/1c43709da13e3480049379d41e473ad9_thumb.png",
                        "preview_url": "https://s3.dev.printful.com/files/1c4/1c43709da13e3480049379d41e473ad9_preview.png",
                        "visible": false
                    },
                    {
                        "id": 76564072,
                        "type": "preview",
                        "hash": "2749bee4a392c4ee2f034c7246706329",
                        "url": null,
                        "filename": "mockup-6da92239.jpg",
                        "mime_type": "image/jpeg",
                        "size": 32944,
                        "width": 600,
                        "height": 600,
                        "dpi": 72,
                        "status": "ok",
                        "created": 1539329982,
                        "thumbnail_url": "https://s3.dev.printful.com/files/274/2749bee4a392c4ee2f034c7246706329_thumb.png",
                        "preview_url": "https://s3.dev.printful.com/files/274/2749bee4a392c4ee2f034c7246706329_preview.png",
                        "visible": false
                    }
                ],
                "options": [
                    {
                        "id": "embroidery_type",
                        "value": "flat"
                    },
                    {
                        "id": "thread_colors",
                        "value": []
                    },
                    {
                        "id": "thread_colors_3d",
                        "value": []
                    },
                    {
                        "id": "thread_colors_chest_left",
                        "value": []
                    }
                ],
                "sku": null,
                "discontinued": false,
                "out_of_stock": false
            }
        ],
        "is_sample": false,
        "needs_approval": false,
        "not_synced": false,
        "has_discontinued_items": false,
        "can_change_hold": true,
        "costs": {
            "currency": "USD",
            "subtotal": "12.95",
            "discount": "0.00",
            "shipping": "2.60",
            "digitization": "0.00",
            "additional_fee": "0.00",
            "fulfillment_fee": "0.00",
            "tax": "1.35",
            "vat": "0.00",
            "total": "16.90"
        },
        "retail_costs": {
            "currency": "USD",
            "subtotal": null,
            "discount": null,
            "shipping": null,
            "tax": null,
            "vat": null,
            "total": null
        },
        "shipments": [],
        "gift": null,
        "packing_slip": null,
        "dashboard_url": "https://www.printful.local/dashboard?order_id=11360229"
    },
    "extra": [],
    "debug": []
}</pre>

**Request body:**
<pre>{
    "external_id": "9887112",
    "recipient": {
        "name": "John Doe",
        "address1": "19749 Dearborn St",
        "city": "Chatsworth",
        "state_code": "CA",
        "country_code": "US",
        "zip": "91311"
    },
    "items": [{
        "variant_id": 2,
        "quantity": 1,
        "name": "Niagara Falls poster",
        "retail_price": "19.99",
        "files": [{
            "url": "http://example.com/files/posters/poster_2.jpg"
        }]
    }, {
        "variant_id": 1,
        "quantity": 3,
        "name": "Grand Canyon poster",
        "retail_price": "17.99",
        "files": [{
            "url": "http://example.com/files/posters/poster_3.jpg"
        }]
    }],
    "retail_costs": {
        "shipping": "24.50"
    }
}</pre>

**Response data:**
<pre>{
    "code": 200,
    "result": {
        "id": 21509,
        "external_id": "9887112",
        "status": "draft",
        "shipping": "STANDARD",
        "created": 1390825006,
        "updated": 1390825006,
        "recipient": {
            "name": "John Doe",
            "company": null,
            "address1": "19749 Dearborn St",
            "address2": null,
            "city": "Chatsworth",
            "state_code": "CA",
            "state_name": "California",
            "country_code": "US",
            "country_name": "United States",
            "zip": "91311",
            "phone": null,
            "email": null
        },
        "items": [{
            "id": 17619,
            "external_id": null,
            "variant_id": 2,
            "quantity": 1,
            "price": "18.00",
            "retail_price": "19.99",
            "name": "Niagara Falls poster",
            "product": {
                "variant_id": 2,
                "product_id": 1,
                "image": "https://www.printful.com/storage/products/poster_24x36.jpg",
                "name": "Unframed Poster 24×36"
            },
            "files": [{
                "id": 11819,
                "type": "default",
                "hash": null,
                "url": "http://example.com/files/posters/poster_2.jpg",
                "filename": null,
                "mime_type": null,
                "size": 0,
                "width": null,
                "height": null,
                "dpi": null,
                "status": "waiting",
                "created": 1390824712,
                "thumbnail_url": null,
                "preview_url": null,
                "visible": true
            }],
            "options": []
        }, {
            "id": 17620,
            "external_id": null,
            "variant_id": 1,
            "quantity": 3,
            "price": "13.00",
            "retail_price": "17.99",
            "name": "Grand Canyon poster",
            "product": {
                "variant_id": 1,
                "product_id": 1,
                "image": "https://www.printful.com/storage/products/poster_18x24.jpg",
                "name": "Unframed Poster 18×24"
            },
            "files": [{
                "id": 11820,
                "type": "default",
                "hash": null,
                "url": "http://example.com/files/posters/poster_3.jpg",
                "filename": null,
                "mime_type": null,
                "size": 0,
                "width": null,
                "height": null,
                "dpi": null,
                "status": "waiting",
                "created": 1390824712,
                "thumbnail_url": null,
                "preview_url": null,
                "visible": true
            }],
            "options": []
        }],
        "costs": {
            "subtotal": "57.00",
            "discount": "0.00",
            "shipping": "9.95",
            "tax": "5.13",
            "total": "72.08"
        },
        "retail_costs": {
            "subtotal": "73.96",
            "discount": "0.00",
            "shipping": "24.50",
            "tax": "0.00",
            "total": "98.46"
        },
        "shipments": []
    }
}</pre>

**Request body:**
<pre>{
    "recipient": {
        "name": "John Doe",
        "address1": "19749 Dearborn St",
        "city": "Chatsworth",
        "state_code": "CA",
        "country_code": "US",
        "zip": "91311"
    },
    "items": [{
        "variant_id": 1118,
        "quantity": 1,
        "files": [{
            "url": "http://example.com/files/tshirts/shirt_front.ai"
        }, {
            "type": "back",
            "url": "http://example.com/files/tshirts/shirt_back.ai"
        }, {
            "type": "preview",
            "url": "http://example.com/files/tshirts/shirt_mockup.jpg"
        }],
        "options": []
    }]
}</pre>

**Response data:**
<pre>{
    "code": 200,
    "result": {
        "id": 21516,
        "external_id": null,
        "status": "draft",
        "shipping": "STANDARD",
        "created": 1390825437,
        "updated": 1390825437,
        "recipient": {
            "name": "John Doe",
            "company": null,
            "address1": "19749 Dearborn St",
            "address2": null,
            "city": "Chatsworth",
            "state_code": "CA",
            "state_name": "California",
            "country_code": "US",
            "country_name": "United States",
            "zip": "91311",
            "phone": null,
            "email": null
        },
        "items": [{
            "id": 17627,
            "external_id": null,
            "variant_id": 1118,
            "quantity": 1,
            "price": "20.50",
            "retail_price": null,
            "name": "Alternative 1070 Short Sleeve Men T-Shirt (Black / M)",
            "product": {
                "variant_id": 1118,
                "product_id": 14,
                "image": "https://www.printful.com/storage/products/14/1095.jpg",
                "name": "Alternative 1070 Short Sleeve Men T-Shirt (Black / M)"
            },
            "files": [{
                "id": 11822,
                "type": "default",
                "hash": null,
                "url": "http://example.com/files/tshirts/shirt_front.ai",
                "filename": null,
                "mime_type": null,
                "size": 0,
                "width": null,
                "height": null,
                "dpi": null,
                "status": "waiting",
                "created": 1390825349,
                "thumbnail_url": null,
                "preview_url": null,
                "visible": true
            }, {
                "id": 11823,
                "type": "back",
                "hash": null,
                "url": "http://example.com/files/tshirts/shirt_back.ai",
                "filename": null,
                "mime_type": null,
                "size": 0,
                "width": null,
                "height": null,
                "dpi": null,
                "status": "waiting",
                "created": 1390825349,
                "thumbnail_url": null,
                "preview_url": null,
                "visible": true
            }, {
                "id": 11824,
                "type": "preview",
                "hash": null,
                "url": "http://example.com/files/tshirts/shirt_mockup.jpg",
                "filename": null,
                "mime_type": null,
                "size": 0,
                "width": null,
                "height": null,
                "dpi": null,
                "status": "waiting",
                "created": 1390825349,
                "thumbnail_url": null,
                "preview_url": null,
                "visible": true
            }],
            "options": []
        }],
        "costs": {
            "subtotal": "20.50",
            "discount": "0.00",
            "shipping": "5.50",
            "tax": "1.85",
            "total": "27.85"
        },
        "retail_costs": {
            "subtotal": null,
            "discount": null,
            "shipping": null,
            "tax": null,
            "total": null
        },
        "shipments": []
    }
}</pre>
# Order

## Get list of orders
**GET** /orders    
> Examples


## Create a new order
**POST** /orders    
> Examples

**Request body:**
<pre>{
    "recipient": {
        "name": "John Doe",
        "address1": "19749 Dearborn St",
        "city": "Chatsworth",
        "state_code": "CA",
        "country_code": "US",
        "zip": "91311"
    },
    "items": [{
        "variant_id": 1,
        "quantity": 1,
        "files": [{
            "url": "http://example.com/files/posters/poster_1.jpg"
        }]
    }]
}</pre>

**Response data:**
<pre>{
    "code": 200,
    "result": {
        "id": 21510,
        "external_id": null,
        "status": "draft",
        "shipping": "STANDARD",
        "created": 1390825082,
        "updated": 1390825082,
        "recipient": {
            "name": "John Doe",
            "company": null,
            "address1": "19749 Dearborn St",
            "address2": null,
            "city": "Chatsworth",
            "state_code": "CA",
            "state_name": "California",
            "country_code": "US",
            "country_name": "United States",
            "zip": "91311",
            "phone": null,
            "email": null
        },
        "items": [{
            "id": 17621,
            "external_id": null,
            "variant_id": 1,
            "quantity": 1,
            "price": "13.00",
            "retail_price": null,
            "name": "Unframed Poster 18×24",
            "product": {
                "variant_id": 1,
                "product_id": 1,
                "image": "https://www.printful.com/storage/products/poster_18x24.jpg",
                "name": "Unframed Poster 18×24"
            },
            "files": [{
                "id": 11818,
                "type": "default",
                "hash": null,
                "url": "http://example.com/files/posters/poster_1.jpg",
                "filename": null,
                "mime_type": null,
                "size": 0,
                "width": null,
                "height": null,
                "dpi": null,
                "status": "waiting",
                "created": 1390823900,
                "thumbnail_url": null,
                "preview_url": null,
                "visible": true
            }],
            "options": []
        }],
        "costs": {
            "subtotal": "13.00",
            "discount": "0.00",
            "shipping": "7.95",
            "tax": "1.17",
            "total": "22.12"
        },
        "retail_costs": {
            "subtotal": null,
            "discount": null,
            "shipping": null,
            "tax": null,
            "total": null
        },
        "shipments": []
    }
}</pre>

**Request body:**
<pre>{
    "recipient": {
        "name": "John Doe",
        "address1": "19749 Dearborn St",
        "city": "Chatsworth",
        "state_code": "CA",
        "country_code": "US",
        "zip": "91311"
    },
    "items": [{
        "sync_variant_id": 1,
        "quantity": 1
    }]
}</pre>

**Response data:**
<pre>{
    "code": 200,
    "result": {
        "id": 11360229,
        "external_id": null,
        "store": 952434,
        "status": "draft",
        "error": null,
        "shipping": "PRINTFUL_FAST",
        "created": 1539584164,
        "updated": 1539584164,
        "recipient": {
            "name": "John Doe",
            "company": null,
            "address1": "19749 Dearborn St",
            "address2": null,
            "city": "Chatsworth",
            "state_code": "CA",
            "state_name": "California",
            "country_code": "US",
            "country_name": "United States",
            "zip": "91311",
            "phone": null,
            "email": null
        },
        "notes": null,
        "items": [
            {
                "id": 7253102,
                "external_id": null,
                "variant_id": 4011,
                "sync_variant_id": 866913817,
                "external_variant_id": "5bc04fbe956147",
                "quantity": 1,
                "price": "12.95",
                "retail_price": null,
                "name": "Short-Sleeve Unisex T-Shirt - S",
                "product": {
                    "variant_id": 4011,
                    "product_id": 71,
                    "image": "https://s3.dev.printful.com/products/71/4012_1517927381.jpg",
                    "name": "Bella + Canvas 3001 Unisex Short Sleeve Jersey T-Shirt with Tear Away Label (White / S)"
                },
                "files": [
                    {
                        "id": 76564071,
                        "type": "default",
                        "hash": "1c43709da13e3480049379d41e473ad9",
                        "url": null,
                        "filename": "printfile-23aeb205.png",
                        "mime_type": "image/png",
                        "size": 18660,
                        "width": 1800,
                        "height": 2400,
                        "dpi": 150,
                        "status": "ok",
                        "created": 1539329978,
                        "thumbnail_url": "https://s3.dev.printful.com/files/1c4/1c43709da13e3480049379d41e473ad9_thumb.png",
                        "preview_url": "https://s3.dev.printful.com/files/1c4/1c43709da13e3480049379d41e473ad9_preview.png",
                        "visible": false
                    },
                    {
                        "id": 76564072,
                        "type": "preview",
                        "hash": "2749bee4a392c4ee2f034c7246706329",
                        "url": null,
                        "filename": "mockup-6da92239.jpg",
                        "mime_type": "image/jpeg",
                        "size": 32944,
                        "width": 600,
                        "height": 600,
                        "dpi": 72,
                        "status": "ok",
                        "created": 1539329982,
                        "thumbnail_url": "https://s3.dev.printful.com/files/274/2749bee4a392c4ee2f034c7246706329_thumb.png",
                        "preview_url": "https://s3.dev.printful.com/files/274/2749bee4a392c4ee2f034c7246706329_preview.png",
                        "visible": false
                    }
                ],
                "options": [
                    {
                        "id": "embroidery_type",
                        "value": "flat"
                    },
                    {
                        "id": "thread_colors",
                        "value": []
                    },
                    {
                        "id": "thread_colors_3d",
                        "value": []
                    },
                    {
                        "id": "thread_colors_chest_left",
                        "value": []
                    }
                ],
                "sku": null,
                "discontinued": false,
                "out_of_stock": false
            }
        ],
        "is_sample": false,
        "needs_approval": false,
        "not_synced": false,
        "has_discontinued_items": false,
        "can_change_hold": true,
        "costs": {
            "currency": "USD",
            "subtotal": "12.95",
            "discount": "0.00",
            "shipping": "2.60",
            "digitization": "0.00",
            "additional_fee": "0.00",
            "fulfillment_fee": "0.00",
            "tax": "1.35",
            "vat": "0.00",
            "total": "16.90"
        },
        "retail_costs": {
            "currency": "USD",
            "subtotal": null,
            "discount": null,
            "shipping": null,
            "tax": null,
            "vat": null,
            "total": null
        },
        "shipments": [],
        "gift": null,
        "packing_slip": null,
        "dashboard_url": "https://www.printful.local/dashboard?order_id=11360229"
    },
    "extra": [],
    "debug": []
}</pre>

**Request body:**
<pre>{
    "recipient": {
        "name": "John Doe",
        "address1": "19749 Dearborn St",
        "city": "Chatsworth",
        "state_code": "CA",
        "country_code": "US",
        "zip": "91311"
    },
    "items": [{
        "external_variant_id": "5bc04fbe956148",
        "quantity": 1
    }]
}</pre>

**Response data:**
<pre>{
    "code": 200,
    "result": {
        "id": 11360229,
        "external_id": null,
        "store": 952434,
        "status": "draft",
        "error": null,
        "shipping": "PRINTFUL_FAST",
        "created": 1539584164,
        "updated": 1539584164,
        "recipient": {
            "name": "John Doe",
            "company": null,
            "address1": "19749 Dearborn St",
            "address2": null,
            "city": "Chatsworth",
            "state_code": "CA",
            "state_name": "California",
            "country_code": "US",
            "country_name": "United States",
            "zip": "91311",
            "phone": null,
            "email": null
        },
        "notes": null,
        "items": [
            {
                "id": 7253102,
                "external_id": null,
                "variant_id": 4011,
                "sync_variant_id": 866913817,
                "external_variant_id": "5bc04fbe956147",
                "quantity": 1,
                "price": "12.95",
                "retail_price": null,
                "name": "Short-Sleeve Unisex T-Shirt - S",
                "product": {
                    "variant_id": 4011,
                    "product_id": 71,
                    "image": "https://s3.dev.printful.com/products/71/4012_1517927381.jpg",
                    "name": "Bella + Canvas 3001 Unisex Short Sleeve Jersey T-Shirt with Tear Away Label (White / S)"
                },
                "files": [
                    {
                        "id": 76564071,
                        "type": "default",
                        "hash": "1c43709da13e3480049379d41e473ad9",
                        "url": null,
                        "filename": "printfile-23aeb205.png",
                        "mime_type": "image/png",
                        "size": 18660,
                        "width": 1800,
                        "height": 2400,
                        "dpi": 150,
                        "status": "ok",
                        "created": 1539329978,
                        "thumbnail_url": "https://s3.dev.printful.com/files/1c4/1c43709da13e3480049379d41e473ad9_thumb.png",
                        "preview_url": "https://s3.dev.printful.com/files/1c4/1c43709da13e3480049379d41e473ad9_preview.png",
                        "visible": false
                    },
                    {
                        "id": 76564072,
                        "type": "preview",
                        "hash": "2749bee4a392c4ee2f034c7246706329",
                        "url": null,
                        "filename": "mockup-6da92239.jpg",
                        "mime_type": "image/jpeg",
                        "size": 32944,
                        "width": 600,
                        "height": 600,
                        "dpi": 72,
                        "status": "ok",
                        "created": 1539329982,
                        "thumbnail_url": "https://s3.dev.printful.com/files/274/2749bee4a392c4ee2f034c7246706329_thumb.png",
                        "preview_url": "https://s3.dev.printful.com/files/274/2749bee4a392c4ee2f034c7246706329_preview.png",
                        "visible": false
                    }
                ],
                "options": [
                    {
                        "id": "embroidery_type",
                        "value": "flat"
                    },
                    {
                        "id": "thread_colors",
                        "value": []
                    },
                    {
                        "id": "thread_colors_3d",
                        "value": []
                    },
                    {
                        "id": "thread_colors_chest_left",
                        "value": []
                    }
                ],
                "sku": null,
                "discontinued": false,
                "out_of_stock": false
            }
        ],
        "is_sample": false,
        "needs_approval": false,
        "not_synced": false,
        "has_discontinued_items": false,
        "can_change_hold": true,
        "costs": {
            "currency": "USD",
            "subtotal": "12.95",
            "discount": "0.00",
            "shipping": "2.60",
            "digitization": "0.00",
            "additional_fee": "0.00",
            "fulfillment_fee": "0.00",
            "tax": "1.35",
            "vat": "0.00",
            "total": "16.90"
        },
        "retail_costs": {
            "currency": "USD",
            "subtotal": null,
            "discount": null,
            "shipping": null,
            "tax": null,
            "vat": null,
            "total": null
        },
        "shipments": [],
        "gift": null,
        "packing_slip": null,
        "dashboard_url": "https://www.printful.local/dashboard?order_id=11360229"
    },
    "extra": [],
    "debug": []
}</pre>

**Request body:**
<pre>{
    "external_id": "9887112",
    "recipient": {
        "name": "John Doe",
        "address1": "19749 Dearborn St",
        "city": "Chatsworth",
        "state_code": "CA",
        "country_code": "US",
        "zip": "91311"
    },
    "items": [{
        "variant_id": 2,
        "quantity": 1,
        "name": "Niagara Falls poster",
        "retail_price": "19.99",
        "files": [{
            "url": "http://example.com/files/posters/poster_2.jpg"
        }]
    }, {
        "variant_id": 1,
        "quantity": 3,
        "name": "Grand Canyon poster",
        "retail_price": "17.99",
        "files": [{
            "url": "http://example.com/files/posters/poster_3.jpg"
        }]
    }],
    "retail_costs": {
        "shipping": "24.50"
    }
}</pre>

**Response data:**
<pre>{
    "code": 200,
    "result": {
        "id": 21509,
        "external_id": "9887112",
        "status": "draft",
        "shipping": "STANDARD",
        "created": 1390825006,
        "updated": 1390825006,
        "recipient": {
            "name": "John Doe",
            "company": null,
            "address1": "19749 Dearborn St",
            "address2": null,
            "city": "Chatsworth",
            "state_code": "CA",
            "state_name": "California",
            "country_code": "US",
            "country_name": "United States",
            "zip": "91311",
            "phone": null,
            "email": null
        },
        "items": [{
            "id": 17619,
            "external_id": null,
            "variant_id": 2,
            "quantity": 1,
            "price": "18.00",
            "retail_price": "19.99",
            "name": "Niagara Falls poster",
            "product": {
                "variant_id": 2,
                "product_id": 1,
                "image": "https://www.printful.com/storage/products/poster_24x36.jpg",
                "name": "Unframed Poster 24×36"
            },
            "files": [{
                "id": 11819,
                "type": "default",
                "hash": null,
                "url": "http://example.com/files/posters/poster_2.jpg",
                "filename": null,
                "mime_type": null,
                "size": 0,
                "width": null,
                "height": null,
                "dpi": null,
                "status": "waiting",
                "created": 1390824712,
                "thumbnail_url": null,
                "preview_url": null,
                "visible": true
            }],
            "options": []
        }, {
            "id": 17620,
            "external_id": null,
            "variant_id": 1,
            "quantity": 3,
            "price": "13.00",
            "retail_price": "17.99",
            "name": "Grand Canyon poster",
            "product": {
                "variant_id": 1,
                "product_id": 1,
                "image": "https://www.printful.com/storage/products/poster_18x24.jpg",
                "name": "Unframed Poster 18×24"
            },
            "files": [{
                "id": 11820,
                "type": "default",
                "hash": null,
                "url": "http://example.com/files/posters/poster_3.jpg",
                "filename": null,
                "mime_type": null,
                "size": 0,
                "width": null,
                "height": null,
                "dpi": null,
                "status": "waiting",
                "created": 1390824712,
                "thumbnail_url": null,
                "preview_url": null,
                "visible": true
            }],
            "options": []
        }],
        "costs": {
            "subtotal": "57.00",
            "discount": "0.00",
            "shipping": "9.95",
            "tax": "5.13",
            "total": "72.08"
        },
        "retail_costs": {
            "subtotal": "73.96",
            "discount": "0.00",
            "shipping": "24.50",
            "tax": "0.00",
            "total": "98.46"
        },
        "shipments": []
    }
}</pre>

**Request body:**
<pre>{
    "recipient": {
        "name": "John Doe",
        "address1": "19749 Dearborn St",
        "city": "Chatsworth",
        "state_code": "CA",
        "country_code": "US",
        "zip": "91311"
    },
    "items": [{
        "variant_id": 1118,
        "quantity": 1,
        "files": [{
            "url": "http://example.com/files/tshirts/shirt_front.ai"
        }, {
            "type": "back",
            "url": "http://example.com/files/tshirts/shirt_back.ai"
        }, {
            "type": "preview",
            "url": "http://example.com/files/tshirts/shirt_mockup.jpg"
        }],
        "options": []
    }]
}</pre>

**Response data:**
<pre>{
    "code": 200,
    "result": {
        "id": 21516,
        "external_id": null,
        "status": "draft",
        "shipping": "STANDARD",
        "created": 1390825437,
        "updated": 1390825437,
        "recipient": {
            "name": "John Doe",
            "company": null,
            "address1": "19749 Dearborn St",
            "address2": null,
            "city": "Chatsworth",
            "state_code": "CA",
            "state_name": "California",
            "country_code": "US",
            "country_name": "United States",
            "zip": "91311",
            "phone": null,
            "email": null
        },
        "items": [{
            "id": 17627,
            "external_id": null,
            "variant_id": 1118,
            "quantity": 1,
            "price": "20.50",
            "retail_price": null,
            "name": "Alternative 1070 Short Sleeve Men T-Shirt (Black / M)",
            "product": {
                "variant_id": 1118,
                "product_id": 14,
                "image": "https://www.printful.com/storage/products/14/1095.jpg",
                "name": "Alternative 1070 Short Sleeve Men T-Shirt (Black / M)"
            },
            "files": [{
                "id": 11822,
                "type": "default",
                "hash": null,
                "url": "http://example.com/files/tshirts/shirt_front.ai",
                "filename": null,
                "mime_type": null,
                "size": 0,
                "width": null,
                "height": null,
                "dpi": null,
                "status": "waiting",
                "created": 1390825349,
                "thumbnail_url": null,
                "preview_url": null,
                "visible": true
            }, {
                "id": 11823,
                "type": "back",
                "hash": null,
                "url": "http://example.com/files/tshirts/shirt_back.ai",
                "filename": null,
                "mime_type": null,
                "size": 0,
                "width": null,
                "height": null,
                "dpi": null,
                "status": "waiting",
                "created": 1390825349,
                "thumbnail_url": null,
                "preview_url": null,
                "visible": true
            }, {
                "id": 11824,
                "type": "preview",
                "hash": null,
                "url": "http://example.com/files/tshirts/shirt_mockup.jpg",
                "filename": null,
                "mime_type": null,
                "size": 0,
                "width": null,
                "height": null,
                "dpi": null,
                "status": "waiting",
                "created": 1390825349,
                "thumbnail_url": null,
                "preview_url": null,
                "visible": true
            }],
            "options": []
        }],
        "costs": {
            "subtotal": "20.50",
            "discount": "0.00",
            "shipping": "5.50",
            "tax": "1.85",
            "total": "27.85"
        },
        "retail_costs": {
            "subtotal": null,
            "discount": null,
            "shipping": null,
            "tax": null,
            "total": null
        },
        "shipments": []
    }
}</pre>

## Estimate order costs
**POST** /orders/estimate-costs    


## Get order data
**GET** /orders/


## Cancel an order
**DELETE** /orders/


## Update order data
**PUT** /orders/


## Confirm draft for fulfillment
**POST** /orders/
