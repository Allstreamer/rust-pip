# Documentation & Explanations for the PyPi API
This markdown file will serve as a refrence for building our PyPi comunication interface, below you will find:

1. A General explenation of how we will access PyPi
2. API Refrences


## 1. General explenation of how we will access PyPi
### 1.1 Getting Package Information

PyPi offers a public API which allows querrying for Projects information via a `get` request such as:

```GET https://pypi.org/pypi/<project_name>/json```

Which returns JSON data in the format of:

```JSON
{
    "info": {
        "author": "The Python Packaging Authority",
        "author_email": "pypa-dev@googlegroups.com",
        "bugtrack_url": "",
        "classifiers": [
            "Development Status :: 3 - Alpha",
            "Intended Audience :: Developers",
            "License :: OSI Approved :: MIT License",
            "Programming Language :: Python :: 2",
            "Programming Language :: Python :: 2.6",
            "Programming Language :: Python :: 2.7",
            "Programming Language :: Python :: 3",
            "Programming Language :: Python :: 3.2",
            "Programming Language :: Python :: 3.3",
            "Programming Language :: Python :: 3.4",
            "Topic :: Software Development :: Build Tools"
        ],
        "description": "...",
        "description_content_type": null,
        "docs_url": null,
        "download_url": "UNKNOWN",
        "downloads": {
            "last_day": -1,
            "last_month": -1,
            "last_week": -1
        },
        "home_page": "https://github.com/pypa/sampleproject",
        "keywords": "sample setuptools development",
        "license": "MIT",
        "maintainer": null,
        "maintainer_email": null,
        "name": "sampleproject",
        "package_url": "https://pypi.org/project/sampleproject/",
        "platform": "UNKNOWN",
        "project_url": "https://pypi.org/project/sampleproject/",
        "project_urls": {
            "Download": "UNKNOWN",
            "Homepage": "https://github.com/pypa/sampleproject"
        },
        "release_url": "https://pypi.org/project/sampleproject/1.2.0/",
        "requires_dist": null,
        "requires_python": null,
        "summary": "A sample Python project",
        "version": "1.2.0",
        "yanked": false,
        "yanked_reason": null
    },
    "last_serial": 1591652,
    "releases": {
        "1.0": [],
        "1.2.0": [
            {
                "comment_text": "",
                "digests": {
                    "md5": "bab8eb22e6710eddae3c6c7ac3453bd9",
                    "sha256": "7a7a8b91086deccc54cac8d631e33f6a0e232ce5775c6be3dc44f86c2154019d"
                },
                "downloads": -1,
                "filename": "sampleproject-1.2.0-py2.py3-none-any.whl",
                "has_sig": false,
                "md5_digest": "bab8eb22e6710eddae3c6c7ac3453bd9",
                "packagetype": "bdist_wheel",
                "python_version": "2.7",
                "size": 3795,
                "upload_time_iso_8601": "2015-06-14T14:38:05.093750Z",
                "url": "https://files.pythonhosted.org/packages/30/52/547eb3719d0e872bdd6fe3ab60cef92596f95262e925e1943f68f840df88/sampleproject-1.2.0-py2.py3-none-any.whl",
                "yanked": false,
                "yanked_reason": null
            },
            {
                "comment_text": "",
                "digests": {
                    "md5": "d3bd605f932b3fb6e91f49be2d6f9479",
                    "sha256": "3427a8a5dd0c1e176da48a44efb410875b3973bd9843403a0997e4187c408dc1"
                },
                "downloads": -1,
                "filename": "sampleproject-1.2.0.tar.gz",
                "has_sig": false,
                "md5_digest": "d3bd605f932b3fb6e91f49be2d6f9479",
                "packagetype": "sdist",
                "python_version": "source",
                "size": 3148,
                "upload_time_iso_8601": "2015-06-14T14:37:56Z",
                "url": "https://files.pythonhosted.org/packages/eb/45/79be82bdeafcecb9dca474cad4003e32ef8e4a0dec6abbd4145ccb02abe1/sampleproject-1.2.0.tar.gz",
                "yanked": false,
                "yanked_reason": null
            }
        ]
    },
    "urls": [
        {
            "comment_text": "",
            "digests": {
                "md5": "bab8eb22e6710eddae3c6c7ac3453bd9",
                "sha256": "7a7a8b91086deccc54cac8d631e33f6a0e232ce5775c6be3dc44f86c2154019d"
            },
            "downloads": -1,
            "filename": "sampleproject-1.2.0-py2.py3-none-any.whl",
            "has_sig": false,
            "md5_digest": "bab8eb22e6710eddae3c6c7ac3453bd9",
            "packagetype": "bdist_wheel",
            "python_version": "2.7",
            "size": 3795,
            "upload_time_iso_8601": "2015-06-14T14:38:05.234526",
            "url": "https://files.pythonhosted.org/packages/30/52/547eb3719d0e872bdd6fe3ab60cef92596f95262e925e1943f68f840df88/sampleproject-1.2.0-py2.py3-none-any.whl",
            "yanked": false,
            "yanked_reason": null
        },
        {
            "comment_text": "",
            "digests": {
                "md5": "d3bd605f932b3fb6e91f49be2d6f9479",
                "sha256": "3427a8a5dd0c1e176da48a44efb410875b3973bd9843403a0997e4187c408dc1"
            },
            "downloads": -1,
            "filename": "sampleproject-1.2.0.tar.gz",
            "has_sig": false,
            "md5_digest": "d3bd605f932b3fb6e91f49be2d6f9479",
            "packagetype": "sdist",
            "python_version": "source",
            "size": 3148,
            "upload_time_iso_8601": "2015-06-14T14:37:56.000001Z",
            "url": "https://files.pythonhosted.org/packages/eb/45/79be82bdeafcecb9dca474cad4003e32ef8e4a0dec6abbd4145ccb02abe1/sampleproject-1.2.0.tar.gz",
            "yanked": false,
            "yanked_reason": null
        }
    ],
    "vulnerabilities": []
}
```

This request gives vital information such as the latest version of the requested package, download links to it's wheel and vital vulnerability information


## 2. API Refrences

- [2.1 Warehouse.Pypa.io JSON API](https://warehouse.pypa.io/api-reference/json.html)
