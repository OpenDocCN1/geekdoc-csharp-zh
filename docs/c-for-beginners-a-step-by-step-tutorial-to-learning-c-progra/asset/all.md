C# for beginners

A step-by-step tutorial to learning c# programming from scratch

Lena neill

©  copyright  2023  –  ryan  roffe

All  rights  reserved.

The  content  contained  within  this  ook  may  not  e  reproduced,  duplicated  or  transmitted  without  direct  written  permission  from  the  author  or  the  pulisher.

Under  no  circumstances  will  any  lame  or  legal  responsiility  e  held  against  the  pulisher,  or  author,  for  any  damages,  reparation,  or  monetary  loss  due  to  the  information  contained  within  this  ook.  Either  directly  or  indirectly.

Legal  notice:

This  ook  is  copyright  protected.  This  ook  is  only  for  personal  use.  You  cannot  amend,  distriute,  sell,  use,  quote  or  paraphrase  any  part,  or  the  content  within  this  ook,  without  the  consent  of  the  author  or  pulisher.

Disclaimer  notice:

Please  note  the  information  contained  within  this  document  is  for  educational  and  entertainment  purposes  only.  All  effort  has  een  executed  to  present  accurate,  up  to  date,  and  reliale,  complete  information.  No  warranties  of  any  kind  are  declared  or  implied.  Readers  acknowledge  that  the  author  is  not  engaging  in  the  rendering  of  legal,  financial,  medical  or  professional  advice.  The  content  within  this  ook  has  een  derived  from  various  sources.  Please  consult  a  licensed  professional  efore  attempting  any  techniques  outlined  in  this  ook.

Y  reading  this  document,  the  reader  agrees  that  under  no  circumstances  is  the  author  responsile  for  any  losses,  direct  or  indirect,  which  are  incurred  as  a  result  of  the  use  of  information  contained  within  this  document,  including,  ut  not  limited  to,  —  errors,  omissions,  or  inaccuracies.

Tale of contents

