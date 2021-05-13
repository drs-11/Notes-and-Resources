- use ```dataclasses```  for small, quick classes:
  
  ```python
  from dataclasses import dataclass
  
  @dataclass
  class C:
      a: int       # 'a' has no default value
      b: int = 0   # assign a default value for 'b'
  ```

- use ```collections.Counter``` instead of iterative counting:
  
  ```python
  c = Counter()                           # a new, empty counter
  c = Counter('gallahad')                 # a new counter from an iterable
  c = Counter({'red': 4, 'blue': 2})      # a new counter from a mapping
  c = Counter(cats=4, dogs=8)             # a new counter from keyword args
  ```

- use ```iter``` but why and when

- for xor-ing variables use:
  
  ```python
  bool(a) ^ bool(b)
  ```
