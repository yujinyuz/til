# DRF to_representation

> Saturday, July 31, 2021

I was trying out something and as I thought, Serializer.to_representation doesn't get picked up by auto generating documents like drf-spectacular.

For context, I am trying to add [drf-spectacular](https://drf-spectacular.readthedocs.io/en/latest/readme.html) to one of my projects and I want to return a custom response and wanted swagger to pick it up.

As expected, it can't. So I went ahead and just used `drf_spectacular.utils.extend_schema` decorator.





---

_References_

* ...
