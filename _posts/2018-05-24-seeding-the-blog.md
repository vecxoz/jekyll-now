---
layout: post
title: Seeding the Blog
---

When we start something that involves some kind of randomness we prefere to use random seed. Blog is not an exception. And of course the best place for such things is the very first post.

## Seed

Let's seed our blog:

```python
class BlogSeeder(object):
    """Class for blog seeding"""

    def __init__(self, _seed=0):
        self._seed = _seed

    @property
    def seed(self):
        return self._seed

    @seed.setter
    def seed(self, new_seed):
        self._seed = new_seed

    @seed.deleter
    def seed(self):
        self._seed = None

    def do_seed(self):
        np.random.seed(self._seed)
        print('Seeding completed successfully!')

if __name__ == '__main__':
    import numpy as np
    bs = BlogSeeder(42)
    print('Current seed is: %d' % bs.seed)
    bs.do_seed()
```

Result:

```
Current seed is: 42
Seeding completed successfully!
```
