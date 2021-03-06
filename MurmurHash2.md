**Info about MurmurHash2**

Introduction
============

MurmurHash2 is a previous version of MurmurHash, and was published in 2008. It was considerably speedier than MurmurHash1, but was discovered to have a [flaw](https://github.com/aappleby/smhasher/wiki/MurmurHash2Flaw) that, while not affecting most applications, was still worth fixing.

MurmurHash2's mix function is

```
k *= m;
k ^= k >> r;
k *= m;

h *= m;
h ^= k;
```

where `k` is a block of the key, `m` and `r` are constants, and `h` is the 32-bit hash state.