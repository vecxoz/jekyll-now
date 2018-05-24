---
layout: post
title: Seeding the Blog
---

When we start something that involves some kind of randomness we prefere to use random seed. Blog is not an exception. And of course the best place for such things is the very first post.

## Seed

Let's seed our blog:

```python
class Blog(object):
    """Blog class"""

    def __init__(self):
        self._seed = None

    @property
    def seed(self):
        return self._seed

    @seed.setter
    def seed(self, new_seed):
        self._seed = new_seed
        print('Seeding completed successfully!')

    @seed.deleter
    def seed(self):
        self._seed = None
        print('Seed is not set!')

if __name__ == '__main__':
    blog = Blog()
    blog.seed = 42
    print('Current seed is: %d' % blog.seed)
```

Result:

```
Seeding completed successfully!
Current seed is: 42
```
