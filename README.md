# Vulners signature-base software version detection rules

# Description
Vulners rules are used in [Vulners Burp Plugin](https://github.com/vulnersCom/burp-vulners-scanner) for the software:version pairs detection. Using this regular expressions and aliases plugin calls [Vulners Burp API](https://vulners.com/api/v3/burp/software/?) to find vulnerabilities.

# Rule structure

The rule structure is:

```python
"jQuery": {
        "regex": "jQuery v([\\d.]+)",
        "alias": "jquery",
        "type": "software"
    },
```
## "jQuery"
Is the human-readable alias.

## "regex"
Regular expression with single match group to find version of the product.
It will be used on the raw plain-text server HTTP reply.

## "alias"
CPE string or software name alias. CPE is the preffered method.

## "type"
"cpe" or "software".
When "cpe" is selected, alias must me a CPE string like in this example:

```python
"mod_perl": {
        "regex": "mod_perl/([\\d.]+)",
        "alias": "cpe:/a:apache:mod_perl",
        "type": "cpe"
    },
```

# Contributors

Vulners Team <support@vulners.com>



