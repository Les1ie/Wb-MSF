# Wb-MSF
Wb-MSF: Multi-Source Information Diffusion Dataset on Weibo

## Dataset Description
### (Re)Post Cascade

Each cascade is saved in a csv file with following properties:

|   Property   |         Description          |
| :----------: | :--------------------------: |
|   *origin_id*   | precursor post id (be reposted) |
| *origin_uid* |  user id of precursor post   |
|     *id*     |           post id            |
|    *uid*     |           user id            |
|  *created_at*  |        (re)post time         |

- **The properties of italics is the private user information, which are hashed;**
- Property `created_at` is format as `YYYY-mm-DD HH:MM:SS` ;
- If `origin_id` is `NULL` and `origin_uid == uid` , means this post is original and not reposted.

### Followership

Each dataset has a global followership network, format as edge list: each line of `{dataname}_followership.txt` is a pair of comma separated user ids $u,v$ , means $u$ is followed by $v$ and $v$ is one of $u$'s fans. 

### Hash
To protect user privacy, we anonymize the data: i.e., we hash the fields related to `user-id` and `post-id`.

## Download
Due to the limitation of file size, you can download the small-scale version of Wb-MSF from the [release page](https://github.com/Les1ie/Wb-MSF/releases/tag/v0.0.1) of this repository (MSC and SSC both contain 1K cascades).

The full version will be released soon.

## Cite Us
```
@inproceedings{WBMSF_2022,
  author     = {Wu, Zhen and Zhou, Jingya and Wang, Jie and Sun, Xigang},
  title      = {Wb-MSF: A Large-scale Multi-source Information Diffusion Dataset for Social Information Diffusion Prediction},
  booktitle  = {2022 Tenth International Conference on Advanced Cloud and Big Data (CBD)},
  year       = {2022},
}

@inproceedings{HERIGCN_2022,
  author          = {Wu, Zhen and Zhou, Jingya and Liu, Ling and Li, Chaozhuo and Gu, Fei},
  title           = {Deep Popularity Prediction in Multi-Source Cascade with HERI-GCN},
  booktitle       = {2022 IEEE 38th International Conference on Data Engineering (ICDE)},
  year            = {2022}
}
```
