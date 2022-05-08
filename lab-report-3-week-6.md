
# Lab Report 3

## .ssh/config file
The config file was edited in WSL using nano
![image](/assets/images/config.png)

## Logging in using alias
![login](/assets/images/login.png)

## Copying file to server with SCP
```
jason@JasonPC:~$ scp someFile ieng6:~/
someFile                                                                                                                                                             100%    0     0.0KB/s   00:00    
jason@JasonPC:~$ 
```

## SSH Key in Github
![sshKeys](/assets/images//sshkeys.png)

## Private SSH key on ieng6
```
[cs15lsp22ajb@ieng6-203]:~:286$ cd .ssh/
[cs15lsp22ajb@ieng6-203]:.ssh:287$ ls
authorized_keys  id_rsa  id_rsa.pub  known_hosts
```


## Running git commands on ieng6
[Link to commit](https://github.com/JasonMorris1/Live/commit/c5eb1d7a6624a765132effd6884f088ae6cb19e0)
```
[cs15lsp22ajb@ieng6-203]:Live:292$ nano Live.java
[cs15lsp22ajb@ieng6-203]:Live:293$ git add *
[cs15lsp22ajb@ieng6-203]:Live:294$ git commit -m "added a comment"
[main c5eb1d7] added a comment
 1 file changed, 1 insertion(+), 1 deletion(-)
[cs15lsp22ajb@ieng6-203]:Live:295$ git push  
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 309 bytes | 19.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:JasonMorris1/Live.git
   df0f2de..c5eb1d7  main -> main
[cs15lsp22ajb@ieng6-203]:Live:296$ 
```

## Copying markdown-parse wit scp -r
```
jason@JasonPC:/mnt/c/Users/jason/Documents/markdown-parser$ scp -r . ieng6:~/markdown-parse
COMMIT_EDITMSG                                                                                                                                                       100%   15     0.5KB/s   00:00    
config                                                                                                                                                               100%  461    13.7KB/s   00:00    
description                                                                                                                                                          100%   73     2.5KB/s   00:00    
FETCH_HEAD                                                                                                                                                           100%  121     5.3KB/s   00:00    
HEAD                                                                                                                                                                 100%   21     0.7KB/s   00:00    
applypatch-msg.sample                                                                                                                                                100%  478    19.2KB/s   00:00    
commit-msg.sample                                                                                                                                                    100%  896    30.9KB/s   00:00    
fsmonitor-watchman.sample                                                                                                                                            100% 4655   107.4KB/s   00:00    
post-update.sample                                                                                                                                                   100%  189     4.6KB/s   00:00    
pre-applypatch.sample                                                                                                                                                100%  424    13.8KB/s   00:00    
pre-commit.sample                                                                                                                                                    100% 1643    38.2KB/s   00:00    
pre-merge-commit.sample                                                                                                                                              100%  416    12.0KB/s   00:00    
pre-push.sample                                                                                                                                                      100% 1374    54.8KB/s   00:00    
pre-rebase.sample                                                                                                                                                    100% 4898    97.6KB/s   00:00    
pre-receive.sample                                                                                                                                                   100%  544    17.3KB/s   00:00    
prepare-commit-msg.sample                                                                                                                                            100% 1492    36.1KB/s   00:00    
push-to-checkout.sample                                                                                                                                              100% 2783    50.4KB/s   00:00    
update.sample                                                                                                                                                        100% 3650    72.9KB/s   00:00    
index                                                                                                                                                                100% 2112    57.6KB/s   00:00    
exclude                                                                                                                                                              100%  240     6.8KB/s   00:00    
HEAD                                                                                                                                                                 100% 6782   157.3KB/s   00:00    
main                                                                                                                                                                 100% 6782   142.0KB/s   00:00    
HEAD                                                                                                                                                                 100%  199     5.2KB/s   00:00    
main                                                                                                                                                                 100% 4774    79.1KB/s   00:00    
main                                                                                                                                                                 100%  549    23.3KB/s   00:00    
799e1b3b9fa1f2fbc86af878686e58523873b8                                                                                                                               100%  174     6.7KB/s   00:00    
1b99a6db3649ce42fa1b9c11cbb496eed45d48                                                                                                                               100%   43     0.8KB/s   00:00    
d95aa8f8b17bb7433c807c59aaa2417e541de1                                                                                                                               100%   55     1.9KB/s   00:00    
6335a1ae1b43d45ec9de511ec5d90beac9dac9                                                                                                                               100%  168     4.6KB/s   00:00    
3728b578c2373f1fd981c8d15b4529afaeb7c7                                                                                                                               100%   43     1.5KB/s   00:00    
771799ebab3ebc70c76d210f4049db77316ef9                                                                                                                               100%  165     5.0KB/s   00:00    
8858eb92356526619f56f4678bc6a7e069268e                                                                                                                               100%  546     8.9KB/s   00:00    
40b9493f421652d6c42601d7caa96f97dcc1ad                                                                                                                               100%  894    20.1KB/s   00:00    
d70792c17970cd69917926789d713a01f18550                                                                                                                               100%  793    18.1KB/s   00:00    
fb3934cf33b1b8be832b72008ad84257392543                                                                                                                               100%  775    25.7KB/s   00:00    
f3e69fa8da23f465a8ee9507b3b15d82d3242d                                                                                                                               100%  170     4.9KB/s   00:00    
063ad4e37404b6baa7560e422f93d7e7202d65                                                                                                                               100%  567    15.1KB/s   00:00    
91b55154277502dbd7197d01dc993ef43ddb25                                                                                                                               100%   39     1.3KB/s   00:00    
5f33fe81baa0061a22ea41f860dc335928bd1f                                                                                                                               100%  167     7.3KB/s   00:00    
92c047e11f0c24e62c2de50d8a2da4309b3d12                                                                                                                               100%  338     7.2KB/s   00:00    
e1f6ff38cbdf46d3681a539027e093c14513e6                                                                                                                               100%   43     1.8KB/s   00:00    
d131fddb1b2155e16d8b90928173dc5dc633d9                                                                                                                               100%  641    15.5KB/s   00:00    
db4f11da93bdabce19febdb4d28cb751c8fdde                                                                                                                               100%  170     3.3KB/s   00:00    
e5274efe80e84d93dba4071cd627ad881354e4                                                                                                                               100%  687    18.0KB/s   00:00    
3f067ce1466fb3ddb0328665e16805c16bdbe9                                                                                                                               100%  556    11.4KB/s   00:00    
87944111ed9be42ff0385ef06cefc251d26315                                                                                                                               100%  546    14.5KB/s   00:00    
a2f0fbe59da096bcbd550dca9b77cc96c6bfac                                                                                                                               100%  163     3.8KB/s   00:00    
f9c68a7b60785ae5b38a59c4cea4b30c84dba9                                                                                                                               100%   17     0.3KB/s   00:00    
fcfe1de90da22dbead6d52f44858cb0e17bf0b                                                                                                                               100%  166     6.6KB/s   00:00    
b1c25c08908744f1ab7b0379265505a57c964c                                                                                                                               100%   52     1.8KB/s   00:00    
ea2645e6eb412963950dfa113555ac3afd8235                                                                                                                               100%  606    16.6KB/s   00:00    
fac4addecd62ec3debd6e90cff40a669c82be1                                                                                                                               100%  109     2.5KB/s   00:00    
a583e291db2bae94db6fc4c46ee457cb1d88e2                                                                                                                               100%  338     6.5KB/s   00:00    
184552dd2f57b392c12d1fe06e0d47ea5f9017                                                                                                                               100%  168     4.6KB/s   00:00    
1b4eb8f5cd3a90c244c7e538344f5f7f98f741                                                                                                                               100%  171     4.6KB/s   00:00    
9a6a4e2cfb351fa10c03e3a604f8a874f23948                                                                                                                               100%  674    18.9KB/s   00:00    
1bb3ff757b58b7321ad82b96f9b55fa473b280                                                                                                                               100%  309    10.8KB/s   00:00    
1f900ab9226260650b21fe008767c52af83f59                                                                                                                               100%   85     2.3KB/s   00:00    
67cc546e5a2301f65a508338f287d38d71ff9c                                                                                                                               100%  671    18.1KB/s   00:00    
74116a41a9694ab86f21a881ca3d10fda36cd2                                                                                                                               100%  407    12.9KB/s   00:00    
4d6c003dbce782834bba86e13abf7d8dcea4d6                                                                                                                               100%  632    24.7KB/s   00:00    
67415bcb910f4cc7c187e698c028a4f534393d                                                                                                                               100%  631    20.1KB/s   00:00    
4f2744d23d656238daa9da98c4e9d59fc573fb                                                                                                                               100%  597    24.5KB/s   00:00    
f81793e2d3cd9a09eef1ccbd3883f2add96f74                                                                                                                               100%   53     1.2KB/s   00:00    
b7e20edbd99ba9c80edb5871da211ef5607c6c                                                                                                                               100%   72     2.7KB/s   00:00    
d9d29b3a3311d738d1eee88f5326d1cb5f4604                                                                                                                               100%  249     5.4KB/s   00:00    
6d592457223a6c59147afef24bcbe8b12d64f7                                                                                                                               100%  144     3.6KB/s   00:00    
a97f6e0ca20b69ab07faa6dc15995d0f082286                                                                                                                               100%  852    19.9KB/s   00:00    
d2d3275c40e37b0890566d8d061e53723c9f76                                                                                                                               100%  657    27.9KB/s   00:00    
760ea0dfca26a3205592d5539930ba9a426c93                                                                                                                               100%   69     1.9KB/s   00:00    
ba48302752447aeee2e0de801006af407b0d74                                                                                                                               100%  227     6.1KB/s   00:00    
0bcf02495ae662f7542a6f1e0fd9b2d6d54b3e                                                                                                                               100%  337     8.7KB/s   00:00    
56d388a82c86bfdfd21adbde2c8294396bc0b8                                                                                                                               100%  161     3.8KB/s   00:00    
26403df7d65a889fee69565bed1ccc2c2e16c8                                                                                                                               100%  425    15.6KB/s   00:00    
b304d9fda4cbf8d4d69f1edde4691d6a6d6d9e                                                                                                                               100%  327     9.3KB/s   00:00    
9aad32004431cf2fe7713c21c3f9779fb1ea31                                                                                                                               100%  283    10.1KB/s   00:00    
4b854698989156c45c73ba1ba24bc1127ee96e                                                                                                                               100%  254    10.9KB/s   00:00    
3ca5974f8d1b799a76a66f3975ae2bfeba464f                                                                                                                               100%  572    15.2KB/s   00:00    
8b93ba1b869817bcf4525da5d832289c7dda64                                                                                                                               100%   62     1.3KB/s   00:00    
8e45647dfbe284f23598585e924ef7e10455da                                                                                                                               100%  638    16.8KB/s   00:00    
1543eb9acdad58f489e9df9ef6c1606ab54071                                                                                                                               100%   89     1.7KB/s   00:00    
316ae501c35fa4cc04402091b7de613b6e1b4a                                                                                                                               100%  923    37.6KB/s   00:00    
d372ecb5d156a4cdf470e3adfe0ff532619e5b                                                                                                                               100%  173     4.8KB/s   00:00    
196c009966a5e35772c6911a9761c565cb579e                                                                                                                               100%   53     1.0KB/s   00:00    
f4a04f9cea6d2347124923737445cb34f96f8e                                                                                                                               100%  167     3.9KB/s   00:00    
f60d7efad6153858f9469d6bc5038b2f5dc451                                                                                                                               100%   52     1.1KB/s   00:00    
f7c01f974885cdb7d913db1eed6e09760a296c                                                                                                                               100%  679    26.4KB/s   00:00    
876a708711cda8b5c45796718d040fc7497bf5                                                                                                                               100%   63     1.3KB/s   00:00    
1deb0ef26d1ebf4d205c64463e5031c2330e62                                                                                                                               100%  572    17.6KB/s   00:00    
10770bc4886a48f2e0c4d646e2652b0731abcd                                                                                                                               100%  774    21.7KB/s   00:00    
a3eca5f1f2338a2af044b415c3a314d257e64f                                                                                                                               100%  168     4.0KB/s   00:00    
a4f262880c22a33366ec0e5baf43c49464b542                                                                                                                               100%  164     4.6KB/s   00:00    
a55d8b8520dcc03c250a605151cc0d23a45518                                                                                                                               100%  328KB   1.2MB/s   00:00    
2caea5ce51159589169efc8052ccefe6398cf3                                                                                                                               100%  165     3.7KB/s   00:00    
64a27895dfba31aa8e6717ed3337678e282687                                                                                                                               100%  159     3.2KB/s   00:00    
5fc183a83617f77b544cfd38b971a1ac9352ca                                                                                                                               100%  661    15.3KB/s   00:00    
65f84051c36543f7ed4d653ae5210186f8be5a                                                                                                                               100%  162     3.8KB/s   00:00    
58d9868257850f5c3ca721212d8366e0363841                                                                                                                               100%  632    14.1KB/s   00:00    
49512c1a6a161327e6483d06a3006e206b0c90                                                                                                                               100%  178     8.1KB/s   00:00    
7108994d5d87a4fc811fbf5a6351957976711c                                                                                                                               100%   50     1.4KB/s   00:00    
4b2d002badf43c1355b8168bf742ea7d7413c8                                                                                                                               100%  573    20.2KB/s   00:00    
8e942e9666c8f25a77687e34b3d2e747147674                                                                                                                               100%  552    24.1KB/s   00:00    
3074270fb64a732d38e6b21d607cc39ddd65c7                                                                                                                               100%  606    25.1KB/s   00:00    
fac250129c6413ff9942d5cec5f1fdc1b7a580                                                                                                                               100%   62     2.7KB/s   00:00    
53aa2280967ae8fd43fd1fefefe1caec1230ca                                                                                                                               100%  559    14.1KB/s   00:00    
4944f0cc3b01c9ab2ac46954c44a03fad0fa87                                                                                                                               100%  192     6.1KB/s   00:00    
61f384915a65016f66f39f9d95d7cae78f190a                                                                                                                               100%  771    29.8KB/s   00:00    
725535e0fc5326f88735d93981c3a6c2527ce5                                                                                                                               100%  187     6.1KB/s   00:00    
5ddb160379490a87f3a1bc411016519c611c36                                                                                                                               100%  388    14.3KB/s   00:00    
0eacb6528aeb62eec43d3e14586bfdc26c552c                                                                                                                               100%  547    17.6KB/s   00:00    
c11b4b9fe21e5588d1a661d0ec68256ae8af12                                                                                                                               100%   30     1.3KB/s   00:00    
38be43948b0f8d37f8751ce5fbe9a793bdd13e                                                                                                                               100%  339    13.9KB/s   00:00    
a253ea382b8b76c3cf02f3ea855e7db35b8ec2                                                                                                                               100%  573    16.1KB/s   00:00    
9a8f9b4e0b32d447d07de4148366db5b5915e0                                                                                                                               100%  174     7.3KB/s   00:00    
1185c6d8cdbbb1cb874d2b2fdfe7d84d79c8aa                                                                                                                               100%  842    27.6KB/s   00:00    
d07127aed409b3eecf775324ff83798e94359e                                                                                                                               100%   44     1.4KB/s   00:00    
fa577ef5d90e8c6db607874abbe60318feab1a                                                                                                                               100%  229     9.2KB/s   00:00    
79a718b806b9a4d8b99e7221db26f56311aa92                                                                                                                               100%  103     3.7KB/s   00:00    
0a28f3b9a1e58c31bcef4f99fbd946188e8940                                                                                                                               100%  546    23.8KB/s   00:00    
1fcdd0341ee83f611d9b10fe5e65cb7344a78d                                                                                                                               100%   53     2.0KB/s   00:00    
382271f8fa74c1a658ef0c5e5b0639c8e8c112                                                                                                                               100%   45     2.4KB/s   00:00    
b5c9666f731f33d5b3528b1acaef27dad1982c                                                                                                                               100%  859    28.9KB/s   00:00    
0f7e4439e86b815e3f861bb29a3f6a71a83f63                                                                                                                               100%  227     5.2KB/s   00:00    
34cea19350d93f6d14f875b7a42e65c1c3b5cc                                                                                                                               100%  365    15.2KB/s   00:00    
4b0fcba924fab3ff5df14eb5267333632f8fa4                                                                                                                               100%   53     1.2KB/s   00:00    
d648b2da902e729c18d8b844646c8aee18bbfd                                                                                                                               100%  551    12.7KB/s   00:00    
da32caf03f5895c56877ee1cc4c11f528161c1                                                                                                                               100%   56     1.7KB/s   00:00    
b138c72946025813356f5bbf0d1680e0dc6cd4                                                                                                                               100%  573     9.5KB/s   00:00    
01bee410c463f564e4bed848ccfde6836b796e                                                                                                                               100%  377     7.9KB/s   00:00    
d891c38f5c5fc38b32cd138392191e14f8821a                                                                                                                               100%  633    15.9KB/s   00:00    
a780152bada4366d539c882d834273a5b26d33                                                                                                                               100%  215     6.1KB/s   00:00    
b749122d985868e757a98ecbe008ebd370c4b6                                                                                                                               100%   52     2.1KB/s   00:00    
5fe16e3dd37ebe79a36f61f5d0e1a69a653a8a                                                                                                                               100%   39KB 799.4KB/s   00:00    
0bd0570395017b8a63013ffdd4967b43b5c6f0                                                                                                                               100%  545    10.2KB/s   00:00    
470c94ad0affd8834f1810eccba67192fb28f2                                                                                                                               100%  649    20.9KB/s   00:00    
6401752dca340415a71c69c3a140a8b5aed444                                                                                                                               100%   40     1.3KB/s   00:00    
f1a6d1fff2ccf0a497ef4094cb315a6ea83076                                                                                                                               100%  257    11.3KB/s   00:00    
da0a57017850e15abbf99ec66d81432849c3f5                                                                                                                               100%  599    14.7KB/s   00:00    
e828abf75693a894b56fcb0aabdb9aee86230d                                                                                                                               100%   53     2.2KB/s   00:00    
a6a7735e5dbcf68a664cf28bfcf70031a48b70                                                                                                                               100%  142     4.8KB/s   00:00    
cea9218ed0b65a89c3b553dc1c9edb39ed2520                                                                                                                               100%   40     1.1KB/s   00:00    
654c8d59a29b2f56a55f762d56e6751ce2f100                                                                                                                               100%  661    17.3KB/s   00:00    
5ed5df97b510d49c5a040b51cf62859c2f4625                                                                                                                               100%  690    18.9KB/s   00:00    
16acc06b795b791ad97c92fab4e29811c1744a                                                                                                                               100%   51     2.1KB/s   00:00    
1fb7b2ebdf865bdb092f15e463102d8ec51989                                                                                                                               100%  169     4.2KB/s   00:00    
c62298ac805c52e158e949d7d9cbbf84fb9a6d                                                                                                                               100%  562    20.6KB/s   00:00    
fa9b1dbd80a26533374da8cd824a3d2ac9ea33                                                                                                                               100%  980    23.1KB/s   00:00    
d2c78d9315bad3bc40e3322a6f97eb0dbfb105                                                                                                                               100%  815    37.5KB/s   00:00    
62c15a1fa55279739c928dd0ccb04b2b33e0c4                                                                                                                               100%  162     7.0KB/s   00:00    
821892d1ff2fb2ec1437a276b16497beca77bc                                                                                                                               100%  573    14.5KB/s   00:00    
dab40dec77622d03c9036969fef3e33ecab03f                                                                                                                               100%   52     1.8KB/s   00:00    
ba806fb30ec33981c6e6962fa913586ab8c2dc                                                                                                                               100%  864    19.2KB/s   00:00    
b92e1d6669c7cdd7657074033a32a32bc0942f                                                                                                                               100%   30     0.8KB/s   00:00    
ebffae7656a8b34123f1e64c904b040a1e9701                                                                                                                               100%  182     6.5KB/s   00:00    
41299e4512de77a32d7a02bd28e9f9c33cc6ec                                                                                                                               100%  167     6.7KB/s   00:00    
d609b04e98fe9ef3d3304474c49ce8587b1acd                                                                                                                               100%  698    14.4KB/s   00:00    
1c06fe78d79aa2faad7d4fa6e6ce647134d3dc                                                                                                                               100%   53     2.2KB/s   00:00    
2a39a840e351b9dc1e5041653a415f113d06fe                                                                                                                               100%  162     4.9KB/s   00:00    
9b90a3bd2385c7f4344254652e0619a640e693                                                                                                                               100%  183     6.4KB/s   00:00    
5971418c14b1273d10f8f2b0179da42588f446                                                                                                                               100%  338    14.3KB/s   00:00    
179c247fbf8632e75ba76a614191c8ae98c3ce                                                                                                                               100%  634    14.3KB/s   00:00    
b8cb3324205903c82e24c50489af13741be090                                                                                                                               100%   51     1.9KB/s   00:00    
963149acd42865037a8ddf4530a01f99fd2c92                                                                                                                               100%  661    13.4KB/s   00:00    
386b772637b7409e8bddd3666e18f2abe6e94d                                                                                                                               100%  180     3.2KB/s   00:00    
7ade05ed4cb600196769a87d99fe63b9de10c1                                                                                                                               100%  546    12.7KB/s   00:00    
f0cf6e61427757168927bc62b24e772503b783                                                                                                                               100%  548    14.8KB/s   00:00    
fc8a0678cb5d3a62e2d653da65a4fd9c992bb0                                                                                                                               100%  338    14.3KB/s   00:00    
be4c5a6a14a180a727a7f4df3a37eda6dcc653                                                                                                                               100%  572    13.4KB/s   00:00    
21ec5c1f609d3b6c8097d0dce1dca25ecae85f                                                                                                                               100%   74     2.7KB/s   00:00    
acd1a34fe89e33384acff29f16f403442fe58b                                                                                                                               100%   46     1.0KB/s   00:00    
e201149e9c7232e8fe275d668ca3dbbd30fa45                                                                                                                               100%   43     1.7KB/s   00:00    
23e1d7eb4f1d20715b65b909773912a5fd458d                                                                                                                               100%  808    25.0KB/s   00:00    
8b5c3a08bd40b5e93333320c046029516a9650                                                                                                                               100%  790    17.9KB/s   00:00    
b4ab30cefd4cd1064ee1a93e9d17bc328905ab                                                                                                                               100%  928    21.9KB/s   00:00    
e3300373d6d517188508ee7194024c0c46bacb                                                                                                                               100%  832    26.8KB/s   00:00    
6941acefe2b27cfaa607dc25b092ec558b4d28                                                                                                                               100%  606    18.2KB/s   00:00    
dbe3b99a9d10fcd0c1475d801c81c9ce765b85                                                                                                                               100%  170     7.3KB/s   00:00    
9c266b0fe225cc236ca0941fc0ccb825a97bf0                                                                                                                               100%   56     1.2KB/s   00:00    
8dc7e4bb634c72fc071a09fb98903e8e5f105f                                                                                                                               100%   52     1.5KB/s   00:00    
26aaa23cb219437a405da1066994f0a7d06577                                                                                                                               100%  563    12.5KB/s   00:00    
1841d0a40cba88cb9cfba33baa547c15e3aa94                                                                                                                               100%  651    17.7KB/s   00:00    
6240cc67299ab76b58551eacab06ed30ba2cc5                                                                                                                               100%  175     4.5KB/s   00:00    
73f7eb791e63eacfb5effe93b7e368fad6a448                                                                                                                               100%   47     1.2KB/s   00:00    
9772a47a4483ebdb2e0f57a4113d8003669003                                                                                                                               100%  365    11.8KB/s   00:00    
bc7cab722fff4314af8d205787258052a38a17                                                                                                                               100%  181     4.8KB/s   00:00    
pack-c219e088539a204519cd1224b13f408ceda05633.idx                                                                                                                    100% 1380    45.2KB/s   00:00    
pack-c219e088539a204519cd1224b13f408ceda05633.pack                                                                                                                   100% 3236    51.1KB/s   00:00    
ORIG_HEAD                                                                                                                                                            100%   41     1.0KB/s   00:00    
packed-refs                                                                                                                                                          100%  112     2.8KB/s   00:00    
main                                                                                                                                                                 100%   41     1.0KB/s   00:00    
HEAD                                                                                                                                                                 100%   30     0.8KB/s   00:00    
main                                                                                                                                                                 100%   41     1.1KB/s   00:00    
main                                                                                                                                                                 100%   41     1.3KB/s   00:00     
main.yml                                                                                                                                                             100% 1361    28.2KB/s   00:00     
.gitignore                                                                                                                                                           100%  294     7.9KB/s   00:00     
launch.json                                                                                                                                                          100%  702    17.2KB/s   00:00     
invalidLink.md                                                                                                                                                       100%   34     1.4KB/s   00:00     
hamcrest-core-1.3.jar                                                                                                                                                100%   44KB 718.9KB/s   00:00     
junit-4.13.2.jar                                                                                                                                                     100%  376KB   1.3MB/s   00:00     
Makefile                                                                                                                                                             100%  361     7.7KB/s   00:00     
MarkdownParse.class                                                                                                                                                  100% 1953    75.2KB/s   00:00     
MarkdownParse.java                                                                                                                                                   100% 2399    48.4KB/s   00:00     
MarkdownParseTest.class                                                                                                                                              100% 3967    98.6KB/s   00:00     
MarkdownParseTest.java                                                                                                                                               100% 5854   131.7KB/s   00:00     
mdparse                                                                                                                                                              100%   76     1.5KB/s   00:00     
nolink.md                                                                                                                                                            100%   27     1.0KB/s   00:00     
README.md                                                                                                                                                            100%   17     0.6KB/s   00:00     
test-file.md                                                                                                                                                         100%   67     1.7KB/s   00:00     
test-file2.md                                                                                                                                                        100%  115     0.3KB/s   00:00     
test-file3.md                                                                                                                                                        100%   27     0.6KB/s   00:00     
test-file4.md                                                                                                                                                        100%   27     0.7KB/s   00:00     
test-file5.md                                                                                                                                                        100%   39     1.0KB/s   00:00     
test-file6.md                                                                                                                                                        100%   27     0.8KB/s   00:00     
test-file7.md                                                                                                                                                        100%    2     0.1KB/s   00:00     
test-file8.md                                                                                                                                                        100%   29     1.2KB/s   00:00     
test-file9.md                                                                                                                                                        100%  195     4.8KB/s   00:00     
test2.md                                                                                                                                                             100%   52     1.8KB/s   00:00     
test3.md                                                                                                                                                             100%   56     2.1KB/s   00:00     
test4.md                                                                                                                                                             100%   24     0.5KB/s   00:00 
```

## Compiling and running tests for markdown-parse
```
jason@JasonPC:/mnt/c/Users/jason/Documents/markdown-parser$ ssh ieng6
Last login: Sat May  7 23:14:28 2022 from cpe-70-95-165-156.san.res.rr.com
quota: No filesystem specified.
Hello cs15lsp22ajb, you are currently logged into ieng6-203.ucsd.edu

You are using 0% CPU on this system

Cluster Status 
Hostname     Time    #Users  Load  Averages  
ieng6-201   23:20:01   16  15.10,  15.48,  14.12
ieng6-202   23:20:01   18  19.79,  20.32,  19.96
ieng6-203   23:20:01   8   20.38,  21.10,  21.35

 
Sat May 07, 2022 11:24pm - Prepping cs15lsp22
[cs15lsp22ajb@ieng6-203]:~:304$ cd markdown-parse/
[cs15lsp22ajb@ieng6-203]:markdown-parse:305$ ls
Makefile             MarkdownParse.java       MarkdownParseTest.java  invalidLink.md  mdparse    test-file.md   test-file3.md  test-file5.md  test-file7.md  test-file9.md  test3.md
MarkdownParse.class  MarkdownParseTest.class  README.md               lib             nolink.md  test-file2.md  test-file4.md  test-file6.md  test-file8.md  test2.md       test4.md
[cs15lsp22ajb@ieng6-203]:markdown-parse:306$ make test
javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java
java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest
JUnit version 4.13.2
............links:0
..
Time: 0.11

OK (14 tests)

[cs15lsp22ajb@ieng6-203]:markdown-parse:307$ 
```


## Copying entire directory and running tests in one line
```
. ieng6:~/markjason@JasonPC:/mnt/c/Users/jason/Documents/markdown-parser$ scp -r . ieng6:~/markdown-parse; ssh ieng6 "cd markdown-parse; /software/CSE/oracle-java-17/jdk-17.0.1/bin/javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java; /software/CSE/oracle-java-17/jdk-17.0.1/bin/java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest"
COMMIT_EDITMSG                                                                                                                                                       100%   15     0.4KB/s   00:00    
config                                                                                                                                                               100%  461    16.5KB/s   00:00    
description                                                                                                                                                          100%   73     2.4KB/s   00:00    
FETCH_HEAD                                                                                                                                                           100%  121     2.8KB/s   00:00    
HEAD                                                                                                                                                                 100%   21     0.7KB/s   00:00    
applypatch-msg.sample                                                                                                                                                100%  478    14.5KB/s   00:00    
commit-msg.sample                                                                                                                                                    100%  896    23.6KB/s   00:00    
fsmonitor-watchman.sample                                                                                                                                            100% 4655   147.9KB/s   00:00    
post-update.sample                                                                                                                                                   100%  189     5.6KB/s   00:00    
pre-applypatch.sample                                                                                                                                                100%  424     9.8KB/s   00:00    
pre-commit.sample                                                                                                                                                    100% 1643    43.1KB/s   00:00    
pre-merge-commit.sample                                                                                                                                              100%  416    11.8KB/s   00:00    
pre-push.sample                                                                                                                                                      100% 1374    38.9KB/s   00:00    
pre-rebase.sample                                                                                                                                                    100% 4898   119.9KB/s   00:00    
pre-receive.sample                                                                                                                                                   100%  544    14.6KB/s   00:00    
prepare-commit-msg.sample                                                                                                                                            100% 1492    50.9KB/s   00:00    
push-to-checkout.sample                                                                                                                                              100% 2783    72.6KB/s   00:00    
update.sample                                                                                                                                                        100% 3650    79.7KB/s   00:00    
index                                                                                                                                                                100% 2112    47.5KB/s   00:00    
exclude                                                                                                                                                              100%  240     7.1KB/s   00:00    
HEAD                                                                                                                                                                 100% 6782   208.4KB/s   00:00    
main                                                                                                                                                                 100% 6782   138.4KB/s   00:00    
HEAD                                                                                                                                                                 100%  199     4.8KB/s   00:00    
main                                                                                                                                                                 100% 4774   157.8KB/s   00:00    
main                                                                                                                                                                 100%  549    14.9KB/s   00:00    
799e1b3b9fa1f2fbc86af878686e58523873b8                                                                                                                               100%  174     4.9KB/s   00:00    
1b99a6db3649ce42fa1b9c11cbb496eed45d48                                                                                                                               100%   43     1.0KB/s   00:00    
d95aa8f8b17bb7433c807c59aaa2417e541de1                                                                                                                               100%   55     1.5KB/s   00:00    
6335a1ae1b43d45ec9de511ec5d90beac9dac9                                                                                                                               100%  168     0.5KB/s   00:00    
3728b578c2373f1fd981c8d15b4529afaeb7c7                                                                                                                               100%   43     1.3KB/s   00:00    
771799ebab3ebc70c76d210f4049db77316ef9                                                                                                                               100%  165     4.6KB/s   00:00    
8858eb92356526619f56f4678bc6a7e069268e                                                                                                                               100%  546    14.9KB/s   00:00    
40b9493f421652d6c42601d7caa96f97dcc1ad                                                                                                                               100%  894    20.0KB/s   00:00    
d70792c17970cd69917926789d713a01f18550                                                                                                                               100%  793    35.2KB/s   00:00    
fb3934cf33b1b8be832b72008ad84257392543                                                                                                                               100%  775    22.0KB/s   00:00    
f3e69fa8da23f465a8ee9507b3b15d82d3242d                                                                                                                               100%  170     7.5KB/s   00:00    
063ad4e37404b6baa7560e422f93d7e7202d65                                                                                                                               100%  567    14.8KB/s   00:00    
91b55154277502dbd7197d01dc993ef43ddb25                                                                                                                               100%   39     0.9KB/s   00:00    
5f33fe81baa0061a22ea41f860dc335928bd1f                                                                                                                               100%  167     4.7KB/s   00:00    
92c047e11f0c24e62c2de50d8a2da4309b3d12                                                                                                                               100%  338     7.9KB/s   00:00    
e1f6ff38cbdf46d3681a539027e093c14513e6                                                                                                                               100%   43     1.3KB/s   00:00    
d131fddb1b2155e16d8b90928173dc5dc633d9                                                                                                                               100%  641    27.9KB/s   00:00    
db4f11da93bdabce19febdb4d28cb751c8fdde                                                                                                                               100%  170     4.2KB/s   00:00    
e5274efe80e84d93dba4071cd627ad881354e4                                                                                                                               100%  687    13.0KB/s   00:00    
3f067ce1466fb3ddb0328665e16805c16bdbe9                                                                                                                               100%  556    11.6KB/s   00:00    
87944111ed9be42ff0385ef06cefc251d26315                                                                                                                               100%  546    11.5KB/s   00:00    
a2f0fbe59da096bcbd550dca9b77cc96c6bfac                                                                                                                               100%  163     4.2KB/s   00:00    
f9c68a7b60785ae5b38a59c4cea4b30c84dba9                                                                                                                               100%   17     0.6KB/s   00:00    
fcfe1de90da22dbead6d52f44858cb0e17bf0b                                                                                                                               100%  166     6.9KB/s   00:00    
b1c25c08908744f1ab7b0379265505a57c964c                                                                                                                               100%   52     2.2KB/s   00:00    
ea2645e6eb412963950dfa113555ac3afd8235                                                                                                                               100%  606    11.8KB/s   00:00    
fac4addecd62ec3debd6e90cff40a669c82be1                                                                                                                               100%  109     2.3KB/s   00:00    
a583e291db2bae94db6fc4c46ee457cb1d88e2                                                                                                                               100%  338    15.3KB/s   00:00    
184552dd2f57b392c12d1fe06e0d47ea5f9017                                                                                                                               100%  168     6.9KB/s   00:00    
1b4eb8f5cd3a90c244c7e538344f5f7f98f741                                                                                                                               100%  171     4.6KB/s   00:00    
9a6a4e2cfb351fa10c03e3a604f8a874f23948                                                                                                                               100%  674    24.3KB/s   00:00    
1bb3ff757b58b7321ad82b96f9b55fa473b280                                                                                                                               100%  309     6.5KB/s   00:00    
1f900ab9226260650b21fe008767c52af83f59                                                                                                                               100%   85     1.8KB/s   00:00    
67cc546e5a2301f65a508338f287d38d71ff9c                                                                                                                               100%  671    15.7KB/s   00:00    
74116a41a9694ab86f21a881ca3d10fda36cd2                                                                                                                               100%  407     9.3KB/s   00:00    
4d6c003dbce782834bba86e13abf7d8dcea4d6                                                                                                                               100%  632    16.3KB/s   00:00    
67415bcb910f4cc7c187e698c028a4f534393d                                                                                                                               100%  631    12.1KB/s   00:00    
4f2744d23d656238daa9da98c4e9d59fc573fb                                                                                                                               100%  597    12.1KB/s   00:00    
f81793e2d3cd9a09eef1ccbd3883f2add96f74                                                                                                                               100%   53     1.3KB/s   00:00    
b7e20edbd99ba9c80edb5871da211ef5607c6c                                                                                                                               100%   72     1.5KB/s   00:00    
d9d29b3a3311d738d1eee88f5326d1cb5f4604                                                                                                                               100%  249     5.8KB/s   00:00    
6d592457223a6c59147afef24bcbe8b12d64f7                                                                                                                               100%  144     2.9KB/s   00:00    
a97f6e0ca20b69ab07faa6dc15995d0f082286                                                                                                                               100%  852    20.8KB/s   00:00    
d2d3275c40e37b0890566d8d061e53723c9f76                                                                                                                               100%  657    14.1KB/s   00:00    
760ea0dfca26a3205592d5539930ba9a426c93                                                                                                                               100%   69     1.0KB/s   00:00    
ba48302752447aeee2e0de801006af407b0d74                                                                                                                               100%  227     4.9KB/s   00:00    
0bcf02495ae662f7542a6f1e0fd9b2d6d54b3e                                                                                                                               100%  337     6.9KB/s   00:00    
56d388a82c86bfdfd21adbde2c8294396bc0b8                                                                                                                               100%  161     3.1KB/s   00:00    
26403df7d65a889fee69565bed1ccc2c2e16c8                                                                                                                               100%  425     9.5KB/s   00:00    
b304d9fda4cbf8d4d69f1edde4691d6a6d6d9e                                                                                                                               100%  327     7.7KB/s   00:00    
9aad32004431cf2fe7713c21c3f9779fb1ea31                                                                                                                               100%  283     6.8KB/s   00:00    
4b854698989156c45c73ba1ba24bc1127ee96e                                                                                                                               100%  254     4.1KB/s   00:00    
3ca5974f8d1b799a76a66f3975ae2bfeba464f                                                                                                                               100%  572    12.4KB/s   00:00    
8b93ba1b869817bcf4525da5d832289c7dda64                                                                                                                               100%   62     1.5KB/s   00:00    
8e45647dfbe284f23598585e924ef7e10455da                                                                                                                               100%  638    15.4KB/s   00:00    
1543eb9acdad58f489e9df9ef6c1606ab54071                                                                                                                               100%   89     1.8KB/s   00:00    
316ae501c35fa4cc04402091b7de613b6e1b4a                                                                                                                               100%  923    19.4KB/s   00:00    
d372ecb5d156a4cdf470e3adfe0ff532619e5b                                                                                                                               100%  173     4.4KB/s   00:00    
196c009966a5e35772c6911a9761c565cb579e                                                                                                                               100%   53     1.7KB/s   00:00    
f4a04f9cea6d2347124923737445cb34f96f8e                                                                                                                               100%  167     3.3KB/s   00:00    
f60d7efad6153858f9469d6bc5038b2f5dc451                                                                                                                               100%   52     1.4KB/s   00:00    
f7c01f974885cdb7d913db1eed6e09760a296c                                                                                                                               100%  679    16.6KB/s   00:00    
876a708711cda8b5c45796718d040fc7497bf5                                                                                                                               100%   63     1.2KB/s   00:00    
1deb0ef26d1ebf4d205c64463e5031c2330e62                                                                                                                               100%  572    11.9KB/s   00:00    
10770bc4886a48f2e0c4d646e2652b0731abcd                                                                                                                               100%  774    16.3KB/s   00:00    
a3eca5f1f2338a2af044b415c3a314d257e64f                                                                                                                               100%  168     3.6KB/s   00:00    
a4f262880c22a33366ec0e5baf43c49464b542                                                                                                                               100%  164     3.2KB/s   00:00    
a55d8b8520dcc03c250a605151cc0d23a45518                                                                                                                               100%  328KB 606.2KB/s   00:00    
2caea5ce51159589169efc8052ccefe6398cf3                                                                                                                               100%  165     4.2KB/s   00:00    
64a27895dfba31aa8e6717ed3337678e282687                                                                                                                               100%  159     2.8KB/s   00:00    
5fc183a83617f77b544cfd38b971a1ac9352ca                                                                                                                               100%  661    15.9KB/s   00:00    
65f84051c36543f7ed4d653ae5210186f8be5a                                                                                                                               100%  162     3.5KB/s   00:00    
58d9868257850f5c3ca721212d8366e0363841                                                                                                                               100%  632    17.1KB/s   00:00    
49512c1a6a161327e6483d06a3006e206b0c90                                                                                                                               100%  178     4.5KB/s   00:00    
7108994d5d87a4fc811fbf5a6351957976711c                                                                                                                               100%   50     1.3KB/s   00:00    
4b2d002badf43c1355b8168bf742ea7d7413c8                                                                                                                               100%  573    13.6KB/s   00:00    
8e942e9666c8f25a77687e34b3d2e747147674                                                                                                                               100%  552    12.3KB/s   00:00    
3074270fb64a732d38e6b21d607cc39ddd65c7                                                                                                                               100%  606    16.5KB/s   00:00    
fac250129c6413ff9942d5cec5f1fdc1b7a580                                                                                                                               100%   62     1.4KB/s   00:00    
53aa2280967ae8fd43fd1fefefe1caec1230ca                                                                                                                               100%  559    13.8KB/s   00:00    
4944f0cc3b01c9ab2ac46954c44a03fad0fa87                                                                                                                               100%  192     4.1KB/s   00:00    
61f384915a65016f66f39f9d95d7cae78f190a                                                                                                                               100%  771    19.9KB/s   00:00    
725535e0fc5326f88735d93981c3a6c2527ce5                                                                                                                               100%  187     4.2KB/s   00:00    
5ddb160379490a87f3a1bc411016519c611c36                                                                                                                               100%  388     9.3KB/s   00:00    
0eacb6528aeb62eec43d3e14586bfdc26c552c                                                                                                                               100%  547    15.4KB/s   00:00    
c11b4b9fe21e5588d1a661d0ec68256ae8af12                                                                                                                               100%   30     0.9KB/s   00:00    
38be43948b0f8d37f8751ce5fbe9a793bdd13e                                                                                                                               100%  339     9.1KB/s   00:00    
a253ea382b8b76c3cf02f3ea855e7db35b8ec2                                                                                                                               100%  573    11.8KB/s   00:00    
9a8f9b4e0b32d447d07de4148366db5b5915e0                                                                                                                               100%  174     5.1KB/s   00:00    
1185c6d8cdbbb1cb874d2b2fdfe7d84d79c8aa                                                                                                                               100%  842    19.4KB/s   00:00    
d07127aed409b3eecf775324ff83798e94359e                                                                                                                               100%   44     0.9KB/s   00:00    
fa577ef5d90e8c6db607874abbe60318feab1a                                                                                                                               100%  229     7.5KB/s   00:00    
79a718b806b9a4d8b99e7221db26f56311aa92                                                                                                                               100%  103     2.6KB/s   00:00    
0a28f3b9a1e58c31bcef4f99fbd946188e8940                                                                                                                               100%  546    15.7KB/s   00:00    
1fcdd0341ee83f611d9b10fe5e65cb7344a78d                                                                                                                               100%   53     1.4KB/s   00:00    
382271f8fa74c1a658ef0c5e5b0639c8e8c112                                                                                                                               100%   45     1.1KB/s   00:00    
b5c9666f731f33d5b3528b1acaef27dad1982c                                                                                                                               100%  859    23.8KB/s   00:00    
0f7e4439e86b815e3f861bb29a3f6a71a83f63                                                                                                                               100%  227     5.1KB/s   00:00    
34cea19350d93f6d14f875b7a42e65c1c3b5cc                                                                                                                               100%  365     8.5KB/s   00:00    
4b0fcba924fab3ff5df14eb5267333632f8fa4                                                                                                                               100%   53     1.8KB/s   00:00    
d648b2da902e729c18d8b844646c8aee18bbfd                                                                                                                               100%  551    13.4KB/s   00:00    
da32caf03f5895c56877ee1cc4c11f528161c1                                                                                                                               100%   56     2.1KB/s   00:00    
b138c72946025813356f5bbf0d1680e0dc6cd4                                                                                                                               100%  573    23.6KB/s   00:00    
01bee410c463f564e4bed848ccfde6836b796e                                                                                                                               100%  377    10.1KB/s   00:00    
d891c38f5c5fc38b32cd138392191e14f8821a                                                                                                                               100%  633    27.7KB/s   00:00    
a780152bada4366d539c882d834273a5b26d33                                                                                                                               100%  215     6.8KB/s   00:00    
b749122d985868e757a98ecbe008ebd370c4b6                                                                                                                               100%   52     2.1KB/s   00:00    
5fe16e3dd37ebe79a36f61f5d0e1a69a653a8a                                                                                                                               100%   39KB 778.0KB/s   00:00    
0bd0570395017b8a63013ffdd4967b43b5c6f0                                                                                                                               100%  545    23.0KB/s   00:00    
470c94ad0affd8834f1810eccba67192fb28f2                                                                                                                               100%  649    28.2KB/s   00:00    
6401752dca340415a71c69c3a140a8b5aed444                                                                                                                               100%   40     1.1KB/s   00:00    
f1a6d1fff2ccf0a497ef4094cb315a6ea83076                                                                                                                               100%  257    10.5KB/s   00:00    
da0a57017850e15abbf99ec66d81432849c3f5                                                                                                                               100%  599    23.2KB/s   00:00    
e828abf75693a894b56fcb0aabdb9aee86230d                                                                                                                               100%   53     1.4KB/s   00:00    
a6a7735e5dbcf68a664cf28bfcf70031a48b70                                                                                                                               100%  142     4.4KB/s   00:00    
cea9218ed0b65a89c3b553dc1c9edb39ed2520                                                                                                                               100%   40     1.7KB/s   00:00    
654c8d59a29b2f56a55f762d56e6751ce2f100                                                                                                                               100%  661    28.3KB/s   00:00    
5ed5df97b510d49c5a040b51cf62859c2f4625                                                                                                                               100%  690    30.2KB/s   00:00    
16acc06b795b791ad97c92fab4e29811c1744a                                                                                                                               100%   51     1.8KB/s   00:00    
1fb7b2ebdf865bdb092f15e463102d8ec51989                                                                                                                               100%  169     5.4KB/s   00:00    
c62298ac805c52e158e949d7d9cbbf84fb9a6d                                                                                                                               100%  562    11.1KB/s   00:00    
fa9b1dbd80a26533374da8cd824a3d2ac9ea33                                                                                                                               100%  980    39.7KB/s   00:00    
d2c78d9315bad3bc40e3322a6f97eb0dbfb105                                                                                                                               100%  815    29.1KB/s   00:00    
62c15a1fa55279739c928dd0ccb04b2b33e0c4                                                                                                                               100%  162     5.2KB/s   00:00    
821892d1ff2fb2ec1437a276b16497beca77bc                                                                                                                               100%  573    22.7KB/s   00:00    
dab40dec77622d03c9036969fef3e33ecab03f                                                                                                                               100%   52     2.2KB/s   00:00    
ba806fb30ec33981c6e6962fa913586ab8c2dc                                                                                                                               100%  864    19.5KB/s   00:00    
b92e1d6669c7cdd7657074033a32a32bc0942f                                                                                                                               100%   30     0.9KB/s   00:00    
ebffae7656a8b34123f1e64c904b040a1e9701                                                                                                                               100%  182     4.8KB/s   00:00    
41299e4512de77a32d7a02bd28e9f9c33cc6ec                                                                                                                               100%  167     4.7KB/s   00:00    
d609b04e98fe9ef3d3304474c49ce8587b1acd                                                                                                                               100%  698    23.2KB/s   00:00    
1c06fe78d79aa2faad7d4fa6e6ce647134d3dc                                                                                                                               100%   53     1.8KB/s   00:00    
2a39a840e351b9dc1e5041653a415f113d06fe                                                                                                                               100%  162     5.0KB/s   00:00    
9b90a3bd2385c7f4344254652e0619a640e693                                                                                                                               100%  183     8.6KB/s   00:00    
5971418c14b1273d10f8f2b0179da42588f446                                                                                                                               100%  338     6.8KB/s   00:00    
179c247fbf8632e75ba76a614191c8ae98c3ce                                                                                                                               100%  634    12.4KB/s   00:00    
b8cb3324205903c82e24c50489af13741be090                                                                                                                               100%   51     1.0KB/s   00:00    
963149acd42865037a8ddf4530a01f99fd2c92                                                                                                                               100%  661    19.4KB/s   00:00    
386b772637b7409e8bddd3666e18f2abe6e94d                                                                                                                               100%  180     3.5KB/s   00:00    
7ade05ed4cb600196769a87d99fe63b9de10c1                                                                                                                               100%  546    22.4KB/s   00:00    
f0cf6e61427757168927bc62b24e772503b783                                                                                                                               100%  548    14.2KB/s   00:00    
fc8a0678cb5d3a62e2d653da65a4fd9c992bb0                                                                                                                               100%  338     6.9KB/s   00:00    
be4c5a6a14a180a727a7f4df3a37eda6dcc653                                                                                                                               100%  572    16.4KB/s   00:00    
21ec5c1f609d3b6c8097d0dce1dca25ecae85f                                                                                                                               100%   74     2.3KB/s   00:00    
acd1a34fe89e33384acff29f16f403442fe58b                                                                                                                               100%   46     1.0KB/s   00:00    
e201149e9c7232e8fe275d668ca3dbbd30fa45                                                                                                                               100%   43     0.9KB/s   00:00    
23e1d7eb4f1d20715b65b909773912a5fd458d                                                                                                                               100%  808    22.7KB/s   00:00    
8b5c3a08bd40b5e93333320c046029516a9650                                                                                                                               100%  790    29.2KB/s   00:00    
b4ab30cefd4cd1064ee1a93e9d17bc328905ab                                                                                                                               100%  928    26.0KB/s   00:00    
e3300373d6d517188508ee7194024c0c46bacb                                                                                                                               100%  832    18.8KB/s   00:00    
6941acefe2b27cfaa607dc25b092ec558b4d28                                                                                                                               100%  606    10.5KB/s   00:00    
dbe3b99a9d10fcd0c1475d801c81c9ce765b85                                                                                                                               100%  170     3.5KB/s   00:00    
9c266b0fe225cc236ca0941fc0ccb825a97bf0                                                                                                                               100%   56     2.3KB/s   00:00    
8dc7e4bb634c72fc071a09fb98903e8e5f105f                                                                                                                               100%   52     1.4KB/s   00:00    
26aaa23cb219437a405da1066994f0a7d06577                                                                                                                               100%  563     8.5KB/s   00:00    
1841d0a40cba88cb9cfba33baa547c15e3aa94                                                                                                                               100%  651    27.6KB/s   00:00    
6240cc67299ab76b58551eacab06ed30ba2cc5                                                                                                                               100%  175     7.1KB/s   00:00    
73f7eb791e63eacfb5effe93b7e368fad6a448                                                                                                                               100%   47     1.4KB/s   00:00    
9772a47a4483ebdb2e0f57a4113d8003669003                                                                                                                               100%  365    15.8KB/s   00:00    
bc7cab722fff4314af8d205787258052a38a17                                                                                                                               100%  181     9.5KB/s   00:00    
pack-c219e088539a204519cd1224b13f408ceda05633.idx                                                                                                                    100% 1380    30.2KB/s   00:00    
pack-c219e088539a204519cd1224b13f408ceda05633.pack                                                                                                                   100% 3236   127.0KB/s   00:00    
ORIG_HEAD                                                                                                                                                            100%   41     1.4KB/s   00:00    
packed-refs                                                                                                                                                          100%  112     3.4KB/s   00:00    
main                                                                                                                                                                 100%   41     1.5KB/s   00:00    
HEAD                                                                                                                                                                 100%   30     0.7KB/s   00:00    
main                                                                                                                                                                 100%   41     1.7KB/s   00:00    
main                                                                                                                                                                 100%   41     1.3KB/s   00:00    
main.yml                                                                                                                                                             100% 1361    42.5KB/s   00:00    
.gitignore                                                                                                                                                           100%  294     9.4KB/s   00:00    
launch.json                                                                                                                                                          100%  702    29.7KB/s   00:00    
invalidLink.md                                                                                                                                                       100%   34     1.2KB/s   00:00    
hamcrest-core-1.3.jar                                                                                                                                                100%   44KB 660.3KB/s   00:00    
junit-4.13.2.jar                                                                                                                                                     100%  376KB   1.2MB/s   00:00    
Makefile                                                                                                                                                             100%  361     9.3KB/s   00:00    
MarkdownParse.class                                                                                                                                                  100% 1953    54.9KB/s   00:00    
MarkdownParse.java                                                                                                                                                   100% 2399    93.0KB/s   00:00    
MarkdownParseTest.class                                                                                                                                              100% 3967   135.9KB/s   00:00    
MarkdownParseTest.java                                                                                                                                               100% 5854   154.2KB/s   00:00    
mdparse                                                                                                                                                              100%   76     1.9KB/s   00:00    
nolink.md                                                                                                                                                            100%   27     1.0KB/s   00:00    
README.md                                                                                                                                                            100%   17     0.4KB/s   00:00    
test-file.md                                                                                                                                                         100%   67     2.4KB/s   00:00    
test-file2.md                                                                                                                                                        100%  115     3.7KB/s   00:00    
test-file3.md                                                                                                                                                        100%   27     0.9KB/s   00:00    
test-file4.md                                                                                                                                                        100%   27     0.8KB/s   00:00    
test-file5.md                                                                                                                                                        100%   39     1.6KB/s   00:00    
test-file6.md                                                                                                                                                        100%   27     1.1KB/s   00:00    
test-file7.md                                                                                                                                                        100%    2     0.1KB/s   00:00    
test-file8.md                                                                                                                                                        100%   29     0.9KB/s   00:00    
test-file9.md                                                                                                                                                        100%  195     8.4KB/s   00:00    
test2.md                                                                                                                                                             100%   52     2.3KB/s   00:00    
test3.md                                                                                                                                                             100%   56     2.0KB/s   00:00    
test4.md                                                                                                                                                             100%   24     1.0KB/s   00:00    
JUnit version 4.13.2
............links:0
..
Time: 0.188

OK (14 tests)

jason@JasonPC:/mnt/c/Users/jason/Documents/markdown-parser$ 
``` 