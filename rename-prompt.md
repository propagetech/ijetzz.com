You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "ABOUT US",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "air-cargo-services.html",
    "context": {
      "title": "AIR CARGO SERVICES",
      "first_heading": "AIR CARGO SERVICES"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "CONTACT US",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/5e3a198b9f557dce8bcf744d800929a9.css",
    "context": {
      "path": "css/5e3a198b9f557dce8bcf744d800929a9.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/9e78a9df7c3f211b97abb945170ccdbd.css",
    "context": {
      "path": "css/9e78a9df7c3f211b97abb945170ccdbd.css"
    }
  },
  {
    "path": "css/c363a15baf9b3719c1570c22b012b369.css",
    "context": {
      "path": "css/c363a15baf9b3719c1570c22b012b369.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "customs-and-regulatory.html",
    "context": {
      "title": "CUSTOMS & REGULATORY",
      "first_heading": "CUSTOMS & REGULATORY"
    }
  },
  {
    "path": "domestic-coverage.html",
    "context": {
      "title": "Domestic Coverage",
      "first_heading": "DOMESTIC COVERAGE"
    }
  },
  {
    "path": "factory-relocation.html",
    "context": {
      "title": "FACTORY RELOCATION",
      "first_heading": "FACTORY RELOCATION"
    }
  },
  {
    "path": "full-truck-load-and-less-than-truckload.html",
    "context": {
      "title": "FULL TRUCK LOAD (FTL) & LESS THAN TRUCKLOAD (LTL)",
      "first_heading": "FULL TRUCK LOAD (FTL) & LESS THAN TRUCKLOAD (LTL)"
    }
  },
  {
    "path": "home-shifting-office-relocation.html",
    "context": {
      "title": "HOME SHIFTING / OFFICE RELOCATION",
      "first_heading": "HOME SHIFTING / OFFICE RELOCATION"
    }
  },
  {
    "path": "imgs/0083f9530494bdf966eeb8bbe4e7b575.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/09edfdf2991adbcf899db0474b29b357.webp",
    "context": {
      "refs": [
        {
          "alt": "Industrial",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/139937a669fb91a46e2990b80c6da59a.webp",
    "context": {
      "refs": [
        {
          "alt": "LOGISTICS AND TRANSPORTATION SERVICES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1684065a4bee3cf18d0048ccb872cf16.webp",
    "context": {
      "refs": [
        {
          "alt": "Dangerous Goods Prohibited",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1c205e81b0e2cf22ceccc777b84ffcdf.webp",
    "context": {
      "refs": [
        {
          "alt": "Marineparts",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/204904366e61f1a4a323f3b5d85b930c.webp",
    "context": {
      "refs": [
        {
          "alt": "Logistics & Transportation Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2622bb6f19814d8882d051ca2b98892a.webp",
    "context": {
      "refs": [
        {
          "alt": "IJETZZ LOGISTICS PVT LTD",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2ad60ee79d36f970c4b56834c07cb098.webp",
    "context": {
      "refs": [
        {
          "alt": "Air Cargo Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3582e1b0d7d329ee9e5f530e6bfc248e.webp",
    "context": {
      "refs": [
        {
          "alt": "FACTORY RELOCATION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/380da0176660b43eb07040ba671b9a9b.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3c55b175f3da93e980f26beed1b00fb8.webp",
    "context": {
      "refs": [
        {
          "alt": "Full Truck Load (FTL)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/43ada02e57b1acb25bf2ed100222e76e.webp",
    "context": {
      "refs": [
        {
          "alt": "Automotives",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/478923b6acb389c62e9faa495dfc1c7f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/560484127460839c85f8b273e1165b83.webp",
    "context": {
      "refs": [
        {
          "alt": "Timeliness",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/56e04d733164ef50294a61ab45c8bb68.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/577efe6a13aa8e286127b3d7885fa163.webp",
    "context": {
      "refs": [
        {
          "alt": "Electronics",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5bb7ba20fef37bb5da6909ec0f3c82b6.webp",
    "context": {
      "refs": [
        {
          "alt": "Integrity",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/653556a1fcc223ec8de25b841f082c7c.webp",
    "context": {
      "refs": [
        {
          "alt": "Factory Relocation",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6c553143ef00bf2c6c4a99b5be4b9da6.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/7f9d3f900282af0ebd24601bd42aad59.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8092f2b2b257a68b4031a3a316056660.webp",
    "context": {
      "refs": [
        {
          "alt": "Retail",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/859ec94052b336283d6753ce9f600a20.webp",
    "context": {
      "refs": [
        {
          "alt": "Less Than Truckload (LTL)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8c1ff1494af58c8108a8e47ce89922d1.webp",
    "context": {
      "refs": [
        {
          "alt": "Managed Transportation Solutions",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8cda47f76c87f385632df80379afb0ae.webp",
    "context": {
      "refs": [
        {
          "alt": "Consumers",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/915d8a7ba9bcbe8f775e47744cb3e895.webp",
    "context": {
      "refs": [
        {
          "alt": "Full Truck Load (FTL) &\u00a0Less Than Truckload (LTL)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9755b9bce534fab102a4907fc3ae9565.webp",
    "context": {
      "refs": [
        {
          "alt": "Thinking the way forward",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/979506230a79ba148523dcba583748cd.webp",
    "context": {
      "refs": [
        {
          "alt": "Home Shifting / Office Relocation",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a22d2c18afda191b9ca430b9c5bf281a.webp",
    "context": {
      "refs": [
        {
          "alt": "Caring Attitude",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a22e86420565601cdcd891c1f3a768ba.webp",
    "context": {
      "refs": [
        {
          "alt": "Healthcare",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a74e559972cca6947b79ab1dcb16aa5c.webp",
    "context": {
      "refs": [
        {
          "alt": "Quality",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a779ee126523a62ff0476daff626b250.webp",
    "context": {
      "refs": [
        {
          "alt": "AIR CARGO SERVICES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aa7a0f5a8fbb13dbd9e2e5d96de990e0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ac0525804fccededeca16da91e34c8fd.webp",
    "context": {
      "refs": [
        {
          "alt": "Aerospace",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae4454f4d4fc031bb5e44144a7d58770.webp",
    "context": {
      "refs": [
        {
          "alt": "Ijetzz presentation",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b4be9d345a1c872b7b13d59a28c2b9d6.webp",
    "context": {
      "refs": [
        {
          "alt": "INDUSTRIES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b787bce823d10daaee6c7579e8672b2a.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Vision",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c6e4a54a64571d27bf1813ae6a860114.webp",
    "context": {
      "refs": [
        {
          "alt": "Chemicals",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cac155920cbf19d5f02d4d2b68d01ea6.webp",
    "context": {
      "refs": [
        {
          "alt": "Banned Commodities",
          "title": ""
        },
        {
          "alt": "CUSTOMS & REGULATORY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d837bccf1bc41a59fb51a8c758dff95c.webp",
    "context": {
      "refs": [
        {
          "alt": "http://tracks.ijetzz.com/main.php",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/da6393b3d529d91b0f03de007e028fc5.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Mission",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dcfa6c5f230af023e0f42c1032aa3995.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e2fc37e54f871206034e33be8a7b74c8.webp",
    "context": {
      "refs": [
        {
          "alt": "Train Cargo Service",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e327bcb8dbc145e8cedd75aa7817d9fb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e58aa1c3f609135538c743f96676b800.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec5ca1fc60472068a5d5936707e5ad90.webp",
    "context": {
      "refs": [
        {
          "alt": "HOME SHIFTING / OFFICE RELOCATION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0f52be119533804197f1edfba5f2028.webp",
    "context": {
      "refs": [
        {
          "alt": "SUPPLY CHAIN SOLUTIONS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc2ee8ec425d6d10e33bec226a3df6de.webp",
    "context": {
      "refs": [
        {
          "alt": "TRAIN CARGO SERVICE",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc980022d26373fa9a8dd728c56cfb28.webp",
    "context": {
      "refs": [
        {
          "alt": "Quality Transport Solutions",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "IJETZZ LOGISTICS PVT LTD | HOME",
      "first_heading": "Thinking the way forward"
    }
  },
  {
    "path": "industries.html",
    "context": {
      "title": "INDUSTRIES",
      "first_heading": "INDUSTRIES"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "logistics-and-transportation-services.html",
    "context": {
      "title": "LOGISTICS AND TRANSPORTATION SERVICES",
      "first_heading": "LOGISTICS AND TRANSPORTATION SERVICES"
    }
  },
  {
    "path": "supply-chain-solutions.html",
    "context": {
      "title": "SOLUTIONS",
      "first_heading": "SUPPLY CHAIN SOLUTIONS"
    }
  },
  {
    "path": "tracking.html",
    "context": {
      "title": "Tracking",
      "first_heading": "TRACKING"
    }
  },
  {
    "path": "train-cargo-service.html",
    "context": {
      "title": "TRAIN CARGO SERVICE",
      "first_heading": "TRAIN CARGO SERVICE"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.