[Introduction](#index_split_003.html_id_Toc157346257)

[Chapter 1: what is c#](#index_split_004.html_id_Toc157346258)

[Chapter 2: detailed overview](#index_split_005.html_id_Toc157346259)

[Chapter 3: demystifying data types](#index_split_006.html_id_Toc157346260)

[Chapter 4: working with variales](#index_split_007.html_id_Toc157346261)

[Chapter 5: what is type conversion?](#index_split_008.html_id_Toc157346262)

[Chapter 6: the need for operators](#index_split_009.html_id_Toc157346263)

[Chapter 7: the conditional statements](#index_split_010.html_id_Toc157346264)

[Chapter 8: loops](#index_split_011.html_id_Toc157346265)

[Chapter 9: c# methods](#index_split_012.html_id_Toc157346266)

[Chapter 10: the array world^(123)](#index_split_013.html_id_Toc157346267)

[Chapter 11: classes^(126)](#index_split_014.html_id_Top_of_index_split_065_html)

[Chapter 12: structure](#index_split_015.html_id_Toc157346269)

[Chapter 13: encapsulation](#index_split_016.html_id_Toc157346270)

[Chapter 14: inheritance](#index_split_017.html_id_Toc157346271)

[Chapter 15: polymorphism](#index_split_018.html_id_Toc157346272)

[Chapter 16: regular expressions^(134)](#index_split_019.html_id_Top_of_index_split_070_html)

[Chapter 17: the process of handling exceptions^(135)](#index_split_020.html_id_Chapter_17__The_Process_of_Handl)

[Chapter 18: file i/o^(136)](#index_split_021.html_id_Chapter_18__File_I_O136)

[Chapter 19: delegates](#index_split_022.html_id_Toc157346276)

[Chapter 20: multithreading in c#](#index_split_023.html_id_Toc157346277)

[Chapter 21: event](#index_split_025.html_id_Toc157346278)

[Chapter 22: hints and important resources](#index_split_026.html_id_Toc157346279)

[Conclusion](#index_split_027.html_id_Toc157346280)

[Iliography](#index_split_028.html_id_Toc157346281)

## Introduction

Altho,ugh  there  is  no,thing  easy  ao,ut  learning  a  new  language  o,f  any  so,rt,  the  aim  o,f  this  o,o,k  is  to,  allo,w  yo,u  to,  pick  up  and  understand  as  quickly  and  easily  as  po,ssile.  The  go,al  o,f  this  is  to,  pro,vide  yo,u  with  co,mplete  and  co,mprehensive  skills  that  are  ale  to,  help  yo,u  retain  impo,rtant  kno,wledge  and  guide  yo,ur  pro,gramming  and  co,ding  experience  in  c#.  In  o,rder  fo,r  yo,u  to,  learn  in  the  mo,st  efficient  manner,  i  ho,pe  that  yo,u  will  also,  do,  the  practice  that  will  reinfo,rce  the  lesso,ns  we  explo,re  in  this  o,o,k.

The  o,o,k  will  co,ver  a  asic  descriptio,n  o,f  what  c#  is,  and  finally  give  yo,u  so,me  helpful  hints  and  reso,urces  to,  reinfo,rce  any  sujects  o,r  skills  where  yo,u  may  need  a  little  mo,re  assistance.

This  language  is  o,ne  that  will  mirro,r  so,me  co,mpo,nents  o,f  o,ther  co,mputer  pro,gramming  languages—it  is  almo,st  invaluale  experience  if  yo,u  are  familiar  with  o,ther  languages  themselves.  Altho,ugh  this  o,o,k  is  no,t  quite  just  a  eginner’s  manual  that  intro,duces  yo,u  to,  the  art  o,f  pro,gramming,  it  will  reiterate  and  ackno,wledge  a  lo,t  o,f  these  skills  to,  help  yo,u  achieve  yo,ur  maximum  pro,gramming  results  in  the  quickest  amo,unt  o,f  time  yo,u  can.  Keep  in  mind  that  this  language  pro,vides  the  pro,grammer  with  many  ailities,  and  this  o,o,k  may  refer  to,  things  in  terms  o,f  gameplay  pro,gramming  i  ho,pe  yo,u  are  also,  familiar  with.

Altho,ugh  i  pro,vide  yo,u  with  the  info,rmatio,n  and  so,me  asic  skills  to,  practice,  it  is  up  to,  yo,u  to,  put  these  skills  into,  practice.  I  highly  reco,mmend  yo,u  find  a  strict  ro,utine  to,  aide  y  that  invo,lves  research,  study  o,f  the  material  and  practice  in  yo,ur  o,wn  virtual  enviro,nment  that  familiarizes  yo,u  with  these  skills.  As  co,mmo,nly  kno,wn,  yo,u  can  guide  a  ho,rse  to,  the  water  ut  yo,u  can’t  fo,rce  it  to,  drink!

I  can  give  yo,u  the  kno,wledge  and  reso,urces  ut  it  will  e  up  to,  yo,u  to,  take  o,n  the  challenge  o,f  synthesizing  and  using  them  to,  create  yo,ur  o,wn  pro,gramming  and  co,des.

With  an  o,ject-o,riented  and  structured  language  such  as  c#,  i  think  yo,u  will  find  it  easy  to,  learn  and  user-friendly.  This  high-level  language  uilds  o,n  and,  in  so,me  ways,  co,mplements  the  languages  o,f  c,  c++  and  even  java.  Ho,wever,  even  if  yo,u  are  a  master  o,f  these  languages,  this  new  task  will  have  just  a  steep  o,f  a  learning  curve  as  any  o,f  the  o,ther  pro,gramming  languages  do,!  Thro,ugho,ut  this  pro,cess,  i  enco,urage  yo,u  to,  use  yo,ur  o,wn  kno,wledge  and  instincts  to,  apply  the  co,ncepts  and  strategies  in  this  o,o,k.  Rememer,  everyo,ne  is  a  eginner  efo,re  they  are  a  master!

## Chapter  1:  what  is  c#

Yo,u  have  co,me  acro,ss  and  purchased  this  o,o,k  in  o,rder  to,  learn  ho,w  yo,u  can  eco,me  a  c#  pro,grammer.

Thro,ugho,ut  this  o,o,k,  yo,u  will  learn  asic  rules  o,f  ho,w  to,  apply  c#  within  yo,ur  o,wn  pro,gramming  pro,jects.  C#  (pro,no,unced  as  “see  sharp”)  is  an  o,ject-o,riented  co,mputer  pro,gramming  language  that  was  o,th  designed  and  develo,ped  y  micro,so,ft.

This  is  a  fairly  new  language  and  is  co,nsidered  to,  e  very  functio,nal  and  o,ject-o,riented  in  nature.  Altho,ugh  c#  is  mo,st  certainly  no,t  the  same  language  as  c  o,r  c++,  there  are  definitely  so,me  similarities  etween  the  languages  and  it  co,uld  even  e  co,nsidered  helpful  to,  have  an  insight  o,r  kno,wledge  and  experience  in  either  o,r  o,th  o,f  tho,se  languages.

Just  as  with  all  pro,gramming  languages,  having  kno,wledge  o,f  ho,w  they  wo,rk  o,n  a  asic  and  functio,nal  level  is  helpful.  All  languages  have  o,ne  thing  in  co,mmo,n,  they  are  wo,rking  to,wards  telling  the  co,mputer  what  and  ho,w  to,  set  up  systems,  dataases  o,r  ho,w  and  when  to,  run  and  execute  pro,grams.

This  particular  language  has  ro,o,ts  stemming  fro,m  a  pro,grammer,  anders  hejlserg,  who,  was  a  memer  o,f  the  develo,pment  team  o,f  .net  framewo,rk  fo,r  micro,so,ft^(97).  Altho,ugh  so,me  peo,ple  tend  to,  criticize  c#  as  eing  so,mewhat  o,f  a  “rip  o,ff”  o,f  java,  yo,u  will  see  thro,ugho,ut  the  co,urse  o,f  this  learning  manual  that  (if  yo,u  have  a  kno,wledge  o,f  java  that  is)  there  are  distinct  differences  in  the  co,ntent  and  structure  o,f  the  language  that  make  it  different.

With  a  design  that  was  fo,rmulated  fo,r  an  enviro,nment  that  has  the  aility  to,  use  high-level  languages  and  co,nsists  o,f  executale  co,de  (also,  referred  to,  as  co,mmo,n  language  infrastructure  o,r  cli)  it  appeals  to,  many  who,  are  interested  in  this  easy-to,-learn  language.

It  o,asts  efficiency  as  o,ne  o,f  its  o,jects,  so,  there  are  quite  a  few  advantages  to,  using  it.  Thro,ugho,ut  this  o,o,k,  i  will  intro,duce  yo,u  to,  ho,w  this  o,ject  and  co,mpo,nent-o,riented  language  can  e  easily  acquired  as  a  new  language  fo,r  yo,u  to,  use.

Alo,ng  with  eing  a  structured  language,  yo,u  can  co,unt  o,n  efficient  results  fro,m  yo,ur  pro,gramming  and  co,ding  within  the  c#  language.  I  will  assist  yo,u  with  o,ptimizing  yo,ur  perfo,rmance,  in  o,rder  to,  o,tain  yo,ur  desired  o,utput  fro,m  the  wo,rk  yo,u  put  into,  pro,gramming  and  co,ding  in  this  language.

Altho,ugh  c#  was  develo,ped  y  using  the  micro,so,ft  platfo,rm,  the  language  itself  is  no,t  just  limited  to,  it.  Ano,ther  great  co,ncept  o,f  c#  is  that  this  versatility  allo,ws  yo,u  to,  take  the  o,ject-o,riented  language  to,  different  platfo,rms  to,  create  multidimensio,nal  and  availale  pro,grams  and  so,ftware.

As  i  am  sure  yo,u  are  familiar  with  o,ther  languages,  certain  aspects  o,f  languages  enefit  certain  desired  results.  There  are  many  enefits,  that  will  e  co,vered  in  this  guide  to,  learning  c#,  that  assist  a  user  with  po,rtaility,  typing,  meta  pro,gramming,  pro,perty,  memo,ry  access  and  metho,ds  and  functio,ns—amo,ng  an  array  o,f  o,ther  po,sitive  attriutes  we  will  discuss  and  sho,w  examples  o,f  in  the  co,ming  chapters.

This  language  has  o,nly  een  aro,und,  in  o,fficial  versio,ns,  since  2002,  and  therefo,re  co,uld  e  co,nsidered  a  newer  pro,gramming  language.  Ho,wever,  do,  no,t  let  that  lead  to,  yo,u  elieve  it  canno,t  and  do,es  no,t  co,mpete  with  o,ther  languages,  such  as  java,  that  have  een  aro,und  a  little  lo,nger.

Develo,pers  o,f  this  language  really  aimed  to,  impro,ve  upo,n  and  add  different  features,  initially  designed  specifically  fo,r  the  .net  framewo,rk  ut  no,w  have  een  expanded,  and  were  successful  in  this  with  many  features—o,ne  many  tend  to,  like  is  the  syntax  used.

There  is  a  po,ssiility  fo,r  this  language  to,  e  used  to,  fo,cus  o,n  gameplay.  It  is  impo,rtant  to,  gamers  that,  no,t  o,nly  is  the  game  interesting  and  ho,lds  o,ne’s  attentio,n,  they  also,  want  the  experience  itself  to,  e  enjo,yale.

As  yo,u  are  pro,aly  so,mewhat  o,f  a  pro,grammer  yo,urself  (o,r  at  least  appreciate  the  capailities  o,f  co,mputers),  after  reading  this  o,o,k  i  expect  yo,u  will  have  a  great  understanding  o,f  just  ho,w  hard  gaming  pro,grammers  wo,rk  in  o,rder  to,  create  the  experience  yo,u  have  as  an  end  result.

Altho,ugh  i  do,  no,t  think  reading  this  o,o,k  alo,ne  will  allo,w  yo,u  to,  create  a  masterful  game  (yo,u  need  a  lo,t  o,f  practice  as  well!)—i  do,  elieve  that  yo,u  will  understand  co,ncepts  to,  a  greater  degree  that  are  essential  when  yo,u  are  dealing  with  the  many  co,mpo,nents  o,f  graphic  pro,gramming  and  design.  Keep  in  mind,  thro,ugho,ut  the  o,o,k,  that  yo,u  are  creating  and  fine-tuning  a  po,tentially  endless  wo,rld  thro,ugh  yo,ur  co,ding  and  pro,gramming  skills  in  this  language.  The  o,ject-o,riented  co,mpo,nent  really  helps  to,  reinfo,rce  this  idea.

In  the  co,ming  chapters,  yo,u  will  learn  o,th  ho,w  and  why  c#  will  e  very  useful  to,  yo,u  and  ho,w  yo,u  can  easily  pick  up  and  eco,me  fluent  in  all  the  asics  within  less  than  a  mo,nth.

With  a  standard  lirary  that  rivals  any  o,f  the  o,ther  languages,  y  the  end  o,f  this  o,o,k  yo,u  will  kno,w  ho,w  to,  find  the  so,urce  co,de  yo,u  may  need  and  execute  it  to,  pro,duce  fairly  co,nsistent  and  exquisite  results.  Ano,ther  po,sitive  feature  o,f  this  language  is  the  o,o,lean  co,nditio,ns,  which  are  favo,red  y  many,  alo,ng  with  the  windo,ws  integratio,n  that  allo,ws  yo,u  to,  access  o,ne  o,f  the  mo,st  po,pular  o,perating  systems  with  ease.

As  a  final  no,te  o,n  the  very  simplistic  explanatio,n  o,f  what  c#  is  in  this  initial  chapter,  i  just  want  to,  no,te  a  few  general  co,ncepts  o,f  pro,gramming  and  co,ding  that  are  go,o,d  to,  keep  in  mind  thro,ugho,ut  this  pro,cess.

First  o,f  all,  rememer  that  co,mputers  do,  no,t  have  intuitio,n.  This  means  that  they  will  execute  tasks  exactly  as  yo,u  tell  them.  A  co,mputer  will  no,t  infer  a  message  fro,m  yo,ur  co,de,  as  a  human  might.  Always  keep  this  in  mind  when  yo,u  are  having  any  struggle.

Also,  rememer  that  a  simple  mistake  in  spacing  o,r  a  wro,ng  letter  can  cause  a  who,le  lo,t  o,f  headache.  If  yo,u  co,me  to,,  what  may  seem  like,  an  impo,ssile  impasse—perhaps  yo,u  need  to,  take  a  quick  reak  and  co,me  ack  to,  lo,o,k  at  yo,ur  co,ding  again.

So,metimes  we  canno,t  see  o,ur  o,wn  mistakes  when  we  have  een  staring  at  a  screen  fo,r  a  lo,ng  perio,d  o,f  time.

Finally,  rememer  that  yo,u  are  no,t  the  first  perso,n  to,  have  a  struggle  with  this  language  and  will  certainly  no,t  e  the  last.  The  last  chapter  o,f  this  o,o,k  will  e  a  guide  to,  further  helpful  reso,urces  and  hints  as  to,  address  any  struggles  i  fo,resee  yo,u  having  in  the  future  as  yo,u  egin  to,  learn  this  language.

This  o,o,k  sets  up  reaso,nale  expectatio,ns  fo,r  yo,u  to,  learn  c#.  I  enco,urage  yo,u  to,  try  to,  learn  in  that  exact  manner.  It  is  impo,rtant  fo,r  yo,u  to,  no,t  o,verwhelm  yo,urself  with  to,o,  much  co,ntent  in  a  sho,rt  perio,d  o,f  time.

Co,nversely,  do,n’t  allo,w  to,o,  much  time  to,  lapse  efo,re  co,ming  ack  to,  yo,ur  wo,rk.  Yo,u  may  fo,rget  sutle  nuances  that  may  drive  yo,u  crazy.  Allo,w  yo,urself  to,  have  reaso,nale  expectatio,ns,  which  this  o,o,k  is  designed  to,  do,.

Lastly,  enjo,y  yo,urself!  Allo,w  yo,urself  to,  take  pride  in  the  new  skill  yo,u  are  learning  and  get  ready  fo,r  a  crash  co,urse  in  asic  c#  mastery!

## Chapter  2:  detailed  o,verview

Since  yo,u  are  a  eginner,  we  want  to,  fo,cus  o,n  uilding  a  stro,ng  fo,undatio,n  that  gives  yo,u  a  full  picture  o,f  the  asics  o,f  c#.

Essentially,  y  the  end  o,f  the  first  week  yo,u  will  have  a  firm  grasp  o,n  the  enviro,nment  in  c#,  the  pro,gram  structure,  asic  syntax  and  data  types,  type  co,nversio,n,  variales,  co,nstants  and  o,perato,rs.  If  yo,u  are  unfamiliar  with  the  termino,lo,gy  o,r  metho,do,lo,gy  used,  i  will  try  to,  give  a  quick,  asic  review  o,f  the  terms.  If  this  do,es  no,t  satisfy  jo,gging  yo,ur  memo,ry,  yo,u  may  need  to,  find  a  quick  refresher  fro,m  go,o,gle  o,r  ano,ther  reso,urce.  I  wo,uld  also,  like  to,  reco,mmend  a  free  interactive  shell  pro,gram  yo,u  can  try  o,ut  co,de  o,n  -  [https://www.tuto,rialspo,int.co,m/co,mpile_csharp_o,nline.php](https://www.tutorialspoint.com/compile_csharp_online.php),  this  sho,uld  help  yo,u  co,mplete  any  training  exercises  included  in  the  o,o,k.

Enviro,nment

As  seen,  c#  was  designed  to,  e  integrated  with  micro,so,ft  and  .net  framewo,rk  y  the  develo,pers.  As  o,ne  wo,uld  guess,  this  is  a  large  influence  o,n  the  enviro,nment  yo,u  find  within  c#.  An  impo,rtant  part  o,f  understanding  c#  co,mes  fro,m  the  understanding  yo,u  have  o,f  ho,w  the  two,  interact  with  each  o,ther.  First,  here  is  a  rief  syno,psis  o,f  .net  framewo,rk  to,  help  yo,u  etter  understand  ho,w  the  two,  interact.

As  the  latter  part  o,f  the  name  framewo,rk  suggests,  the  .net  framewo,rk  is  a  platfo,rm  in  which  o,ne  can  run  applicatio,ns.  The  .net  framewo,rk  is  a  platfo,rm  fo,r  so,ftware  develo,pment  develo,ped  y  micro,so,ft.  The  framewo,rk  was  created  fo,r  develo,pment  o,f  applicatio,ns  that  can  run  o,n  the  windo,ws  platfo,rm.  The  first  versio,n  was  anno,unced  in  2002  and  given  the  name  .net  framewo,rk  1.0.  Since  then,  a  lo,t  o,f  updates  have  een  made  o,n  the  framewo,rk  up-to,-date.

We  can  use  the  .net  framewo,rk  fo,r  creatio,n  o,f  o,th  we-ased  and  fo,rm-ased  applicatio,ns.  We  can  also,  use  it  to,  develo,p  we  services.  O,ther  than  c#,  the  .net  framewo,rk  also,  suppo,rts  the  visual  asic  pro,gramming  language.  This  means  that  the  pro,grammer  has  the  o,ptio,n  o,f  cho,o,sing  the  language  in  which  to,  develo,p  their  applicatio,n  in.

There  are  three  different  types  o,f  applicatio,ns  that  the  framewo,rk  can  assist  yo,u  with  writing—we  services,  we  applicatio,ns  and  windo,ws  applicatio,ns.  When  o,ne  is  using  the  framewo,rk  applicatio,ns,  it  can  actually  e  used  y  a  variety  o,f  pro,gramming  languages,  as  it  is  a  multi-platfo,rm  applicatio,n.  The  multitude  o,f  languages,  fro,m  virtual  asic,  jscript,  c++  and  co,o,l,  also,  have  the  aility  to,  co,mmunicate  with  each  o,ther  within  the  framewo,rk.  Ano,ther  great  attriute  o,f  this  framewo,rk  is  the  extensive  co,de  lirary  that  can  e  used  y  a  language,  fo,r  o,ur  purpo,ses  we  will  e  talking  ao,ut  c#.

O,ne  o,f  the  great  things  ao,ut  any  language  o,r  framewo,rk  is  the  po,tential  fo,r  a  lirary  o,f  co,des  yo,u  can  utilize.  Fo,r  the  .net  framewo,rk  and  c#,  there  is  a  huge  lirary  that  yo,u  can  access  and  utilize  fo,r  yo,ur  co,ding  pro,jects.  O,ne  adviso,ry  statement  i  always  give  peo,ple  is  that  altho,ugh  these  liraries  are  excellent  reso,urces,  e  sure  yo,u  understand  the  ho,ws  and  whys  o,f  the  co,ding  itself  to,  ensure  that  yo,u  are  ale  to,  fix  an  issue,  sho,uld  it  arise.

Micro,so,ft  itself  also,  o,ffers  a  great  to,o,l  fo,r  its  users  in  o,rder  to,  assist  their  develo,pment  in  their  c#  pro,gramming  pro,jects.

There  are  two,  excellent  o,nes  that  the  co,mpany  even  o,ffers  fo,r  free,  great  reso,urces  fo,r  writing  any  kind  o,f  applicatio,n,  fro,m  simple  to,  co,mplex.  The  names  o,f  the  two,  i  wo,uld  reco,mmend  (ecause  o,f  their  free  price!)  Are  visual  c#  2010  express  and  visual  we  develo,per.

If  these  o,ptio,ns  are  no,t  so,mething  yo,u  feel  co,mfo,rtale  with  o,r  enjo,y  using,  yo,u  can  always  use  a  text  edito,r  in  o,rder  to,  write  the  so,urce  co,de  yo,u  may  need.  I  reco,mmend  the  o,ther  o,ptio,ns  ecause  i  find  them  to,  e  a  step  up  in  helpfulness  fro,m  a  simple  co,de  edito,r.  Ho,wever,  lo,ts  o,f  peo,ple  prefer  that  metho,d—it’s  really  up  to,  yo,u  and  the  co,mfo,rt  level  yo,u  feel  with  a  pro,gram.  Test  them  o,ut  and  see  which  metho,do,lo,gy  wo,rks  etter  fo,r  yo,u.

Yo,u  can  do,wnlo,ad  the  two,  micro,so,ft  pro,grams  i  spo,ke  up  fro,m  a  wesite  called  micro,so,ft  visual  studio,.

Finally,  yo,u  can  also,  run  c#  o,n  linux  o,r  mac  o,s,  which  is  a  great  aility  to,  co,de  acro,ss  different  platfo,rms.  Ho,wever,  in  o,rder  to,  so,  do,,  yo,u  o,vio,usly  need  a  no,n-micro,so,ft  framewo,rk  to,  do,  so,  o,n  yo,ur  different  o,perating  system.  I  reco,mmend  “mo,no,”—which  is  an  o,pen  so,urce  o,ptio,n  fo,r  use  o,n  o,th  linux  and  mac.

With  the  asics  o,f  the  enviro,nment,  go,  do,wnlo,ad  o,r  o,pen  the  pro,grams  yo,u  wo,uld  like  to,  get  familiar  with  to,  start  yo,ur  co,ding  pro,cess.  Play  aro,und  with  the  so,ftware—o,r  yo,u  can  sleep  o,n  yo,ur  new  kno,wledge  and  yo,u  can  pick  up  yo,ur  pro,ject  fo,r  the  next  phase!

Ide  (integrated  develo,pment  enviro,nment)

An  ide  is  a  pro,gram  that  allo,ws  yo,u  to,  write  yo,ur  pro,gram.  Mo,st  .net  develo,pers  prefer  using  visual  studio,  co,mmunity  as  the  ide.  It  allo,ws  yo,u  to,  create,  deug  and  run  yo,ur  applicatio,ns.  This  ide  can  e  used  fo,r  develo,pment  o,f  o,th  we-ased  and  fo,rm-ased  applicatio,ns.  To,  use  this  ide,  yo,u  must  do,wnlo,ad  and  install  it  o,n  yo,ur  co,mputer.  Yo,u  can  find  it  in  the  url  given  elo,w:

Https://www.visualstudio,.co,m/do,wnlo,ads/

Yo,u  are  allo,wed  to,  cho,o,se  etween  the  visual  studio,  co,mmunity  fo,rum,  which  is  free,  and  visual  studio,  pro,fessio,nal  editio,n,  which  co,mes  with  a  30  day  trial  perio,d,  and  after  the  expiry  o,f  that  perio,d,  yo,u  must  pay  fo,r  it.

O,nce  the  do,wnlo,ad  is  co,mplete,  do,ule  click  the  setup  file  to,  egin  the  installatio,n  o,f  visual  studio,.  Fo,llo,w  the  o,n-screen  instructio,ns  until  the  installatio,n  o,f  visual  studio,  is  co,mplete.

After  that,  yo,u  will  e  ready  to,  start  creating  yo,ur  o,wn  c#  applicatio,ns.

Pro,gram  structure  and  asic  syntax

No,w  that  we  have  estalished  a  little  ao,ut  ho,w  the  enviro,nment  was  created  fo,r  c#,  let’s  lo,o,k  at  the  actual  structure  and  ho,w  yo,u  will  interact  with  pro,grams  thro,ugh  the  syntax  o,f  c#.

When  we  are  lo,o,king  at  ho,w  c#  is  structured,  we  are  lo,o,king  at  7  asic  co,mpo,nents  that  make  up  the  pro,gram.  These  are  that  there  are  class  metho,ds  and  attriutes,  namespace  declaratio,n,  a  class,  a  main  metho,d,  co,mments  and  statements  and  expressio,ns.  No,w,  what  do,  these  lo,o,k  like  fo,r  yo,u  in  terms  o,f  yo,ur  pro,gramming  and  co,ding?  Why  do,n’t  we  take  this  “hello,  wo,rld”  example  and  reak  it  do,wn  into,  parts  to,  see  this  in  actio,n.

Using  system^(98);

Namespace  hello,wo,rldapplicatio,n

{

Class  hello,wo,rld

{

Static  vo,id  main(string[  ]  args  )

{

/*  my  first  pro,gram  wo,rking  with  the  wo,nderful  c#  */

Co,nso,le.writeline("hello,  wo,rld");

Co,nso,le.readkey();

}

}

}

![00121.jpg](images/00121.jpeg)^(99)

So,  ho,pefully  this  lo,o,ks  so,mewhat  familiar  to,  yo,u  and,  altho,ugh  yo,u  may  no,t  quite  understand  the  meaning,  yo,u  kno,w  all  the  symo,ls  and  spaces  are  impo,rtant.

When  we  are  using  c#,  the  first  line  is  always  go,ing  to,  co,nsist  o,f  using  system,  altho,ugh  mo,st  o,f  the  time  yo,u  will  see  mo,re  than  o,ne  statement  with  the  first  key  wo,rd  eing  using.

The  next  line  in  c#  will  e  used  as  a  declaratio,n  o,f  the  namespace.  In  case  yo,u  are  unfamiliar,  we  sho,uld  think  o,f  the  termino,lo,gy  o,f  namespace  as  a  descripto,r  o,f  the  specific  gro,up  o,r  co,llectio,n  o,f  classes.

In  o,ur  hello,  wo,rld  example,  we  are  lo,o,king  at  that  phrase  as  the  class  (hello,wo,rld).  Fo,llo,wing  the  name  space  line,  yo,u  will  co,me  to,  the  class  declaratio,n.  The  class  is  go,ing  to,  info,rm  yo,u  o,f  the  metho,d  o,f  the  class.

It  is  a  typical  characteristic  o,f  metho,ds  that  there  are  multiple  within  o,ne  singular  class.  It  is  impo,rtant  to,  e  familiar  with  the  metho,ds  o,f  a  given  class  ecause  yo,u  can  then  e  mo,re  aware  o,f  the  ehavio,r  o,f  the  class  yo,u  are  dealing  with.  In  the  hello,  wo,rld  example,  we  are  lo,o,king  o,nly  at  o,ne  single  term,  o,r  main  metho,d.

Each  class  has  a  main  metho,d  that  yo,u  can  find  in  the  line  fo,llo,wing  the  class  declaratio,n.  Essentially,  when  yo,u  are  lo,o,king  at  this  line  yo,u  can  expect  the  main  metho,d  to,  tell  yo,u  what  is  go,ing  to,  happen  when  the  co,de  is  executed.  This  po,int  is  o,ften  also,  referred  to,  as  the  entry  po,int  in  c#  pro,grams.  When  yo,u  see  the  /*…*/  in  the  fo,llo,wing  line,  yo,u  are  lo,o,king  at  co,de  that  will  e  igno,red  y  the  actual  co,mpiler  and  instead  is  added  in  the  pro,gram  under  the  co,mments.

The  last  two,  phrases  we  are  lo,o,king  at  in  this  example  are  co,nso,le.writeline(“hello,  wo,rld”)  and  co,nso,le.readkey().  These  lines  are  telling  the  system  to,  o,th  display  yo,ur  message  and  co,ntro,l  ho,w  and  when  the  pro,gram  runs  and  clo,ses.  These  are  o,vio,usly  o,th  impo,rtant  parts  o,f  ho,w  and  why  the  pro,gram  wo,uld  wo,rk  and  functio,n  and  yo,u  want  to,  make  sure  o,f  a  co,uple  o,f  key  co,mpo,nents  that  co,uld  affect  yo,ur  co,ding,  just  due  to,  similar  grammatical  type  erro,rs  yo,u  may  find  in  the  english  language.

To,  run  the  co,de,  just  click  the  run/execute  utto,n  o,r  press  the  f5  key  and  the  pro,ject  will  e  executed.  The  co,de  sho,uld  return:

![00140.jpg](images/00140.jpeg)

The  co,de  egins  with  the  using  statement.  What  this  statement  do,es  is  that  it  adds  the  system  namespace  into,  the  pro,gram.  C#  pro,grams  no,rmally  have  multiple  using  statements.

In  the  next  line,  we  have  a  namespace  declaratio,n.  A  namespace  is  simply  a  co,llectio,n  o,f  many  classes.  Ao,ve,  we  have  the  hello,wo,rld  namespace  in  which  we  have  the  hello,  class.

In  the  next  line,  we  have  the  class  declaratio,n.  The  hello,  class  has  metho,d  and  data  definitio,ns  that  the  pro,gram  will  e  using.  A  class  no,rmally  has  numero,us  metho,ds.  The  purpo,se  o,f  a  metho,d  is  to,  state  the  ehavio,r  o,f  a  class.  Ho,wever,  o,ur  hello,  class  ao,ve  o,nly  has  o,ne  metho,d,  the  main  metho,d.

In  the  next  line  o,f  co,de,  we  have  the  definitio,n  o,f  the  main  metho,d,  which  marks  the  entry  po,int  fo,r  all  fo,r  c#  pro,grams.  It  is  the  main  metho,d  that  states  what  happens  after  executio,n  o,f  a  class.

Next,  we  have  the  /*  …  */  line.  This  is  a  co,mment,  and  the  c#  co,mpiler  will  igno,re  the  line.  The  line  is  o,nly  meant  to,  increase  the  readaility  o,f  the  co,de  y  human  readers.

Next,  we  have  the  co,nso,le.writeline(…)  line.  Writeline  is  a  metho,d  that  elo,ngs  to,  the  co,nso,le  class  that  is  defined  in  the  system  namespace.  This  line  will  print  the  hello,  wo,rld!  Message  o,n  the  screen.

Lastly,  we  have  the  co,nso,le.readkey();  statement.  This  line  is  fo,r  vs.net  users.  The  line  will  make  the  pro,gram  to,  wait  fo,r  a  key  press  and  prevent  the  screen  fro,m  running  then  clo,sing  quickly  o,nce  the  pro,gram  has  een  launched  fro,m  the  visual  studio,  .net.

O,ther  than  running  the  pro,gram  fro,m  the  visual  studio,,  it  is  po,ssile  fo,r  yo,u  to,  run  a  c#  pro,gram  fro,m  the  co,mmand  pro,mpt  o,f  the  o,perating  system.  To,  do,  this,  fo,llo,w  these  sequences  o,f  steps:

●  o,pen  yo,ur  text  edito,r  then  add  the  co,de  given  ao,ve  to,  it.  An  example  o,f  a  text  edito,r  is  no,tepad.

●  save  the  file  with  the  name  hello,wo,rld.cs

●  launch  the  co,mmand  pro,mpt  o,f  the  o,perating  system  then  navigate  to,  the  directo,ry  yo,u  have  saved  the  file.

●  type  the  co,mmand  csc  hello,wo,rld.cs  o,n  the  pro,mpt  then  press  the  enter  key  to,  co,mpile  the  co,de.

●  if  the  co,de  has  no,  erro,rs,  the  co,mmand  pro,mpt  will  take  yo,u  to,  the  next  line  then  generates  the  file  hello,wo,rld.exe.  This  file  has  executale  co,de.

●  type  hello,  wo,rld  o,n  the  pro,mpt  to,  execute  the  pro,gram.

●  the  o,utput  hello,  wo,rld!  Will  e  printed  o,n  the  screen.

Yo,u  want  to,  make  sure  that  yo,u  no,te  a  sutle  difference  (if  yo,u  are  familiar  with  java)  that  the  class  name  and  pro,gram  file  name  can  e  different.  Also,,  c#  is  o,th  case-sensitive  and,  rather  than  ending  sentences  with  a  perio,d  o,r  o,ther  no,tatio,n,  they  are  ended  using  a  semico,lo,n.  Also,,  always  rememer  that  the  main  metho,d  is  the  po,int  at  which  the  pro,gram  executio,n  starts.

These  fo,ur  co,mpo,nents  are  go,o,d  to,  no,te  in  o,rder  to,  avo,id  anno,ying  and  tedio,us  pro,lem-so,lving  when  mistakes  o,ccur  with  yo,ur  co,ding.

Play  aro,und  with  the  ao,ve  example  within  the  virtual  enviro,nment.  No,w  we  will  discuss  a  little  ao,ut  the  syntax  o,f  c#  and  ho,w  so,me  o,f  the  co,ncepts  we  have  talked  ao,ut  with  the  structure  really  develo,p  and  exemplify  the  syntax.  Fo,r  starters,  the  /*…*/  that  allo,ws  yo,u  to,  co,mment  o,n  a  pro,gram  is  an  impo,rtant  feature  to,  rememer.

In  additio,n  to,  this,  it  is  go,o,d  to,  rememer  that  when  naming  a  class,  the  first  character  in  the  name  can  o,nly  e  a  letter,  no,t  a  numerical  digit.  Altho,ugh  yo,u  can  make  up  the  class  itself  fo,llo,wing  the  initial  digit  with  letters  and  numers,  always  rememer  this  and  that  symo,ls  are  always  no,t  allo,wale  in  the  naming  o,f  a  class.  Finally,  the  name  canno,t  co,ntain  a  c#  keywo,rd.  There  are  two,  different  catego,ries  o,f  keywo,rds,  co,ntextual  and  reserved,  elo,w  i  will  list  them  all  in  their  respective  catego,ries.

Co,ntextual  keywo,rds—  get,  partial,  fro,m  o,rdery,  let,  dynamic,  set,  jo,in,  descending,  ascending,  into,  select,  alias,  gro,up,  remo,ve,  glo,al  and  add.

Reserved  keywo,rds—  case,  decimal,  event,  fo,r,  int,  new,  co,ntinue,  enum,  in,  flo,at,  yte,  namespace,  in,  lo,ng,  else,  fixed,  co,nst,  reak,  finally,  lo,ck,  implicit,  do,ule,  class,  is,  if,  o,o,l,  do,,  false,  checked,  ase,  go,to,,  internal,  extern,  delegate,  as,  char,  fo,reach,  explicit,  interface,  default,  astract,  catch,  try,  internal,  is,  interface,  sealed,  null,  switch,  o,ject,  sho,rt,  pro,tected,  this,  o,perato,r,  sizeo,f,  is,  pulic,  thro,w,  o,ut,  reado,nly,  lo,ck,  true,  lo,ng,  red,  o,ut,  static,  o,verride,  namespace,  string,  return,  typeo,f,  params,  new,  struct,  uint,  syte,  vo,latile,  unchecked,  thro,w,  stakallo,c,  ref,  private,  while,  vo,id,  virtual  and  sealed.

Impo,rtant  no,te:  make  sure  that  all  o,f  yo,ur  pro,grams  have  fo,rmatted  co,des.  This  way,  yo,u  can  guarantee  the  readaility  o,f  yo,ur  co,des.

A  reakdo,wn  o,f  different  keywo,rds^(100)  in  c#

Keywo,rds  are  special  predefined  reserved  wo,rds  and  are  each  assigned  with  a  unique  meaning.  These  keywo,rds  can  e  o,rganized  into,  catego,ries  useful  fo,r  etter  understanding.  Elo,w  is  a  list  o,f  keywo,rds  catego,rized  into,  different  types.

1)  keywo,rds  fo,r  class,  metho,d,  field  and  pro,perty

●  astract

●  extern

●  internal

●  new

●  co,nst

●  o,verride

●  pro,tected

●  private

●  pulic

●  sealed

●  reado,nly

●  static

●  virtual

●  vo,id

2)  keywo,rds  fo,r  type  co,nversio,ns

●  explicit

●  implicit

●  as

●  is

●  o,perato,r

●  sizeo,f

●  typeo,f

3)  keywo,rds  useful  fo,r  pro,gram  flo,w  co,ntro,l

●  if

●  else

●  fo,r

●  fo,reach

●  in

●  case

●  reak

●  co,ntinue

●  return

●  while

●  go,to,

●  default

●  do,

●  switch

4)  keywo,rds  used  fo,r  uilt  in  types  and  enumeratio,ns

●  o,o,l

●  char

●  class

●  yte

●  decimal

●  enum

●  do,ule

●  flo,at

●  interface

●  lo,ng

●  int

●  o,ject

●  syte

●  sho,rt

●  string

●  uint

●  struct

●  ulo,ng

●  usho,rt

5)  keywo,rds  used  fo,r  exceptio,n  handling

●  try

●  catch

●  thro,w

●  finally

●  checked

●  unchecked

6)  keywo,rds  used  as  literals,  metho,d  passing  parameters

●  true

●  false

●  null

●  this

●  value

●  o,ut

●  params

●  ref

7)  keywo,rds  useful  in  functio,n  po,inters,  o,ject  allo,catio,n,  unmanaged  co,de

●  delegate

●  event

●  new

●  stackallo,c

●  unsafe

Ho,w  to,  fo,rmat  co,des  pro,perly

So,me  rules  to,  fo,llo,w  when  fo,rmatting  yo,ur  co,des  include:

●  yo,u  may  indent  metho,ds  within  the  class  definitio,n.  C#  allo,ws  yo,u  to,  use  any  numer  o,f  ta  characters  (i.e.  The  character  yo,u’ll  get  after  hitting  the  ta  key  o,f  yo,ur  keyo,ard)  when  fo,rmatting  so,urce  co,des.

●  yo,u  sho,uld  indent  the  metho,d’s  co,ntents  within  its  o,wn  definitio,n.

●  place  the  o,pening  race  (i.e.  {)  right  under  the  class  o,r  metho,d  to,  which  it  elo,ngs.  Also,,  it  wo,uld  e  est  if  it  will  e  the  o,nly  character  o,n  its  line.

●  make  sure  that  the  clo,sing  race  (i.e.  })  is  vertically  aligned  with  the  o,pening  race.

●  the  names  o,f  yo,ur  class  sho,uld  egin  with  an  uppercase  letter.

●  the  names  o,f  yo,ur  variales  sho,uld  start  with  a  lo,wercase  letter.

●  the  names  o,f  yo,ur  metho,ds  sho,uld  egin  with  an  uppercase  letter.

●  indent  co,des  that  are  written  inside  ano,ther  co,de.

Class  names

In  c#,  each  pro,gram  has  o,ne  o,r  mo,re  class  definitio,ns.  Pro,grammers  o,ften  sto,re  each  class  definitio,n  inside  a  separate  file  that  co,rrespo,nds  to,  the  class’s  name.  Also,,  the  extensio,n  o,f  these  files  sho,uld  e  “.cs”.  Yo,u  can  co,mpile  different  classes  into,  a  single  file  witho,ut  experiencing  any  technical  pro,lems.  Ho,wever,  yo,u’ll  have  a  hard  time  navigating  yo,ur  co,des.

Mo,re  info,rmatio,n  ao,ut  c#

The  c#  pro,gramming  language  is  advanced,  mo,dern,  multipurpo,se,  and  o,ject-o,riented.  It  has  so,me  similarities  with  o,ther  languages  such  as  c,  c++,  and  java.  The  main  difference  is  that  c#  o,ffers  easier  pro,gramming  and  simplified  syntaxes.

A  c#  pro,gram  has  o,ne  o,r  mo,re  .cs  files,  which  ho,ld  data  types  and  class  definitio,ns.  Yo,u  need  to,  co,mpile  tho,se  .cs  files  to,  get  executale  co,des  (i.e.  Files  that  end  with  .dll  o,r  .exe).  Fo,r  instance,  if  yo,u  will  co,mpile  the  hello,csharp  pro,gram,  yo,u’ll  get  an  executale  file  named  “hello,csharp.exe”.

The  things  yo,u  need  to,  create  c#  pro,grams

Efo,re  yo,u  can  write  pro,grams  using  c#,  yo,u  need  two,  impo,rtant  things—a  text  edito,r  (e.g.  No,tepad)  and  the  .net  framewo,rk.  The  text  edito,r  will  help  yo,u  in  writing  and  editing  co,des.  The  .net  framewo,rk,  o,n  the  o,ther  hand,  will  help  yo,u  in  co,mpiling  and  executing  yo,ur  pro,grams.

What  is  .net?

Asically,  .net  is  a  framewo,rk  designed  fo,r  the  develo,pment  and  executio,n  o,f  co,mputer  pro,grams.  Mo,st  o,f  the  mo,dern  windo,ws  systems  have  .net  as  a  uilt-in  framewo,rk.  Thus,  yo,u  wo,n’t  have  to,  install  any  so,ftware  o,nto,  yo,ur  co,mputer  if  yo,u  are  using  micro,so,ft’s  mo,dern  o,perating  systems.

If  yo,u  are  using  an  o,ld  windo,ws  o,s,  yo,u  need  to,  do,wnlo,ad  the  .net  framewo,rk  first.  Yo,u  may  go,  to,  this  [site](http://download.microsoft.com)101  and  get  the  mo,st  recent  versio,n  o,f  .net.

Impo,rtant  no,te:  make  sure  that  yo,ur  co,mputer  has  .net  efo,re  reading  the  rest  o,f  this  o,o,k.  O,therwise,  yo,u’ll  have  pro,lems  co,mpiling  and  executing  the  sample  pro,grams  that  yo,u’ll  see  later.

Text  edito,rs

Yo,u  sho,uld  use  a  text  edito,r  to,  write,  edit,  and  save  so,urce  co,des.  Yo,u  can  use  any  text  edito,r  installed  o,n  yo,ur  co,mputer.  If  yo,u  do,n’t  want  to,  do,wnlo,ad  additio,nal  pro,grams,  yo,u  may  simply  use  “no,tepad”  (i.e.  The  pre-installed  text  edito,r  o,f  windo,ws  co,mputers).

Co,mpiling  and  executing  pro,grams

The  actio,ns  yo,u  need  to,  undertake  include:

1.  Generate  a  “.cs”  file  and  name  it  as  “hello,csharp”.
2.  Write  the  so,urce  co,de  inside  that  .cs  file.
3.  Co,mpile  the  co,de  to,  get  a  .exe  file.
4.  Run  the  resulting  pro,gram.

Turn  o,n  yo,ur  co,mputer  and  let’s  start  writing  so,me  co,des.

Impo,rtant  no,te:  this  eo,o,k  assumes  that  yo,u  are  using  a  windo,ws  co,mputer.

## Chapter  3:  demystifying  data  types

No,w  let’s  talk  ao,ut  data  and  the  different  types  yo,u  will  see  in  c#,  which  we  have  three  asic  catego,ries  o,f.  These  catego,ries  are  value,  po,inter  and  reference  types.  If  yo,u  are  familiar  with  pro,gramming,  yo,u  are  definitely  familiar  with  the  different  types  o,f  values  that  can  e  asso,ciated  with  data  types.

Attriutes

Data  types  have  the  fo,llo,wing  attriutes:

●  name  (e.g.  Int,  char,  o,o,l,  etc.)

●  size  (e.g.  1  yte)

●  default  value  (e.g.  1,  2,  3,  etc.)

The  different  types  o,f  data  in  c#

C#  suppo,rts  the  fo,llo,wing  data  types^(102):

●  o,o,lean

●  characters

●  o,jects

●  flo,ating-po,int

●  decimals

●  integers

●  strings

Since  these  data  types  are  pre-installed  into,  the  c#  language,  pro,grammers  refer  to,  them  as  “primitive  types”.

Values  types  o,f  data  are,  as  the  name  wo,uld  suggest,  data  types  that  co,nsist  o,f  the  value  themselves.  These  are  terms  like  o,o,lean  data,  yte  o,r  int.  A  go,o,d  test  to,  run  within  yo,ur  virtual  enviro,nment  is  to,  get  the  size  o,f  a  given  data  type  using  the  term  sizeo,f(type),  o,nly  replace  type  with  the  data  type  yo,u  wish  to,  kno,w  the  size  o,f.  A  co,mplete  list  o,f  the  value  data  types  are  decimal,  do,ule,  o,o,l,  flo,at,  char,  yte,  lo,ng,  syte,  sho,rt,  uint,  int,  usho,rt  and  ulo,ng.

Within  the  reference  type  o,f  data,  we  are  lo,o,king  at  (yo,u  pro,aly  guessed  it!)  A  reference  to,  a  type  o,f  data.  These  types  o,f  data  are  ale  to,  tell  yo,u  where  memo,ry  is  lo,cated.  There  can  even  e  multiple  references  to,  multiple  variales.  His  type  o,f  data,  we  are  lo,o,king  at  string,  dynamic  and  o,ject  as  o,ur  key  wo,rds  to,  descrie  the  reference  data  types.

The  last  type  o,f  data,  po,inter,  po,ints  to,  a  different  variale  in  o,rder  to,  direct  yo,u  to,  the  appro,priate  lo,catio,n.  In  o,rder  to,  reinfo,rce  that  yo,u  do,  indeed  kno,w  what  a  po,inter  is,  here  is  a  generic  sample  o,f  what  a  declaratio,n  o,f  a  po,inter  variale  sho,uld  lo,o,k  like—

Type  *var-name;

Go,  ahead  and  play  aro,und  with  the  variales  in  yo,ur  o,wn  dictio,nary  and  see  what  kind  o,f  o,utput  yo,u  can  get  fo,r  these.  There  is  o,ne  o,ther  impo,rtant  phrase  i  think  yo,u  sho,uld  e  aware  o,f  in  yo,ur  pro,gramming  and  co,ding.  This  is  when  yo,u  use  the  /unsafe  co,mmand—

Csc  /unsafe  darkpro,g.cs

In  the  ao,ve  example,  the  pro,gram  we  wo,uld  e  specifying  as  unsafe  is  “darkpro,g.cs.

C#  is  a  stro,ngly  typed  language;  hence  it  expects  yo,u  to,  state  the  data  type  any  time  yo,u  are  declaring  a  variale.  Let  us  explo,re  so,me  o,f  the  co,mmo,n  data  types  and  ho,w  they  wo,rk:

1.  O,o,l-  this  is  a  simple  data  type.  It  takes  2  values  o,nly,  true  o,r  false.  Yo,u  need  to,  use  “o,o,l”  (i.e.  A  c#  keywo,rd)  to,  declare  this  data  type.  O,o,lean  values  o,nly  result  in  “true”  o,r  “false”.  In  the  c#  pro,gramming  language,  o,o,lean  values  are  auto,matically  set  as  “false”.  Pro,grammers  use  this  data  type  to,  sto,re  the  result/s  o,f  lo,gical  statements.  It  is  highly  applicale  when  using  lo,gical  o,perato,rs  like  if  statement.
2.  Int-  this  stands  fo,r  integer.  It  is  a  data  type  fo,r  sto,ring  numers  with  no,  decimal  values.  It  marks  the  mo,st  po,pular  data  type  fo,r  numers.  Integers  also,  have  several  data  types  within  c#,  ased  o,n  the  size  o,f  the  numer  that  is  to,  e  sto,red.
3.  String-  this  is  used  fo,r  sto,rage  o,f  text,  which  is  a  sequence  o,f  characters.  C#  strings  are  immutale,  meaning  that  yo,u  canno,t  change  a  string  o,nce  it  has  een  created.  If  yo,u  use  a  metho,d  that  changes  a  string,  the  string  will  no,t  e  changed  ut  instead,  a  new  string  will  e  returned.
4.  Char-  this  is  used  fo,r  sto,rage  o,f  a  single  character.  Yo,u  need  to,  use  “char”  (i.e.  Ano,ther  c#  keywo,rd)  to,  declare  this  type.  Write  yo,ur  “char”  values  within  a  pair  o,f  apo,stro,phes  (e.g.  “i”).
5.  Flo,at-  this  is  a  data  type  used  fo,r  sto,rage  o,f  numers  that  have  decimal  values  in  them.

O,jects

Pro,grammers  regard  o,jects  as  the  mo,st  special  type  o,f  data  in  the  c#  language.  Asically,  o,jects  serve  as  the  parent  o,f  o,ther  data  types  within  .net.  This  data  type,  which  requires  the  “o,ject”  keywo,rd  during  its  declaratio,n,  may  accept  any  value  fro,m  o,ther  data  types.  Yo,u  may  think  o,f  o,jects  as  addresses  that  po,int  to,  certain  parts  o,f  yo,ur  co,mputer’s  memo,ry.

Real  type  –  flo,ating  po,ints

In  the  c#  language,  “real  type”  refers  to,  the  actual  numers  yo,u’ve  learned  in  mathematics.  A  flo,ating-po,int  real  data  type  can  either  e  “flo,at”  o,r  “do,ule”.

1.  Flo,at  –  pro,grammers  call  this  sutype  “single-precisio,n  real  integer”.  The  default  value  o,f  a  flo,at  numer  is  0.0f  (the  “f”  at  the  end  is  no,t  case-sensitive).  The  letter  “f”  indicates  that  the  value  is  a  “flo,at”.
2.  Do,ule  –  pro,grammers  use  the  term  “do,ule-precisio,n  real  integer”  when  referring  to,  this  sutype.  Its  default  value  is  0.0d  (i.e.  The  letter  “d”  at  the  end  is  no,t  case-sensitive.).  C#  auto,matically  tags  real  numers  as  “do,ule”  so,  yo,u  do,n’t  really  need  to,  add  “d”  at  the  end  o,f  the  value.

Real  type  –  decimals

This  pro,gramming  language  suppo,rts  “decimal  arithmetic”,  a  mathematical  appro,ach  that  uses  decimal  values  to,  represent  numers.  This  appro,ach  preserves  its  accuracy  regardless  o,f  the  values  it  wo,rks  o,n.

C#  uses  the  “decimal”  data  type  to,  represent  this  kind  o,f  real  numer.  This  data  type  is  128  its  lo,ng  and  is  accurate  up  to,  the  29^(th)  decimal  value.  Ecause  o,f  its  excellent  accuracy,  these  are  used  y  pro,grammers  fo,r  financial  co,mputatio,ns  (e.g.  Payments,  taxes,  interest,  etc.).

Integers

This  data  type  co,nsists  o,f  8  sutypes,  which  are:

  syte  –  an  syte  is  a  signed  integer  that  is  8  its  lo,ng.  That  means  it  can  co,ntain  up  to,  256  values  (i.e.  2⁸).  Additio,nally,  sytes  can  e  either  negative  o,r  po,sitive.

  yte  –  this  sutype  co,ntains  unsigned  integers  that  are  8  its  lo,ng.  It  is  almo,st  identical  to,  syte.  The  o,nly  difference  is  that  yte  can  never  e  negative.

  sho,rt  –  these  integers  are  signed  and  16-its  lo,ng.

  usho,rt  –  these  are  signed  integers  who,se  length  is  16  its.

  int  –  this  is  pro,aly  the  mo,st  po,pular  data  type  in  c#.  Pro,grammers  use  this  data  type  ecause  it  is  perfectly  co,mpatile  with  32-it  pro,cesso,rs  and  ig  eno,ugh  fo,r  typical  co,mputatio,ns.  It  is  a  signed  integer  who,se  length  is  32  its.

  uint  –  this  32-it  integer  is  unsigned.  Thus,  it  can  o,nly  e  po,sitive.

  lo,ng  –  this  integer  is  64  its  lo,ng.  It  can  e  either  po,sitive  o,r  negative.

  ulo,ng  –  this  is  similar  to,  “lo,ng”  integers.  The  o,nly  difference  is  that  “ulo,ng”  can  o,nly  assume  po,sitive  values.

Strings

A  string  is  a  set  o,r  sequence  o,f  characters.  C#  requires  yo,u  to,  use  “string”  (i.e.  A  keywo,rd)  when  declaring  values  that  elo,ng  to,  this  data  type.  Yo,u  have  to,  write  each  string  etween  a  pair  o,f  quo,tatio,n  marks.  This  language  allo,ws  yo,u  to,  perfo,rm  vario,us  o,peratio,ns  o,n  strings  (e.g.  Co,ncatenatio,n,  character  replacement,  character  search,  etc.).

The  sizeo,f()  metho,d  allo,ws  us  to,  kno,w  the  size  o,f  a  variale  o,r  data  type.  The  size  is  returned  in  the  fo,rm  o,f  ytes.  Co,nsider  the  fo,llo,wing  example^(103):

Using  system;

Namespace  typeapp  {

Class  inttype  {

Static  vo,id  main(string[]  args)  {

Co,nso,le.writeline("size  o,f  int:  {0}",  sizeo,f(int));

Co,nso,le.readline();

}

}

}

The  co,de  sho,uld  return:

![00179.jpg](images/00179.jpeg)

Which  means  that  an  integer  takes  a  sto,rage  size  o,f  4  ytes?

## Chapter  4:  wo,rking  with  variales

Yo,u  can  use  a  variale  to,  sto,re,  retrieve,  and  mo,dify  changeale  data.  As  a  pro,grammer,  yo,u  need  to,  use  variales^(104)  in  sto,ring  and  pro,cessing  info,rmatio,n.

The  characteristics  o,f  a  variale

A  variale  has  the  fo,llo,wing  characteristics:

●  name  (also,  kno,wn  as  “identifier”)

●  data  type

●  value  (i.e.  The  info,rmatio,n  yo,u  want  to,  sto,re).

Variales  are  sectio,ns  o,f  co,mputer  memo,ry  that  have  a  name.  They  sto,re  values  and  allo,w  a  co,mputer  pro,gram  to,  access  their  co,ntents.  Yo,u  may  place  a  variale  inside  the  stack  (i.e.  The  wo,rking  memo,ry  o,f  yo,ur  co,mputer  pro,gram)  o,r  within  the  pro,gram’s  dynamic  memo,ry.

Characters,  o,o,leans,  and  integers  are  kno,wn  as  value  types  since  they  keep  their  data  within  the  pro,gram’s  stack.  O,n  the  o,ther  hand,  strings,  arrays,  and  o,jects  are  kno,wn  as  “reference  types”  ecause  they  do,n’t  ho,ld  the  values  inside  them.  Instead,  they  serve  as  markers  that  po,int  to,  the  part  o,f  co,mputer  memo,ry  where  the  data  is  sto,red.

Ho,w  to,  name  a  variale

Yo,u  need  to,  name  yo,ur  variales  efo,re  using  them.  The  variale’s  name  serves  as  an  identifier:  it  helps  the  pro,gram  in  lo,cating  and  specifying  the  variale.  C#  allo,ws  yo,u  to,  cho,o,se  variale  names  freely.  Ho,wever,  just  like  any  o,ther  language,  c#  has  so,me  rules  regarding  variale  names.  These  rules  are  as  fo,llo,ws:

●  yo,u  may  use  an  undersco,re  (i.e.  “_”),  letters,  and  numers  to,  create  a  variale  name.

●  yo,u  can’t  use  a  numer  to,  start  the  name.  Thus,  firstsample  is  valid  while  1stsample  is  no,t.  Camelcase  fo,r  lo,cal  variales,  such  as  co,st,  o,rderdetail,  dateo,firth,  and  firstname

●  yo,u  can’t  use  c#  keywo,rds  in  naming  yo,ur  variales.  This  simple  rule  prevents  co,mpilatio,n  and  runtime  erro,rs  in  yo,ur  pro,grams.  If  yo,u  really  want  to,  use  keywo,rds  fo,r  yo,ur  variales,  yo,u  may  egin  the  name  using  the  “”  symo,l  (e.g.  O,o,l,  int,  char,  etc.).

●  a  meaningful  o,r  descriptive  name  that  is  neither  to,o,  lo,ng  no,r  to,o,  sho,rt  to,  identify  the  info,rmatio,n  sto,red  in  a  variale  just  y  lo,o,king  at  it

●  can  co,ntain  the  letters  a–z  and  a–z,  the  numers  0–9,  and  the  undersco,re  (_)  character—o,ther  symo,ls  are  no,t  allo,wed

●  no,  spaces  and  canno,t  start  with  a  numer

Valid  names

●  co,st,  name,  o,rder,  o,rder1,  _o,rder1,  inco,me

●  o,rder_detail,  o,rderdetail,  dateo,firth,  ho,urlyrate,  firstname,  first_name,  isvalid

Invalid  names

●  1  (numer)

●  class,  while,  if,  pro,tected  (keywo,rd)

●  1o,rder,  1name  (starts  with  a  numer)

Ho,w  to,  declare  a  variale

Yo,u  sho,uld  declare  a  variale  efo,re  using  it.  When  declaring  a  variale:

1.  Specify  the  variale’s  data  type  (e.g.  Char)
2.  Specify  the  variale’s  name  (e.g.  Sample)
3.  Set  the  variale’s  initial  value.  This  step  is  co,mpletely  o,ptio,nal.

The  fo,rmat  fo,r  variale  declaratio,ns  is:

Data_type  name  =  initial_value;

Here  are  so,me  samples  o,f  valid  variale  declaratio,ns:

Int  year  =  2000;

String  =  yo,urname;

Char  =  test;

Impo,rtant  no,te:  yo,u  need  to,  end  yo,ur  each  o,f  yo,ur  c#  statements  using  a  semico,lo,n.  If  yo,u’ll  fo,rget  to,  add  even  a  single  semico,lo,n  character,  yo,ur  pro,grams  will  generate  undesirale  and/o,r  unexpected  results.

Ho,w  to,  assign  a  value

Just  like  any  o,ther  co,mputer  language,  c#  allo,ws  yo,u  to,  assign  a  value  to,  a  variale.  This  pro,cess,  kno,wn  as  “value  assignment”,  requires  yo,u  to,  use  the  equals  sign.  Pro,grammers  refer  to,  this  symo,l  as  the  “assignment  o,perato,r”.  Write  the  variale’s  name  o,n  the  left  side  o,f  the  o,perato,r.  Then,  specify  the  value  yo,u  want  to,  assign  o,n  the  o,ther  side.  Check  the  fo,llo,wing  examples:

Test  =  x;

Yo,urname  =  “jo,hn  do,e”;

Ho,w  to,  initialize  a  variale

In  pro,gramming,  “initializatio,n”  is  the  pro,cess  o,f  assigning  a  value  to,  a  new  variale.  Thus,  yo,u’ll  set  this  “initial  value”  while  declaring  a  variale.

The  default  value  o,f  a  variale^(105)

If  yo,u  wo,n’t  assign  any  value  fo,r  yo,ur  variale,  c#  will  perfo,rm  an  auto,mated  initializatio,n  (i.e.  It  will  assign  a  default  value  to,  the  empty  variale).  The  fo,llo,wing  tales  will  sho,w  yo,u  the  default  value  o,f  each  data  type:

![00048.jpg](images/00048.jpeg)

The  co,de  given  elo,w  will  sho,w  yo,u  ho,w  to,  declare  variales  and  assign  values.

//  this  is  an  example

Yte  years  =  10;

Sho,rt  days  =  31;

Decimal  pi  =  3.14;

O,o,l  isittasty  =  true;

Char  sample  =  x;

String  animal  =  “do,g”;

Impo,rtant  no,te:  lines  that  egin  with  two,  fo,rward  slashes  (i.e.  //)  are  “co,mments”.  In  pro,gramming,  co,mments  are  descriptive  text  added  to,  the  co,de  to,  impro,ve  its  readaility.  Language  co,mpilers  igno,re  these  lines.  Thus,  co,mments  wo,n’t  affect  the  functio,nality  o,f  yo,ur  co,mputer  pro,grams.

Creating  an  identifier

If  yo,u  lo,o,k  thro,ugh  so,me  o,f  the  suggestio,ns  that  co,me  with  micro,so,ft,  yo,u  will  find  that  they  will  reco,mmend  that  yo,u  use  a  camel  no,tatio,n  when  yo,u  are  wo,rking  with  the  variales,  and  it  will  reco,mmend  that  yo,u  wo,rk  with  the  pascal  no,tatio,n  when  yo,u  want  to,  wo,rk  with  the  metho,ds.  Wo,rking  with  the  camel  no,tatio,n  will  mean  that  yo,u  will  keep  the  first  letter  o,f  yo,ur  name  as  lo,wer  case.  If  yo,u  are  creating  an  identifier  that  has  a  co,mpo,und  wo,rd  then  yo,u  will  make  sure  that  the  first  letter  o,f  yo,ur  seco,nd  wo,rd  will  start  with  an  uppercase  letter:

Payment  co,mpletepayment

Mathematics  firstclass

The  pascal  no,tatio,n  will  take  things  a  it  differently.  This  no,tatio,n  style  requires  yo,u  to,  start  the  first  wo,rd  using  an  uppercase  letter.  The  first  letter  in  all  o,f  the  o,ther  wo,rds  in  the  sequence  sho,uld  also,  e  written  in  uppercase  as  well.  So,me  examples  o,f  using  the  pascal  no,tatio,n  include:

Writeline()  readline()

Start()  main()

When  it  co,mes  to,  naming  these  identifiers,  yo,u  can  wo,rk  with  numers  and  undersco,res  as  well.  Ut,  if  fo,r  so,me  reaso,n  yo,u  can’t  egin  the  name  o,f  these  identifiers  with  a  numer,  yo,u  can  write  o,ut  so,mething  like  seven  o,o,ks,  ut  yo,u  can’t  write  o,ut  ‘7o,o,ks.’

No,w,  these  no,tatio,ns  are  no,t  required,  and  yo,u  can  change  them  aro,und  as  much  as  yo,u  wo,uld  like.  Ut  this  is  co,nsidered  a  pro,per  co,ding  practice  if  yo,u’re  wo,rking  with  c#  so,  it  is  est  to,  fo,llo,w  these  rules  so,  the  co,de  will  wo,rk  exactly  the  way  that  yo,u  want  it.

As  yo,u  can  see,  c#  is  a  pretty  easy  language  to,  learn.  Yo,u  do,  no,t  need  to,  wo,rry  ao,ut  a  lo,t  o,f  rules  that  are  to,o,  co,mplicated  to,  rememer  like  the  o,ther  pro,gramming  languages,  and  yet  yo,u  will  still  have  a  lo,t  o,f  the  po,wer  and  the  flexiility  to,  get  the  mo,st  o,ut  o,f  co,ding.

Definite  assignment

C#  enfo,rces  a  definite  assignment  po,licy.  This  means  that  yo,u  will  need  to,  initialize  the  lo,cal  variale  with  the  value  efo,re  using  it.  Suppo,se  the  fo,llo,wing  is  written:

Co,nso,le.writeline(name);

Erro,r:  use  o,f  unassigned  lo,cal  variale  ‘name’

If  yo,u  try  to,  use  a  variale  that  hasn’t  een  declared,  yo,ur  co,de  wo,n’t  co,mpile.  In  this  case,  the  co,mpiler  will  tell  yo,u  that  so,mething  is  wro,ng.  Trying  to,  utilize  a  variale  minus  having  a  value  assigned  to,  it  also,  causes  an  erro,r.

In  o,rder  to,  initialize  the  variale  with  a  value,  yo,u  simply  have  to,  use  the  assignment  o,perato,r  “=”.  The  variale  name  is  lo,cated  to,  the  left  side  o,f  the  o,perato,r  and  o,n  the  right  side  is  the  value  in  the  fo,llo,wing  manner.

Name  =  "pirzada";  age  =  35;  weight  =  70;  ismarried  =  true;

O,n  declaring  a  variale  with  a  type,  it  canno,t  e  redeclared  with  a  new  type,  and  it  canno,t  e  assigned  a  value  that  is  no,t  co,mpatile  with  its  declared  type.  Fo,r  example,  yo,u  canno,t  declare  an  int  and  then  assign  it  a  o,o,lean  value  o,f  true/false.

Age  =  true;

Erro,r:  canno,t  implicitly  co,nvert  type  ‘o,o,l’  to,  ‘int’

If  i  try  to,  assign  a  string  to,  an  age  variale,  it  is  declared  an  int  datatype.

Age  =  "pirzada";

O,r

Age  =  name;

The  ao,ve  statement  will  give  a  co,mpile-time  erro,r  ecause  the  string  value  canno,t  e  assigned  to,  an  int  type  variale.

Yo,u  can  co,mine  the  declaratio,n  and  initializatio,n  statements  at  the  same  time  o,n  the  same  line  as  sho,wn  elo,w,  which  is  mo,re  co,nvenient.

String  name  =  "pirzada";  int  age  =  35;  int  weight  =  70;  o,o,l  ismarried  =  true;

Yo,u  can  also,  use  a  mathematical  expressio,n.

Int  wo,wexp  =  (3  +  2)  *  4;  co,nso,le.writeline(wo,wexp);

O,utput:

20

The  right  side  is  eing  evaluated  and  then  assigned  to,  the  variale  o,n  the  left.  Meaning  3+2  is  5  and  5  *  4  is  20,  which  will  e  assigned  to,  the  wo,wexp  variale.

Yo,u  can  also,  assign  the  same  value  to,  multiple  different  variales  all  at  the  same  time.

Int  a,  ,  c;  a  =  =  c  =  786;  co,nso,le.writeline(a);  co,nso,le.writeline();  co,nso,le.writeline(c);

O,utput:

786

786

786

Using  type  inference

C#  3.0  intro,duced  the  implicitly  typed  variale  with  the  var  keywo,rd.  No,w  yo,u  can  declare  a  lo,cal  variale  witho,ut  giving  an  explicit  o,r  real  type.  The  variale  still  receives  a  type  at  co,mpile  time,  ut  the  type  is  pro,vided  y  the  co,mpiler.

Actually,  the  var  keywo,rd  instructs  the  co,mpiler  to,  infer  the  type  o,f  variale  fro,m  the  expressio,n  o,n  the  right  side  o,f  the  initializatio,n  statement.  The  co,mpiler  is  given  the  task  to,  determine  and  assign  the  suitale  type.

Var  varialename  =  varialevalue;  //  syntax

Var  is  o,ptio,nal,  and  it’s  just  fo,r  co,nvenience.

Let’s  use  the  same  variales  as  ao,ve.

Var  name  =  "pirzada";  var  age  =  35;  var  weight  =  70;  var  ismarried  =  true;

No,w  the  variales  are  implicitly  typed  lo,cal  variales,  meaning  that  yo,u  do,n’t  have  to,  explicitly  specify  the  type.  The  co,mpiler  is  tasked  to,  determine  and  assign  the  suitale  type.  A  string  variale  is  indicated  y  do,ule  quo,tes,  char  variale  is  deno,ted  y  single  quo,tes,  and  a  o,o,l  type  is  deno,ted  y  true  and  false  values.

Suggestio,n:  using  var  is  co,nvenient,  ut  use  it  o,nly  when  the  type  is  o,vio,us  fro,m  the  right  side  o,f  the  assignment.

Do,ule  is  used  to,  deno,te  a  literal  numer  with  a  decimal  po,int  unless  yo,u  add  the  m/m  suffix  to,  indicate  a  decimal  variale  o,r  the  f/f  suffix  to,  indicate  flo,at  variale.

Var  value  =  24899.45m;  var  numer  =  20.8f;

To,  initialize  numer,  yo,u  need  to,  add  f  as  a  suffix  after  20.8  to,  explicitly  tell  the  co,mpiler  to,  change  20.8  to,  a  flo,at.  Similarly,  to,  initialize  value,  yo,u  need  to,  add  m  as  a  suffix  to,  change  24899.45  into,  a  decimal  type.

A  few  rules  yo,u  need  to,  fo,llo,w:

●  var  can  o,nly  e  declared  and  initialized  in  a  single  statement.  O,therwise,  the  co,mpiler  do,esn’t  have  anything  fro,m  which  to,  infer  the  type.

●  var  is  no,t  suppo,sed  to,  e  utilized  o,n  fields  at  class  sco,pe.

●  the  initializer  canno,t  e  null  and  must  e  an  expressio,n.

●  multiple,  implicitly  typed  variales  canno,t  e  initialized  in  the  same  statement.

●  an  o,ject  canno,t  e  initialized  unless  a  new  o,ject  is  created  in  the  initializer.

Default  value  expressio,ns

Default  value  expressio,ns  are  especially  useful  in  co,minatio,n  with  generic  types  when  yo,u  do,n’t  kno,w  in  advance  what  the  default  value  fo,r  the  given  type  will  e.

Default(t)  expressio,n:  o,ld  way

A  default  value  expressio,n  default(t)  returns  the  default  value  o,f  a  type  t,  where  t  is  a  reference  type  o,r  a  value  type.

T  varialename  =  default(t);  //  syntax

Example:

Var  name  =  default(string);  var  age  =  default(int);  var  weight  =  default(int);  var  ismarried  =  default(o,o,l);

Default  literal:  new  way

The  default  literal  is  a  new  feature  in  c#  7.1  that  is  used  to,  get  the  default  value  o,f  the  specified  data  type  when  the  statement  is  executed.  This  feature  wo,rks  fo,r  value  types  as  well  as  reference  types.

No,te:  default  literal  is  equivalent  to,  default(t)  where  t  is  the  inferred  type.

String  name  =  default;  int  age  =  default;  int  weight  =  default;  o,o,l  ismarried  =  default;  co,nso,le.writeline(name);  co,nso,le.writeline(age);  co,nso,le.writeline(weight);  co,nso,le.writeline(ismarried);

In  the  o,utput  elo,w,  a  null  value  is  printed  as  a  lank  line.

O,utput  fo,r  default  literal  &  default(t):

0  0  false

New  o,perato,r:

Using  the  new  o,perato,r  invo,kes  the  default  co,nstructo,r  o,f  a  value  type.  This  allo,ws  yo,u  to,  create  a  variale  using  the  new  keywo,rd,  which  auto,matically  sets  the  variale  to,  its  default  value.

No,te:  all  values  in  c#  are  an  instance  o,f  a  specific  type.

Var  age  =  new  int();  var  ismarried  =  new  o,o,l();  co,nso,le.writeline(age);  co,nso,le.writeline(ismarried);

O,utput:

0

False

## Chapter  5:  what  is  type  co,nversio,n?

In  general,  an  o,perato,r  wo,rks  o,n  arguments  that  elo,ng  to,  the  same  type.  Ho,wever,  the  c#  language  o,ffers  a  wide  range  o,f  data  types  that  yo,u  can  use  fo,r  certain  situatio,ns.  To,  co,nduct  any  pro,cess  o,n  variales  that  elo,ng  to,  different  types,  yo,u  sho,uld  co,nvert  o,ne  o,f  tho,se  variales  first.  In  c#,  data  type  co,nversio,n^(106)  can  e  implicit  o,r  explicit.

Each  c#  expressio,n  has  a  data  type.  This  data  type  results  fro,m  the  literals,  variales,  values,  and  structures  used  inside  the  expressio,n.  Asically,  yo,u  might  use  an  expressio,n  who,se  type  is  inco,mpatile  fo,r  the  situatio,n.  When  this  happens,  yo,u’ll  get  o,ne  o,f  these  results:

●  the  pro,gram  will  give  yo,u  a  co,mpile-time  erro,r.

●  the  pro,gram  will  perfo,rm  an  auto,mated  co,nversio,n.  That  means  the  pro,gram  will  get  the  right  expressio,n  type.

Co,nverting  an  “s”  type  to,  “t”  type  allo,ws  yo,u  to,  treat  “s”  as  “t”  while  running  yo,ur  pro,gram.  So,metimes,  this  pro,cess  requires  the  pro,grammer  to,  validate  the  type  co,nversio,n.  Check  the  examples  elo,w:

●  co,nverting  “o,jects”  to,  “strings”  will  need  verificatio,n  during  the  pro,gram’s  runtime.  This  verificatio,n  ensures  that  yo,u  really  want  to,  use  the  values  as  strings.

●  co,nverting  “string”  values  to,  “o,ject”  values  do,esn’t  need  any  validatio,n.  That’s  ecause  the  “string”  type  is  a  ranch  o,f  the  “o,ject”  type.  Yo,u  can  co,nvert  strings  to,  their  “parent”  class  witho,ut  lo,sing  data  o,r  getting  any  erro,r.

●  yo,u  wo,n’t  have  to,  perfo,rm  verificatio,n  while  co,nverting  int  values  to,  lo,ng  values.  The  “lo,ng”  data  type  co,vers  all  o,f  the  po,ssile  values  o,f  the  “int”  type.  That  means  the  data  can  e  transfo,rmed  witho,ut  any  erro,r.

●  co,nverting  “do,ule”  values  to,  “lo,ng”  values  invo,lves  validatio,n.  Yo,u  might  experience  lo,ss  o,f  data,  depending  o,n  the  values  yo,u’re  wo,rking  o,n.

Impo,rtant  no,te:  c#  has  certain  restrictio,ns  when  it  co,mes  to,  changing  data  types.  Here  are  the  po,ssile  type  co,nversio,ns  suppo,rted  y  this  language:

Explicit  co,nversio,n

Use  this  co,nversio,n  if  there’s  a  chance  o,f  info,rmatio,n  lo,ss.  Fo,r  instance,  yo,u’ll  experience  info,rmatio,n  lo,ss  while  co,nverting  flo,ating-po,int  values  to,  integer  values  (i.e.  The  fractio,nal  sectio,n  will  disappear).  Yo,u  might  also,  lo,se  so,me  data  while  co,nverting  a  wide-range  type  to,  a  narro,w-range  type  (e.g.  Lo,ng-to,-int  co,nversio,n,  do,ule-to,-flo,at  co,nversio,n,  etc.).  To,  co,mplete  this  pro,cess,  yo,u  need  to,  use  the  “type”  o,perato,r.  Check  the  examples  elo,w:

Class  example

{

Static  vo,id  main()

{

Do,ule  yo,urdo,ule  =  2.1d;

System.co,nso,le.writeline(yo,urdo,ule);

Lo,ng  yo,urlo,ng  =  (lo,ng)yo,urdo,ule;

System.co,nso,le.writeline(yo,urlo,ng);

Yo,urdo,ule  =  2e9d;

System.co,nso,le.writeline(yo,urdo,ule);

Int  yo,urint  =  (int)yo,urdo,ule;

System.co,nso,le.writeline(yo,urint);

}

}

If  co,mpiled  and  executed  co,rrectly,  that  pro,gram  will  give  yo,u  these  results:

![00063.jpg](images/00063.jpeg)

Implicit  co,nversio,n^(107)

Yo,u  can  o,nly  perfo,rm  this  co,nversio,n  if  data  lo,ss  is  impo,ssile.  This  co,nversio,n  is  referred  to,  as  implicit  ecause  it  do,esn’t  require  any  o,perato,r.  The  c#  co,mpiler  will  perfo,rm  implicit  co,nversio,n  whenever  yo,u  assign  narro,w-range  values  to,  variales  that  have  a  wide-range.

String  co,nversio,n

C#  allo,ws  yo,u  to,  co,nvert  any  data  type  to,  “string”.  The  co,mpiler  will  perfo,rm  this  co,nversio,n  pro,cess  auto,matically  if  yo,u  will  use  “+”  and  at  least  o,ne  no,n-string  argument.  Here,  the  no,n-string  argument  will  eco,me  a  string  and  the  “+”  o,perato,r  will  pro,duce  a  new  value.

The  implicit  type  co,nversio,n  is  perfo,rmed  to,  do,  actio,ns  like  co,nversio,ns  that  are  fro,m  a  ase  class  to,  a  derived  class.  These  are  perfo,rmed  in  what  is  referred  to,  as  a  “type  safe”  manner.  The  o,ther  type  o,f  co,nversio,n,  explicit,  require  a  cast  o,perato,r  in  o,rder  to,  co,mplete  their  functio,n.  There  are  16  different  functio,ns  within  c#  that  are  ale  to,  e  used  as  a  uilt  in  type  o,f  the  co,nversio,n  metho,ds.  Here  are  so,me  examples  yo,u  sho,uld  practice  eco,ming  familiar  with  within  the  c#  enviro,nment.

●  to,char-  allo,ws  yo,u  to,  take  a  type  and  co,nvert  it  to,  a  single  unico,de  character

●  to,yte-  allo,ws  yo,u  to,  get  a  yte  y  co,nverting  it  fro,m  a  type

●  to,datetime-  allo,ws  yo,u  to,  get  a  date  time  structure  y  co,nverting  a  type  (either  string  o,r  integer)

●  to,o,o,lean-  allo,ws  yo,u  to,  get  a  o,o,lean  value  fro,m  co,nverting  a  type

●  to,do,ule-  allo,ws  yo,u  to,  get  a  do,ule  type  fro,m  co,nverting  a  type

●  to,decimal-  allo,ws  yo,u  to,  get  either  an  integer  o,r  decimal  type  co,nverted  fro,m  a  flo,ating  po,int

●  to,int64-  allo,ws  a  64  it  integer  to,  e  co,nverted  fro,m  a  type

●  to,int32-  allo,ws  a  32  it  integer  to,  e  co,nverted  fro,m  a  type

●  to,int16-  allo,ws  a  16  it  integer  to,  e  co,nverted  fro,m  a  type

●  to,syte-  allo,ws  a  signed  yte  type  to,  e  co,nverted  fro,m  a  type

●  to,string-  allo,ws  a  string  to,  e  co,nverted  fro,m  a  type

●  to,single-  allo,ws  a  small,  flo,ating  po,int  numer  to,  e  co,nverted  fro,m  a  type

●  to,uint64-  allo,ws  an  unsigned  it  integer  to,  e  co,nverted  fro,m  a  type

●  to,uint32-  allo,ws  an  unsigned  lo,ng  type  to,  e  co,nverted  fro,m  a  type

●  to,uint16-  allo,ws  an  unsigned  int  type  to,  e  co,nverted  fro,m  a  type

●  to,type-  allo,ws  a  specified  type  to,  e  co,nverted  fro,m  a  type

Fo,r  yo,ur  exercise  to,day,  i  enco,urage  yo,u  to,  go,  find  pro,gramming  that  do,es  each  and  every  o,ne  o,f  these  functio,ns/co,nversio,ns  in  o,rder  to,  get  mo,re  familiar  with  what  they  invo,lve  and  ho,w  they  can  assist  yo,u  in  yo,ur  o,wn  pro,gramming.

Rememer  that  altho,ugh  yo,ur  co,ding  may  e  lo,ng,  yo,ur  o,utput  will  e  sho,rt—ut  sho,uld  always  pro,duce  the  answer  yo,u  were  trying  to,  achieve  fro,m  the  co,ding  in  questio,n  that  yo,u  have  do,ne.

## Chapter  6:  the  need  fo,r  o,perato,rs

In  this  chapter,  we  will  take  so,me  time  to,  talk  ao,ut  the  o,perato,rs^(108)  that  yo,u  can  wo,rk  with  inside  the  c#  language.

Y  reading  this  material,  yo,u’ll  kno,w  ho,w  these  o,perato,rs  wo,rk  and  ho,w  yo,u  can  use  them  in  yo,ur  so,urce  co,des.  These  o,perato,rs  are  pretty  simple  to,  understand  and  use  ut  this  do,esn’t  mean  they’re  useless,  in  fact,  they  can  help  make  sure  that  yo,ur  co,de  will  perfo,rm  the  tasks  that  yo,u  require  it  to,  co,mplete.  Witho,ut  using  so,me  o,f  these  o,perato,rs,  yo,ur  pro,gram  will  lack  functio,nality,  and  wo,n’t  wo,rk  all  that  well.  These  o,perato,rs  may  e  simple  to,  understand,  ut  they  really  add  a  to,n  o,f  po,wer  to,  enhance  the  o,verall  capaility  o,f  yo,ur  co,de.

O,perato,rs  are  impo,rtant  no,  matter  which  type  o,f  co,ding  language  that  yo,u  are  wo,rking  with.  We  will  go,  into,  detail  o,n  the  different  o,perato,rs  separately  so,  that  yo,u  can  understand  ho,w  each  o,ne  is  suppo,sed  to,  wo,rk  and  ho,w  yo,u  can  wo,rk  with  each  o,ne  to,  fulfill  a  variety  o,f  purpo,ses  and  acco,mplish  different  tasks.

O,perato,rs  –  the  asics

O,perato,rs  help  yo,u  in  pro,cessing  o,jects  and  data  types.  They  accept  inputs  and  o,perands  to,  pro,duce  a  result.  The  c#  language  uses  special  characters  (e.g.  “.”,  “+”,  “^”,  etc.)  As  o,perato,rs.  Also,,  c#  co,des  can  take  up  to,  three  different  o,perands.

The  different  types  o,f  o,perato,rs

C#  pro,grammers  divide  o,perato,rs  into,  the  fo,llo,wing  types:

Assignment  o,perato,r

While  there  are  so,me  o,ther  o,ptio,ns  that  yo,u  can  go,  with  when  it  co,mes  to,  wo,rking  with  the  assignment  o,perato,rs,  this  is  the  mo,st  co,mmo,n  way  that  yo,u  will  use  these  o,perato,rs.  In  additio,n,  there  are  a  few  different  types  o,f  assignment  o,perato,rs  that  yo,u  can  wo,rk  with,  ut  the  mo,st  co,mmo,n  o,ne  is  the  equal  sign.  So,me  o,f  the  o,perato,rs  that  yo,u  can  to,  wo,rk  with  inside  o,f  yo,ur  c#  co,de  includes  the  fo,llo,wing:

●  =

The  functio,n  o,f  this  o,perato,r  is  to,  allo,w  yo,u  to,  perfo,rm  simple  assignment  o,peratio,ns.  It  can  assign  the  value  to,  a  variale  that  yo,u  are  wo,rking  o,n  at  that  time.  Fo,r  example,  writing  int  sample  =  100  will  tell  the  pro,gram  that  yo,u  want  to,  assign  100  to,  the  variale  that  is  called  ‘sample.’  it  wo,n’t  perfo,rm  any  additio,nal  tasks  o,n  this  variale  o,r  o,n  the  value  invo,lved.

●  +=

This  is  the  additive  assignment  o,perato,r.  Its  functio,n  is  to,  add  up  the  values  o,f  yo,ur  two,  o,perands  and  then  assign  the  sum  to,  yo,ur  left-hand  o,perand.

●  -=

Pro,grammers  will  o,ften  refer  to,  this  as  the  ‘sutractive’  assignment  o,perato,r.  Its  functio,n  is  to,  sutract  the  value  o,f  the  o,perand  o,n  the  right  side  fro,m  the  o,ne  o,n  the  left  side  and  then  assign  the  difference  to,  the  left-hand  o,perand.

●  *=

The  functio,n  o,f  this  o,perato,r  is  to,  multiply  the  values  o,f  each  o,perand  and  then  assign  the  pro,duct  to,  the  left-hand  o,perand.

●  /=

The  functio,n  o,f  this  o,perato,r  is  to,  divide  up  the  two,  variales  and  then  take  the  result  and  assign  it  to,  the  variale  o,n  the  left.

When  yo,u  are  wo,rking  with  the  assignment  o,perato,rs,  make  sure  that  yo,u  have  o,th  o,perands  that  elo,ng  to,  the  same  type  o,f  data.  If  yo,u  find  that  the  vario,us  o,perands  yo,u  are  using  are  no,t  co,mpatile,  so,me  issues  co,uld  arise  which  can  result  in  an  erro,r  in  the  pro,gram  if  yo,u  try  to,  execute  it  and  will  require  additio,nal  time  and  effo,rt  to,  fix.

In  c#,  yo,u  need  to,  use  the  equals  sign  (i.e.  =)  to,  assign  values.  Here’s  the  syntax  that  yo,u  need  to,  use  when  assigning  a  value:

Name_o,f_o,perand  =  expressio,n,  literal,  o,r  seco,nd_o,perand

Here  are  so,me  examples:

Int  y  =  99;

String  hello,  =  “go,o,d  mo,rning.”;

Char  sample  =  ‘z’;

Impo,rtant  no,te:  c#  allo,ws  yo,u  to,  cascade  (i.e.  Use  several  times  within  a  single  expressio,n)  the  assignment  o,perato,r.  That  means  yo,u  wo,n’t  have  to,  enter  multiple  equals  signs  if  yo,u  are  creating  variales  o,f  the  same  data  type.  The  examples  given  elo,w  will  illustrate  this  rule:

Int  d  =  1,  e  =  2,  f  =  3;

String  hi  =  “go,o,d  mo,rning.”,  ye  =  “farewell.”,  thanks  =  “thank  yo,u.”;

Lo,gical  o,perato,rs

A  lo,gical  (also,  kno,wn  as  “o,o,lean”)  o,perato,r  accepts  and  returns  o,o,lean  values  (i.e.  True  o,r  false).  Here  are  the  fo,ur  lo,gical  o,perato,rs  o,f  c#:

●  “&&”  –  pro,grammers  refer  to,  this  o,perato,r  as  “lo,gical  and”.  It  will  give  yo,u  “true”  if  o,th  o,f  the  o,perands  are  true.

●  “^”  –  this  is  kno,wn  as  the  “exclusive  o,r”  o,perato,r.  It  will  give  yo,u  true  if  o,ne  o,f  the  o,perands  is  true.

●  “||”  –  this  is  the  “lo,gical  o,r”  o,perato,r.  Yo,u  will  get  true  if  at  least  o,ne  o,f  the  o,perato,rs  is  true.

●  “!”  –  this  o,perato,r,  kno,wn  as  the  “lo,gical  negatio,n”  o,perato,r,  reverses  the  value  o,f  an  o,perand.

Study  the  co,de  to,  understand  the  use  o,f  these  o,perato,rs^(109):

Class  test

{

Static  vo,id  main()

{

O,o,l  x  =  true,  y  =  false;

System.co,nso,le.writeline(x  &&  y);

System.co,nso,le.writeline(x  ||  y);

System.co,nso,le.writeline(!X);

System.co,nso,le.writeline(x  ^  y);

//  this  is  an  example.

}

}

O,nce  yo,u  have  co,mpiled  and  run  this  co,de,  yo,u  will  see  the  fo,llo,wing  results:

![00022.jpg](images/00022.jpeg)

Arithmetic  o,perato,rs

These  o,perato,rs  help  yo,u  in  perfo,rming  math  o,peratio,ns.  This  catego,ry  co,nsists  o,f  the  fo,llo,wing  o,perato,rs:

●  “+”  –  use  this  o,perato,r  to,  perfo,rm  additio,n  using  two,  o,perands  to,gether  o,r  values  (e.g.  Int  x  =  1  +  1)

●  “-”  –  this  o,perato,r  allo,ws  yo,u  to,  perfo,rm  sutractio,n  in  yo,ur  co,des.  It  deducts  the  value  o,f  the  right  o,perand  fro,m  that  o,f  the  left  o,perand  (e.g.  Int  x  =  2  –  1)

●  “*”  –  with  this  o,perato,r,  yo,u  can  multiply  the  values  o,f  two,  o,perands  (e.g.  Int  r  =  6  *  6)

●  “/”  –  use  this  o,perato,r  to,  divide  numer  values  in  yo,ur  c#  co,des.  Asically,  “/”  divides  the  value  o,f  the  left-hand  o,perand  y  that  o,f  the  right-hand  o,perand.

●  “++”  –  this  is  kno,wn  as  the  “increment  o,perato,r”.  It  increases  the  value  o,f  an  o,perand  y  o,ne.  Unlike  the  o,nes  discussed  ao,ve,  this  o,perato,r  wo,rks  o,n  a  single  o,perand.  Also,,  yo,u  may  write  it  efo,re  o,r  after  the  o,perand.  (e.g.  99++,  1++,  ++5,  etc.)

●  “--”  –  this  o,perato,r  is  the  exact  o,ppo,site  o,f  the  increment  o,perato,r.  Yo,u  can  use  it  to,  decrease  an  o,perand’s  value  y  o,ne.  Yo,u  may  write  it  efo,re  o,r  after  the  o,perand  yo,u  want  to,  mo,dify.

●  “%”  -  this  is  o,ften  called  the  remainder  o,r  is  co,mmo,nly  kno,wn  as  the  ‘mo,dulo,’  o,perato,r.  Its  functio,n  is  to,  divide  the  left-hand  o,perand  y  the  right  o,perand  and  then  returns  the  remainder.

The  co,de  given  elo,w  will  sho,w  yo,u  ho,w  these  o,perato,rs  wo,rk:

Class  test

{

Static  vo,id  main()

{

Do,ule  d  =  100,  e  =  3;

System.co,nso,le.writeline(d  +  e);

System.co,nso,le.writeline(d  -  e);

System.co,nso,le.writeline(d  /  e);

System.co,nso,le.writeline(d  *  e);

System.co,nso,le.writeline(++d);

System.co,nso,le.writeline(--e);

//  this  is  an  example.

}

}

O,nce  yo,u  co,mpile  and  execute  that  co,de,  yo,u’ll  see  this  o,n  yo,ur  co,mmand  pro,mpt:

![00124.jpg](images/00124.jpeg)

Inary  o,perato,rs

These  o,perato,rs  wo,rk  o,n  inary  numers.  In  the  it  wo,rld,  all  o,f  the  info,rmatio,n  is  expressed  as  a  sequence  o,f  zero,s  and  o,nes.  That  means  yo,u  need  to,  master  inary  o,perato,rs  if  yo,u  want  to,  e  a  successful  pro,grammer.

A  inary  o,perato,r  wo,rks  exactly  like  a  lo,gical  o,ne.  Actually,  yo,u  may  think  that  inary  and  lo,gical  o,perato,rs  use  different  inputs  ut  co,nduct  the  same  pro,cesses.  A  lo,gical  o,perato,r  uses  o,o,lean  values  to,  pro,duce  results.  A  inary  o,perato,r,  o,n  the  o,ther  hand,  wo,rks  o,n  numers  presented  as  inary  digits.  Here  are  the  inary  o,perato,rs  yo,u’ll  enco,unter  while  using  c#:

●  “&”  –  this  is  called  “inary  and”.  It  indicates  the  po,sitio,n/s  where  o,th  o,f  the  o,perands  have  “1”.

●  “^”  –  pro,grammers  refer  to,  this  o,perato,r  as  “inary  exclusive  o,r”.  It  will  place  “1”  in  each  po,sitio,n  where  the  values  are  different.

●  “|”  –  this  is  the  “inary  o,r”  o,perato,r.  It  indicates  the  po,sitio,n/s  where  any  o,f  the  o,perands  has  “1”.

●  “~”  –  this  acts  as  the  negatio,n  o,perato,r  fo,r  inary  values.  Just  like  “!”,  it  reverses  the  current  value  o,f  a  variale.

●  “<<”  –  this  is  the  “inary  left  shift”  o,perato,r.  It  mo,ves  the  its  o,f  a  inary  numer  to,  the  left.  This  mo,vement  depends  o,n  the  value  that  yo,u’ll  assign  (e.g.  4  <<  1,  4  <<  3,  4  <<  2,  etc.).

Relatio,nal/co,mpariso,n  o,perato,rs

The  next  type  o,f  o,perato,r  that  yo,u  can  use  is  kno,wn  as  the  relatio,nal  o,perato,r.  These  o,perato,rs  are  very  useful  ecause  they  allo,w  yo,u  to,  co,mpare  the  values  o,f  two,  o,f  yo,ur  o,perands.  Each  o,f  these  o,perato,rs  gives  a  o,o,lean  value  as  the  final  o,utput.  Ecause  o,f  this  functio,n,  these  o,perato,rs  are  the  est  to,  use  when  yo,u  want  to,  create  so,me  co,nditio,nal  statements.  We  will  have  a  lo,o,k  at  so,me  o,f  the  relatio,nal  o,perato,rs  that  yo,u  can  wo,rk  with  to,  make  yo,ur  c#  co,de,  ut  fo,r  these  examples  assume  that  ‘e  =  150’  and  that  ‘d  =  100.’

●  “==”  –  this  is  the  equality  o,perato,r.  It  checks  whether  the  two,  o,perands  are  equal  (e.g.  X  ==  y).  The  functio,n  o,f  this  the  o,perato,r  is  to,  allo,w  yo,u  to,  check  the  equality  o,f  two,  values.  If  the  two,  values  end  up  eing  equal,  the  o,perand  will  tell  yo,u  it  is  true.  O,therwise,  the  o,perand  will  tell  yo,u  it  is  false.  Fo,r  example,  saying  the  d  ==  e  wo,uld  sho,w  up  as  false.

●  “>”  –  the  functio,n  o,f  this  o,perato,r  is  to,  check  whether  the  o,perand  o,n  the  left  is  greater  than  the  o,perand  o,n  the  right.  If  it  is,  then  the  o,perato,r  will  tell  yo,u  it  is  true.  Fo,r  example,  saying  that  e  >  d  wo,uld  e  true.

●  “<”  –  this  is  actually  less  than  an  o,perato,r,  it  allo,ws  yo,u  to,  check  whether  the  o,perand  o,n  the  left  side  is  less  than  the  o,perand  o,n  the  right  side.  It  will  give  yo,u  “true”  if  the  left-hand  o,perand’s  value  is  less  than  that  o,f  the  right-hand  o,perand  (e.g.  Y  <  x).

●  “>=”  –  with  this  o,perato,r,  yo,u  can  determine  whether  the  value  o,f  the  left-hand  o,perand  is  greater  than  o,r  equal  to,  that  o,f  the  right-hand  o,perand.  The  functio,n  o,f  this  o,perand  is  that  it  will  say  the  value  o,f  the  o,perand  o,n  the  left  side  is  truly  greater  than  o,r  equal  to,,  the  o,perand  o,n  the  right  side.  O,therwise,  it  will  tell  yo,u  the  statement  is  false.  Fo,r  example,  saying  that  e  >=d  evaluates  as  true.

●  “<=”  –  this  o,perato,r  will  give  yo,u  true  if  the  value  o,f  the  left-hand  o,perand  is  less  than  o,r  equal  to,  that  o,f  the  right-hand  o,perand.

●  “!=”  –  the  functio,n  o,f  this  o,perato,r  is  to,  allo,w  yo,u  to,  test  the  inequality  o,f  two,  values/o,perands.  If  the  values  end  up  no,t  eing  equal,  it  will  tell  yo,u  this  is  true.  Fo,r  example,  e  !=  d  wo,uld  result  in  the  o,perato,r  saying  it’s  true.

When  yo,u  are  wo,rking  with  these  relatio,nal  o,perato,rs,  always  rememer  that  yo,u  will  get  a  o,o,lean  result  each  time.  What  this  means  is  that  the  answer  yo,u  get  will  e  either  true  o,r  false.  Yo,u  also,  have  to,  check  if  yo,u  are  using  two,  equal  signs  when  yo,u  are  wo,rking  with  the  equality  o,perato,r.  If  yo,u  end  up  getting  these  o,perato,rs  mixed  up  with  yo,ur  assignment  o,perato,r,  yo,u  will  pro,aly  get  an  erro,r  message,  and  that  pro,gram  will  no,t  wo,rk  o,ut  the  way  that  yo,u  want.

Co,nditio,nal  o,perato,r

C#  users  refer  to,  “?”  As  the  co,nditio,nal  o,perato,r.  Asically,  this  o,perato,r  uses  the  result  o,f  a  o,o,lean  expressio,n  to,  determine  which  statement  sho,uld  e  pro,cessed.  This  is  called  “ternary  o,perato,r”  ecause  it  wo,rks  o,n  three  o,perands.  Here,  the  first  value  sho,uld  e  o,o,lean,  while  the  remaining  values  need  to,  elo,ng  to,  the  same  data  type  (e.g.  Characters,  strings,  numers,  etc.).

The  syntax  o,f  this  o,perato,r  is:

First_o,perand  ?  Seco,nd_o,perand  :  third_o,perand;

Here’s  ho,w  it  wo,rks:  if  “first_o,perand”  is  true,  the  pro,gram  will  wo,rk  o,n  “seco,nd_o,perand”.  If  “first_o,perand”  is  false,  ho,wever,  the  pro,gram  will  wo,rk  o,n  “third_o,perand”.

## Chapter  7:  the  co,nditio,nal  statements

C#  has  co,nditio,nal  statements,  mo,stly  used  fo,r  co,ntro,lling  the  flo,w  o,f  executio,n.  The  co,nditio,nal  statements  expect  the  pro,grammer  to,  specify  a  co,nditio,n  o,r  a  set  o,f  co,nditio,ns  and  the  co,rrespo,nding  set  o,f  statements  to,  e  executed  if  a  co,nditio,n  is  fo,und  to,  e  true.  The  pro,grammer  can  also,  specify  the  set  o,f  statements  that  are  to,  e  executed  if  the  co,nditio,n  is  no,t  true.

Let  us  discuss  the  vario,us  co,nditio,nal  statements  suppo,rted  in  c#.

If  statement

This  statement  is  used  to,  evaluate  a  o,o,lean  expressio,n  efo,re  a  set  o,f  statements  can  e  executed.  If  the  co,nditio,n  stands  true,  then  there  will  e  executio,n  o,f  o,ne  set  o,f  statements,  o,therwise,  ano,ther  set  o,f  statements  will  e  executed.  Here  is  the  syntax  fo,r  this  statement^(110):

If(o,o,lean_expressio,n)  {

/*  statement(s)  to,  execute  if  ao,ve  o,o,lean  expressio,n  is  true  */

}

Here  is  an  example:

Using  system;

Namespace  decisio,nmaking  {

Class  ifstatement  {

Static  vo,id  main(string[]  args)  {

/*  defining  a  lo,cal  variale  */

Int  x  =  5;

/*  check  a  o,o,lean  co,nditio,n  via  if  statement  */

If  (x  <  10)  {

/*  to,  e  printed  o,f  the  co,nditio,n  is  true  */

Co,nso,le.writeline("x  is  less  than  10");

}

Co,nso,le.writeline("the  value  o,f  x  is  :  {0}",  x);

Co,nso,le.readline();

}

}

}

The  co,de  returns  the  fo,llo,wing  o,utput:

![00016.jpg](images/00016.jpeg)

The  co,nditio,n  was  fo,und  to,  e  true,  that  is,  the  value  o,f  variale  x  is  less  than  10,  hence,  and  the  statement  just  elo,w  the  co,nditio,n  was  executed.  What  if  the  co,nditio,n  was  false?

Using  system;

Namespace  decisio,nmaking  {

Class  ifstatement  {

Static  vo,id  main(string[]  args)  {

/*  defining  a  lo,cal  variale  */

Int  x  =  15;

/*  check  a  o,o,lean  co,nditio,n  via  if  statement  */

If  (x  <  10)  {

/*  to,  e  printed  o,f  the  co,nditio,n  is  true  */

Co,nso,le.writeline("x  is  less  than  10");

}

Co,nso,le.writeline("the  value  o,f  x  is  :  {0}",  x);

Co,nso,le.readline();

}

}

}

The  co,de  returns  the  fo,llo,wing:

![00098.jpg](images/00098.jpeg)

The  co,nditio,n  was  fo,und  to,  e  false,  hence  the  statement  o,utside  its  lo,ck  was  executed.

If-else  statement

This  is  simply  a  co,minatio,n  o,f  an  if  statement  with  an  else  part.  The  if  part  is  executed  if  the  co,nditio,n  is  true,  while  the  else  part  is  executed  when  the  co,nditio,n  is  false.  The  two,  parts  canno,t  all  e  executed  at  o,nce.  Here  is  the  syntax  fo,r  the  statement:

If(o,o,lean_expressio,n)

{

//  co,de  executes  if  the  co,nditio,n  is  true.

}

Else

{

//  co,de  executed  if  the  co,nditio,n  is  false

}

Co,nsider  the  example  given  elo,w:

Using  system;

Namespace  decisio,nmaking  {

Class  ifelsestatement  {

Static  vo,id  main(string[]  args)  {

/*  defining  a  lo,cal  variale  */

Int  x  =  5;

/*  a  check  o,f  the  o,o,lean  co,nditio,n  */

If  (x  <  10)  {

/*  if  the  co,nditio,n  is  true,  the  fo,llo,wing  will  e  printed  */

Co,nso,le.writeline("x  is  less  than  10");

}  else  {

/*  if  the  co,nditio,n  is  false,  the  fo,llo,wing  will  e  printed  */

Co,nso,le.writeline("x  greater  than  10");

}

Co,nso,le.writeline("the  value  o,f  x  is  :  {0}",  x);

Co,nso,le.readline();

}

}

}

The  co,de  returns  the  fo,llo,wing:

![00115.jpg](images/00115.jpeg)

The  if  co,nditio,n  evaluated  to,  a  true,  hence  the  statement  within  its  lo,ck  has  een  executed.  What  if  the  co,nditio,n  was  false?

Using  system;

Namespace  decisio,nmaking  {

Class  ifelsestatement  {

Static  vo,id  main(string[]  args)  {

/*  defining  a  lo,cal  variale  */

Int  x  =  15;

/*  a  check  o,f  the  o,o,lean  co,nditio,n  */

If  (x  <  10)  {

/*  if  the  co,nditio,n  is  true,  the  fo,llo,wing  will  e  printed  */

Co,nso,le.writeline("x  is  less  than  10");

}  else  {

/*  if  the  co,nditio,n  is  false,  the  fo,llo,wing  will  e  printed  */

Co,nso,le.writeline("x  greater  than  10");

}

Co,nso,le.writeline("the  value  o,f  x  is  :  {0}",  x);

Co,nso,le.readline();

}

}

}

The  co,de  gives  the  fo,llo,wing  o,utput:

![00036.jpg](images/00036.jpeg)

The  if  co,nditio,n  evaluated  to,  a  false,  hence  the  statement  within  the  else  lo,ck  has  een  executed.  Yo,u  must  have  no,ticed  that  part  o,utside  the  two,  lo,cks  has  een  executed  in  o,th  cases.  That  is  what  happens.

Else…if  statement

In  so,me  cases,  we  may  e  in  need  o,f  checking  a  multiple  numer  o,f  co,nditio,ns.  In  such  a  case,  we  can  use  the  else  if  statement.  It  takes  the  syntax  given  elo,w:

If(o,o,lean_expressio,n  a)  {

/*  runs  if  the  o,o,lean  expressio,n  a  is  true  */

}

Else  if(  o,o,lean_expressio,n  )  {

/*  runs  if  the  o,o,lean  expressio,n  is  true  */

}

Else  if(  o,o,lean_expressio,n  c)  {

/*  runs  if  the  o,o,lean  expressio,n  c  is  true  */

}  else  {

/*  to,  run  if  no,ne  o,f  ao,ve  co,nditio,ns  is  true  */

}

Here  is  an  example:

Using  system;

Namespace  decisio,nmaking  {

Class  elseifstatement  {

Static  vo,id  main(string[]  args)  {

/*  defining  a  lo,cal  variale  */

Int  x  =  5;

/*  checking  the  o,o,lean  co,nditio,n  */

If  (x  ==  1)  {

/*  print  this  statement  if  the  co,nditio,n  is  true  */

Co,nso,le.writeline("value  o,f  x  is  1");

}

Else  if  (x  ==  2)  {

/*  print  this  statement  if  the  if  else  if  co,nditio,n  is  true*/

Co,nso,le.writeline("value  o,f  x  is  2");

}

Else  if  (x  ==  3)  {

/*  print  this  statement  if  the  if  else  if  co,nditio,n  is  true  */

Co,nso,le.writeline("value  o,f  x  is  3");

}  else  {

/*  print  this  statement  if  no,ne  o,f  the  ao,ve  co,nditio,ns  is  true  */

Co,nso,le.writeline("all  co,nditio,ns  are  false");

}

Co,nso,le.writeline("exact  value  o,f  x  is:  {0}",  x);

Co,nso,le.readline();

}

}

}

The  co,de  prints  the  fo,llo,wing  result:

![00080.jpg](images/00080.jpeg)

All  the  co,nditio,ns  were  fo,und  to,  e  false;  hence  the  lo,ck  o,f  co,de  o,utside  the  co,nditio,ns  has  een  executed.  Let  us  set  the  value  o,f  variale  x  to,  2  and  see  what  happens  with  the  co,de:

Using  system;

Namespace  decisio,nmaking  {

Class  elseifstatement  {

Static  vo,id  main(string[]  args)  {

/*  defining  a  lo,cal  variale  */

Int  x  =  2;

/*  checking  the  o,o,lean  co,nditio,n  */

If  (x  ==  1)  {

/*  print  this  statement  if  the  co,nditio,n  is  true  */

Co,nso,le.writeline("value  o,f  x  is  1");

}

Else  if  (x  ==  2)  {

/*  print  this  statement  if  the  if  else  if  co,nditio,n  is  true*/

Co,nso,le.writeline("value  o,f  x  is  2");

}

Else  if  (x  ==  3)  {

/*  print  this  statement  if  the  if  else  if  co,nditio,n  is  true  */

Co,nso,le.writeline("value  o,f  x  is  3");

}  else  {

/*  print  this  statement  if  no,ne  o,f  the  ao,ve  co,nditio,ns  is  true  */

Co,nso,le.writeline("all  co,nditio,ns  are  false");

}

Co,nso,le.writeline("exact  value  o,f  x  is:  {0}",  x);

Co,nso,le.readline();

}

}

}

The  o,utput  is  sho,wn  elo,w:

![00070.jpg](images/00070.jpeg)

An  else  if  co,nditio,n  evaluated  to,  a  true  hence  the  statement  within  its  lo,ck  was  executed.  The  lo,ck  o,f  co,de  o,utside  all  the  co,nditio,ns  was  also,  executed.  Yo,u  can  play  aro,und  with  the  co,de  y  mo,difying  the  value  o,f  x  to,  vario,us  values  and  see  what  will  happen.

Nested  if  statements

C#  allo,ws  us  to,  nest  co,nditio,nal  statements.  We  can  nest  o,th  the  if  and  the  else  if  statements,  which  means  that  we  use  them  inside  ano,ther  if  o,r  else  if  statement.  The  fo,llo,wing  syntax  demo,nstrates  ho,w  we  nest  the  if  statement  in  c#:

If(  o,o,lean_expressio,n  a)  {

/*  to,  execute  if  the  o,o,lean  expressio,n  a  is  true  */

If(o,o,lean_expressio,n  )  {

/*  to,  execute  if  the  o,o,lean  expressio,n  is  true  */

}

}

The  else  if  statement  can  e  nested  using  the  syntax  given  ao,ve.

Co,nsider  the  example  given  elo,w:

Using  system;

Namespace  decisio,nmaking  {

Class  nestedif  {

Static  vo,id  main(string[]  args)  {

//*  defining  lo,cal  variales  */

Int  x  =  1;

Int  y  =  2;

/*  checking  the  o,o,lean  co,nditio,n  */

If  (x  ==  1)  {

/*  if  the  co,nditio,n  is  true,  check  the  if  co,nditio,n  elo,w  */

If  (y  ==  2)  {

/*  if  the  co,nditio,n  is  true,  print  the  fo,llo,wing  */

Co,nso,le.writeline("value  o,f  x  is  1  and  is  2");

}

}

Co,nso,le.writeline("exact  value  o,f  x  is  :  {0}",  x);

Co,nso,le.writeline("exact  value  o,f  y  is  :  {0}",  y);

Co,nso,le.readline();

}

}

}

The  co,de  returns:

![00017.jpg](images/00017.jpeg)

O,th  if  co,nditio,ns  evaluated  to,  a  true,  hence  the  statement  within  the  nested  if  were  executed.  If  either  o,r  o,th  co,nditio,ns  evaluated  to,  a  false,  then  this  statement  co,uld  no,t  have  een  executed.  Here  is  an  example:

Using  system;

Namespace  decisio,nmaking  {

Class  nestedif  {

Static  vo,id  main(string[]  args)  {

//*  defining  lo,cal  variales  */

Int  x  =  1;

Int  y  =  2;

/*  checking  the  o,o,lean  co,nditio,n  */

If  (x  ==  1)  {

/*  if  the  co,nditio,n  is  true,  check  the  if  co,nditio,n  elo,w  */

If  (y  ==  3)  {

/*  if  the  co,nditio,n  is  true,  print  the  fo,llo,wing  */

Co,nso,le.writeline("value  o,f  x  is  1  and  is  2");

}

}

Co,nso,le.writeline("exact  value  o,f  x  is  :  {0}",  x);

Co,nso,le.writeline("exact  value  o,f  y  is  :  {0}",  y);

Co,nso,le.readline();

}

}

}

In  the  ao,ve  co,de,  the  nested  if  co,nditio,n  checks  whether  the  value  o,f  variale  y  is  3,  which  is  false.  The  statement  within  this  lo,ck  will  no,t  e  executed.  The  c#  co,mpiler  will  skip  this  sectio,n  and  pro,ceed  to,  execute  the  co,de  o,utside  the  co,nditio,ns.  It  returns  the  fo,llo,wing:

![00144.jpg](images/00144.jpeg)

Switch  statement^(111)

This  statement  is  the  same  as  using  multiple  if  statements.  It  is  created  with  a  list  o,f  po,ssiilities,  an  actio,n  fo,r  every  po,ssiility  and  a  default  sectio,n  to,  e  executio,n  in  case  any  o,f  the  o,ptio,ns  do,esn’t  evaluate  to,  a  true.  Here  is  syntax  fo,r  this  statement:

Switch(expressio,n)

{

Case  <value_1>

//  co,de

Reak;

Case  <value_2>

//  co,de

Reak;

Case  <value_n>

//  co,de

Reak;

Default

//  co,de

Reak;

}

Here  is  an  example:

Using  system;

Pulic  class  switchstatement

{

Pulic  static  vo,id  main()

{

Int  a  =  3;

Switch  (a)

{

Case  1:

Co,nso,le.writeline("the  value  o,f  x  is  1");

Reak;

Case  2:

Co,nso,le.writeline("the  value  o,f  x  is  2");

Reak;

Case  3:

Co,nso,le.writeline("the  value  o,f  x  is  3");

Reak;

Default:

Co,nso,le.writeline("unkno,wn  value  o,f  x");

Reak;

}

}

}

The  co,de  returns  the  fo,llo,wing:

![00005.jpg](images/00005.jpeg)

The  value  o,f  variale  was  initialized  to,  3.  After  executing  the  co,de,  the  case  co,de  fo,r  3  will  e  matched,  hence  the  statement  within  its  lo,ck  will  e  executed.  If  no,ne  o,f  the  case  co,nditio,ns  is  true,  then  the  default  sectio,n  will  e  executed.  This  is  demo,nstrated  elo,w:

Using  system;

Pulic  class  switchstatement

{

Pulic  static  vo,id  main()

{

Int  a  =  5;

Switch  (a)

{

Case  1:

Co,nso,le.writeline("the  value  o,f  x  is  1");

Reak;

Case  2:

Co,nso,le.writeline("the  value  o,f  x  is  2");

Reak;

Case  3:

Co,nso,le.writeline("the  value  o,f  x  is  3");

Reak;

Default:

Co,nso,le.writeline("unkno,wn  value  o,f  x");

Reak;

}

}

}

The  co,de  returns  the  o,utput  given  elo,w:

![00034.jpg](images/00034.jpeg)

The  case  lael  within  the  switch  statement  has  to,  e  unique.  The  switch  statement  is  usale  with  expressio,ns  o,f  any  type  including  strings,  integers,  o,o,l,  char,  enum  rtc.  Here  is  ho,w  to,  use  it  with  a  string:

Using  system;

Pulic  class  switchstatement

{

Pulic  static  vo,id  main()

{

String  firstname  =  "nicho,las";

Switch  (firstname)

{

Case  "samuel":

Co,nso,le.writeline("yo,ur  first  name  is  samuel");

Reak;

Case  "nicho,las":

Co,nso,le.writeline("yo,ur  first  name  is  nicho,las");

Reak;

Case  "ismack":

Co,nso,le.writeline("yo,ur  first  name  is  ismack");

Reak;

}

}

}

The  co,de  returns  the  fo,llo,wing  o,utput:

![00158.jpg](images/00158.jpeg)

Go,to,  in  switch^(112)

In  so,me  cases  when  using  the  switch  statement,  we  may  need  to,  skip  to,  a  certain  case.  This  can  e  do,ne  using  either  a  jump  o,r  go,to,  statement.  Co,nsider  the  example  given  elo,w:

Using  system;

Pulic  class  switchstatement

{

Pulic  static  vo,id  main()

{

String  firstname  =  "nicho,las";

Switch  (firstname)

{

Case  "text":

Co,nso,le.writeline("is  yo,ur  first  name");

Reak;

Case  "samuel":

Co,nso,le.writeline("samuel");

Reak;

Case  "nicho,las":

Co,nso,le.writeline("nicho,las");

Go,to,  case  "text";

Reak;

Case  "ismack":

Co,nso,le.writeline("ismack");

Reak;

}

}

}

The  co,de  returns  the  fo,llo,wing  o,utput:

![00176.jpg](images/00176.jpeg)

Nested  switch

A  switch  statement  can  e  created  within  ano,ther  switch  statement.  This  gives  us  a  nested  switch.  Here  is  an  example:

Using  system;

Pulic  class  nestedswitch

{

Pulic  static  vo,id  main()

{

Int  x  =  10;

Switch  (x)

{

Case  10:

Co,nso,le.writeline(10);

Switch  (x  -  1)

{

Case  9:

Co,nso,le.writeline(9);

Switch  (x  -  2)

{

Case  8:

Co,nso,le.writeline(8);

Reak;

}

Reak;

}

Reak;

Case  20:

Co,nso,le.writeline(20);

Reak;

Case  125:

Co,nso,le.writeline(25);

Reak;

Default:

Co,nso,le.writeline(30);

Reak;

}

}

}

The  o,utput  is  as  fo,llo,ws:

## Chapter  8:  lo,o,ps

As  a  pro,grammer,  yo,u’ll  use  a  lo,o,p  statement  to,  run  certain  co,de  lo,cks  repeatedly.  Lo,o,ps  play  an  impo,rtant  part  in  c#  pro,gramming.  Hence,  yo,u  sho,uld  study  this  material  carefully  as  well  if  yo,u  want  to,  master  this  language  in  a  sho,rt  while.

Lo,o,ps  –  the  asics

While  creating  pro,grams,  yo,u  o,ften  need  to,  execute  co,de  sequences  multiple  times.  Typing  the  same  lo,cks  o,f  co,de  several  times  can  e  extremely  o,ring.  Thus,  yo,u  need  to,  find  a  quick  and  simple  way  to,  repeat  co,des.  Fo,rtunately,  the  c#  language  suppo,rts  lo,o,p  statements.

A  lo,o,p  is  a  to,o,l  that  runs  co,de  fragments  repeatedly.  Yo,u  can  use  it  to,  run  co,des  fo,r  a  certain  numer  o,f  times  o,r  as  lo,ng  as  a  given  co,nditio,n  is  fulfilled.  C#  o,ffers  different  types  o,f  lo,o,p  statements.  Let’s  analyze  each  type  in  detail:

The  while  lo,o,p^(113)

This  is  the  simplest  lo,o,p  statement  in  c#.  Its  syntax  is:

While  (the_assigned_co,nditio,n)

{

The_lo,o,p’s_o,dy;

}

In  this  syntax,  “the_assigned_co,nditio,n”  is  an  expressio,n  that  pro,duces  a  o,o,lean  value.  This  co,nditio,n  dictates  ho,w  many  times  the  “o,dy”  will  run.  The  “o,dy”,  o,n  the  o,ther  hand,  is  the  statement  (o,r  gro,up  o,f  statements)  that  yo,u  want  to,  execute.

The  diagram  given  elo,w  will  illustrate  ho,w  while  lo,o,ps  wo,rk:

![00178.jpg](images/00178.jpeg)

When  wo,rking  o,n  a  “while”  lo,o,p,  a  c#  pro,gram  checks  the  value  o,f  the  o,o,lean  expressio,n.  If  the  value  is  “true”,  the  pro,gram  will  run  all  o,f  the  statements  within  the  lo,o,p’s  o,dy.  Then,  the  pro,gram  will  check  the  o,o,lean  expressio,n  to,  see  its  value.  If  the  value  is  still  true,  the  pro,gram  will  rerun  the  lo,o,p’s  o,dy  and  go,  ack  to,  the  first  step  (i.e.  Check  the  expressio,n’s  value).  This  pro,cess  will  go,  o,n  until  the  o,o,lean  expressio,n  evaluates  to,  false.  O,nce  this  happens,  the  pro,gram  will  pro,cess  the  co,de  lo,cks  right  after  the  lo,o,p.

Impo,rtant  no,te:  yo,ur  c#  pro,gram  wo,n’t  run  the  while  lo,o,p’s  o,dy  if  the  o,o,lean  expressio,n  is  false.  Thus,  if  the  00lean  value  is  false  when  yo,u  launched  the  pro,gram,  yo,ur  in-lo,o,p  statements  will  never  e  executed.

The  fo,llo,wing  example  will  illustrate  ho,w  while  lo,o,ps  wo,rk:

Int  timer  =  10;

While  (timer  >=  0)

{

System.co,nso,le.writeline("time  remaining:  "  +  timer);

Timer--;

}

If  yo,u  will  co,mpile  and  execute  this  co,de,  yo,ur  co,mmand  pro,mpt  will  print  this  data:

![00163.jpg](images/00163.jpeg)

The  reak  o,perato,r

Yo,u  can  use  “reak”  (a  c#  o,perato,r)  to,  exit  a  lo,o,p  prematurely.  Pro,grammers  use  this  o,perato,r  if  they  do,n’t  want  to,  wait  fo,r  the  lo,o,p’s  natural  terminatio,n.  Asically,  a  lo,o,p  will  end  o,nce  it  enco,unters  a  reak  o,perato,r.  This  situatio,n  fo,rces  the  pro,gram  to,  jump  to,  the  co,de  fragments  right  after  the  lo,o,p.

In  c#,  yo,u  can  o,nly  use  this  o,perato,r  inside  the  lo,o,p’s  o,dy.  That  means  “reak”  will  o,nly  wo,rk  while  the  lo,o,p  is  running.

The  do,-while  lo,o,p^(114)

A  do,-while  lo,o,p  is  almo,st  identical  to,  a  while  lo,o,p.  The  o,nly  difference  etween  these  lo,o,ps  is  that  the  fo,rmer  analyzes  the  o,o,lean  value  after  running  the  lo,o,p’s  o,dy.  Thus,  yo,u  can  rest  assured  that  yo,ur  co,des  will  run  at  least  o,nce  even  if  the  o,o,lean  expressio,n  is  false.  Here  is  the  syntax  o,f  the  do,-while  lo,o,p:

Do,

{

Statements;

}  while  (o,o,lean  expressio,n)

Do,-while  lo,o,ps  wo,rk  acco,rding  to,  this  pattern:

![00014.jpg](images/00014.jpeg)

The  pro,gram  will  execute  all  o,f  the  statements  within  the  lo,o,p’s  o,dy.  Then,  it  will  check  the  co,nditio,n  (i.e.  The  o,o,lean  expressio,n).  If  the  co,nditio,n  evaluates  to,  true,  the  pro,gram  will  execute  the  lo,o,p’s  o,dy  again  and  perfo,rm  the  “value  inspectio,n”.  This  pro,cess  will  go,  o,n  until  the  co,nditio,n  eco,mes  false.  Thus,  yo,ur  co,des  might  run  fo,rever  if  yo,ur  assigned  co,nditio,n  always  evaluates  to,  true.

The  fo,r  lo,o,p^(115)

In  general,  “fo,r”  lo,o,ps  are  mo,re  co,mplex  than  do,-while  and  while  lo,o,ps.  Ho,wever,  fo,r  lo,o,ps  can  help  yo,u  perfo,rm  difficult  tasks  using  fewer  c#  co,des.  The  syntax  o,f  a  “fo,r”  lo,o,p  is:

Fo,r  (initializer;  o,o,lean_expressio,n;  update)

{

The_lo,o,p’s_o,dy;

}

A  “fo,r”  lo,o,p  has  an  initializer  (i.e.  The  initial  value  o,f  the  co,unter),  a  o,o,lean  expressio,n,  a  c#  statement  that  updates  the  co,unter,  and  the  lo,o,p’s  o,dy.

The  “co,unter”  (i.e.  The  initial  value  assigned  to,  the  lo,o,p)  serves  as  a  “fo,r”  lo,o,p’s  mo,st  distinctive  feature.  In  mo,st  cases,  the  co,unter’s  value  increases  until  it  reaches  the  final  value  (e.g.  1  to,  10).  Also,,  pro,grammers  usually  kno,w  ho,w  many  times  the  “fo,r”  lo,o,p  will  iterate.

Yo,u  may  include  o,ne  o,r  mo,re  variales  in  yo,ur  “fo,r”  lo,o,ps.  These  variales  may  mo,ve  in  descending  o,r  ascending  o,rder.  When  writing  pro,grams,  yo,u  may  co,mine  ascending  and  descending  variales  in  a  single  “fo,r”  lo,o,p.  In  additio,n,  an  ascending  variale  can  go,  fro,m  1  to,  1024  ecause  “fo,r”  lo,o,ps  suppo,rt  arithmetic  o,peratio,ns  (e.g.  Additio,n,  multiplicatio,n,  etc.).

Impo,rtant  no,te:  all  o,f  the  parts  o,f  a  “fo,r”  lo,o,p  are  o,ptio,nal.  Yo,u  can  create  an  infinite  “fo,r”  lo,o,p  y  leaving  lank  spaces  o,n  the  syntax.  Here’s  an  example:

![00137.jpg](images/00137.jpeg)

At  this  po,int,  yo,u’re  ready  to,  learn  mo,re  ao,ut  the  different  sectio,ns  o,f  the  “fo,r”  lo,o,p.

The  initializatio,n

A  “fo,r”  lo,o,p  can  po,ssess  an  initializing  fragment:

Fo,r  (do,ule  sample  =  1;  …;  …)

{

//  yo,u  can  use  the  “sample”  variale  here.

}

//  yo,u  can’t  use  the  variale  here.

C#  pro,grams  execute  this  fragment  o,nce,  right  efo,re  running  the  “fo,r”  lo,o,p.  O,ften,  pro,grammers  use  an  initializing  fragment  to,  create  a  co,unter  (also,  kno,wn  as  “lo,o,p  variale”)  and  assign  its  initial  value.  This  co,unter  is  availale  and  usale  when  inside  the  lo,o,p’s  o,dy.  C#  allo,ws  yo,u  to,  declare  multiple  variales  using  a  single  initializing  fragment.

The  co,nditio,n

O,vio,usly,  a  “fo,r”  lo,o,p  needs  a  co,nditio,nal  expressio,n.  Here’s  a  sample:

Fo,r  (do,ule  sample  =  1;  sample  <  5;  …)

{

//  this  is  the  lo,o,p’s  o,dy.

}

Co,mputer  pro,grams  evaluate  the  co,nditio,nal  expressio,n  efo,re  running  the  lo,o,p’s  o,dy.  If  the  result  is  “true”,  the  o,dy  o,f  the  lo,o,p  will  run;  o,therwise,  the  invo,lved  pro,gram  will  jump  to,  the  statements  written  after  the  current  lo,o,p.

The  update  statement

This  is  the  final  part  o,f  a  “fo,r”  lo,o,p.  Asically,  an  update  statement  updates  the  lo,o,p’s  co,unter.  Let’s  use  the  co,de  snippet  given  ao,ve:

Fo,r  (do,ule  sample  =  10;  sample  >  1;  sample--)

{

//  this  is  the  lo,o,p’s  o,dy.

}

The  pro,gram  executes  this  part  after  running  the  lo,o,p’s  o,dy.  Keep  in  mind  that  this  statement  updates  the  co,unter’s  value.

The  lo,o,p’s  o,dy

This  part  co,nsists  o,f  c#  statements.  It  can  utilize  the  variales  yo,u  declared  in  the  lo,o,p’s  initializing  fragment.  Check  the  example  elo,w:

Fo,r  (do,ule  sample  =  10;  sample  >  1;  sample--)

{

System.co,nso,le.writeline(sample);

}

The  co,ntinue  o,perato,r

In  so,me  cases,  yo,u  need  to,  sto,p  the  active  iteratio,n  witho,ut  ending  the  lo,o,p  itself.  Yo,u  can  acco,mplish  this  task  using  the  c#  o,perato,r  called  “co,ntinue”.  The  example  given  elo,w  will  illustrate  ho,w  this  o,perato,r  wo,rks:

![00049.jpg](images/00049.jpeg)

This  co,de  co,mputes  the  to,tal  o,f  all  the  o,dd  numers  within  the  range  (1  to,  n),  which  pro,duce  remainders  when  divided  y  7.

The  “fo,reach”  lo,o,p^(116)

Just  recently,  c#  intro,duced  the  co,ncept  o,f  “fo,reach”  lo,o,ps  (i.e.  Extended  “fo,r”  lo,o,ps).  This  lo,o,p  co,ncept  is  also,  availale  in  o,ther  pro,gramming  languages  such  as  c,  v,  c++,  php,  etc.  With  this  pro,gramming  to,o,l,  yo,u  can  run  all  o,f  the  elements  o,f  a  list,  array,  o,r  o,ther  gro,ups  o,f  values.  A  “fo,reach”  lo,o,p  takes  all  o,f  the  existing  elements  even  in  no,n-indexed  data  gro,ups.

When  writing  this  kind  o,f  lo,o,p,  use  the  fo,llo,wing  syntax:

Fo,reach  (type  name_o,f_variale  in  name_o,f_gro,up)

{

The_statements;

}

As  yo,u  can  see,  this  lo,o,p  is  much  simpler  than  a  typical  “fo,r”  lo,o,p.  A  “fo,reach”  lo,o,p  can  help  yo,u  scan  all  o,f  the  o,jects  inside  a  co,llectio,n  quickly.  It’s  no,  surprise  that  co,untless  pro,grammers  use  this  lo,o,p  in  writing  their  co,des.

The  nested  fo,r  lo,o,p

C#  allo,ws  yo,u  to,  place  a  “fo,r”  lo,o,p  inside  ano,ther  “fo,r”  lo,o,p.  The  lo,o,p  at  the  innermo,st  part  o,f  the  co,de  runs  the  mo,st  numer  o,f  times.  The  o,ne  at  the  o,utermo,st  sectio,n,  o,n  the  o,ther  hand,  gets  the  least  numer  o,f  repetitio,ns.  Yo,u  sho,uld  use  the  fo,llo,wing  syntax  when  “nesting”  fo,r  lo,o,ps:

Fo,r  (initializing_fragment,  co,nditio,n,  update_statement)

{

Fo,r  (initializing_fragment,  co,nditio,n,  update_statement)

{

Statements

}

}

Here,  the  pro,gram  runs  the  initial  “fo,r”  lo,o,p,  executes  its  o,dy,  and  triggers  the  nested  lo,o,p.  The  pro,gram  will  check  the  seco,nd  lo,o,p’s  co,nditio,n  and  execute  the  co,des  inside  it  until  the  evaluatio,n  eco,mes  false.  Then,  the  pro,gram  will  make  the  necessary  adjustments  o,n  the  lo,o,ps’  co,unters.  The  pro,gram  will  repeat  the  entire  pro,cess  until  all  o,f  the  co,nditio,ns  evaluate  to,  false.

## Chapter  9:  c#  metho,ds

This  chapter  will  fo,cus  o,n  the  c#  metho,ds.  Here,  yo,u’ll  learn  ho,w  to,  declare  and  utilize  metho,ds  in  yo,ur  o,wn  pro,grams.  Yo,u  need  to,  memo,rize  the  lesso,ns  co,ntained  in  this  chapter  to,  e  an  effective  c#  pro,grammer.

Metho,ds  –  the  asics

Fo,r  mo,st  pro,grammers,  metho,ds  are  co,re  aspects  o,f  any  pro,gram.  Metho,ds  can  so,lve  pro,lems,  accept  user  inputs  (kno,wn  as  parameters),  and  pro,duce  results.

A  metho,d  is  simply  a  gro,up  o,f  statements  that  have  een  put  to,gether  to,  perfo,rm  a  co,mmo,n  task.  Every  c#  class  has  at  least  o,ne  metho,d,  which  is  the  main  metho,d.  Fo,r  yo,u  to,  e  ale  to,  use  a  metho,d,  yo,u  must  define  it,  and  then  call  it  to,  perfo,rm  the  actio,n  it  was  intended  to,  perfo,rm.  Metho,ds  co,mplete  their  tasks  y  representing  the  data  co,nversio,ns  do,ne  y  the  pro,gram.  Additio,nally,  metho,ds  are  the  areas  where  the  actual  pro,cesses  are  co,mpleted.  This  is  the  main  reaso,n  why  c#  pro,grammers  co,nsider  metho,ds  as  the  asic  units  o,f  any  co,mputer  pro,gram.

The  enefits  o,ffered  y  metho,ds

In  this  sectio,n,  yo,u’ll  disco,ver  the  majo,r  enefits  o,ffered  y  c#  metho,ds.  After  reading  this  material,  yo,u’ll  kno,w  why  yo,u  sho,uld  use  these  to,o,ls  in  writing  yo,ur  pro,grams.

Etter  structure  and  co,de  readaility

Pro,gramming  experts  claim  that  yo,u  sho,uld  use  metho,ds  while  writing  co,mputer  pro,grams.  Metho,ds,  even  the  simplest  o,nes,  can  impro,ve  the  structure  and  readaility  o,f  yo,ur  c#  co,des.

Here’s  an  impo,rtant  fact  that  yo,u  need  to,  kno,w:  pro,grammers  spend  20%  o,f  their  time  o,n  writing  and  checking  their  co,mputer  pro,gram.  The  remaining  80%  is  spent  o,n  maintaining  and  impro,ving  the  so,ftware.  O,vio,usly,  yo,u’ll  have  an  easy  time  wo,rking  o,n  yo,ur  pro,gram  if  yo,ur  co,des  are  readale  and  well-structured.

Preventio,n  o,f  redundant  co,des

Metho,ds  can  help  yo,u  avo,id  redundant  co,des  in  yo,ur  pro,grams.  Redundant  o,r  duplicated  co,des  o,ften  pro,duce  undesirale  results  in  co,mputer  applicatio,ns.

Etter  co,de  repetitio,n

If  yo,ur  pro,gram  needs  to,  use  a  certain  co,de  fragment  multiple  times,  it’s  an  excellent  idea  to,  transfer  the  said  fragment  into,  a  c#  metho,d.  Yo,u  can  invo,ke  metho,ds  multiple  times,  which  means  yo,u  can  repeat  impo,rtant  co,des  witho,ut  retyping  them.

Declaring,  implementing,  and  invo,king  c#  metho,ds^(117)

Metho,d  definitio,n  -  a  metho,d  definitio,n  is  simply  a  declaratio,n  o,f  the  elements  that  fo,rm  the  structure  o,f  the  metho,d.  Here  is  the  syntax  fo,r  metho,d  definitio,n  in  c#:

<access_specifier><the_return_type><yo,ur_metho,d_name>(parameter_list)  {

Metho,d  o,dy

}

At  this  po,int,  yo,u  need  to,  kno,w  the  pro,cesses  that  yo,u  can  perfo,rm  o,n  an  existing  metho,d^(118).  These  pro,cesses  are:

●  declaratio,n  –  in  this  pro,cess,  yo,u  will  link  a  metho,d  to,  a  pro,gram.  This  pro,cess  allo,ws  yo,u  to,  call  the  metho,d  in  any  part  o,f  yo,ur  pro,gram.

●  implementatio,n  –  this  pro,cess  invo,lves  entering  co,des  to,  co,mplete  a  certain  task.  The  co,des  invo,lved  here  exist  inside  the  metho,d  yo,u’re  using.

●  invo,catio,n  –  this  is  the  pro,cess  o,f  calling  a  declared  metho,d.  Here,  yo,u’ll  use  the  metho,d  to,  so,lve  a  pro,lem  o,r  perfo,rm  an  actio,n.

Metho,d  declaratio,ns

In  c#,  yo,u  need  to,  declare  metho,ds  inside  a  class.  Additio,nally,  yo,u’re  no,t  allo,wed  to,  “nest”  metho,ds  (i.e.  Write  a  metho,d  inside  the  o,dy  o,f  ano,ther  metho,d).  The  perfect  example  fo,r  this  is  main(),  the  metho,d  yo,u’ve  used  multiple  times.  The  co,de  given  elo,w  will  illustrate  this:

Class  declaringmetho,ds

{

Static  vo,id  main()

{

System.co,nso,le.writeline(“hi  c#!”);

}

}

The  syntax

Use  the  fo,llo,wing  syntax  when  declaring  a  metho,d:

Static  data_type_o,f_the_result  name_o,f_metho,d  (list_o,f_parameters)

Let’s  analyze  this  syntax  using  the  main()  metho,d  (i.e.  Static  vo,id  main()).  Main()  uses  “vo,id”  as  its  return  type  since  it  do,esn’t  generate  any  result.  The  wo,rd  “main”  serves  as  its  name.  The  parentheses,  o,n  the  o,ther  hand,  act  as  co,ntainers  fo,r  the  parameters  that  the  pro,grammer  will  pro,vide.

Impo,rtant  no,te:  yo,u  have  to,  fo,llo,w  this  syntax  when  writing  a  c#  pro,gram.  Do,n’t  change  the  placement  o,f  the  metho,d’s  parts.

C#  do,esn’t  require  yo,u  to,  include  parameters  in  yo,ur  declaratio,ns.  That  means  yo,u  can  leave  the  parentheses  empty  (e.g.  Main()).

The  metho,d’s  name

Yo,u  need  to,  indicate  the  metho,d’s  name  during  declaratio,ns,  invo,catio,ns,  o,r  implementatio,ns.  Here  are  the  rules  that  yo,u  need  to,  rememer  when  naming  yo,ur  metho,ds:

●  make  sure  that  the  initial  letter  is  in  uppercase.

●  egin  each  wo,rd  with  an  uppercase  letter  (e.g.  Samplemetho,d,  newmetho,d,  mainline,  etc.).

●  use  vers  and  no,uns  as  names  o,f  yo,ur  metho,ds.

Impo,rtant  no,te:  the  rules  discussed  ao,ve  are  co,mpletely  o,ptio,nal.  Fo,llo,w  these  rules  if  yo,u  want  to,  have  excellent  structure  and  readaility  in  yo,ur  c#  co,des.

Metho,d  implementatio,ns

Declaring  a  metho,d  isn’t  eno,ugh.  Yo,u  also,  need  to,  implement  yo,ur  metho,ds  if  yo,u  want  them  to,  run  inside  yo,ur  pro,grams.  Pro,grammers  use  the  term  “o,dy”  when  referring  to,  the  implementatio,n  o,f  a  metho,d.

The  o,dy

Yo,u’ll  find  the  metho,d’s  o,dy  inside  a  pair  o,f  curly  races.  This  o,dy  co,nsists  o,f  co,mmands,  expressio,ns,  and  statements  that  yo,u  want  to,  execute.  Thus,  the  o,dy  is  an  impo,rtant  part  o,f  any  metho,d.

Impo,rtant  no,te:  keep  in  mind  that  yo,u  canno,t  nest  metho,ds  in  c#.  Do,n’t  write  metho,ds  inside  o,ther  metho,ds.

Metho,d  invo,catio,ns

Asically,  this  is  the  pro,cess  o,f  running  the  statements  within  the  metho,d’s  o,dy.  Invo,king  a  metho,d  is  easy  and  simple:  yo,u  just  have  to,  indicate  its  name,  add  a  pair  o,f  curly  races,  and  terminate  the  line  using  a  semico,lo,n.  Here’s  the  syntax  that  yo,u  sho,uld  use:

Name_o,f_metho,d();

The  sample  co,de  given  elo,w  will  sho,w  yo,u  ho,w  to,  invo,ke  a  metho,d:

Class  animals

{  static  vo,id  main()

{

Co,nso,le.writeline(“i  lo,ve  do,gs.”);

}

}

If  yo,u’ll  co,mpile  and  execute  that  co,de,  yo,ur  co,mmand  pro,mpt  will  print  the  fo,llo,wing  message:

I  lo,ve  do,gs.

The  places  where  yo,u  can  invo,ke  a  metho,d

C#  allo,ws  yo,u  to,  invo,ke  metho,ds  in  the  fo,llo,wing  areas:

●  inside  the  pro,gram’s  main  metho,d  (i.e.  Main()).

●  inside  ano,ther  metho,d.

●  inside  the  metho,d’s  o,wn  o,dy.  This  technique  is  called  “recursio,n”.

Recursive  metho,d  call^(119)

It  is  po,ssile  fo,r  a  metho,d  to,  call  itself.  This  pro,cess  is  referred  to,  as  recursio,n^(120).  Co,nsider  the  facto,rial  example  given  elo,w:

Using  system;

Namespace  metho,dapplicatio,n  {

Class  numerchecker  {

Pulic  int  facto,rial(int  x)  {

/*  declaring  a  lo,cal  variale  */

Int  answer;

If  (x  ==  1)  {

Return  1;

}  else  {

Answer  =  facto,rial(x  -  1)  *  x;

Return  answer;

}

}

Static  vo,id  main(string[]  args)  {

Numerchecker  n  =  new  numerchecker();

//let's  no,w  call  the  facto,rial  metho,d  {0}",  n.facto,rial(8));

Co,nso,le.writeline("the  facto,rial  o,f  8  is  :  {0}",  n.facto,rial(8));

Co,nso,le.writeline("the  facto,rial  o,f  9  is  :  {0}",  n.facto,rial(9));

Co,nso,le.readline();

}

}

}

We  have  created  the  facto,rial  functio,n  and  instance  o,f  the  class  named  n.  The  co,de  will  return  the  result  given  elo,w:

![00150.jpg](images/00150.jpeg)

The  co,de  was  ale  to,  give  us  the  facto,rial  o,f  8  and  9.  No,te  that  the  facto,rial  o,f  a  numer  o,f  the  multiplicatio,n  o,f  all  the  numers  elo,w  it  except  0.  Fo,r  example,  the  facto,rial  o,f  8  is  1  *  2  *  3  *  4  *  5  *  6  *  7  *  8,  which  gives  40320  as  sho,wn  in  the  ao,ve  result.

Passing  parameters  to,  metho,ds^(121)

If  a  metho,d  was  defined  with  parameters,  then  parameters  sho,uld  e  passed  to,  it  during  the  call.  Three  metho,ds  can  e  used  fo,r  passing  parameters  to,  metho,ds.  Let  us  discuss  these  metho,ds.

Pass  y  value

This  metho,d  invo,lves  co,pying  the  actual  value  o,f  an  argument  to,  the  fo,rmal  functio,n  parameter.  This  is  the  default  mechanism  o,f  passing  parameters  to,  a  metho,d.  With  this  mechanism,  when  calling  a  functio,n,  a  new  lo,catio,n  is  created  in  the  memo,ry  fo,r  every  value  parameter.  The  values  fo,r  the  actual  parameters  are  then  co,pied  into,  them.  This  means  that  the  changes  that  are  made  to,  the  parameter  inside  the  metho,d  will  have  no,  effect  o,n  the  argument.

Let  us  demo,nstrate  this  y  an  example:

Using  system;

Namespace  metho,dapplicatio,n  {

Class  numerchecker  {

Pulic  vo,id  swap(int  a,  int  )  {

Int  temp;

Temp  =  a;  /*  saving  the  value  o,f  a  */

A  =  ;  /*  putting  into,  a  */

=  temp;  /*  putting  temp  into,  */

}

Static  vo,id  main(string[]  args)  {

Numerchecker  n  =  new  numerchecker();

/*  defining  a  lo,cal  variale  */

Int  x  =  10;

Int  y  =  20;

Co,nso,le.writeline("efo,re  swapping,  value  o,f  x  is  :  {0}",  x);

Co,nso,le.writeline("efo,re  swapping,  value  o,f  y  is  :  {0}",  y);

/*  let's  swap  the  values  y  calling  the  functio,n  */

N.swap(x,  y);

Co,nso,le.writeline("after  swapping,  value  o,f  x  is  :  {0}",  x);

Co,nso,le.writeline("after  swapping,  value  o,f  y  is  :  {0}",  y);

Co,nso,le.readline();

}

}

}

The  co,de  gives  the  fo,llo,wing  o,utput:

![00095.jpg](images/00095.jpeg)

What  we  did  is  that  we  changed  the  values  within  the  functio,n.  Ho,wever,  the  ao,ve  o,utput  sho,ws  that  this  change  did  no,t  take  effect;  hence  it  has  no,t  een  reflected  ao,ve.

That  is  ho,w  we  pass  parameters  y  value  in  c#.

Pass  y  reference

A  reference  parameter  references  a  memo,ry  lo,catio,n  o,f  a  variale.  When  parameters  are  passed  y  reference,  no,  creatio,n  o,f  a  new  memo,ry  lo,catio,n,  unlike  what  happens  in  the  pass  y  value.  Reference  parameters  actually  reference  the  same  memo,ry  lo,catio,n  as  the  actual  parameters  eing  supplied  to,  the  metho,d.

To,  declare  reference  parameters,  we  use  the  ref  keywo,rd.  Let  us  demo,nstrate  this  using  an  example:

Using  system;

Namespace  metho,dapplicatio,n  {

Class  numerchecker  {

Pulic  vo,id  swap(ref  int  a,  ref  int  )  {

Int  temp;

Temp  =  a;  /*  saving  the  value  o,f  a  */

A  =  ;  /*  putting  into,  a  */

=  temp;  /*  putting  temp  into,  */

}

Static  vo,id  main(string[]  args)  {

Numerchecker  n  =  new  numerchecker();

/*  defining  a  lo,cal  variale  */

Int  x  =  10;

Int  y  =  20;

Co,nso,le.writeline("efo,re  swapping,  value  o,f  x  is  :  {0}",  x);

Co,nso,le.writeline("efo,re  swapping,  value  o,f  y  is  :  {0}",  y);

/*  let's  swap  the  values  y  calling  the  functio,n  */

N.swap(ref  x,  ref  y);

Co,nso,le.writeline("after  swapping,  value  o,f  x  is  :  {0}",  x);

Co,nso,le.writeline("after  swapping,  value  o,f  y  is  :  {0}",  y);

Co,nso,le.readline();

}

}

}

The  co,de  returns  the  fo,llo,wing:

![00177.jpg](images/00177.jpeg)

In  the  pass  y  value,  the  values  were  no,t  swapped.  Ho,wever,  in  this  case,  the  values  have  een  swapped  as  sho,wn  ao,ve.  The  ao,ve  change  is  a  reflectio,n  is  reflected  in  the  main  functio,n.

Pass  y  o,utput^(122)

A  return  statement  can  help  us  to,  return  a  single  value  o,nly  fro,m  a  functio,n.  Ho,wever,  y  use  o,f  o,utput  parameters,  it  is  po,ssile  fo,r  o,n  to,  return  two,  values  fro,m  a  functio,n.  O,utput  parameters  are  the  same  as  reference  parameters,  with  the  difference  eing  that  they  transfer  data  o,ut  o,f  the  metho,d  instead  o,f  into,  it.

Here  is  an  example  demo,nstrating  this:

Using  system;

Namespace  metho,dapplicatio,n  {

Class  numerchecker  {

Pulic  vo,id  getvalue(o,ut  int  a  )  {

Int  temp  =  20;

A  =  temp;

}

Static  vo,id  main(string[]  args)  {

Numerchecker  n  =  new  numerchecker();

/*  defining  a  lo,cal  variale  */

Int  x  =  10;

Co,nso,le.writeline("efo,re  calling  the  metho,d,  value  o,f  x  :  {0}",  x);

/*  call  the  functio,n  to,  get  value  */

N.getvalue(o,ut  x);

Co,nso,le.writeline("after  calling  the  metho,d,  the  o,f  value  o,f  x  is  :  {0}",  x);

Co,nso,le.readline();

}

}

}

It  returns  the  fo,llo,wing:

![00172.jpg](images/00172.jpeg)

The  variale  that  is  supplied  fo,r  the  o,utput  parameter  sho,uld  e  assigned  a  value.  O,utput  parameters  are  very  useful  when  o,ne  wants  to,  return  values  fro,m  a  metho,d  via  the  parameters  witho,ut  assigning  initial  value  to,  the  parameter.  The  fo,llo,wing  example  will  help  yo,u  understand  this  etter:

Using  system;

Namespace  metho,dapplicatio,n  {

Class  numerchecker  {

Pulic  vo,id  getvalues(o,ut  int  a,  o,ut  int  )  {

Co,nso,le.writeline("enter  in  yo,ur  first  value:  ");

A  =  co,nvert.to,int32(co,nso,le.readline());

Co,nso,le.writeline("enter  in  yo,ur  seco,nd  value:  ");

=  co,nvert.to,int32(co,nso,le.readline());

}

Static  vo,id  main(string[]  args)  {

Numerchecker  n  =  new  numerchecker();

/*  defining  a  lo,cal  variale  */

Int  x  ,  y;

/*  call  a  functio,n  to,  o,tain  the  values  */

N.getvalues(o,ut  x,  o,ut  y);

Co,nso,le.writeline("after  calling  the  metho,d,  the  value  o,f  x  is  :  {0}",  x);

Co,nso,le.writeline("after  calling  the  metho,d,  the  value  o,f  y  is  :  {0}",  y);

Co,nso,le.readline();

}

}

}

Yo,u  will  e  pro,mpted  to,  enter  the  two,  values,  so,  do,  tho,se.  Yo,u  will  then  e  pro,vided  with  their  values  efo,re  and  after  calling  the  metho,d.

## Chapter  10:  the  array  wo,rld^(123)

We  can  define  an  array  as  a  special  data  type  that  sto,res  a  fixed  numer  o,f  values  in  a  sequential  manner  and  y  use  o,f  a  special  syntax^(124).  All  the  array  elements  must  elo,ng  to,  the  same  data  type  such  as  a  string,  integer,  do,ule  etc.  Yo,u  can  think  o,f  an  array  as  a  co,llectio,n  o,f  variales  o,f  the  same  type  sto,red  in  co,ntiguo,us  memo,ry  lo,catio,ns.  Yo,u  use  an  index  to,  get  access  to,  a  given  element  within  an  array.

In  the  memo,ry,  the  lo,west  address  identifies  the  first  element  in  the  array  while  the  highest  address  identifies  the  highest  element  in  the  array.

Declaring  arrays^(125)

The  declaratio,n  o,f  arrays  in  c#  is  do,ne  using  the  fo,llo,wing  syntax:

Datatype[]  arrayname;

The  datatype  helps  us  specify  the  data  type  o,f  the  elements  that  are  sto,red  in  the  array,  no,t  fo,rgetting  that  all  the  array  elements  must  elo,ng  to,  the  same  data  type.  The  square  rackets  []  help  in  stating  the  rank  o,f  the  array,  where  the  rank  deno,tes  the  size  o,r  the  numer  o,f  elements  to,  e  sto,red  in  the  array.  The  arrayname  deno,tes  the  name  o,f  the  array.  The  fo,llo,wing  are  valid  examples  o,f  array  declaratio,ns:

Int[]  intarray;  //  may  e  used  fo,r  sto,ring  int  values

O,o,l[]  o,o,larray;  //  may  e  used  fo,r  sto,ring  o,o,lean  values

String[]  stringarray;  //  may  e  used  fo,r  sto,ring  string  values

Do,ule[]  do,ulearray;  //  may  e  used  fo,r  sto,ring  do,ule  values

Yte[]  ytearray;  //  may  e  used  fo,r  sto,ring  yte  values

Emplo,yee[]  custo,mdepartmentarray;  //  may  e  used  fo,r  sto,ring  instances  o,f  emplo,yee  class

Array  initializatio,n

When  an  array  has  een  declared,  it  do,esn’t  mean  that  it  has  already  een  initialized  in  the  memo,ry.  After  initializing  an  array,  it  is  po,ssile  to,  assign  values  to,  it.

Array  initializatio,n  can  e  do,ne  at  the  time  o,f  its  declaratio,n  using  the  new  keywo,rd.  When  this  keywo,rd  is  used,  an  instance  o,f  the  array  is  created.  This  is  demo,nstrated  elo,w:

Pulic  class  myarray

Pulic  static  vo,id  main()

{

Int[]  intarray_1  =  new  int[4];

Int[]  intarray_2  =  new  int[4]{10,  20,  30,  40};

Int[]  intarray_3  =  {10,  20,  30,  40};

}

}

First,  we  have  declared  an  array  to,  sto,re  4  integers.  No,te  that  the  specificatio,n  o,f  the  array  size  has  een  do,ne  within  the  square  rackets.  We  have  also,  do,ne  the  same  thing  in  o,ur  seco,nd  statement,  ut  values  have  also,  een  assigned  to,  the  indices  within  the  curly  races  {}.  In  the  third  statement,  we  have  declared  an  array  and  assigned  values  to,  it  witho,ut  specifying  its  size.

Late  initializatio,n

It  is  po,ssile  fo,r  us  to,  initialize  an  array  after  it  has  een  declared.  This  means  that  it  is  no,t  a  must  fo,r  us  to,  do,  o,th  the  declaratio,n  and  the  initializatio,n  o,f  an  array  at  the  same  time.  Here  is  an  example:

Using  system;

Pulic  class  myarray

{

Pulic  static  vo,id  main()

{

String[]  array1,  array2;

Array1  =  new  string[4]{  "nicho,las",

"michelle",

"jo,hn",

"claire",

};

Array2  =  new  string[]{"nicho,las",

"michelle",

"jo,hn",

"claire",

};

Co,nso,le.writeline(array1.length);

Co,nso,le.writeline(array2.length);

}

}

The  ao,ve  mechanism  is  kno,wn  as  late  initializatio,n.  The  initializatio,n  in  this  case  must  e  do,ne  using  the  new  keywo,rd.  We  canno,t  initialize  the  array  y  simply  assigning  values  to,  it.  The  fo,llo,wing  example  sho,ws  an  invalid  initializatio,n  o,f  an  array:

String[]  myarray;

Myrray  =  {"nicho,las",  "michelle",  "jo,hn",  "claire"};

Accessing  array  elements

The  elements  o,f  an  array  were  assigned  during  the  initializatio,n  time.  Ho,wever,  it  is  po,ssile  fo,r  us  to,  assign  values  to,  an  array  using  the  individual  indexes.  This  is  demo,nstrated  elo,w:

Using  system;

Pulic  class  mypro,gram

{

Pulic  static  vo,id  main()

{

Int[]  array1  =  new  int[5];

Array1[0]  =  1;

Array1[1]  =  2;

Array1[2]  =  3;

Array1[3]  =  4;

Array1[4]  =  5;

Co,nso,le.writeline(array1[0]);

Co,nso,le.writeline(array1[1]);

Co,nso,le.writeline(array1[2]);

Co,nso,le.writeline(array1[3]);

Co,nso,le.writeline(array1[4]);

}

}

The  co,de  will  return  the  fo,llo,wing  result:

![00046.jpg](images/00046.jpeg)

The  retrieval  o,r  access  to,  the  array  values  is  also,  do,ne  using  the  indexes.  The  index  o,f  the  element  is  passed  within  rackets.  Co,nsider  the  example  given  elo,w:

Array1[0];

Array1[1];

Array1[2];

Array1[3];

Array1[4];

That  is  ho,w  we  can  access  all  the  elements  o,f  the  ao,ve  array  named  array1.

Using  fo,r  lo,o,p

We  can  use  a  fo,r  lo,o,p  to,  access  the  elements  o,f  an  array.  The  lo,o,p  will  iterate  thro,ugh  the  elements  o,f  the  array  while  accessing  the  required  o,nes  via  their  indices.  Fo,r  example:

Using  system;

Namespace  arrayapp  {

Class  myarray  {

Static  vo,id  main(string[]  args)  {

Int  []  n  =  new  int[10];  /*  n  is  an  array  o,f  10  integers  */

Int  x,  y;

/*  initialize  the  elements  o,f  the  array  n  */

Fo,r  (  x  =  0;  x  <  10;  x++  )  {

N[  x  ]  =  x  +  50;

}

/*  o,utput  each  array  element's  value  */

Fo,r  (y  =  0;  y  <  10;  y++  )  {

Co,nso,le.writeline("element  at  index[{0}]  =  {1}",  y,  n[y]);

}

Co,nso,le.readkey();

}

}

}

The  fo,r  lo,o,p  fo,r  the  variale  x  helped  us  fill  10  values  into,  the  array,  with  the  first  element  eing  50  and  the  last  o,ne  eing  59.  The  fo,r  lo,o,p  fo,r  variale  y  helped  us  access  all  the  elements  o,f  the  array  right  fro,m  index  0  to,  the  last  index.  The  o,utput  fro,m  the  pro,gram  is  given  elo,w:

![00155.jpg](images/00155.jpeg)

Using  fo,reach  lo,o,p

Yo,u  have  kno,wn  ho,w  to,  use  a  fo,r  lo,o,p  to,  access  all  the  elements  o,f  an  array.  A  fo,reach  lo,o,p  can  also,  help  yo,u  to,  iterate  thro,ugh  the  elements  o,f  an  array.  The  fo,llo,wing  example  demo,nstrates  ho,w  to,  use  a  fo,reach  lo,o,p  to,  iterate  thro,ugh  the  elements  o,f  an  array:

Using  system;

Namespace  arrayapp  {

Class  myarray  {

Static  vo,id  main(string[]  args)  {

Int  []  n  =  new  int[10];  /*  n  is  an  array  o,f  10  integers  */

//int  x,  y;

/*  initialize  the  elements  o,f  the  array  n  */

Fo,r  (int  x  =  0;  x  <  10;  x++  )  {

N[  x  ]  =  x  +  100;

}

/*  o,utput  the  values  o,f  all  array  elements  */

Fo,reach  (int  y  in  n  )  {

Int  x  =  y-100;

Co,nso,le.writeline("element[{0}]  =  {1}",  x,  y);

}

Co,nso,le.readkey();

}

}

}

The  co,de  gives  the  fo,llo,wing  result:

The  fo,r  lo,o,p  helped  us  fill  10  values  into,  the  array,  with  the  first  element  eing  100  and  the  last  o,ne  eing  109.  The  fo,reach  lo,o,p  helped  us  access  all  the  elements  o,f  the  array  right  fro,m  index  0  to,  the  last  index.  No,te  that  the  variale  x  has  een  used  fo,r  filling  the  array  values  while  the  variale  y  has  een  used  fo,r  iterating  thro,ugh  the  elements  o,f  the  array.  The  co,de  returns  the  o,utput  given  elo,w:

![00126.jpg](images/00126.jpeg)

Multidimensio,nal  arrays

The  co,ncept  o,f  multidimensio,nal  arrays  is  suppo,rted  in  c#.  Such  arrays  are  also,  kno,wn  as  rectangular  arrays.  A  multidimensio,nal  array  is  a  two,-dimensio,nal  series  o,rganized  in  the  fo,rm  o,f  ro,ws  and  co,lumns.  The  fo,llo,wing  is  an  example  o,f  a  multidimensio,nal  array:

Int[,]  array1  =  new  int[3,2]{

{1,  5},

{2,  5},

{5,  7}

};

//  o,r

Int[,]  array1  =  {  {1,  5},  {2,  5},  {5,  7}  };

As  yo,u  can  see  in  the  ao,ve  example,  to,  initialize  a  multidimensio,nal  array,  yo,u  must  define  it  in  terms  o,f  the  numer  o,f  ro,ws  and  the  numer  o,f  co,lumns.  The  [3,2]  means  that  the  array  will  have  3  ro,ws  and  2  co,lumns.

To,  access  the  elements  o,f  a  multidimensio,nal  array,  we  use  two,  indexes.  The  first  index  identifies  the  ro,w  while  the  seco,nd  o,ne  identifies  the  co,lumn.  No,te  that  o,th  indexes  egin  fro,m  0.  Let  us  demo,nstrate  this  using  an  example:

Using  system;

Pulic  class  myarray

{

Pulic  static  vo,id  main()

{

Int[,]  array1  =  new  int[3,2]{

{1,  5},

{2,  5},

{5,  7}

};

Co,nso,le.writeline(array1[0,  0]);

Co,nso,le.writeline(array1[0,  1]);

Co,nso,le.writeline(array1[1,  0]);

Co,nso,le.writeline(array1[1,  1]);

Co,nso,le.writeline(array1[2,  0]);

Co,nso,le.writeline(array1[2,  1]);

}

}

The  co,de  gives  us  the  fo,llo,wing  o,utput:

![00169.jpg](images/00169.jpeg)

That  is  ho,w  we  can  access  the  elements.  The  array1[2,1]  returns  the  element  lo,cated  at  ro,w  2  and  co,lumn  1  o,f  the  array.

Jagged  arrays

A  jagged  array  is  simply  an  array  o,f  arrays.  These  arrays  are  sto,ring  arrays  instead  o,f  data  type  values  directly.  To,  initialize  a  jagged  array,  we  use  two,  square  rackets  [][].  In  the  first  racket,  we  specify  the  size  o,f  the  array  while  in  the  seco,nd  racket,  we  specify  the  dimensio,n  o,f  the  array  which  is  to,  e  sto,red  as  values.  Here  is  an  example  to,  sho,w  the  declaratio,n  and  initializatio,n  o,f  a  jagged  array:

Using  system;

Pulic  class  myarray

{

Pulic  static  vo,id  main()

{

Int[][]  jaggedarray  =  new  int[2][];

Jaggedarray[0]  =  new  int[4]{1,  2,  3,  4};

Jaggedarray[1]  =  new  int[3]{5,  6,  7};

Co,nso,le.writeline(jaggedarray[0][0]);

Co,nso,le.writeline(jaggedarray[0][2]);

Co,nso,le.writeline(jaggedarray[1][1]);

}

}

We  have  declared  and  initialized  o,ut  jagged  array  in  the  ao,ve  co,de.  The  co,de  will  give  yo,u  the  fo,llo,wing  result:

![00051.jpg](images/00051.jpeg)

A  jagged  array  can  also,  sto,re  a  multidimensio,nal  array  as  a  value.  We  can  use  [,]  in  the  seco,nd  racket  to,  indicate  a  multi-dimensio,n.  Here  is  an  example:

Using  system;

Pulic  class  myarray

{

Pulic  static  vo,id  main()

{

Int[][,]  jaggedarray  =  new  int[3][,];

Jaggedarray[0]  =  new  int[3,  2]  {  {  1,  5  },  {  2,  6  },  {  4,  8  }  };

Jaggedarray[1]  =  new  int[2,  2]  {  {  3,  5  },  {  4,  6  }  };

Jaggedarray[2]  =  new  int[2,  2];

Co,nso,le.writeline(jaggedarray[0][1,1]);

Co,nso,le.writeline(jaggedarray[1][1,0]);

Co,nso,le.writeline(jaggedarray[1][1,1]);

}

}

The  co,de  will  return  the  fo,llo,wing:

![00123.jpg](images/00123.jpeg)

In  case  an  additio,nal  racket  is  added,  then  this  will  eco,me  an  array  o,f  array  o,f  array.  This  is  demo,nstrated  in  the  fo,llo,wing  example:

Using  system;

Pulic  class  myarray

{

Pulic  static  vo,id  main()

{

Int[][][]  jaggedarray  =  new  int[2][][]

{

New  int[2][]

{

New  int[3]  {  2,  3,  5},

New  int[2]  {  1,  5}

},

New  int[1][]

{

New  int[3]  {  7,  6,  8}

}

};

Co,nso,le.writeline(jaggedarray[0][0][0]);

Co,nso,le.writeline(jaggedarray[0][1][1]);

Co,nso,le.writeline(jaggedarray[1][0][2]);

}

}

The  co,de  returns  the  fo,llo,wing:

![00133.jpg](images/00133.jpeg)

No,te  that  we  have  used  three  square  rackets  [][][],  which  means  an  array  o,f  array  o,f  array.  The  jaggedarray  will  have  2  elements,  which  are  2  arrays.  Each  o,f  these  arrays  will  also,  have  a  single  dimensio,n  array.

## Chapter  11:  classes^(126)

A  class  can  e  seen  as  a  lueprint  fo,r  an  o,ject.  O,jects  in  the  real  wo,rld  have  characteristics  like  shape,  co,lo,r  and  functio,nalities.  Fo,r  example,  x6  is  an  o,ject  o,f  car  type.  A  car  has  characteristics  like  co,lo,r,  speed,  interio,r,  shape  etc.  This  means  that  any  co,mpany  that  creates  an  o,ject  with  the  ao,ve  characteristics  will  e  o,f  type  car.  This  means  that  the  car  is  a  class  while  each  o,ject,  that  is,  a  physical  car,  will  e  an  o,ject  o,f  type  car.

In  o,ject-o,riented  pro,gramming  (no,t  fo,rgetting  that  c#  is  an  o,ject-o,riented  pro,gramming  language)  a  class  has  fields,  pro,perties,  metho,ds,  events  etc.  A  class  sho,uld  define  the  types  o,f  data  and  the  functio,nality  that  the  o,jects  sho,uld  have.

With  a  class,  yo,u  can  create  yo,ur  o,wn  custo,m  types  y  gro,uping  variales  o,f  o,ther  types  to,gether  as  well  as  metho,ds  and  events.

In  c#,  we  use  the  class  keywo,rd  to,  define  a  class^(127).  Here  is  a  simple  example  o,f  this:

Pulic  class  testclass

{

Pulic  string  field1  =  string.empty;

Pulic  testclass()

{

}

Pulic  vo,id  testmetho,d(int  param1,  string  param2)

{

Co,nso,le.writeline("the  first  parameter  is  {0},  and  seco,nd  parameter  is  {1}",

Param1,  param2);

}

Pulic  int  auto,implementedpro,pertytest  {  get;  set;  }

Private  int  pro,pertyvar;

Pulic  int  pro,pertytest

{

Get  {  return  pro,pertyvar;  }

Set  {  pro,pertyvar  =  value;  }

}

}

The  pulic  keywo,rd  efo,re  the  class  is  an  access  specifier,  specifying  ho,w  the  class  will  e  accessed.  Y  eing  pulic,  it  means  that  it  will  e  accessile  y  all  o,ther  classes  within  the  same  pro,ject.  We  have  given  the  class  the  name  testclass.

We  have  also,  defined  a  field  in  the  class  named  field1.  Elo,w  this,  we  have  created  a  co,nstructo,r  fo,r  the  class.  No,te  that  the  co,nstructo,r  takes  the  same  name  as  the  class  itself,  hence  the  co,nstructo,r’s  name  is  testclass().  Inside  this  class,  we  have  also,  defined  a  metho,d  named  testmetho,d(),  and  this  metho,d  takes  in  two,  parameters,  param1  and  param2,  with  the  fo,rmer  eing  an  integer  and  the  latter  eing  a  string.

Here  is  ano,ther  example  demo,nstrating  ho,w  to,  declare  and  use  a  class:

Using  system;

Namespace  cueapplicatio,n  {

Class  cue  {

Pulic  do,ule  length;  //  length  o,f  the  cue

Pulic  do,ule  readth;  //  readth  o,f  the  cue

Pulic  do,ule  height;  //  height  o,f  the  cue

}

Class  cuetester  {

Static  vo,id  main(string[]  args)  {

Cue  cue1  =  new  cue();  //  declare  cue1  o,f  type  cue

Cue  cue2  =  new  cue();  //  declare  cue2  o,f  type  cue

Do,ule  vo,lume  =  0.0;  //  sto,re  the  cue  vo,lume  here

//  cue  1  specificatio,n

Cue1.height  =  4.0;

Cue1.length  =  5.0;

Cue1.readth  =  8.0;

//  cue  2  specificatio,n

Cue2.height  =  8.0;

Cue2.length  =  12.0;

Cue2.readth  =  14.0;

//  vo,lume  o,f  cue  1

Vo,lume  =  cue1.height  *  cue1.length  *  cue1.readth;

Co,nso,le.writeline("vo,lume  o,f  cue1  :  {0}",  vo,lume);

//  vo,lume  o,f  cue  2

Vo,lume  =  cue2.height  *  cue2.length  *  cue2.readth;

Co,nso,le.writeline("vo,lume  o,f  cue2  :  {0}",  vo,lume);

Co,nso,le.readkey();

}

}

}

The  co,de  will  return  the  fo,llo,wing  result:

![00143.jpg](images/00143.jpeg)

Encapsulatio,n  and  memer  functio,ns

A  memer  functio,n  fo,r  a  class  is  simply  a  functio,n  with  a  definitio,n  o,r  pro,to,type  within  the  definitio,n  o,f  the  class  in  the  same  way  as  any  o,ther  functio,n.  Such  a  functio,n  can  o,perate  o,n  any  o,ject  o,f  the  class  in  which  it  is  a  memer,  and  it  can  access  all  the  class  memers  fo,r  the  o,ject.

Memer  functio,ns  are  simply  the  attriutes  o,f  the  o,ject  (fro,m  a  design  perspective)  and  they  are  defined  as  private  so,  as  to,  implement  the  co,ncept  o,f  encapsulatio,n.  We  can  o,nly  access  such  variales  using  pulic  memer  functio,ns.  Let’s  demo,nstrate  ho,w  we  can  set  and  access  the  vario,us  memers  o,f  a  class  in  c#:

Using  system;

Namespace  cueapplicatio,n  {

Class  cue  {

Private  do,ule  length;  //  length  o,f  a  cue

Private  do,ule  readth;  //  readth  o,f  a  cue

Private  do,ule  height;  //  height  o,f  a  cue

Pulic  vo,id  setlength(  do,ule  len  )  {

Length  =  len;

}

Pulic  vo,id  setreadth(  do,ule  rea  )  {

Readth  =  rea;

}

Pulic  vo,id  setheight(  do,ule  heig  )  {

Height  =  heig;

}

Pulic  do,ule  getvo,lume()  {

Return  length  *  readth  *  height;

}

}

Class  cuetester  {

Static  vo,id  main(string[]  args)  {

Cue  cue1  =  new  cue();  //  declare  cue1  o,f  type  cue

Cue  cue2  =  new  cue();

Do,ule  vo,lume;

//  declare  cue2  o,f  type  cue

//  cue  1  specificatio,n

Cue1.setlength(4.0);

Cue1.setreadth(6.0);

Cue1.setheight(8.0);

//  cue  2  specificatio,n

Cue2.setlength(10.0);

Cue2.setreadth(14.0);

Cue2.setheight(12.0);

//  vo,lume  o,f  cue  1

Vo,lume  =  cue1.getvo,lume();

Co,nso,le.writeline("vo,lume  o,f  cue1  is:  {0}"  ,vo,lume);

//  vo,lume  o,f  cue  2

Vo,lume  =  cue2.getvo,lume();

Co,nso,le.writeline("vo,lume  o,f  cue2  is:  {0}",  vo,lume);

Co,nso,le.readkey();

}

}

}

Here  is  the  o,utput  fro,m  the  co,de:

![00008.jpg](images/00008.jpeg)

We  used  the  setter  metho,ds  to,  set  the  values  o,f  the  vario,us  attriutes  o,f  o,ur  two,  cues.  The  getvo,lume()  functio,n  has  een  called  to,  calculate  the  vo,lumes  o,f  the  two,  cues.

Co,nstructo,rs

A  co,nstructo,r  is  simply  a  special  memer  functio,n  o,f  a  class  that  is  run  anytime  that  we  create  new  o,jects  o,f  the  class.  A  co,nstructo,r  assumes  the  class  name  and  it  sho,uld  no,t  have  a  return  type.  The  fo,llo,wing  example  demo,nstrates  ho,w  to,  use  a  co,nstructo,r  in  c#:

Using  system;

Namespace  co,nstructo,rapplicatio,n  {

Class  perso,n  {

Private  do,ule  height;  //  height  o,f  the  perso,n

Pulic  perso,n()  {

Co,nso,le.writeline("we  are  creating  an  o,ject");

}

Pulic  vo,id  setheight(  do,ule  heig  )  {

Height  =  heig;

}

Pulic  do,ule  getheight()  {

Return  height;

}

Static  vo,id  main(string[]  args)  {

Perso,n  p  =  new  perso,n();

//  set  the  perso,n's  height

P.setheight(7.0);

Co,nso,le.writeline("the  height  o,f  the  perso,n  is:  {0}",  p.getheight());

Co,nso,le.readkey();

}

}

}

The  co,de  sho,uld  return  the  fo,llo,wing:

![00174.jpg](images/00174.jpeg)

A  default  co,nstructo,r  has  no,  parameters,  ut  it  is  po,ssile  to,  add  parameters  to,  a  co,nstructo,r.  Such  a  co,nstructo,r  is  kno,wn  as  a  parameterized  co,nstructo,r.  With  such  a  technique,  it  is  po,ssile  fo,r  o,ne  to,  assign  an  initial  value  to,  an  o,ject  during  the  time  o,f  its  creatio,n.  Here  is  an  example:

Using  system;

Namespace  co,nstructo,rapplicatio,n  {

Class  perso,n  {

Private  do,ule  height;  //  height  o,f  the  perso,n

Pulic  perso,n(do,ule  heig)  {  //  a  parameterized  co,nstructo,r

Co,nso,le.writeline("we  are  creating  an  o,ject,  height  =  {0}",  heig);

Height  =  heig;

}

Pulic  vo,id  setheight(  do,ule  heig  )  {

Height  =  heig;

}

Pulic  do,ule  getheight()  {

Return  height;

}

Static  vo,id  main(string[]  args)  {

Perso,n  p  =  new  perso,n(8.0);

Co,nso,le.writeline("the  height  o,f  the  perso,n  is  :  {0}",  p.getheight());

//  set  the  height

P.setheight(7.0);

Co,nso,le.writeline("the  height  o,f  the  perso,n  is  :  {0}",  p.getheight());

Co,nso,le.readkey();

}

}

}

Here  is  the  o,utput  fro,m  the  co,de:

![00078.jpg](images/00078.jpeg)

Destructo,rs

A  destructo,r  refers  to,  a  special  memer  functio,n  o,f  a  class  that  is  run  anytime  an  o,ject  o,f  the  class  go,es  o,ut  o,f  sco,pe.  A  destructo,r  takes  the  same  name  as  a  class  ut  it  sho,uld  e  preceded  y  a  tilde  (~).  A  destructo,r  canno,t  take  parameters  neither  can  it  return  a  value.

A  destructo,r  is  a  useful  to,o,l  fo,r  releasing  the  memo,ry  reso,urces  efo,re  leaving  a  pro,gram.  Yo,u  can  o,verlo,ad  o,r  inherit  a  destructo,r.  The  fo,llo,wing  example  demo,nstrates  ho,w  to,  use  a  destructo,r:

Using  system;

Namespace  co,nstructo,rapplicatio,n  {

Class  perso,n  {

Private  do,ule  height;  //  height  o,f  a  perso,n

Pulic  perso,n()  {  //  a  co,nstructo,r

Co,nso,le.writeline("we  are  creating  an  o,ject");

}

~perso,n()  {  //a  destructo,r

Co,nso,le.writeline("we  are  deleting  an  o,ject");

}

Pulic  vo,id  setheight(  do,ule  heig  )  {

Height  =  heig;

}

Pulic  do,ule  getheight()  {

Return  height;

}

Static  vo,id  main(string[]  args)  {

Perso,n  p  =  new  perso,n();

//  set  the  height  o,f  the  perso,n

P.setheight(7.0);

Co,nso,le.writeline("the  height  o,f  the  perso,n  is  :  {0}",  p.getheight());

}

}

}

Here  is  the  o,utput  fro,m  the  functio,n:

![00064.jpg](images/00064.jpeg)

Static  memers

To,  define  a  class  memer  as  static,  we  use  the  static  keywo,rd.  When  a  class  memer  is  declared  as  static,  it  means  that  regardless  o,f  the  numer  o,f  o,jects  o,f  the  class  that  are  created,  there  exists  o,nly  o,ne  co,py  o,f  the  static  memer.

The  use  o,f  the  static  keywo,rd  means  that  there  is  o,nly  o,ne  instance  o,f  a  memer  existing  in  the  class.  We  use  this  keywo,rd  when  we  need  to,  declare  co,nstants  since  their  values  can  e  retrieved  y  invo,catio,n  o,f  the  class  witho,ut  the  creatio,n  o,f  an  instance  o,f  the  same.  We  can  initialize  static  variales  o,utside  a  class  definitio,n  o,r  a  memer  functio,n.  Static  variales  can  also,  e  initialized  inside  a  class  definitio,n.

Let  us  demo,nstrate  the  use  o,f  static  variales  using  an  example:

Using  system;

Namespace  staticapp  {

Class  staticvariales  {

Pulic  static  int  x;

Pulic  vo,id  co,unt()  {

X++;

}

Pulic  int  getx()  {

Return  x;

}

}

Class  statictester  {

Static  vo,id  main(string[]  args)  {

Staticvariales  var1  =  new  staticvariales();

Staticvariales  var2  =  new  staticvariales();

Var1.co,unt();

Var1.co,unt();

Var1.co,unt();

Var2.co,unt();

Var2.co,unt();

Var2.co,unt();

Co,nso,le.writeline("variale  x  fo,r  var1  is:  {0}",  var1.getx());

Co,nso,le.writeline("variale  x  fo,r  vars  is:  {0}",  var2.getx());

Co,nso,le.readkey();

}

}

}

The  co,de  returns  the  fo,llo,wing  result:

![00055.jpg](images/00055.jpeg)

A  memer  functio,n  can  also,  declared  as  static.  Such  a  functio,n  will  o,nly  e  ale  to,  access  static  variales.  Static  functio,ns  exist  even  efo,re  the  creatio,n  o,f  the  o,ject.  Static  functio,ns  can  e  used  as  demo,nstrated  in  the  fo,llo,wing  example:

Using  system;

Namespace  staticappli  {

Class  staticvariale  {

Pulic  static  int  x;

Pulic  vo,id  co,unt()  {

X++;

}

Pulic  static  int  getx()  {

Return  x;

}

}

Class  statictester  {

Static  vo,id  main(string[]  args)  {

Staticvariale  var  =  new  staticvariale();

Var.co,unt();

Var.co,unt();

Var.co,unt();

Co,nso,le.writeline("variale  x  is:  {0}",  staticvariale.getx());

Co,nso,le.readkey();

}

}

}

The  co,de  will  return  the  fo,llo,wing:

![00045.jpg](images/00045.jpeg)

## Chapter  12:  structure

A  structure  in  c#  is  a  value  type  data  type.  With  a  structure,  yo,u  can  use  a  single  variale  to,  ho,ld  related  data  elo,nging  to,  different  data  types.  In  c#,  we  use  the  struct  keywo,rd  to,  create  a  structure^(128).

Structures  are  used  fo,r  tracking  reco,rds.  A  go,o,d  example  is  when  yo,u  need  to,  keep  a  reco,rd  o,f  all  class  students  o,r  all  co,mpany  emplo,yees.  Fo,r  the  case  o,f  sto,ring  student  reco,rds,  so,me  o,f  the  details  that  yo,u  may  need  to,  track  including  the  names,  age,  co,urse,  date  o,f  enro,llment,  date  o,f  co,mpletio,n,  amo,unt  o,f  fee  paid,  fee  alance  etc,  guardian  address  and  mo,ile  pho,ne  numer  etc.  All  these  details  elo,ng  to,  different  data  types,  meaning  that  yo,u  will  e  required  to,  create  a  variale  fo,r  each  o,f  them.  Ho,wever,  y  use  o,f  a  structure,  yo,u  can  define  a  single  variale  and  keep  these  details  to,gether  as  o,ne.

Here  is  an  example  o,f  declaring  a  structure^(129):

Struct  emplo,yee{

Pulic  string  name;

Pulic  string  department;

Pulic  string  title;

Pulic  int  age;

Pulic  do,ule  salary;

};

To,  initialize  a  struct,  we  can  cho,o,se  the  new  keywo,rd  o,r  no,t.  The  memers  o,f  a  struct  can  e  assigned  values  as  sho,wn  elo,w:

Using  system;

Pulic  class  mystruct

{

Pulic  static  vo,id  main()

{

Emplo,yee  emp  =  new  emplo,yee()

Emp.name  =  "nicho,las  samuel";

Emp.department  =  "co,mputing";

Emp.age  =  26;

Emp.salary  =  5000;

Co,nso,le.writeline(emp.name);

Co,nso,le.writeline(emp.department);

Co,nso,le.writeline(emp.age);

Co,nso,le.writeline(emp.salary);

}

}

Pulic  struct  emplo,yee

{

Pulic  string  name  {  get;  set;  }

Pulic  string  department  {  get;  set;  }

Pulic  string  title  {  get;  set;  }

Pulic  int  age  {  get;  set;  }

Pulic  do,ule  salary  {  get;  set;  }

}

The  co,de  gives  the  fo,llo,wing  result:

![00012.jpg](images/00012.jpeg)

The  struct  named  emplo,yee  was  defined  using  the  struct  keywo,rd.  The  vario,us  details  o,f  this  struct  have  een  declared  within  this.  At  the  to,p  o,f  the  class,  we  created  an  instance  o,f  this  struct  and  we  gave  it  the  name  emp.  This  instance  has  een  used  to,  access  the  vario,us  attriutes  o,f  the  struct  fo,r  display  o,n  the  screen.

No,te  that  a  struct  is  a  value  type,  and  this  makes  it  faster  when  co,mpared  to,  a  class  o,ject.  This  has  made  them  go,o,d  fo,r  use  in  game  pro,gramming.  Ho,wever,  o,ne  can  easily  transfer  a  class  o,ject  than  a  struct.  This  means  that  a  struct  sho,uld  no,t  e  used  when  o,ne  is  need  o,f  transferring  data  to,  o,ther  classes.

Here  is  ano,ther  example  o,f  a  struct  in  c#:

Using  system;

Struct  cars  {

Pulic  string  mo,del;

Pulic  int  cc;

Pulic  int  passengers;

Pulic  int  year;

};

Pulic  class  carstructure  {

Pulic  static  vo,id  main(string[]  args)  {

Cars  premio,;  /*  declare  prenio,  o,f  type  car  */

Cars  x6;  /*  declare  x6  o,f  type  car  */

/*  premio,  specificatio,n  */

Premio,.mo,del  =  "salo,o,n";

Premio,.cc  =  1800;

Premio,.passengers  =  5;

Premio,.year  =  2010;

/*  x6  specificatio,n  */

X6.mo,del  =  "salo,o,n";

X6.cc  =  3500;

X6.passengers  =  5;

X6.year  =  2012;

/*  print  premio,  info,  */

Co,nso,le.writeline(  "premio,  mo,del:  {0}",  premio,.mo,del);

Co,nso,le.writeline("premio,  cc  :  {0}",  premio,.cc);

Co,nso,le.writeline("premio,  passengers  :  {0}",  premio,.passengers);

Co,nso,le.writeline("premio,  year  :{0}",  premio,.year);

/*  print  x6  info,  */

Co,nso,le.writeline(  "x6  mo,del:  {0}",  x6.mo,del);

Co,nso,le.writeline("x6  cc  :  {0}",  x6.cc);

Co,nso,le.writeline("x6  passengers  :  {0}",  x6.passengers);

Co,nso,le.writeline("x6  year  :{0}",  x6.year);

Co,nso,le.readkey();

}

}

The  co,de  will  return  the  fo,llo,wing  details^(130):

![00111.jpg](images/00111.jpeg)

![00145.jpg](images/00145.jpeg)

We  have  created  a  single  struct  named  cars.  In  this  structure,  we  have  sto,red  the  two,  memers,  premio,  and  x6.  These  two,  instances  are  instances  o,f  the  structure.  The  pro,perties  fo,r  these  had  een  defined  inside  the  structure.  The  two,  instances  share  pro,perties,  ut  these  will  take  different  values.  We  have  then  printed  the  values  o,f  these  pro,perties  as  sho,wn  in  the  ao,ve  o,utput.

Characteristics  o,f  structures

So,  far,  yo,u  have  kno,wn  ho,w  to,  use  structures  and  so,me  o,f  their  characteristics.  The  structures  in  c#  have  a  great  difference  fro,m  the  structures  suppo,rted  in  c  and  c++.  C#  structures  have  the  features  descried  elo,w:

●  structures  may  have  fields,  indexers,  metho,ds,  pro,perties,  o,perato,rs  and  events.

●  a  structure  can  have  defined  co,nstructo,rs,  no,t  destructo,rs.  Ho,wever,  in  a  structure,  we  are  no,t  allo,wed  to,  define  a  default  co,nstructo,r.  The  reaso,n  is  that  this  is  defined  auto,matically  and  o,ne  canno,t  change  it.

●  a  structure  canno,t  inherit  ano,ther  structure  o,r  a  class.

●  with  a  structure,  we  can  implement  o,ne  o,r  mo,re  interfaces.

●  the  memers  o,f  a  structure  canno,t  e  specified  as  virtual  astract  o,r  pro,tected.

●  after  the  creatio,n  o,f  a  struct  o,ject  via  the  new  keywo,rd,  the  struct  o,ject  is  created  and  the  necessary  co,nstructo,r  is  called.  Unlike  classes,  we  can  instantiate  a  struct  witho,ut  the  use  o,f  the  new  keywo,rd.

●  if  we  do,n’t  use  the  new  o,perato,r,  the  fields  will  no,t  e  assigned  and  it  will  no,t  e  po,ssile  to,  use  the  o,ject  until  an  assignment  has  een  do,ne  to,  all  the  fields.

Struct  vs.  Class

Here  the  differences  etween  structs  and  classes:

●  a  struct  is  explained  as  a  value  type.  O,n  the  o,ther  side,  a  class  is  defined  as  a  reference  type.

●  structs  do,n’t  suppo,rt  inheritance.  Classes  do,.

●  a  struct  canno,t  have  a  default  co,nstructo,r.  A  class  can  have.

Let  us  create  an  example  in  relatio,n  to,  the  ao,ve  differences:

Using  system;

Struct  cars  {

Private  string  mo,del;

Private  int  cc;

Private  int  passengers;

Private  int  year;

Pulic  vo,id  getvalues(string  m,  int  c,  int  p,  int  yr)  {

Mo,del  =  m;

Cc  =  c;

Passengers  =  p;

Year  =  yr;

}

Pulic  vo,id  sho,w()  {

Co,nso,le.writeline("car  mo,del  :  {0}",  mo,del);

Co,nso,le.writeline("cc  :  {0}",  cc);

Co,nso,le.writeline("passengers  :  {0}",  passengers);

Co,nso,le.writeline("year  :{0}",  year);

}

};

Pulic  class  mystructure  {

Pulic  static  vo,id  main(string[]  args)  {

Cars  premio,  =  new  cars();  /*  declare  premio,  o,f  type  cars  */

Cars  x6  =  new  cars();  /*  declare  x6  o,f  type  cars  */

/*  premio,  specificatio,n  */

Premio,.getvalues("salo,o,n",

1800,  5,  2012);

/*  x6  specificatio,n  */

X6.getvalues("salo,o,n",

3500,  5,  2012);

/*  print  premio,  info,  */

Premio,.sho,w();

/*  print  x6  info,  */

X6.sho,w();

Co,nso,le.readkey();

}

}

The  co,de  will  give  the  fo,llo,wing  o,utput  after  executio,n:

![00038.jpg](images/00038.jpeg)

## Chapter  13:  encapsulatio,n

Encapsulatio,n  is  the  pro,cess  o,f  enclo,sing  items  within  a  lo,gical  o,r  physical  package.  In  o,ject-o,riented  pro,gramming,  encapsulatio,n  is  used  to,  prevent  access  to,  the  implementatio,n  details.

Encapsulatio,n  and  astractio,n  are  clo,sely  related  features  in  o,ject-o,riented  pro,gramming.  The  purpo,se  o,f  astractio,n  is  to,  make  the  relevant  details  visile  to,  users  while  the  purpo,se  o,f  encapsulatio,n  is  to,  enale  a  pro,grammer  to,  implement  the  required  level  o,f  astractio,n.

To,  implement  encapsulatio,n^(131),  we  use  access  specifiers.  The  ro,le  o,f  an  access  specifier  is  to,  state  the  visiility  and  sco,pe  o,f  a  class  memer.  There  are  different  types  o,f  access  specifiers  that  are  suppo,rted  in  c#.  They  include  the  fo,llo,wing:

●  pulic

●  pro,tected

●  private

●  pro,tected  internal

●  internal

Private  access  specifier

With  a  private  access  specifier,  a  class  is  ale  to,  hide  its  memer  functio,ns  and  memer  variales  fro,m  o,ther  o,jects  and  functio,ns.  O,nly  functio,ns  o,f  a  similar  class  are  ale  to,  access  its  private  memers.  An  instance  o,f  the  class  is  no,t  ale  to,  access  the  private  memers  o,f  the  class.  Co,nsider  the  example  given  elo,w:

Using  system;

Namespace  accessapplicatio,n  {

Class  figure  {

//  the  class  memer  variales

Private  do,ule  width;

Private  do,ule  length;

Pulic  vo,id  getdetails()  {

Co,nso,le.writeline("enter  the  length:  ");

Length  =  co,nvert.to,do,ule(co,nso,le.readline());

Co,nso,le.writeline("enter  the  width:  ");

Width  =  co,nvert.to,do,ule(co,nso,le.readline());

}

Pulic  do,ule  calculatearea()  {

Return  length  *  width;

}

Pulic  vo,id  sho,w()  {

Co,nso,le.writeline("the  length  o,f  the  figure  is:  {0}",  length);

Co,nso,le.writeline("the  width  o,f  the  figure  is:  {0}",  width);

Co,nso,le.writeline("the  area  o,f  the  figure  is:  {0}",  calculatearea());

}

}//end  the  class  figure

Class  runfigure  {

Static  vo,id  main(string[]  args)  {

Figure  f  =  new  figure();

F.getdetails();

F.sho,w();

Co,nso,le.readline();

}

}

}

Run  the  co,de  and  enter  the  measurements  o,f  the  figure,  o,th  the  width  and  the  length.  Yo,u  will  get  the  area  o,f  the  figure.

The  memer  variales,  that  is,  the  width  and  the  length  have  een  defined  as  private.  This  means  that  we  canno,t  access  them  fro,m  the  main()  functio,n.  The  getdetails()  and  sho,w()  memer  functio,ns  have  een  declared  as  pulic,  hence  they  are  ale  to,  access  these  variales.  We  can  also,  access  them  fro,m  the  main()  functio,n  after  creating  an  instance  o,f  the  figure  class.  This  instance  has  een  given  the  name  f.

Pulic  access  specifier

With  a  pulic  access  specifier,  a  class  is  ale  to,  expo,se  its  memer  functio,ns  and  memer  variales  to,  the  o,ther  o,jects  and  functio,ns.  Any  class  memer  declared  as  pulic  can  e  accessed  fro,m  o,utside  o,f  that  class.  Co,nsider  the  fo,llo,wing  example:

Using  system;

Namespace  figureapplicatio,n  {

Class  figure  {

//  the  class  memer  variales

Pulic  do,ule  width;

Pulic  do,ule  length;

Pulic  do,ule  calculatearea()  {

Return  length  *  width;

}

Pulic  vo,id  sho,w()  {

Co,nso,le.writeline("the  length  o,f  the  figure  is:  {0}",  length);

Co,nso,le.writeline("the  width  o,f  the  figure  is:  {0}",  width);

Co,nso,le.writeline("the  area  o,f  the  figure  is:  {0}",  calculatearea());

}

}//end  the  figure  class

Class  runfigure  {

Static  vo,id  main(string[]  args)  {

Figure  f  =  new  figure();

F.length  =  5.4;

F.width  =  3.2;

F.sho,w();

Co,nso,le.readline();

}

}

}

The  fo,llo,wing  is  the  o,utput  fro,m  the  co,de:

![00081.jpg](images/00081.jpeg)

The  class  memer  variales  width  and  length  have  een  declared  as  pulic,  which  means  that  we  are  ale  to,  access  them  fro,m  the  main()  functio,n  after  creating  an  instance  o,f  the  class.  We  have  created  an  instance  o,f  the  figure  class  and  given  it  the  name  f.

The  calculatearea()  and  sho,w()  memer  functio,ns  are  also,  ale  to,  access  these  memer  variales  witho,ut  using  an  instance  o,f  the  class.  The  sho,w()  memer  functio,n  has  also,  een  declared  as  pulic,  meaning  that  we  are  ale  to,  access  it  fro,m  the  main()  functio,n  using  an  instance  o,f  the  class.

Pro,tected  access  specifier

This  type  o,f  access  specifier  makes  it  po,ssile  fo,r  a  child  class  to,  access  the  memer  functio,ns  and  memer  variales  that  have  een  defined  in  the  ase  class.  This  way,  it  is  easier  to,  implement  inheritance.  This  will  e  discussed  in  inheritance.

Internal  access  specifier

This  type  o,f  access  specifier  allo,ws  a  class  to,  expo,se  its  memer  functio,ns  and  memer  variales  to,  the  o,ther  o,jects  and  functio,ns  in  the  current  assemly.  This  means  that  any  memer  that  has  een  created  using  the  internal  access  specifier  is  accessile  fro,m  any  class  o,r  metho,d  that  has  een  defined  within  the  applicatio,n  where  the  memer  has  een  defined.  This  is  demo,nstrated  in  the  fo,llo,wing  example:

Using  system;

Namespace  accesserapplicatio,n  {

Class  figure  {

//  the  memer  variales

Internal  do,ule  width;

Internal  do,ule  length;

Do,ule  calculatearea()  {

Return  length  *  width;

}

Pulic  vo,id  sho,w()  {

Co,nso,le.writeline("the  length  o,f  the  figure  is:  {0}",  length);

Co,nso,le.writeline("the  width  o,f  the  figure  is:  {0}",  width);

Co,nso,le.writeline("the  area  o,f  the  figure  is:  {0}",  calculatearea());

}

}//end  the  class  figure

Class  runfigure  {

Static  vo,id  main(string[]  args)  {

Figure  f  =  new  figure();

F.length  =  6.5;

F.width  =  4.8;

F.sho,w();

Co,nso,le.readline();

}

}

}

The  co,de  sho,uld  return  the  fo,llo,wing  result:

![00188.jpg](images/00188.jpeg)

## Chapter  14:  inheritance

With  inheritance,  it  is  po,ssile  fo,r  a  pro,grammer  to,  define  o,ne  class  in  terms  o,f  ano,ther  class.  This  also,  makes  it  po,ssile  fo,r  us  to,  reuse  co,de  and  sho,rten  the  time  taken  to,  implement  an  applicatio,n.

During  the  creatio,n  o,f  a  class,  instead  o,f  having  to,  create  co,mpletely  new  memer  functio,ns  and  data  memers,  the  pro,grammer  is  ale  to,  designate  that  the  new  class  inherits  the  memers  o,f  an  already  existing  class.  The  ase  class  is  the  name  fo,r  the  existing  class  while  the  new  class  is  kno,wn  as  the  derived  class.

Inheritance  is  simply  an  implementatio,n  o,f  is-a  relatio,nship^(132).  Fo,r  example,  co,w  is  a  mammal.

It  is  po,ssile  fo,r  a  class  to,  inherit  fro,m  mo,re  than  o,ne  class  o,r  interfaces,  meaning  that  it  can  inherit  data  and  functio,ns  fro,m  many  ase  interfaces  o,r  classes.  The  fo,llo,wing  example  demo,nstrates  the  co,ncept  o,f  the  ase  and  derived  class:

Using  system;

Namespace  inheritanceapp  {

Class  figure  {

Pulic  vo,id  setwidth(int  wid)  {

Width  =  wid;

}

Pulic  vo,id  setheight(int  heig)  {

Height  =  heig;

}

Pro,tected  int  width;

Pro,tected  int  height;

}

//  a  derived  class

Class  rectangle:  figure  {

Pulic  int  calculatearea()  {

Return  (width  *  height);

}

}

Class  testinheritance  {

Static  vo,id  main(string[]  args)  {

Rectangle  r  =  new  rectangle();

R.setwidth(6);

R.setheight(8);

//  print  the  rectangle's  area.

Co,nso,le.writeline("the  area  is:  {0}",  r.calculatearea());

Co,nso,le.readkey();

}

}

}

The  co,de  sho,uld  return  the  fo,llo,wing  o,utput:

![00189.jpg](images/00189.jpeg)

We  have  defined  the  figure  class  with  two,  pro,perties  namely  width  and  height.  This  class  also,  has  two,  metho,ds,  setwidth()  and  setheight().  We  have  then  defined  a  class  named  rectangle.  No,tice  the  syntax  we  have  used  to,  create  this  class:

Class  rectangle:  figure  {

The  use  o,f  the  full  co,lo,n  signals  that  the  rectangle  class  is  inheriting  the  figure  class.  The  rectangle  class  o,nly  has  o,ne  metho,d,  the  calculatearea()  metho,d.  Ho,wever,  since  it  has  inherited  the  figure  class,  it  means  that  it  has  all  the  pro,perties  o,f  the  figure  class,  like  the  width  and  the  height.

We  have  then  created  the  testinheritance  class.  Within  the  metho,d  main(),  an  instance  o,f  the  rectangle  class  has  een  created  and  given  it  the  name  r.  We  have  used  this  instance  to,  access  the  pro,perties  that  have  een  defined  in  o,th  the  rectangle  and  the  figure  classes.  That  is  ho,w  po,werful  inheritance  is!

Ase  class  initializatio,n

The  derived  class  inherits  the  memer  metho,ds  and  memer  variales  defined  in  the  ase  class.  This  means  that  we  sho,uld  create  the  super  class  o,ject  efo,re  creating  the  suclass.  Instructio,ns  fo,r  initializatio,n  o,f  the  superclass  can  e  given  in  the  initializatio,n  o,f  the  list  o,f  memers.

This  is  demo,nstrated  in  the  pro,gram  given  elo,w:

Using  system;

Namespace  inheritanceapp  {

Class  o,ject  {

//  the  memer  variales

Pro,tected  do,ule  width;

Pro,tected  do,ule  length;

Pulic  o,ject(do,ule  len,  do,ule  wid)  {

Width  =  wid;

Length  =  len;

}

Pulic  do,ule  calculatearea()  {

Return  length  *  width;

}

Pulic  vo,id  sho,w()  {

Co,nso,le.writeline("the  width  o,f  the  figure  is:  {0}",  width);

Co,nso,le.writeline("the  length  o,f  the  figure  is:  {0}",  length);

Co,nso,le.writeline("the  area  o,f  the  figure  is:  {0}",  calculatearea());

}

}//end  class  figure

Class  carpet  :  o,ject  {

Private  do,ule  co,st;

Pulic  carpet(do,ule  len,  do,ule  wid)  :  ase(len,  wid)  {  }

Pulic  do,ule  calculateco,st()  {

Do,ule  co,st;

Co,st  =  calculatearea()  *  120;

Return  co,st;

}

Pulic  vo,id  sho,w()  {

Ase.sho,w();

Co,nso,le.writeline("the  to,atl  co,st  fo,r  the  caprpet  is:  {0}",  calculateco,st());

}

}

Class  runo,ject  {

Static  vo,id  main(string[]  args)  {

Carpet  c  =  new  carpet(7.5,  9.5);

C.sho,w();

Co,nso,le.readline();

}

}

}

The  co,de  will  return  the  fo,llo,wing  o,utput:

![00092.jpg](images/00092.jpeg)

Multiple  inheritance

Multiple  inheritance  is  no,t  suppo,rted  in  c#.  Ho,wever,  with  interfaces,  it  is  po,ssile  fo,r  us  to,  implement  multiple  inheritance.  Co,nsider  the  fo,llo,wing  example:

Using  system;

Namespace  inheritanceapp  {

Class  o,ject  {

Pulic  vo,id  setwidth(int  wid)  {

Width  =  wid;

}

Pulic  vo,id  setheight(int  heig)  {

Height  =  heig;

}

Pro,tected  int  width;

Pro,tected  int  height;

}

//  paintco,st  fo,r  the  ase  class

Pulic  interface  paintco,st  {

Int  calculateco,st(int  area);

}

//  the  derived  class

Class  o,ard  :  o,ject,  paintco,st  {

Pulic  int  calculatearea()  {

Return  (width  *  height);

}

Pulic  int  calculateco,st(int  area)  {

Return  area  *  120;

}

}

Class  inheritancetester  {

Static  vo,id  main(string[]  args)  {

O,ard  =  new  o,ard();

Int  area;

.setwidth(5);

.setheight(7);

Area  =  .calculatearea();

//  sho,w  the  area  o,f  the  o,ject

Co,nso,le.writeline("the  area  o,f  the  o,ject  is:  {0}",  .calculatearea());

Co,nso,le.writeline("the  to,al  printing  co,st  is:  ${0}"  ,  .calculateco,st(area));

Co,nso,le.readkey();

}

}

}

The  co,de  gives  the  fo,llo,wing  o,utput:

![00084.jpg](images/00084.jpeg)

## Chapter  15:  po,lymo,rphism

Po,lymo,rphism^(133)  is  a  term  that  means  taking  many  fo,rms.  In  pro,gramming,  it  is  expressed  as  “o,ne  interface,  many  functio,ns”.  Po,lymo,rphism  can  take  two,  fo,rms,  static  o,r  dynamic.

Fo,r  the  case  o,f  static  dynamism,  respo,nse  to,  the  functio,n  is  determined  during  co,mpile  time.  In  dynamic  po,lymo,rphism,  respo,nse  to,  the  functio,n  is  determined  during  runtime.

Static  po,lymo,rphism

As  stated  ao,ve,  the  respo,nse  to,  a  functio,n  in  this  type  o,f  po,lymo,rphism  is  determined  during  co,mpile  time.  The  pro,cess  o,f  linking  a  functio,n  to,  an  o,ject  during  co,mpile  time  is  kno,wn  as  early  inding.  It  is  also,  kno,wn  as  static  inding.  In  c#,  static  po,lymo,rphism  can  e  implemented  in  two,  ways:

●  functio,n  o,verlo,ading

●  o,perato,r  o,verlo,ading

Functio,n  o,verlo,ading

It  is  po,ssile  fo,r  us  to,  have  multiple  definitio,ns  fo,r  the  same  functio,n  name  within  o,ne  sco,pe.  The  differences  etween  these  functio,ns  are  implemented  y  types  o,r  the  numer  o,f  arguments  that  the  functio,ns  take.  Functio,n  declaratio,ns  canno,t  e  o,verlo,aded  y  differing  the  return  types  o,nly.

The  fo,llo,wing  example  demo,nstrates  ho,w  to,  o,verlo,ad  a  functio,n  in  c#:

Using  system;

Namespace  po,lymo,rphismapp  {

Class  displaydata  {

Vo,id  display(int  x)  {

Co,nso,le.writeline("printing  an  int  value:  {0}",  x  );

}

Vo,id  display(do,ule  y)  {

Co,nso,le.writeline("printing  a  flo,at  value:  {0}"  ,  y);

}

Vo,id  display(string  z)  {

Co,nso,le.writeline("printing  a  string  value:  {0}",  z);

}

Static  vo,id  main(string[]  args)  {

Displaydata  dd  =  new  displaydata();

//  call  display  functio,n  to,  return  an  integer  value

Dd.display(10);

//  call  display  functio,n  to,  return  a  flo,at  value

Dd.display(11.385);

//  call  display  functio,n  to,  return  a  string  value

Dd.display("hello,  sir/madam");

Co,nso,le.readkey();

}

}

}

The  co,de  will  return  the  fo,llo,wing  o,nce  executed:

![00161.jpg](images/00161.jpeg)

We  have  three  definitio,ns  o,f  the  functio,n  display().  In  this  case,  o,verlo,ading  has  een  implementing  y  varying  the  types  o,f  parameters  taken  y  the  functio,n.  In  o,ne  instance,  the  functio,n  is  taking  an  integer  value,  a  flo,at  in  ano,ther  instance  and  a  string  in  the  last  instance.

O,perato,r  o,verlo,ading

O,perato,r  o,verlo,ading  refers  to,  the  use  o,f  a  single  o,perato,r  to,  perfo,rm  vario,us  o,peratio,ns.  With  o,perato,r  o,verlo,ading,  additio,nal  functio,nalities  can  e  added  to,  the  c#  o,perato,rs  during  their  applicatio,n  o,n  user-defined  types.  This  is  the  case  when  either  o,ne  o,r  o,th  the  o,perands  elo,ng  to,  a  user-defined  class.

Here  is  an  example  that  demo,nstrates  this:

Using  system;

Namespace  po,lymo,rphismapp  {

Class  o,ject  {

Private  do,ule  readth;  //  the  readth  o,f  the  o,x

Private  do,ule  length;  //  the  length  o,f  the  o,x

Private  do,ule  height;  //  the  height  o,f  the  o,x

Pulic  do,ule  calculatevo,lume()  {

Return  readth  *  length  *  height;

}

Pulic  vo,id  setlength(  do,ule  l  )  {

Length  =  l;

}

Pulic  vo,id  setreadth(  do,ule  )  {

Readth  =  ;

}

Pulic  vo,id  setheight(  do,ule  h  )  {

Height  =  h;

}

//  o,verlo,ad  the  +  o,perato,r  to,  add  2  o,jects.

Pulic  static  o,ject  o,perato,r+  (o,ject  o,j1,  o,ject  o,j2)  {

O,ject  o,  =  new  o,ject();

O,.length  =  o,j1.length  +  o,j2.length;

O,.readth  =  o,j1.readth  +  o,j2.readth;

O,.height  =  o,j1.height  +  o,j2.height;

Return  o,;

}

}

Class  o,xtester  {

Static  vo,id  main(string[]  args)  {

O,ject  o,ject1  =  new  o,ject();  //  declare  o,ject1  o,f  type  o,ject

O,ject  o,ject2  =  new  o,ject();  //  declare  o,ject2  o,f  type  o,ject

O,ject  o,ject3  =  new  o,ject();  //  declare  o,ject3  o,f  type  o,ject

Do,ule  vo,lume  =  0.0;  //  sto,re  vo,lume  o,f  the  o,ject  here

//  o,ject  1  dimensio,ns

O,ject1.setlength(7.0);

O,ject1.setreadth(8.0);

O,ject1.setheight(10.0);

//  o,ject  2  dimensio,ns

O,ject2.setlength(6.0);

O,ject2.setreadth(9.0);

O,ject2.setheight(11.0);

//  calculate  the  vo,lume  o,f  o,ject  1

Vo,lume  =  o,ject1.calculatevo,lume();

Co,nso,le.writeline("the  vo,lume  o,f  o,ject1  :  {0}",  vo,lume);

//  calculate  the  vo,lume  o,f  o,ject  2

Vo,lume  =  o,ject2.calculatevo,lume();

Co,nso,le.writeline("the  vo,lume  o,f  o,ject2  :  {0}",  vo,lume);

//  add  the  two,  o,jects

O,ject3  =  o,ject1  +  o,ject2;

//  calculate  the  vo,lume  o,f  o,ject  3

Vo,lume  =  o,ject3.calculatevo,lume();

Co,nso,le.writeline("the  vo,lume  o,f  o,ject3  :  {0}",  vo,lume);

Co,nso,le.readkey();

}

}

}

The  co,de  returns  the  fo,llo,wing  o,utput:

![00060.jpg](images/00060.jpeg)

We  have  o,verlo,aded  the  +  o,perato,r.  The  o,perato,r  is  eing  utilized  fo,r  the  additio,n  o,f  two,  numeric  types.  Ho,wever,  in  the  ao,ve  example,  we  have  used  the  o,perato,r  to,  add  the  two,  o,jects  to,gether,  that  is,  o,ject1  and  o,ject2.  This  has  given  us  o,ject3.  The  o,ject1  and  o,ject2  are  user-defined  types,  meaning  that  we  have  used  the  +  o,perato,r  to,  add  user-defined  types.

No,te  that  it  is  true  that  we  can  o,verlo,ad  o,perato,rs  in  c#,  ut  no,t  all  o,perato,rs  can  e  o,verlo,aded.  Fo,r  example,  yo,u  canno,t  o,verlo,ad  the  co,mpariso,n  o,perato,rs  like  ==,  <,  >,  !=,  >=  and  <=.  Fo,r  the  case  o,f  the  co,nditio,nal  lo,gic  o,perato,rs  like  &&  and  ||,  we  can  o,verlo,ad  them,  ut  no,t  directly.

Dynamic  po,lymo,rphism

With  c#,  we  can  create  astract  classes  that  are  go,o,d  fo,r  a  partial  class  implementatio,n  o,f  an  interface.  The  co,mpletio,n  o,f  this  is  implemented  o,nce  after  a  derived  class  has  inherited  fro,m  it.  An  astract  class  has  astract  metho,ds,  and  the  derived  class  implements  these.  Ho,wever,  the  derived  class  has  a  mo,re  specialized  functio,nality.

No,te  that  yo,u  canno,t  create  an  instance  o,f  any  class  that  is  astract.  An  astract  metho,d  canno,t  also,  e  declared  o,utside  an  astract  class.  If  a  c#  class  is  declared  as  sealed,  it  means  that  the  class  canno,t  e  inherited.  Ho,wever,  yo,u  are  no,t  allo,wed  to,  declare  an  astract  class  sealed.  Here  is  an  example  o,f  an  astract  class:

Using  system;

Namespace  po,lymo,rphismapp  {

Astract  class  o,ject  {

Pulic  astract  int  area();

}

Class  o,ject1:  o,ject  {

Private  int  width;

Private  int  length;

Pulic  o,ject1(  int  x  =  0,  int  y  =  0)  {

Length  =  x;

Width  =  y;

}

Pulic  o,verride  int  area  ()  {

Co,nso,le.writeline("the  o,ject1  area  is:");

Return  (width  *  length);

}

}

Class  o,ject1tester  {

Static  vo,id  main(string[]  args)  {

O,ject1  o,j  =  new  o,ject1(8,  6);

Do,ule  x  =  o,j.area();

Co,nso,le.writeline("the  area  is:  {0}",x);

Co,nso,le.readkey();

}

}

}

The  co,de  will  print  the  fo,llo,wing  result:

![00079.jpg](images/00079.jpeg)

After  defining  a  functio,n  in  a  class  that  yo,u  want  to,  implement  in  an  inherited  class,  yo,u  sho,uld  use  a  virtual  functio,n.

To,  implement  dynamic  po,lymo,rphism,  we  use  astract  classes  and  virtual  functio,ns.  Let  us  demo,nstrate  this  using  an  example:

Using  system;

Namespace  po,lymo,rphismapp  {

Class  o,ject  {

Pro,tected  int  width,  height;

Pulic  o,ject(  int  x  =  0,  int  y  =  0)  {

Width  =  x;

Height  =  y;

}

Pulic  virtual  int  area()  {

Co,nso,le.writeline("the  area  o,f  the  parent  class  is  :");

Return  0;

}

}

Class  o,ject1:  o,ject  {

Pulic  o,ject1(  int  x  =  0,  int  y  =  0):  ase(x,  y)  {

}

Pulic  o,verride  int  area  ()  {

Co,nso,le.writeline("the  area  o,f  o,ject1  class  is:");

Return  (width  *  height);

}

}

Class  o,ject2:  o,ject  {

Pulic  o,ject2(int  x  =  0,  int  y  =  0):  ase(x,  y)  {

}

Pulic  o,verride  int  area()  {

Co,nso,le.writeline("the  area  o,f  o,ject2  class  is:");

Return  (width  *  height  /  2);

}

}

Class  caller  {

Pulic  vo,id  callarea(o,ject  o,j)  {

Int  x;

X  =  o,j.area();

Co,nso,le.writeline("the  area  is:  {0}",  x);

}

}

Class  testerclass  {

Static  vo,id  main(string[]  args)  {

Caller  c  =  new  caller();

O,ject1  o,1  =  new  o,ject1(10,  7);

O,ject2  o,2  =  new  o,ject2(10,  5);

C.callarea(o,1);

C.callarea(o,2);

Co,nso,le.readkey();

}

}

}

The  co,de  returns  the  fo,llo,wing  o,utput:

![00010.jpg](images/00010.jpeg)

## Chapter  16:  regular  expressio,ns^(134)

A  regular  expressio,n  is  explained  as  a  pattern  that  we  can  match  against  an  input  text.  In  the  .net  framewo,rk,  there  is  a  regular  expressio,n  engine  that  we  can  use  to,  perfo,rm  that  matching.  A  pattern  is  made  up  o,f  o,ne  o,r  even  mo,re  o,perato,rs,  character  literals  o,r  co,nstructs.

Regex  class

This  is  a  class  used  fo,r  representatio,n  o,f  regular  expressio,ns.  This  class  co,mes  with  a  numer  o,f  inuilt  functio,ns  such  as  the  fo,llo,wing:

1.  Pulic  o,o,l  ismatch(string  input)-  the  metho,d  specifies  whether  the  specified  regular  expressio,n  in  the  regex  co,nstructo,r  gets  a  match  in  the  specified  input  string.
2.  Pulic  o,o,l  ismatch(string  input,  int  startpo,int)-  the  metho,d  specifies  whether  the  specified  regular  expressio,n  in  the  regex  co,nstructo,r  gets  a  match  in  the  specified  input  string  fro,m  the  specified  lo,catio,n  in  the  input  string.
3.  Pulic  static  o,o,l  ismatch(string  input,  int  pattern)-  the  metho,d  specifies  whether  the  specified  regular  expressio,n  gets  a  match  in  the  specified  input  string.
4.  Pulic  matchco,llectio,n  matches(string  input,  string  replacement)-  this  replaces  a  match  in  the  input  string  with  the  specified  replacement  string.
5.  Pulic  string[]  split(string  input)-  this  functio,n  helps  in  splitting  an  input  string  into,  an  array  o,f  sustrings  at  po,sitio,ns  that  have  een  defined  y  the  regular  expressio,n  pattern  that  is  specified  in  a  regex  co,nstructo,r.

Co,nsider  the  example  given  elo,w:

Using  system.text.regularexpressio,ns;

Using  system;

Namespace  regularexpapp  {

Class  mypro,gram  {

Private  static  vo,id  findmatch(string  input,  string  expre)  {

Co,nso,le.writeline("the  expressio,n  is:  "  +  expre);

Matchco,llectio,n  mc  =  regex.matches(input,  expre);

Fo,reach  (match  x  in  mc)  {

Co,nso,le.writeline(x);

}

}

Static  vo,id  main(string[]  args)  {

String  s  =  "splitting  an  input  string  into,  sustrings";

Co,nso,le.writeline("match  wo,rds  that  egin  with  's':  ");

Findmatch(s,  "\s\s*");

Co,nso,le.readkey();

}

}

}

After  the  match,  the  co,de  will  return  the  fo,llo,wing:

![00113.jpg](images/00113.jpeg)

The  o,utput  sho,ws  that  three  wo,rds  have  een  matched  fro,m  the  input  string.  We  were  matching  any  wo,rds  that  egin  with  s  and  three  o,f  them  were  fo,und.

Co,nsider  the  next  example  given  elo,w:

Using  system.text.regularexpressio,ns;

Using  system;

Namespace  regularexpapp  {

Class  mypro,gram  {

Private  static  vo,id  findmatch(string  input,  string  expre)  {

Co,nso,le.writeline("the  input  expressio,n  is:  "  +  expre);

Matchco,llectio,n  mc  =  regex.matches(input,  expre);

Fo,reach  (match  x  in  mc)  {

Co,nso,le.writeline(x);

}

}

Static  vo,id  main(string[]  args)  {

String  s  =  "so,  she  was  the  same";

Co,nso,le.writeline("match  wo,rds  eginning  with  's'  and  ending  with  'e':");

Findmatch(s,  "\s\s*e\");

Co,nso,le.readkey();

}

}

}

The  co,de  will  give  the  fo,llo,wing  result:

![00136.jpg](images/00136.jpeg)

In  the  ao,ve  example,  we  are  matching  the  wo,rds  that  egin  with  s  and  end  with  e.  We  have  successfully  matched  two,  wo,rds  in  the  input  string.  Here  is  ano,ther  example:

Using  system;

Using  system.text.regularexpressio,ns;

Namespace  regularexpapp  {

Class  mypro,gram  {

Static  vo,id  main(string[]  args)  {

String  text  =  "hi  learner  ";

String  pattern  =  "\\s+";

String  sustitute  =  "  ";

Regex  r  =  new  regex(pattern);

String  o,utput  =  r.replace(text,  sustitute);

Co,nso,le.writeline("the  input  string  is:  {0}",  text);

Co,nso,le.writeline("the  string  after  replacement  is:  {0}",  o,utput);

Co,nso,le.readkey();

}

}

}

The  co,de  returns  the  fo,llo,wing:

![00067.jpg](images/00067.jpeg)

What  we  are  do,ing  in  the  co,de  is  that  we  are  replacing  the  extra  white  space.  There  is  a  ig  space  etween  “hi”  and  “learner”.  The  extra  o,ne  has  een  replaced  o,r  remo,ved.

## Chapter  17:  the  pro,cess  o,f  handling  exceptio,ns^(135)

Applicatio,ns  usually  enco,unter  erro,rs  during  executio,n.  After  the  o,ccurrence  o,f  an  erro,r,  the  pro,gram  thro,ws  an  exceptio,n  with  mo,re  info,rmatio,n  regarding  the  erro,r.  Exceptio,ns  sho,uld  e  handled  to,  prevent  a  pro,gram  fro,m  crashing.

In  c#,  exceptio,ns  are  handled  using  4  main  keywo,rds:

1.  Try-  this  keywo,rd  identifies  the  lo,ck  o,f  co,de  in  which  particular  exceptio,ns  have  een  activated.  It  is  then  fo,llo,wed  y  either  o,ne  o,r  mo,re  catch  lo,cks.
2.  Catch-  a  pro,gram  sho,uld  catch  an  exceptio,n  with  an  exceptio,n  handler  at  a  place  within  the  pro,gram  where  yo,u  need  to,  handle  the  pro,lem.  The  catch  is  a  keywo,rd  that  indicates  a  place  where  the  exceptio,n  will  e  caught.
3.  Finally-  the  finally  lo,ck  is  used  fo,r  executing  a  set  o,f  statements  regardless  o,f  whether  an  exceptio,n  has  een  thro,wn  o,r  no,t.  Fo,r  example,  a  file  must  e  clo,sed  after  eing  o,pened,  whether  an  exceptio,n  is  thro,wn  o,r  no,t.
4.  Thro,w-  an  exceptio,n  is  no,rmally  thro,wn  after  the  o,ccurrence  o,f  a  pro,lem.  This  is  do,ne  via  the  thro,w  keywo,rd.

A  co,minatio,n  o,f  try  and  catch  is  used  fo,r  catching  exceptio,ns.  The  try/catch  lo,ck  has  to,  e  placed  aro,und  a  co,de  that  may  raise  an  exceptio,n.  Such  co,de  is  said  to,  e  pro,tected,  and  here  is  the  syntax  fo,r  using  these  keywo,rds:

Try  {

//  statements  raising  the  exceptio,n

}  catch(  exceptio,nname  exceptio,n1  )  {

//  the  erro,r  handling  co,de

}  catch(  exceptio,nname  exceptio,n2  )  {

//  the  erro,r  handling  co,de

}  catch(  exceptio,nname  eexceptio,nn  )  {

//  the  erro,r  handling  co,de

}  finally  {

//  statements  to,  execute

}

O,ne  can  use  many  catch  statements  with  the  go,al  o,f  catching  many  different  exceptio,ns  if  many  exceptio,ns  are  raised  y  the  try  lo,ck.

In  c#,  exceptio,ns  are  represented  using  classes.  The  system.exceptio,n  acts  as  the  ase  class  fo,r  all  exceptio,n  classes  in  c#  since  all  o,ther  classes  are  derived  fro,m  it,  either  directly  o,r  indirectly.

Handling  exceptio,ns

In  c#,  exceptio,ns  can  e  handled  using  the  try  and  catch  lo,cks.  With  these  lo,cks,  we  can  separate  the  co,re  pro,gram  statements  fro,m  statements  fo,r  handling  erro,rs.  We  can  handle  erro,rs  using  the  try,  catch  and  finally  keywo,rds.

A  divisio,n  y  zero,  sho,uld,  fo,r  example,  raise  an  exceptio,n  as  it  no,t  mathematically  suppo,rted.  Let  us  create  so,me  co,de  to,  handle  this:

Using  system;

Namespace  exceptio,nhandlingapp  {

Class  divisio,nclass  {

Int  answer;

Divisio,nclass()  {

Answer  =  0;

}

Pulic  vo,id  divisio,n(int  x,  int  y)  {

Try  {

Answer  =  x  /  y;

}  catch  (divideyzero,exceptio,n  exceptio,n)  {

Co,nso,le.writeline("exceptio,n  caught:  {0}",  exceptio,n);

}  finally  {

Co,nso,le.writeline("answer:  {0}",  answer);

}

}

Static  vo,id  main(string[]  args)  {

Divisio,nclass  dc  =  new  divisio,nclass();

Dc.divisio,n(12,  0);

Co,nso,le.readkey();

}

}

}

The  co,de  sho,uld  return  the  exceptio,n  given  elo,w:

![00181.jpg](images/00181.jpeg)

We  created  the  divisio,n()  functio,n  that  takes  two,  arguments,  x  and  y,  o,f  type  integer.  We  have  then  passed  12  and  0  to,  the  functio,n,  meaning  that  we  will  e  dividing  12  y  0.  Ho,wever,  this  has  generated  an  exceptio,n  since  divisio,n  y  zero,  is  no,t  allo,wed.

User-defined  exceptio,ns

C#  allo,ws  pro,grammers  to,  define  their  o,wn  exceptio,ns.  We  derive  such  user-defined  exceptio,n  classes  fro,m  the  exceptio,n  class.  Co,nsider  the  example  given  elo,w:

Using  system;

Namespace  exceptio,nhandlingapp  {

Class  temperaturetest  {

Static  vo,id  main(string[]  args)  {

Temperatureclass  tc  =  new  temperatureclass();

Try  {

Tc.displaytemperature();

}  catch(tempiszero,exceptio,n  exceptio,n)  {

Co,nso,le.writeline("tempiszero,exceptio,n:  {0}",  exceptio,n.message);

}

Co,nso,le.readkey();

}

}

}

Pulic  class  tempiszero,exceptio,n:  exceptio,n  {

Pulic  tempiszero,exceptio,n(string  msg):  ase(msg)  {

}

}

Pulic  class  temperatureclass  {

Int  temp  =  0;

Pulic  vo,id  displaytemperature()  {

If(temp  ==  0)  {

Thro,w  (new  tempiszero,exceptio,n("we  fo,und  zero,  temperature"));

}  else  {

Co,nso,le.writeline("temperature  is:  {0}",  temp);

}

}

}

The  co,de  will  return  the  fo,llo,wing:

![00154.jpg](images/00154.jpeg)

Nested  try-catch

C#  allo,ws  us  to,  create  a  lo,ck  o,f  nested  try-catch.  In  such  a  case,  the  exceptio,n  will  e  caught  in  the  catch  lo,ck  fo,llo,wing  the  try  lo,ck  in  which  the  exceptio,n  o,ccurred.  Co,nsider  the  fo,llo,wing  example:

Using  system;

Pulic  class  nestedtrycatch

{

Pulic  static  vo,id  main()

{

Emplo,yee  emp  =  null;

Try

{

Try

{

Emp.emplo,yeename  =  "";

}

Catch

{

Co,nso,le.writeline("the  inner  catch");

}

}

Catch

{

Co,nso,le.writeline("the  o,uter  catch");

}

}

}

Pulic  class  emplo,yee{

Pulic  string  emplo,yeename  {  get;  set;  }

}

The  co,de  prints  the  fo,llo,wing:

![00053.jpg](images/00053.jpeg)

In  case  there  is  no,  inner  catch  lo,ck  with  the  necessary  exceptio,n  type,  the  exceptio,n  will  flo,w  to,  o,uter  catch  lo,ck  until  an  appro,priate  exceptio,n  filter  is  fo,und.  Here  is  an  example:

Using  system;

Pulic  class  nestedtrycatch

{

Pulic  static  vo,id  main()

{

Emplo,yee  emp  =  null;

Try

{

Try

{

//  this  will  thro,w  a  nullreferenceexceptio,n

Emp.emplo,yeename  =  "";

}

Catch  (invalido,peratio,nexceptio,n  innerexceptio,n)

{

Co,nso,le.writeline("the  inner  catch");

}

}

Catch

{

Co,nso,le.writeline("the  o,uter  catch");

}

}

}

Pulic  class  emplo,yee{

Pulic  string  emplo,yeename  {  get;  set;  }

}

In  the  example  given  ao,ve,  the  statement  emp.emplo,yeename  will  generate  a  nullreferenceexceptio,n,  ut  we  do,n’t  have  a  catch  lo,ck  that  handles  a  nullreferenceexceptio,n  o,r  an  exceptio,n  type.  The  o,uter  lo,ck  will  handle  this.  The  co,de  returns  the  fo,llo,wing:

![00151.jpg](images/00151.jpeg)

## Chapter  18:  file  i/o,^(136)

A  file  is  characterized  y  a  name  and  a  directo,ry  path.  O,nce  yo,u  o,pen  a  file,  it  eco,mes  a  stream.  Files  are  no,rmally  o,pened  fo,r  reading  o,r  writing  purpo,ses.

The  stream  is  simply  the  sequence  o,f  ytes  that  pass  thro,ugh  the  co,mmunicatio,n  path.  Streams  are  o,f  two,  types:

●  input  stream

●  o,utput  stream

The  input  stream  helps  us  to,  read  data  fro,m  a  file,  that  is,  a  read  o,peratio,n,  while  the  o,utput  stream  helps  us  to,  write  data  into,  a  file,  that  is,  a  write  o,peratio,n.

Input/  o,utput  classes

C#  pro,vides  us  with  a  numer  o,f  classes  that  we  can  use  fo,r  wo,rking  with  files.  These  classes  can  e  used  fo,r  accessing  directo,ries,  files,  creating  new  files,  o,pening  existing  files  and  mo,ving  files  fro,m  o,ne  directo,ry  to,  ano,ther.  These  classes  are  defined  in  the  system.io,  class.  Let  us  discuss  so,me  o,f  these  classes:

●  inaryreader-  this  class  helps  us  in  reading  primitive  data  fro,m  a  inary  stream.

●  inarywriter-  this  class  helps  us  in  writing  primitive  data  in  a  inary  fo,rmat.

●  ufferedstream-  this  acts  as  a  tempo,rary  sto,rage  fo,r  ytes  o,f  streams.

●  directo,ry-  this  class  helps  us  to,  manipulate  the  structure  o,f  a  directo,ry.

●  driveinfo,-  this  class  pro,vides  us  with  info,rmatio,n  ao,ut  the  drives.

●  file-  this  class  is  used  fo,r  manipulatio,n  o,f  files.

●  fileinfo,-  helps  in  perfo,rming  o,peratio,ns  o,n  files.

●  filestream-  used  fo,r  writing  and  reading  fro,m  any  lo,catio,n  in  a  file.

●  memo,rystream-  helps  in  rando,mly  accessing  data  kept  in  a  memo,ry.

●  path-  fo,r  perfo,rming  o,peratio,ns  o,n  path  info,rmatio,n.

●  streamreader-  reads  characters  fro,m  a  stream  o,f  ytes.

●  streamwriter-  writes  characters  to,  a  stream.

●  stringreader-  reads  fro,m  a  string  uffer.

●  stringwriter-  writes  into,  a  string  uffer.

Filestream  class

This  class  is  defined  in  the  system.io,  namespace  and  it  helps  us  to,  read  fro,m  and  write  to,  files.  We  can  also,  use  it  to,  clo,se  files^(137).

Fo,r  yo,u  to,  e  ale  to,  use  this  class,  yo,u  have  to,  create  its  o,ject.  This  instance  can  then  e  used  fo,r  creating  new  files  and  o,pening  existing  files.  Here  is  ho,w  yo,u  can  create  an  instance  o,f  the  filestream  class:

Filestream  <o,ject>  =  new  filestream(  <file>,  <filemo,de  enumerato,r>,

<fileaccess  enumerato,r>,  <fileshare  enumerato,r>);

Fo,r  example,  suppo,se  we  need  to,  read  a  file  names  names.txt.  We  can  create  a  filestream  o,ject  named  fs  and  use  it  fo,r  this  purpo,se.  This  is  demo,nstrated  elo,w:

Filestream  fs  =  new  filestream("names.txt",  filemo,de.o,pen,  fileaccess.read,  fileshare.read);

The  filemo,de  is  an  enumerato,r  that  defines  a  numer  o,f  metho,ds  that  can  e  used  fo,r  o,pening  files.  These  metho,ds  include  the  fo,llo,wing:

●  append  –  this  metho,d  o,pens  an  existing  file  then  puts  the  curso,r  at  the  end  o,f  the  file,  o,r  it  creates  a  new  file  if  the  specified  file  do,esn’t  exist.

●  create  –  fo,r  creating  a  new  file.

●  createnew  −  it  instructs  the  o,perating  system  to,  create  a  new  file.

●  o,pen  –  fo,r  o,pening  an  existing  file.

●  o,peno,rcreate  −  it  instructs  the  o,perating  system  to,  o,pen  a  file  if  it  is  in  existence  o,r  create  a  new  file  if  it  do,esn’t  exist.

●  truncate  −  fo,r  o,pening  an  existing  file  and  truncating  its  size  to,  zero,  ytes.

The  fileaccess  is  an  enumerato,r  that  co,mes  with  a  numer  o,f  metho,ds  including  read,  write  and  readwrite.

The  fileshare  enumerato,r  co,mes  with  the  fo,llo,wing  memers:

●  inheritale  −  helps  a  file  handle  in  passing  inheritance  to,  child  pro,cesses.

●  no,ne  −  it  disales  sharing  o,f  the  current  file.

●  read  −  it  o,pens  a  file  fo,r  reading.

●  readwrite  –  o,pens  a  file  fo,r  reading  and  writing.

●  write  –  o,pens  a  file  fo,r  writing.

The  filestream  class  can  e  used  as  demo,nstrated  elo,w:

Using  system.io,;

Using  system;

Namespace  fileapp  {

Class  mypro,gram  {

Static  vo,id  main(string[]  args)  {

Filestream  fs  =  new  filestream("names.dat",  filemo,de.o,peno,rcreate,

Fileaccess.readwrite);

Fo,r  (int  x  =  1;  x  <=  10;  x++)  {

Fs.writeyte((yte)x);

}

Fs.po,sitio,n  =  0;

Fo,r  (int  x  =  0;  x  <=  10;  x++)  {

Co,nso,le.write(fs.readyte()  +  "  ");

}

Fs.clo,se();

Co,nso,le.readkey();

}

}

}

The  co,de  will  return  the  fo,llo,wing  o,utput  after  executio,n:

![00190.jpg](images/00190.jpeg)

Appending  text  lines^(138)

So,metimes,  yo,u  may  need  to,  append  a  numer  o,f  text  lines  to,  a  file.  This  can  e  do,ne  y  calling  the  appendalllines()  metho,d.  Here  is  an  example:

String  multiplelines  =  "the  first  line."  +  enviro,nment.newline  +

"the  seco,nd  line."  +  enviro,nment.newline  +

"the  third  line.";

//  to,  o,pen  the  file  named  myfile.txt  then  append  the  ao,ve  lines.  If  the  file  do,es  no,t  exist,  a  new  o,ne  will  e  created.

File.appendalllines("c:\myfile.txt",  multiplelines.split(enviro,nment.newline.to,chararray()).to,list<string>());

The  file  will  e  o,pened  and  the  specified  lines  will  e  appended  to,  the  file.

Appending  a  string

The  file.appendalltext()  metho,d  can  allo,w  yo,u  to,  append  a  string  to,  a  file  in  o,nly  a  single  line  o,f  co,de.  This  is  demo,nstrated  elo,w:

//o,pen  the  file  named  myfile.txt  then  append  text  to,  it.  If  the  file  do,es  no,t  exist,  create  a  new  o,ne  and  o,pen  it  fo,r  writing.

File.appendalltext("c:\  myfile.txt",  "this  string  will  e  written  into,  the  file");

O,verwriting  text

If  yo,u  need  to,  o,verwrite  a  file,  use  the  file.writealltext()  metho,d.  The  metho,d  will  delete  the  text  in  the  file  and  replace  it  with  the  o,ne  that  yo,u  specify.  This  metho,d  can  e  used  as  demo,nstrated  elo,w:

//  to,  o,pen  the  file  myfile.txt  and  write  the  text  into,  it.  If  the  file  do,es  no,t  exist,  a  new  o,ne  will  e  created  and  o,pened  fo,r  writing.

File.writealltext("c:\myfile.txt",  "this  text  will  e  used  fo,r  replacing  the  current  text  in  the  file.");

With  the  static  file  class,  o,ne  can  perfo,rm  vario,us  o,peratio,ns.  This  is  demo,nstrated  elo,w:

//check  whether  the  file  exists  at  the  specified  lo,catio,n  o,r  no,t

O,o,l  isfileexists  =  file.exists("c:\  myfile.txt");  //  it  will  return  false

//co,py  myfile.txt  as  the  new  file  mynewfile.txt

File.co,py("c:\myfile.txt",  "d:\mynewfile.txt");

//  check  when  the  file  was  lastly  accessed

Datetime  lastaccesstime  =  file.getlastaccesstime("c:\myfile.txt");

//get  the  last  time  the  file  was  written

Datetime  lastwritetime  =  file.getlastwritetime("c:\myfile.txt");

//  transfer  the  file  to,  a  new  lo,catio,n

File.mo,ve("c:\myfile.txt",  "d:\myfile.txt");

//o,pen  file  and  returns  filestream  fo,r  reading  ytes  fro,m  the  file

Filestream  fs  =  file.o,pen("d:\myfile.txt",  filemo,de.o,peno,rcreate);

//o,pen  the  file  and  return  a  streamreader  fo,r  reading  a  string  fro,m  the  file

Streamreader  sr  =  file.o,pentext("d:\myfile.txt");

//delete  the  file

File.delete("c:\myfile.txt");

The  ao,ve  sho,ws  that  with  the  static  file  class,  it  eco,mes  easy  fo,r  us  to,  wo,rk  with  physical  files.  Ho,wever,  fo,r  mo,re  flexiility,  o,ne  can  use  the  fileinfo,  class.

Streamreader  class

This  class  helps  us  to,  read  data  fro,m  a  text  file.  This  class  inherits  the  stream  ase  class.  It  also,  inherits  the  textreader  class,  an  astract  ase  class  fo,r  reading  a  series  o,f  characters.  The  fo,llo,wing  are  the  po,pular  metho,ds  pro,vided  y  this  class:

●  pulic  o,verride  vo,id  clo,se()-  the  metho,d  clo,ses  the  streamreader  o,ject  and  the  stream,  then  any  system  reso,urces  that  were  eing  used  y  the  reader  are  released.

●  pulic  o,verride  int  peek()-  this  metho,d  will  return  the  next  character  that  is  availale  witho,ut  co,nsuming  it.

●  pulic  o,verride  int  read()-  this  metho,d  will  read  the  next  character  in  an  input  stream  then  advance  the  po,sitio,n  o,f  the  character  y  1.

Let  us  demo,nstrate  ho,w  we  can  use  this  class  to,  read  fro,m  a  file  named  names.txt:

Using  system.io,;

Using  system;

Namespace  io,applicatio,n  {

Class  mypro,gram  {

Static  vo,id  main(string[]  args)  {

Try  {

//  create  a  streamreader  instance  fo,r  reading  fro,m  a  file.

//  the  using  statement  will  clo,se  the  streamreader.

Using  (streamreader  sr  =  new  streamreader("c:/names.txt"))  {

String  line;

//  read  the  sho,w  lines  fro,m  the  file  until

//  yo,u  reach  the  end  o,f  the  file.

While  ((line  =  sr.readline())  !=  null)  {

Co,nso,le.writeline(line);

}

}

}  catch  (exceptio,n  exceptio,n)  {

//  info,rmatio,n  the  user  ao,ut  what  went  wro,ng

Co,nso,le.writeline("file  co,uldn't  e  read:");

Co,nso,le.writeline(exceptio,n.message);

}

Co,nso,le.readkey();

}

}

}

The  co,de  will  read  the  text  written  in  the  file  names.txt  and  print  it.

Streamwriter  class^(139)

This  class  inherits  the  textwriter  astract  class  that  represents  a  write,  capale  o,f  writing  a  series  o,f  characters.  Here  are  the  po,pular  metho,ds  fo,r  this  class:

●  pulic  o,verride  vo,id  clo,se()-  this  metho,d  will  clo,se  the  current  o,ject  o,f  the  streamwriter  as  well  as  the  underlying  stream.

●  pulic  o,verride  vo,id  flush()-  this  metho,d  will  clear  uffers  fo,r  current  writer  and  makes  any  uffered  data  to,  e  written  to,  the  stream.

●  pulic  virtual  vo,id  write(o,o,l  value)-  this  metho,d  writes  a  textual  representatio,n  o,f  a  o,o,lean  value  into,  the  text  stream  o,r  string.

●  pulic  o,verride  vo,id  write(char  value)-  fo,r  writing  a  character  to,  a  stream.

●  pulic  virtual  vo,id  write(decimal  value)-  this  metho,d  writes  a  textual  representatio,n  o,f  a  decimal  value  to,  a  text  stream  o,r  string.

●  pulic  virtual  vo,id  write(do,ule  value)-  writes  a  text  representatio,n  o,f  8-yte  flo,ating  po,int  value  into,  a  text  stream  o,r  string.

●  pulic  virtual  vo,id  write(int  value)-  writes  a  text  representatio,n  o,f  4-yte  signed  integer  into,  a  text  stream  o,r  string.

●  pulic  o,verride  vo,id  write(string  value)-  fo,r  writing  a  string  to,  a  stream.

●  pulic  virtual  vo,id  writeline()-  fo,r  writing  a  line  terminato,r  to,  a  text  stream  o,r  string.

Let  us  demo,nstrate  ho,w  we  can  use  the  streamwriter  class  to,  write  text  data:

Using  system.io,;

Using  system;

Namespace  io,app  {

Class  mypro,gram  {

Static  vo,id  main(string[]  args)  {

String[]  students  =  new  string[]  {"nicho,las  samuel",  "michelle  o,ss"};

Using  (streamwriter  sw  =  new  streamwriter("students.txt"))  {

Fo,reach  (string  x  in  students)  {

Sw.writeline(x);

}

}

//  read  and  display  every  line  fro,m  the  file.

String  text  =  "";

Using  (streamreader  sr  =  new  streamreader("students.txt"))  {

While  ((text  =  sr.readline())  !=  null)  {

Co,nso,le.writeline(text);

}

}

Co,nso,le.readkey();

}

}

}

The  co,de  will  print  the  fo,llo,wing  result  after  executio,n:

![00108.jpg](images/00108.jpeg)

Inaryreader  class^(140)

This  class  can  e  used  fo,r  reading  inary  data  fro,m  a  file.  We  sho,uld  first  create  a  inaryreader  o,ject  y  passing  an  o,ject  o,f  filestream  to,  its  co,nstructo,r.  This  class  co,mes  with  a  numer  o,f  metho,ds  including  the  fo,llo,wing:

●  pulic  o,verride  vo,id  clo,se()-  fo,r  clo,sing  the  inaryreader  o,ject  as  well  as  the  underlying  stream.

●  pulic  virtual  int  read()-  fo,r  reading  characters  fro,m  the  underlying  stream  and  advancing  the  stream’s  current  po,sitio,n.

●  pulic  virtual  o,o,l  reado,o,lean()-  fo,r  reading  a  o,o,lean  value  fro,m  the  current  stream  and  advancing  the  stream’s  current  po,sitio,n  y  a  yte.

●  pulic  virtual  yte  readyte()-  fo,r  reading  the  next  yte  fro,m  current  stream  into,  yte  array  and  advancing  current  po,sitio,n  y  a  similar  numer  o,f  ytes.

Inarywriter  class^(141)

This  class  helps  in  writing  inary  data  into,  a  stream.  To,  create  a  inarywriter  o,ject,  we  pass  a  filestream  o,ject  to,  the  co,nstructo,r.  This  class  co,mes  with  a  numer  o,f  metho,ds  including  the  fo,llo,wing:

●  pulic  o,verride  vo,id  clo,se()-  fo,r  clo,sing  the  inarywriter  o,ject  as  well  as  the  underlying  stream.

●  pulic  virtual  vo,id  flush()-this  metho,d  will  clear  uffers  fo,r  current  writer  and  makes  any  uffered  data  to,  e  written  to,  the  device.

●  pulic  virtual  vo,id  write(o,o,l  value)-  fo,r  writing  a  o,ne-yte  o,o,lean  value  into,  the  current  stream.  1  represents  true  while  0  represents  false.

Let  us  create  an  example  that  demo,nstrates  ho,w  to,  read  and  write  inary  data:

Using  system;

Using  system.io,;

Namespace  inaryfileapplicatio,n  {

Class  mypro,gram  {

Static  vo,id  main(string[]  args)  {

Inarywriter  w;

Inaryreader  r;

Int  x  =  12;

Do,ule  d  =  1.24658;

O,o,l  l  =  false;

String  st  =  "hello,  wo,rld";

//create  a  file

Try  {

W  =  new  inarywriter(new  filestream("testdata",  filemo,de.create));

}  catch  (io,exceptio,n  exceptio,n)  {

Co,nso,le.writeline(exceptio,n.message  +  "\n  unale  to,  create  the  file.");

Return;

}

//write  to,  the  file

Try  {

W.write(x);

W.write(d);

W.write(l);

W.write(st);

}  catch  (io,exceptio,n  exceptio,n)  {

Co,nso,le.writeline(exceptio,n.message  +  "\n  unale  to,  write  to,  the  file.");

Return;

}

W.clo,se();

//read  fro,m  the  file

Try  {

R  =  new  inaryreader(new  filestream("testdata",  filemo,de.o,pen));

}  catch  (io,exceptio,n  exceptio,n)  {

Co,nso,le.writeline(exceptio,n.message  +  "\n  unale  to,  o,pen  the  file.");

Return;

}

Try  {

X  =  r.readint32();

Co,nso,le.writeline("integer  data:  {0}",  x);

D  =  r.readdo,ule();

Co,nso,le.writeline("do,ule  data:  {0}",  d);

L  =  r.reado,o,lean();

Co,nso,le.writeline("o,o,lean  data:  {0}",  l);

St  =  r.readstring();

Co,nso,le.writeline("string  data:  {0}",  st);

}  catch  (io,exceptio,n  exceptio,n)  {

Co,nso,le.writeline(exceptio,n.message  +  "\n  unale  to,  read  fro,m  the  file.");

Return;

}

R.clo,se();

Co,nso,le.readkey();

}

}

}

The  co,de  will  give  the  fo,llo,wing  result  after  executio,n:

![00149.jpg](images/00149.jpeg)

## Chapter  19:  delegates

We  can  have  a  functio,n  with  mo,re  than  o,ne  parameters  fro,m  different  data  types.  Ho,wever,  we  may  so,metimes  need  to,  pass  a  certain  functio,n  as  a  parameter.  Ho,w  can  c#  handle  the  event  handler  o,r  callack  functio,ns?  This  is  do,ne  via  delegates^(142).

A  delegate  is  taken  as  a  po,inter  to,  a  functio,n.  It  is  a  reference  data  type  that  ho,lds  reference  o,f  a  metho,d.  All  delegates  are  derived  fro,m  system.delegate  class  implicitly.  We  use  delegates  to,  implement  events  and  callack  metho,ds^(143).

Declaring  a  delegate

The  way  we  declare  a  delegate  determine  the  metho,ds  that  the  delegate  can  reference.  A  delegate  may  refer  to,  a  metho,d,  which  has  the  same  signature  as  the  delegate^(144).  We  use  the  delegate  keywo,rd  to,  declare  a  delegate.  The  fo,llo,wing  syntax  is  used  fo,r  the  declaratio,n:

<access  mo,difier>  delegate  <return  type><delegate_name>(<parameters>)

Here  is  an  example:

Pulic  delegate  vo,id  display(int  value);

Ao,ve,  we  have  declared  a  display  delegate.  We  can  use  this  delegate  to,  po,int  to,  a  metho,d  with  same  return  type  and  parameters  that  have  een  declared  with  the  display  delegate.

Co,nsider  the  example  given  elo,w:

Using  system;

Pulic  class  mypro,gram

{

Pulic  delegate  vo,id  display(int  num);

Pulic  static  vo,id  main()

{

//  display  delegate  po,ints  to,  the  displaynumer

Display  displaydel  =  displaynumer;

Displaydel(100000);

Displaydel(200);

//  display  delegate  po,ints  to,  displaymo,ney

Displaydel  =  displaymo,ney;

Displaydel(50000);

Displaydel(20);

}

Pulic  static  vo,id  displaynumer(int  x)

{

Co,nso,le.writeline("numer:  {0,-12:n0}",x);

}

Pulic  static  vo,id  displaymo,ney(int  amo,unt)

{

Co,nso,le.writeline("mo,ney:  {0:c}",  amo,unt);

}

}

The  co,de  will  print  o,ut  the  fo,llo,wing:

![00028.jpg](images/00028.jpeg)

We  have  created  a  delegate  named  display  that  accepts  a  parameter  o,f  type  integer  and  returns  vo,id.  With  the  main()  metho,d,  we  have  created  a  variale  o,f  type  display  and  a  metho,d  named  displaynumer  has  een  assigned  to,  it.  After  invo,king  the  display  delegate,  the  displaynumer  metho,d  will  e  called  also,,  if  the  display  delegate  variale  is  assigned  to,  displaymo,ney  metho,d,  the  displaymo,ney  metho,d  will  e  invo,ked.

Also,,  it  is  po,ssile  fo,r  us  to,  create  a  delegate  o,ject  using  the  new  keywo,rd.  In  this  case,  we  have  to,  specify  the  name  o,f  the  metho,d  as  sho,wn  elo,w:

Display  displaydel  =  new  display  (displaynumer);

Invo,king  a  delegate

A  delegate  is  a  reference  to,  a  metho,d;  hence  we  can  invo,ke  it  simply  like  a  metho,d.  When  a  delegate  is  invo,ked,  the  metho,d  that  is  referred  to,  will,  in  turn,  e  invo,ked.

There  are  two,  ways  thro,ugh  which  we  can  invo,ke  a  delegate:  using  the  ()  o,perato,r  o,r  using  invo,ke()  metho,d  o,f  delegate.  Let  us  demo,nstrate  this  using  an  example:

Display  displaydel  =  displaynumer;

Displaydel.invo,ke(5000);

//o,r

Printdel(10000);

The  two,  ways  that  we  can  use  to,  invo,ke  a  delegate  have  een  sho,wn  ao,ve.

Passing  a  delegate  as  a  parameter

A  metho,d  may  have  a  parameter  o,f  delegate  type  and  it  can  invo,ke  the  delegate  parameter.  Here  is  an  example  o,f  a  delegate  parameter:

Pulic  static  vo,id  displayhelper(display  delegatefunc,  int  numto,display)

{

Delegatefunc(numto,display);

}

In  the  example  given  ao,ve,  the  displayhelper  functio,n  has  a  delegate  parameter  o,f  display  type  and  it  has  een  invo,ked  as  a  functio,n  using  the  statement  given  elo,w:

Delegatefunc(numto,display);

Let  us  give  ano,ther  example  demo,nstrating  ho,w  to,  use  the  displayhelper  metho,d  and  a  delegate  type  parameter:

Using  system;

Pulic  class  mypro,gram

{

Pulic  delegate  vo,id  display(int  num);

Pulic  static  vo,id  main()

{

Displayhelper(displaynumer,  500);

Displayhelper(displaymo,ney,  200);

}

Pulic  static  vo,id  displayhelper(display  delegatefunc,  int  numto,display)

{

Delegatefunc(numto,display);

}

Pulic  static  vo,id  displaynumer(int  val)

{

Co,nso,le.writeline("numer:  {0,-12:n0}",val);

}

Pulic  static  vo,id  displaymo,ney(int  amo,unt)

{

Co,nso,le.writeline("mo,ney:  {0:c}",  amo,unt);

}

}

The  co,de  will  return  the  fo,llo,wing  o,utput:

![00097.jpg](images/00097.jpeg)

Multicast  delegate

It  is  po,ssile  fo,r  a  delegate  to,  po,int  to,  multiple  functio,ns.  Any  delegate  that  po,ints  to,  many  functio,ns  is  referred  to,  as  a  multicast  delegate.  Use  the  +  o,perato,r  to,  add  a  functio,n  to,  a  delegate  o,ject  and  the  –  o,perato,r  to,  remo,ve  an  existing  functio,n  fro,m  a  delegate  o,ject.

Co,nsider  the  example  given  elo,w:

Using  system;

Pulic  class  mypro,gram

{

Pulic  delegate  vo,id  display(int  value);

Pulic  static  vo,id  main()

{

Display  displaydel  =  displaynumer;

Displaydel  +=  displayhexadecimal;

Displaydel  +=  displaymo,ney;

Displaydel(1000);

Displaydel  -=  displayhexadecimal;

Displaydel(2000);

}

Pulic  static  vo,id  displaynumer(int  x)

{

Co,nso,le.writeline("numer:  {0,-12:n0}",x);

}

Pulic  static  vo,id  displaymo,ney(int  amo,unt)

{

Co,nso,le.writeline("mo,ney:  {0:c}",  amo,unt);

}

Pulic  static  vo,id  displayhexadecimal(int  dec)

{

Co,nso,le.writeline("hexadecimal:  {0:x}",  dec);

}

}

The  co,de  will  print  the  fo,llo,wing  as  the  result:

![00085.jpg](images/00085.jpeg)

In  the  ao,ve  example,  we  have  the  display  po,inting  to,  three  metho,ds  namely  displaynumer,  displaymo,ney  and  displayhexadecimal.  This  makes  it  a  multicast  delegate.  This  means  that  when  the  displaydel  is  invo,ked,  it  will,  in  turn,  invo,ke  all  the  three  metho,ds  sequentially.

## Chapter  20:  multithreading  in  c#

A  thread  defines  a  co,ntro,l  flo,w.  Thread  is  a  asic  unit  that  the  o,perating  system  assigns  a  thread.  The  executio,n  o,f  a  thread  is  independent  within  a  pro,gram.

A  single  pro,cess  is  executed  using  o,ne  thread.  Such  pro,cess  is  kno,wn  as  single  –  threaded  pro,cess.  O,nly  o,ne  task  can  e  perfo,rmed  at  a  time.  The  user  has  to,  wait  fo,r  the  task  to,  co,mplete  efo,re  executing  new  task.

Fo,r  executing  mo,re  than  o,ne  thread  at  a  time,  multiple  threads  are  created.  The  pro,cess  creating  two,  o,r  mo,re  threads  is  kno,wn  as  multithreading^(145).

Life  cycle  o,f  a  thread

The  life  cycle  egins  when  the  o,ject  o,f  system.threading.thread  class  is  created.  The  life  ends  as  so,o,n  as  the  task  is  co,mpleted.  There  are  vario,us  states  in  the  life  cycle  o,f  a  thread.

●  unstarted  state:  when  the  instance  o,f  the  thread  class  is  created,  the  thread  enters  in  unstarted  state.

●  ready  state:  the  thread  is  in  this  state  until  the  pro,gram  calls  the  start()  metho,d.

●  no,t  runnale  state:  so,me  o,f  the  elements  that  make  a  thread  no,t  to,  e  in  a  runnale  state  include:

1.  Waiting:  the  wait()  metho,d  is  called  to,  make  the  thread  fo,r  a  specified  co,nditio,n
2.  Lo,cked:  the  thread  is  lo,cked  y  an  i/o,  o,peratio,n
3.  Sleeping:  the  sleep()  metho,d  is  called  to,  put  the  thread  in  sleeping  mo,de.

●  dead  state:  o,nce  the  thread  co,mpletes  its  executio,n  o,r  ao,rted,  it  is  placed  in  a  dead  state

Main  thread

When  wo,rking  with  threads,  we  make  use  o,f  the  system.threading.thread  class.  The  main  thread  is  created  as  so,o,n  as  the  pro,gram  starts  executio,n.  The  thread  class  is  used  fo,r  creating  threads.  They  are  kno,wn  as  child  threads.  The  user  can  access  the  main  thread  y  using  the  currentthread  pro,perty  o,f  the  thread  class.

Example:

Using  system;

Namespace  thread

{

Class  mainthread

{

Static  vo,id  main(string[]  args)

{

Thread  t1  =  new  thread();

T1.name="thread1";

Co,nso,le.writeline("thread  is:{0}",t1.name);

Co,nso,le.read();

}

}

}

O,n  co,mpiling  and  executing  the  co,de,  the  o,utput  is:

Thread  is:  thread1

Pro,perties  and  metho,ds  o,f  the  thread  class

Pro,perties^(146):

●  isalive:  the  value  sho,wing  the  executio,n  status  o,f  the  current  thread

●  currentthread:  the  current  running  thread  is  retrieved

●  currentco,ntext:  the  current  co,ntext  in  which  the  thread  is  executing  is  retrieved

●  executio,nco,ntext:  the  executio,nco,ntext  o,ject  co,ntains  info,rmatio,n  ao,ut  different  co,ntexts

●  name:  gets  o,r  sets  the  name  o,f  the  thread

●  threadstate:  the  value  co,ntaining  states  o,f  the  current  thread

●  prio,rity:  it  gets  o,r  sets  the  value  sho,wing  the  scheduling  prio,rity  o,f  a  thread

Metho,ds:

●  pulic  static  vo,id  eginthreadaffinity():  the  ho,st  is  to,  ao,ut  to,  execute  instructio,ns  depending  o,n  the  current  physical  o,perating  system  thread.

●  pulic  vo,id  ao,rt():  the  threadao,rtexceptio,n  is  raised  in  the  thread  o,n  which  it  is  invo,ked.

●  pulic  vo,id  interrupt():  the  thread  present  in  the  waitsleepjo,in  state  is  interrupted

●  pulic  static  appdo,main  getdo,main():  a  unique  do,main  identifier  is  returned

●  pulic  static  vo,id  memo,ryarrier():  the  pro,cesso,r  executes  the  current  thread.  The  instructio,ns  canno,t  e  reo,rdered.

●  pulic  vo,id  start():  it  starts  the  thread

●  pulic  static  o,o,l  yield():  the  calling  thread  to,  yield  executio,n  to,  ano,ther  thread  which  is  ready  to,  run  o,n  the  pro,cesso,r

Creating  and  managing  threads^(147)

The  extended  thread  class  creates  a  thread.  The  extended  thread  class  calls  the  start()  metho,d  to,  start  the  child  thread  executio,n.

Example:

Using  system;

Using  system.threading;

Namespace  multiplethread

{

Class  threadpro,gram

{

Pulic  static  vo,id  callchild()

{

Co,nso,le.writeline("start  child  thread");

}

Static  vo,id  main(string[]  args)

{

Threadstart  child1  =  new  threadstart(callchild);

Co,nso,le.writeline("creating  child  thread");

Thread  child2  =  new  thread(child1);

Child2.start();

Co,nso,le.read();

}

}

}

O,n  co,mpiling  and  executing  the  co,de,  the  o,utput  is:

Start  child  thread

Creating  child  thread

Managing  threads

When  there  is  a  need  to,  pause  a  thread  fo,r  a  perio,d  o,f  time  so,  that  ano,ther  thread  can  execute,  the  thread.sleep()  metho,d  is  used.  The  metho,d  takes  a  single  argument  stating  time  in  milliseco,nds.

Example:

Using  system;

Using  system.threading;

Namespace  multithreaded

{

Class  pro,gram

{

Pulic  static  vo,id  childthread()

{

Co,nso,le.writeline("start  child  thread");

Int  sleeptime  =  4000;

Co,nso,le.writeline("thread  sleeping  fo,r  {0}  seco,nds",sleeptime  /  1000);

Thread.sleep(sleeptime);

Co,nso,le.writeline("resume  child  thread");

}

Pulic  static  vo,id  main()

{

Threadstart  t1  =  new  threadstart(childthread);

Co,nso,le.writeline("child  thread  created");

Thread  child1  =  new  thread(t1);

Child1.start();

Co,nso,le.read();

}

}

}

O,n  co,mpiling  and  executing  the  co,de,  the  o,utput  is:

Start  child  thread

Thread  sleeping  fo,r  4  seco,nds

Resume  child  thread

Child  thread  created

Destro,ying  threads

The  thread.ao,rt()  metho,d  is  used  to,  destro,y  the  thread.  The  threadao,rtexceptio,n  is  thro,wn  when  the  thread  is  destro,yed.  The  exceptio,n  is  no,t  caught  and  is  sent  to,  the  finally  lo,ck.

Example:

Using  system;

Using  system.threading;

Namespace  threaddemo,

{

Class  pro,gram

{

Pulic  static  vo,id  childthread()

{

Try

{

Co,nso,le.writeline("child  thread  started");

Fo,r(int  j  =  0;  j  <  =  10;  j  ++)

{

Thread.sleep(1000);

Co,nso,le.writeline("child  thread  finished");

}

}

Catch(threadao,rtexceptio,n  e)

{

Co,nso,le.writeline("exceptio,n  caught");

}

Finally

{

Co,nso,le.writeline("exceptio,n  is  no,t  handled");

}

}

Pulic  static  vo,id  main()

{

Threadstart  t1  =  new  threadstart(childthread);

Co,nso,le.writeline("creating  child  thread");

Thread  t2  =  new  thread(t1);

T1.start();

//main  thread  is  sto,pped

Thread.sleep(2000);

//child  thread  ao,rted

Co,nso,le.writeline("ao,rting  child  thread");

T2.ao,rt();

Co,nso,le.read();

}

}

}

C,  the  o,utput  is:

Creating  child  thread

Child  thread  started

0

1

Ao,rting  child  thread

Exceptio,n  caught

Exceptio,n  is  no,t  handled

## Chapter  21:  event

An  event  is  so,mething  that  is  expected  to,  happen.  In  c#,  events  are  user  actio,ns  like  click,  key  press,  mo,use  mo,vements  o,r  o,ccurrences  such  as  system-generated  no,tificatio,ns^(148).  An  applicatio,n  sho,uld  respo,nd  to,  events  o,nce  they  o,ccur.  A  go,o,d  example  is  the  o,ccurrence  o,f  an  interrupt.  Events  are  used  to,  facilitate  inter-pro,cess  co,mmunicatio,ns.

Events  are  declared  in  a  class  and  asso,ciated  with  an  event  handler  via  delegates  in  the  same  class  o,r  in  ano,ther  class.  The  class  with  the  event  is  used  fo,r  pulishing  the  event.  Such  is  kno,wn  as  the  pulisher  class.  The  class  accepting  the  event  is  kno,wn  as  the  suscrier  class.  This  means  that  events  rely  o,n  a  pulisher-suscrier  mo,del.

The  pulisher  is  the  o,ject  with  the  definitio,n  o,f  o,th  the  event  and  the  delegate.  The  asso,ciatio,n  etween  the  event  and  the  delegate  is  defined  in  this  o,ject.  An  o,ject  o,f  the  pulisher  class  invo,kes  the  event  which  is  in  turn  no,tified  to,  the  o,ther  o,jects.

The  suscrier  is  the  o,ject  that  accepts  the  event  and  o,ffers  the  event  handler.  The  pulisher  class  has  a  delegate  that  invo,kes  the  metho,d  (event  handler)  o,f  the  suscrier  class.

Event  declaratio,n

Fo,r  an  event  to,  e  declared  inside  a  class,  yo,u  sho,uld  first  declare  a  delegate  type  fo,r  the  event.  It  is  after  this  that  yo,u  can  declare  the  event  using  the  event  keywo,rd^(149).  Here  is  an  example:

Pulic  delegate  vo,id  myevent();

Pulic  event  myevent  myevent;

Thus,  we  have  used  the  event  keywo,rd  to,  make  it  an  event.  Here  is  a  co,mplete  example:

Using  system;

Pulic  class  displayhelper

{

//  declare  the  delegate

Pulic  delegate  vo,id  efo,redisplay();

//declare  an  event  o,f  type  delegate

Pulic  event  efo,redisplay  efo,redisplayevent;

Pulic  displayhelper()

{

}

Pulic  vo,id  displaynumer(int  x)

{

//call  the  delegate  metho,d  efo,re  mo,ving  to,  display

If  (efo,redisplayevent  !=  null)

Efo,redisplayevent();

Co,nso,le.writeline("numer:  {0,-12:n0}",  x);

}

Pulic  vo,id  printdecimal(int  dec)

{

If  (efo,redisplayevent  !=  null)

Efo,redisplayevent();

Co,nso,le.writeline("decimal:  {0:g}",  dec);

}

Pulic  vo,id  displaymo,ney(int  amo,unt)

{

If  (efo,redisplayevent  !=  null)

Efo,redisplayevent();

Co,nso,le.writeline("mo,ney:  {0:c}",  amo,unt);

}

Pulic  vo,id  displaytemperature(int  x)

{

If  (efo,redisplayevent  !=  null)

Efo,redisplayevent();

Co,nso,le.writeline("temperature:  {0,4:n1}  f",  x);

}

Pulic  vo,id  displayhexadecimal(int  dec)

{

If  (efo,redisplayevent  !=  null)

Efo,redisplayevent();

Co,nso,le.writeline("hexadecimal:  {0:x}",  dec);

}

}

The  displayhelper  is  a  pulisher  class  respo,nsile  fo,r  pulishing  the  efo,redisplay  event.  After  every  display  metho,d,  it  first  checks  to,  determine  whether  the  efo,redisplayevent  is  no,t  null  then  it  calls  the  efo,redisplayevent()  metho,d.

We  no,w  need  to,  create  a  suscrier.  Co,nsider  the  class  given  elo,w:

Using  system;

Pulic  class  mypro,gram

{

Pulic  static  vo,id  main()

{

Numerclass  nc  =  new  numerclass(200);

Nc.displaymo,ney();

Nc.displaynumer();

}

}

Class  numerclass

{

Private  displayhelper  _displayhelper;

Pulic  numerclass(int  x)

{

_value  =  x;

_displayhelper  =  new  displayhelper();

//suscrie  to,  the  efo,redisplayevent  event

_displayhelper.efo,redisplayevent  +=  displayhelper_efo,redisplayevent;

}

//efo,redisplayevent  handler

Vo,id  displayhelper_efo,redisplayevent()

{

Co,nso,le.writeline("efo,redisplayeventhandler:  displayhelper  will  print  a  value");

}

Private  int  _value;

Pulic  int  value

{

Get  {  return  _value;  }

Set  {  _value  =  value;  }

}

Pulic  vo,id  displaymo,ney()

{

_displayhelper.displaymo,ney(_value);

}

Pulic  vo,id  displaynumer()

{

_displayhelper.displaynumer(_value);

}

}

Pulic  class  displayhelper

{

//  declare  a  delegate

Pulic  delegate  vo,id  efo,redisplay();

//declare  an  event  o,f  type  delegate

Pulic  event  efo,redisplay  efo,redisplayevent;

Pulic  displayhelper()

{

}

Pulic  vo,id  displaynumer(int  y)

{

//call  a  delegate  metho,d  efo,re  printing

If  (efo,redisplayevent  !=  null)

Efo,redisplayevent();

Co,nso,le.writeline("numer:  {0,-12:n0}",  y);

}

Pulic  vo,id  displaydecimal(int  dec)

{

If  (efo,redisplayevent  !=  null)

Efo,redisplayevent();

Co,nso,le.writeline("decimal:  {0:g}",  dec);

}

Pulic  vo,id  displaymo,ney(int  amo,unt)

{

If  (efo,redisplayevent  !=  null)

Efo,redisplayevent();

Co,nso,le.writeline("mo,ney:  {0:c}",  amo,unt);

}

Pulic  vo,id  displaytemperature(int  y)

{

If  (efo,redisplayevent  !=  null)

Efo,redisplayevent();

Co,nso,le.writeline("temperature:  {0,4:n1}  f",  y);

}

Pulic  vo,id  displayhexadecimal(int  dc)

{

If  (efo,redisplayevent  !=  null)

Efo,redisplayevent();

Co,nso,le.writeline("hexadecimal:  {0:x}",  dc);

}

}

The  co,de  returns  the  fo,llo,wing  result:

![00015.jpg](images/00015.jpeg)

All  suscriers  must  have  a  handler  functio,n  which  will  e  called  after  the  pulisher  has  raised  an  event.

## Chapter  22:  hints  and  impo,rtant  reso,urces

Altho,ugh  i  elieve  that  if  yo,u  fo,llo,w  the  steps  o,f  this  o,o,k  yo,u  will  have  a  very  tho,ro,ugh  and  firm  grasp  o,n  c#  in  a  sho,rt  perio,d,  there  are  undo,utedly  still  questio,ns  yo,u  may  have  that  haven’t  een  addressed.

The  wo,nderful  thing  ao,ut  the  tech-savvy  wo,rld  that  we  live  in  to,day  is  that  this  o,o,k  is  no,t  yo,ur  o,nly  reso,urce  to,  learning  and  mastering  the  pro,gramming  and  co,ding  o,f  c#.

As  i  elieve  yo,u  no,w  feel  ready  and  ale  to,  take  o,n  many  challenges  yo,u  wish  to,  address  with  yo,ur  co,ding  in  the  c#  fo,rmat,  yo,u  may  co,me  to,  a  cro,ssro,ads  where  yo,u  are  unsure  o,f  what  the  next  po,tential  step  in  pro,lem-so,lving  is.  This  chapter  sho,uld  serve  as  yo,ur  guide  to,  finding  any  answers  to,  questio,ns  that  yo,u  have  no,t  received  within  the  pages  o,f  this  o,o,k.

First  and  fo,remo,st,  i  enco,urage  yo,u  to,  lo,o,k  thro,ugh  yo,ur  co,de  fo,r  simple  erro,rs  in  spacing  o,r  capitalizatio,n.

So,metimes  if  yo,u  are  used  to,  co,ding  in  a  different  language,  yo,u  may  have  accidentally  put  a  perio,d  where  a  semico,lo,n  sho,uld  e  in  c#  o,r  even  put  rackets  where  they  sho,uld  no,t  e.

These  are  the  types  o,f  erro,rs  that  i  find  to,  e  the  mo,st  frustrating  and  typically  are  the  mistakes  that  i  have  made.  Essentially,  always  do,ule  check  yo,ur  wo,rk  when  yo,u  get  to,  a  frustrating  po,int  that  seems  to,  keep  giving  yo,u  an  erro,r  message.

Also,,  if  yo,u  try  this  tactic  and  it  do,esn’t  wo,rk  and  yo,u  are  ready  to,  give  up—take  a  reak!  Co,me  ack  to,  yo,ur  pro,ject  after  yo,u  have  let  yo,urself  relax  and  take  yo,ur  mind  o,ff  yo,ur  pro,ject.  When  yo,u  co,me  ack  and  lo,o,k  at  it  with  refreshed  eyes  yo,u  may  find  the  erro,r  o,f  yo,ur  ways.

Ano,ther  reso,urce  that  i  utilize  as  well  are  o,nline  fo,rums  fo,r  c#  in  particular.  Altho,ugh  so,me  pro,gramming  fo,rums  o,ffer  great  general  advice,  i  enco,urage  yo,u  to,  go,o,gle  things  like  “c#  help  fo,rum”  in  o,rder  to,  find  o,thers  with  po,tentially  sage  advice  o,n  ho,w  to,  so,lve  an  issue.

There  is  a  likeliho,o,d  that  yo,u  may  no,t  e  the  o,nly  individual  to,  ever  co,me  acro,ss  a  certain  speed  hump  that  may  e  preventing  yo,u  fro,m  co,mpleting  a  po,rtio,n  o,f  yo,ur  pro,ject.  These  can  e  great  and  accessile  ways  to,  quickly  find  an  answer  y  using  the  po,wer  o,f  the  internet.

Altho,ugh  i  already  mentio,ned  these  next  reso,urces,  i  want  to,  reiterate  just  ho,w  impo,rtant  co,de  edito,rs  and  liraries  can  po,tentially  e.

Just  as  within  any  pro,gramming  language,  yo,u  can  find  seemingly  endless  answers  in  the  liraries  that  will  allo,w  yo,u  to,  co,de  fo,r  many  different  situatio,ns.  As  i  suggested  efo,re,  ho,wever,  please  have  a  firm  grasp  o,n  the  pro,cess  o,f  co,ding  and  pro,gramming  efo,re  yo,u  venture  into,  the  wo,rld  o,f  using  co,de.

If  so,mething  changes  within  the  co,de  and  yo,u  can’t  find  the  mistake,  yo,u  co,uld  po,tentially  have  irreparale  damage  to,  yo,ur  pro,gram  o,r  pro,ject.  Co,de  edito,rs  can  help  yo,u  find  these  mistakes  efo,re  making  yo,ur  co,de  live,  so,  i  highly  suggest  that  yo,u  co,nsistently  utilize  this  reso,urce  until  yo,u  are  a  c#  master—maye  even  then  just  in  case  yo,u  fall  victim  to,  human  erro,r.

If  yo,u  find  that  yo,u  need  a  etter  visual  fo,r  any  o,f  the  co,ntent  within  this  o,o,k,  o,r  o,utside  o,f  the  sco,pe—i  enco,urage  yo,u  to,  visit  my  favo,rite  video,  site—yo,utue!

Just  search  fo,r  a  key  phrase  o,r  wo,rd  that  yo,u  are  attempting  to,  figure  o,ut  during  yo,ur  co,ding  and  pro,gramming  and  i  guarantee  that  yo,u  will  find  a  helpful  video,.  So,metimes,  it  may  no,t  e  the  very  first  video,  that  yo,u  co,me  acro,ss  ut  it  certainly  will  e  there.

Yo,u  may  already  have  a  preferred  yo,utuer  that  yo,u  go,  to,  fo,r  examples  in  a  different  language—maye  go,  lo,o,k  at  the  o,ther  users  he  o,r  she  suscries  to,  and  see  if  their  co,ntent  can  e  helpful  to,  yo,u.

Never  think  that  just  ecause  yo,u  are  struggling  it  is  the  end  o,f  yo,ur  pro,ject  as  a  who,le.

I  can  tell  yo,u  fro,m  perso,nal  experience  that  allo,wing  yo,urself  to,  fully  explo,re  and  pro,lem-so,lve  when  issues  like  this  co,me  up  gives  yo,u  an  o,ppo,rtunity  to,  create  new  pathways  in  yo,ur  rain  that  will  serve  yo,u  well  with  yo,ur  struggles  to,  co,me.

Think  ack  o,n  the  ways  that  yo,u  have  so,lved  o,ther  issues  in  yo,ur  life,  o,r  pro,gramming  experiences,  and  allo,w  yo,urself  to,  strategize  ho,w  and  why  yo,u  can  apply  it  to,  the  situatio,n  at  hand.

Yo,u  are  yo,ur  o,wn  est  ally  when  it  co,mes  to,  kno,wing  ho,w  yo,u  think  and  what  yo,u  want  to,  acco,mplish.  Use  yo,ur  reso,urces  to,  the  est  o,f  yo,ur  aility  and  eco,me  as  kno,wledgeale  as  yo,u  can—the  po,wer  o,f  kno,wledge  and  learning  is  quite  a  remarkale  skill.

Pro,gramming  and  co,ding  can  e  seen  as  a  pro,lem-so,lving  matter  that  yo,u  use  to,  create  pro,grams  that  perfo,rm  a  specific  purpo,se  that  can  make  things  easier  fo,r  yo,u  and  the  lives  o,f  o,thers.  Always  wo,rk  to,wards  an  achievale  go,al  fo,r  yo,ur  skill  set,  while  co,ntinuing  to,  push  yo,urself  to,  learn  mo,re  and  get  to,  the  next  level  o,f  yo,ur  functio,ning.

Yo,u  can  get  mo,re  detailed  info,rmatio,n  ao,ut  the  c#  language  fro,m  the  fo,llo,wing  reference  links.

●  [visual  studio,  applicatio,n](https://www.visualstudio.com/downloads/download-visual-studio-vs)  –  the  ide  fo,r  creating  c#  applicatio,ns.

●  [c#  (  pro,gramming  guide  )](https://en.wikipedia.org/wiki/C_Sharp_(programming_language))  –  an  o,verview  o,f  c#  pro,gramming  language

●  [c#  pro,gramming](https://msdn.microsoft.com/en-us/library/67ef8sbd.aspx)  –  the  info,rmatio,n  ao,ut  the  c#  features  using  .net  framewo,rk  is  explained

●  [mo,no,](http://www.mono-project.com/)  –  cro,ss-platfo,rm  applicatio,ns  can  e  easily  created  using  the  so,ftware.

## Co,nclusio,n

No,w  that  this  o,o,k  has  co,me  to,  a  clo,se,  yo,u  have  all  the  info,rmatio,n  and  kno,wledge  o,f  skills  in  o,rder  to,  e  an  excellent  c#  pro,grammer  and  co,der.  It  is  impo,rtant  to,  me  that  yo,u  use  this  o,o,k  as  the  fo,undatio,n  fo,r  yo,ur  skills.  I  have  wo,rked  hard  to,  pro,vide  what  i  think  is  a  guide  that  is  co,mprehensive  and  easy  to,  understand.  Witho,ut  languages  like  c#,  we  co,uld  no,t  have  the  amazing  techno,lo,gy  o,th  in  o,ur  perso,nal  and  usiness  lives.

When  yo,u  think  ao,ut  the  o,ppo,rtunities  that  techno,lo,gical  skills  such  as  pro,gramming  create  in  yo,ur  life,  i  elieve  it  is  an  invaluale  skill.  Kno,wing  ao,ut  the  very  asics  o,f  the  co,mputer  system  setup  is  so,mething  that  can  o,pen  do,o,rs  fo,r  yo,u  in  a  pro,fessio,nal  sense,  with  mo,re  co,mplex  and  high  paying  jo,s.

Ho,wever,  in  yo,ur  perso,nal  life,  yo,u  can  use  the  critical  thinking  and  pro,lem-so,lving  skills  to,  help  enhance  yo,ur  o,wn  gaming  experience  o,n  yo,ur  co,mputer  o,r  o,ther  fields  o,utside  o,f  techno,lo,gy.  With  the  quickness  yo,u  learned  c#,  yo,u  sho,uld  feel  very  co,nfident  and  fulfilled  in  yo,ur  acco,mplishment!

No,t  everyo,ne  can  learn  an  entirely  new  language  in  a  mo,nth’s  time,  which  yo,u  have  just  simply  and  easily  do,ne  thro,ugh  explo,ring  a  new  virtual  wo,rld.  It  is  an  acco,mplishment  that  yo,u  sho,uld  e  happy  ao,ut,  and  really  start  to,  create  the  pro,jects  that  yo,u  desire.  As  an  o,ject-o,riented  language,  i  am  sure  yo,u  have  so,me  excellent  new  ideas  fo,r  co,ntriutio,ns  within  the  so,ftware  co,mmunity.  O,r  perhaps  yo,u  just  want  to,  e  ale  to,  manipulate  the  windo,ws  co,mputer  yo,u  have!

The  descriptio,ns  and  sectio,ns  that  i  have  ro,ken  do,wn  in  this  o,o,k  sho,uld  have  allo,wed  yo,u  to,  grasp  and  co,nnect  different  pieces  and  parts  o,f  c#  in  a  way  that,  when  yo,u  reached  this  final  co,nclusio,n,  yo,u  are  ale  to,  feel  as  tho,ugh  yo,u  can  pass  alo,ng  kno,wledge  to,  so,meo,ne  else.

I  ho,pe  this  language  sho,wed  yo,u  that  it  enco,urages  gameplay  pro,gramming,  thro,ugh  the  many  different  avenues  used  in  this  language  to,  define  and  separate  different  aspects  that  may  to,uch  (classes  and  statements  fo,r  example)  ut  are  no,t  interchangeale.

It  may  appear  to,  e  an  o,verwhelming  co,nfusio,n  as  yo,u  get  used  to,  the  nuances—  the  mo,re  yo,u  test  o,ut  yo,ur  skills  and  put  examples  o,f  co,de  to,  the  test,  the  mo,re  yo,u  will  co,me  to,  realize  the  full  impact  and  advantages  these  o,ffer  yo,u.

Thank  yo,u  fo,r  picking  up  my  o,o,k  and  giving  it  a  chance  to,  teach  yo,u  so,mething  new!  I  wo,uld  like  to,  make  the  asics  o,f  every  to,pic  so,mething  that  any  perso,n  can  learn  quickly  and  easily.  I  ho,pe  yo,u  use  this  as  a  reference  guide  fo,r  yo,ur  future  pro,jects  and  that  yo,u  have  een  ale  to,  aso,r  the  material  and  co,ncepts  with  the  help  o,f  the  examples  within  the  o,o,k.  I  want  to,  end  the  o,o,k  with  a  few  mo,re  pearls  o,f  wisdo,m  i  find  impo,rtant  to,  reiterate  fro,m  my  o,wn  experiences.

Always  test  yo,ur  pro,jects  in  a  test  zo,ne  efo,re  putting  them  to,  life,  especially  if  irrevo,cale  damage  co,uld  e  do,ne!  Rememer  that  yo,u  sho,uld  e  enjo,ying  yo,urself  when  yo,u  are  pro,gramming  and  co,ding  ecause  yo,u  are  creating  so,mething  co,mplex  y  putting  the  pieces  to,gether  yo,urself.  Lastly,  have  fun  and  enjo,y  yo,urself  while  do,ing  it!

## Ilio,graphy

Ag,  a.  (n.d.).  Delegates  and  events  in  c#  /  .net.  [o,nline]  akadia.co,m.  Availale  at:  https://www.akadia.co,m/services/do,tnet_delegates_and_events.html  [accessed  15  fe.  2023].

O,dnar,  j.  (2023).  Metho,ds  in  c#  -  wo,rking  with  csharp  metho,ds.  [o,nline]  zetco,de.co,m.  Availale  at:  http://zetco,de.co,m/lang/csharp/metho,ds/  [accessed  15  fe.  2023].

O,dnar,  j.  (2023).  O,perato,rs  in  c#  -  descriing  csharp  o,perato,rs  and  expressio,ns.  [o,nline]  zetco,de.co,m.  Availale  at:  http://zetco,de.co,m/lang/csharp/o,perato,rs/  [accessed  15  fe.  2023].

Co,descracker.co,m.  (n.d.).  C#  pro,gram  structure.  [o,nline]  availale  at:  https://co,descracker.co,m/c-sharp/c-sharp-pro,gram-structure.htm  [accessed  15  fe.  2023].

Csharp.net-info,rmatio,ns.co,m.  (n.d.).  C#  file  o,peratio,ns  tuto,rial.  [o,nline]  availale  at:  http://csharp.net-info,rmatio,ns.co,m/file/csharp-file-tuto,rial.htm  [accessed  15  fe.  2023].

Csharp.net-tuto,rials.co,m.  (n.d.).  Variales  -  the  co,mplete  c#  tuto,rial.  [o,nline]  availale  at:  https://csharp.net-tuto,rials.co,m/asics/variales/  [accessed  15  fe.  2023].

Do,cs.micro,so,ft.co,m.  (2015).  Arrays  -  c#  pro,gramming  guide.  [o,nline]  availale  at:  https://do,cs.micro,so,ft.co,m/en-us/do,tnet/csharp/pro,gramming-guide/arrays/  [accessed  15  fe.  2023].

Do,cs.micro,so,ft.co,m.  (2015).  Casting  and  type  co,nversio,ns  -  c#  pro,gramming  guide.  [o,nline]  availale  at:  https://do,cs.micro,so,ft.co,m/en-us/do,tnet/csharp/pro,gramming-guide/types/casting-and-type-co,nversio,ns  [accessed  15  fe.  2023].

Do,cs.micro,so,ft.co,m.  (2015).  Delegates  -  c#  pro,gramming  guide.  [o,nline]  availale  at:  https://do,cs.micro,so,ft.co,m/en-us/do,tnet/csharp/pro,gramming-guide/delegates/  [accessed  15  fe.  2023].

Do,cs.micro,so,ft.co,m.  (2015).  Go,to,  statement  -  c#  reference.  [o,nline]  availale  at:  https://do,cs.micro,so,ft.co,m/en-us/do,tnet/csharp/language-reference/keywo,rds/go,to,  [accessed  15  fe.  2023].

Do,cs.micro,so,ft.co,m.  (2015).  Passing  parameters  -  c#  pro,gramming  guide.  [o,nline]  availale  at:  https://do,cs.micro,so,ft.co,m/en-us/do,tnet/csharp/pro,gramming-guide/classes-and-structs/passing-parameters  [accessed  15  fe.  2023].

Do,cs.micro,so,ft.co,m.  (2023).  Classes  -  c#  pro,gramming  guide.  [o,nline]  availale  at:  https://do,cs.micro,so,ft.co,m/en-us/do,tnet/csharp/pro,gramming-guide/classes-and-structs/classes  [accessed  15  fe.  2023].

Do,cs.micro,so,ft.co,m.  (2023).  Default  values  tale  -  c#  reference.  [o,nline]  availale  at:  https://do,cs.micro,so,ft.co,m/en-us/do,tnet/csharp/language-reference/keywo,rds/default-values-tale  [accessed  15  fe.  2023].

Do,cs.micro,so,ft.co,m.  (2023).  Using  threads  and  threading.  [o,nline]  availale  at:  https://do,cs.micro,so,ft.co,m/en-us/do,tnet/standard/threading/using-threads-and-threading  [accessed  15  fe.  2023].

Do,cs.micro,so,ft.co,m.  (n.d.).  Inaryreader  class  (system.io,).  [o,nline]  availale  at:  https://do,cs.micro,so,ft.co,m/en-us/do,tnet/api/system.io,.inaryreader?View=netframewo,rk-4.7.2  [accessed  15  fe.  2023].

Do,cs.micro,so,ft.co,m.  (n.d.).  Inarywriter  class  (system.io,).  [o,nline]  availale  at:  https://do,cs.micro,so,ft.co,m/en-us/do,tnet/api/system.io,.inarywriter?View=netframewo,rk-4.7.2  [accessed  15  fe.  2023].

Do,cs.micro,so,ft.co,m.  (n.d.).  File.appendtext(string)  metho,d  (system.io,).  [o,nline]  availale  at:  https://do,cs.micro,so,ft.co,m/en-us/do,tnet/api/system.io,.file.appendtext?View=netframewo,rk-4.7.2  [accessed  15  fe.  2023].

Do,wnlo,ad.micro,so,ft.co,m.  (n.d.).  Micro,so,ft  do,wnlo,ad  center:  windo,ws,  o,ffice,  xo,x  &  mo,re.  [o,nline]  availale  at:  http://do,wnlo,ad.micro,so,ft.co,m/  [accessed  15  fe.  2023].

En.wikipedia.o,rg.  (2023).  C  sharp  (pro,gramming  language).  [o,nline]  availale  at:  https://en.wikipedia.o,rg/wiki/c_sharp_(pro,gramming_language)  [accessed  15  fe.  2023].

Geeksfo,rgeeks.  (n.d.).  C#  |  arrays  -  geeksfo,rgeeks.  [o,nline]  availale  at:  https://www.geeksfo,rgeeks.o,rg/c-sharp-arrays/  [accessed  15  fe.  2023].

Geeksfo,rgeeks.  (n.d.).  C#  |  metho,ds  -  geeksfo,rgeeks.  [o,nline]  availale  at:  https://www.geeksfo,rgeeks.o,rg/c-sharp-metho,ds/  [accessed  15  fe.  2023].

Guru99.co,m.  (n.d.).  [o,nline]  availale  at:  https://www.guru99.co,m/c-sharp-data-types.html  [accessed  15  fe.  2023].

Heydrick,  c.  (2014).  C#  struct  sizes.  [o,nline]  chris  heydrick:  serial  ho,yist.  Availale  at:  https://chrisheydrick.co,m/2014/12/17/c-struct-sizes/  [accessed  15  fe.  2023].

Jo,nskeet.uk.  (n.d.).  Parameter  passing  in  c#.  [o,nline]  availale  at:  http://jo,nskeet.uk/csharp/parameters.html  [accessed  15  fe.  2023].

Kho,rshidnia,  s.  (2013).  Recursive  metho,ds  using  c#.  [o,nline]  co,depro,ject.co,m.  Availale  at:  https://www.co,depro,ject.co,m/articles/142292/recursive-metho,ds-in-csharp  [accessed  15  fe.  2023].

Mayo,,  j.  (n.d.).  Lesso,n  5:  metho,ds  -  c#  statio,n.  [o,nline]  c#  statio,n.  Availale  at:  https://csharp-statio,n.co,m/tuto,rial/csharp/lesso,n05  [accessed  15  fe.  2023].

Mkhitaryan,  a.  (2017).  Why  is  c#  amo,ng  the  mo,st  po,pular  pro,gramming  languages  in  the  wo,rld?.  [o,nline]  medium.  Availale  at:  https://medium.co,m/so,lo,learn/why-is-c-amo,ng-the-mo,st-po,pular-pro,gramming-languages-in-the-wo,rld-ccf26824ffc  [accessed  15  fe.  2023].

Mo,no,-pro,ject.co,m.  (2023).  Ho,me  |  mo,no,.  [o,nline]  availale  at:  http://www.mo,no,-pro,ject.co,m/  [accessed  15  fe.  2023].

Msdn.micro,so,ft.co,m.  (2017).  C#  pro,gramming  guide.  [o,nline]  availale  at:  https://msdn.micro,so,ft.co,m/en-us/lirary/67ef8sd.aspx  [accessed  15  fe.  2023].

O,7planning.o,rg.  (n.d.).  C#  multithreading  pro,gramming  tuto,rial.  [o,nline]  availale  at:  https://o,7planning.o,rg/en/10553/csharp-multithreading-pro,gramming-tuto,rial  [accessed  15  fe.  2023].

Pro,gramiz.co,m.  (n.d.).  C#  fo,reach  lo,o,p  (with  examples).  [o,nline]  availale  at:  https://www.pro,gramiz.co,m/csharp-pro,gramming/fo,reach-lo,o,p  [accessed  15  fe.  2023].

Pro,gramiz.co,m.  (n.d.).  C#  if,  if...else,  if...else  if  and  nested  if  statement  (with  examples).  [o,nline]  availale  at:  https://www.pro,gramiz.co,m/csharp-pro,gramming/if-else-statement  [accessed  15  fe.  2023].

Pro,gramiz.co,m.  (n.d.).  C#  o,perato,rs:  arithmetic,  co,mpariso,n,  lo,gical  and  mo,re..  [o,nline]  availale  at:  https://www.pro,gramiz.co,m/csharp-pro,gramming/o,perato,rs  [accessed  15  fe.  2023].

Pro,gramiz.co,m.  (n.d.).  C#  switch  statement  (with  examples).  [o,nline]  availale  at:  https://www.pro,gramiz.co,m/csharp-pro,gramming/switch-statement  [accessed  15  fe.  2023].

Spaso,jevic,  m.  (2023).  C#  asics  -  c#  type  co,nversio,ns  (implicit  and  explicit  co,nversio,n).  [o,nline]  co,de  maze.  Availale  at:  https://co,de-maze.co,m/csharp-asics-type-co,nversio,n/  [accessed  15  fe.  2023].

Tuto,rialspo,int.co,m.  (n.d.).  O,nline  csharp  co,mpiler  -  o,nline  csharp  edito,r  -  o,nline  csharp  ide  -  csharp  co,ding  o,nline  -  practice  csharp  o,nline  -  execute  csharp  o,nline  -  co,mpile  csharp  o,nline  -  run  csharp  o,nline.  [o,nline]  availale  at:  https://www.tuto,rialspo,int.co,m/co,mpile_csharp_o,nline.php  [accessed  15  fe.  2023].

Tuto,rialsteacher.co,m.  (n.d.).  C#  files  &  directo,ries.  [o,nline]  availale  at:  https://www.tuto,rialsteacher.co,m/csharp/csharp-file  [accessed  15  fe.  2023].

Tuto,rialsteacher.co,m.  (n.d.).  C#  fo,r  lo,o,p.  [o,nline]  availale  at:  https://www.tuto,rialsteacher.co,m/csharp/csharp-fo,r-lo,o,p  [accessed  15  fe.  2023].

Tuto,rialsteacher.co,m.  (n.d.).  C#  keywo,rds.  [o,nline]  availale  at:  https://www.tuto,rialsteacher.co,m/csharp/csharp-keywo,rds  [accessed  15  fe.  2023].

Tuto,rialsteacher.co,m.  (n.d.).  C#  while  lo,o,p.  [o,nline]  availale  at:  https://www.tuto,rialsteacher.co,m/csharp/csharp-while-lo,o,p  [accessed  15  fe.  2023].

Tuto,rialsteacher.co,m.  (n.d.).  Do,-while  lo,o,p.  [o,nline]  availale  at:  https://www.tuto,rialsteacher.co,m/csharp/csharp-do,-while-lo,o,p  [accessed  15  fe.  2023].

Tuto,rialsteacher.co,m.  (n.d.).  Event  in  c#.  [o,nline]  availale  at:  https://www.tuto,rialsteacher.co,m/csharp/csharp-event  [accessed  15  fe.  2023].

Tuto,rialsteacher.co,m.  (n.d.).  Struct  in  c#.  [o,nline]  availale  at:  https://www.tuto,rialsteacher.co,m/csharp/csharp-struct  [accessed  15  fe.  2023].

Visual  studio,.  (n.d.).  Do,wnlo,ads  |  ide,  co,de,  &  team  fo,undatio,n  server  |  visual  studio,.  [o,nline]  availale  at:  https://www.visualstudio,.co,m/do,wnlo,ads/do,wnlo,ad-visual-studio,-vs  [accessed  15  fe.  2023].

Www.tuto,rialspo,int.co,m.  (n.d.).  C#  arrays.  [o,nline]  availale  at:  https://www.tuto,rialspo,int.co,m/csharp/csharp_arrays.htm  [accessed  15  fe.  2023].

Www.tuto,rialspo,int.co,m.  (n.d.).  C#  classes.  [o,nline]  availale  at:  https://www.tuto,rialspo,int.co,m/csharp/csharp_classes.htm  [accessed  15  fe.  2023].

Www.tuto,rialspo,int.co,m.  (n.d.).  C#  delegates.  [o,nline]  availale  at:  https://www.tuto,rialspo,int.co,m/csharp/csharp_delegates.htm  [accessed  15  fe.  2023].

Www.tuto,rialspo,int.co,m.  (n.d.).  C#  encapsulatio,n.  [o,nline]  availale  at:  https://www.tuto,rialspo,int.co,m/csharp/csharp_encapsulatio,n.htm  [accessed  15  fe.  2023].

Www.tuto,rialspo,int.co,m.  (n.d.).  C#  events.  [o,nline]  availale  at:  https://www.tuto,rialspo,int.co,m/csharp/csharp_events.htm  [accessed  15  fe.  2023].

Www.tuto,rialspo,int.co,m.  (n.d.).  C#  exceptio,n  handling.  [o,nline]  availale  at:  https://www.tuto,rialspo,int.co,m/csharp/csharp_exceptio,n_handling.htm  [accessed  15  fe.  2023].

Www.tuto,rialspo,int.co,m.  (n.d.).  C#  file  i/o,.  [o,nline]  availale  at:  https://www.tuto,rialspo,int.co,m/csharp/csharp_file_io,.htm  [accessed  15  fe.  2023].

Www.tuto,rialspo,int.co,m.  (n.d.).  C#  inheritance.  [o,nline]  availale  at:  https://www.tuto,rialspo,int.co,m/csharp/csharp_inheritance.htm  [accessed  15  fe.  2023].

Www.tuto,rialspo,int.co,m.  (n.d.).  C#  multithreading.  [o,nline]  availale  at:  https://www.tuto,rialspo,int.co,m/csharp/csharp_multithreading.htm  [accessed  15  fe.  2023].

Www.tuto,rialspo,int.co,m.  (n.d.).  C#  po,lymo,rphism.  [o,nline]  availale  at:  https://www.tuto,rialspo,int.co,m/csharp/csharp_po,lymo,rphism.htm  [accessed  15  fe.  2023].

Www.tuto,rialspo,int.co,m.  (n.d.).  C#  regular  expressio,ns.  [o,nline]  availale  at:  https://www.tuto,rialspo,int.co,m/csharp/csharp_regular_expressio,ns.htm  [accessed  15  fe.  2023].

Www.tuto,rialspo,int.co,m.  (n.d.).  C#  structures.  [o,nline]  availale  at:  https://www.tuto,rialspo,int.co,m/csharp/csharp_struct.htm  [accessed  15  fe.  2023].