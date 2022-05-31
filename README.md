# Wb-MSF
Wb-MSF: Multi-Source Information Diffusion Dataset on Weibo

## Dataset Description
### (Re)Post Cascade

Each cascade is saved in a csv file with following properties:

|   Property   |         Description          |
| :----------: | :--------------------------: |
|   *origin*   | precursor post id (be reposted) |
| *origin_uid* |  user id of precursor post   |
|     *id*     |           post id            |
|    *uid*     |           user id            |
|  created_at  |        (re)post time         |

- **The properties of italics is the private user information, which are hashed;**
- Property `created_at` is format as `YYYY-mm-DD HH:MM:SS` ;
- If `origin` is `NULL` and `origin_uid == uid` , means this post is original and not reposted.

### Followership

Each dataset has a global followership network, format as edge list: each line of `{dataname}_followership.txt` is a pair of comma separated user ids $u,v$ , means $u$ is followed by $v$ and $v$ is one of $u$'s fans. 

### Hash
To protect user privacy, we anonymize the data: i.e., we hash the fields related to `user-id` and `post-id`.

## Download
Due to the limitation of file size, you can download the small-scale version of Wb-MSF from the [release page](https://github.com/Les1ie/Wb-MSF/releases/tag/v0.0.1) of this repository (MSC and SSC both contain 1K cascades).

The full version will be released soon.

## Cite Us
```
@inproceedings{wbmsf2022,
  author          = {Wu, Zhen and Zhou, Jingya and Liu, Ling and Wang, Jie and Sun, Xigang},
  booktitle       = {Proceedings of the 31st ACM International Conference on Information and Knowledge Management},
  title           = {Wb-MSF: Multi-Source Information Diffusion Dataset on Weibo},
  year            = {2022}
}
```
