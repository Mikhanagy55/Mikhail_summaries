![18133.png](images/18133.png)

**This summary was created by [Mikha](https://www.linkedin.com/in/mikhail-nagy-99620718a).**  
I hope you find it helpful. Best regards!
[**Git and GitHub|شخبط وانت متطمن**](https://youtu.be/Q6G-J54vgKc?si=pUTe-RGv4Uvmb18j)

# Intro to VCs
كل واحد بيبقى عايز طريقه يtrack بيها الchanges اللي عاملها على ال file بتاعه اياََ كان يعني, يرصد التغيرات اللي حصلت في الstructure بتاعه سواء الfiles, folders, content, etc. ويرصد التغيرات دي مع الوقت ويكون فاهم انه فاليوم الفولاني حصل تغير معين بسبب كذا كذا وهكذا. 
و على مر الوقت يشوف ال file بقى ايه ثم بقى ايه وهكذا **"versions of the file"**. ومثلا حب يعمل Roll back يرجع ل version قديم من شغله على الFile بتاعه, او يعمل `roll forward` or `fast forward` لحاجه قدام.

زمان ايام شغل المَنَفِلَّه كنا نروح ل الfolder اللي فيه كل ال project بتاعك بكل ال files اللي فيه و قبل ما تبدأ تعمل تغيير تقوم واخد copy من الfolder ده,  this folder what is called `stable version`. 
يعمل اللي هو عاوزه لقى نفسه لبس فالخرسانه يروح راجع لل version القديم اللي كان شغال. مَنَفِلَّه مَنَفِلَّه يعني. الموضوع manual جدا ومش هاتعرف ت track ال changes بتاعتك بجد, ووقت ضايع مووت. لو الموضوع كبر هانغرق. وياه لو في اكتر من واحد شغال معايا. 
حتة ال`tracking and managing changes` دي **what is called ***Version Control***
انه يبقى عندي control على الhistory بتاع التغيرات اللي حصلت في ال project files بتاعتي اياََ كانت ال files دي ايه.
نوع ال file هيختلف شويه فالfeatures اللي هقدر اعملها بالversion control. 

في ال1970s كانت اول محاول لي التخلي عن شغل المَنَفِلَّه, ونقعد نcopy بقى وكده و اسامي folders وموال, وبدأو يعملو اول version control فال 70s.
ساعات بيسموها `version control system` او  `source control manager` لكن الفكره واحده.

 > 1. **Fast Forward (in Git and VCS)**
   >-**Definition:** 
  > A **fast forward** is a type of merge in **Git** , where the branch pointer is simply moved forward to the latest commit of another branch **without creating a new merge commit**.
-------------------------------------------------------------------
>🔁 2. **Roll Forward (in Databases, Backups, or Deployment Contexts)**
📌 **Definition:**
  A **roll forward** means **applying changes (logs, transactions, or versions)** to move **from an older state to a newer one**, especially after a **rollback** or failure. It’s widely used in:
  -**Database recovery**
  -**System restore operations**
  -**Deployment or migration rollouts**


_________________________________________________________________________________________
# History of Git  
![Pasted%20image%2020250402161612.png](images/Pasted%20image%2020250402161612.png)

المعلم **Linus Torvalds**  بعد ما عمل <mark>**Linux**</mark> ك open source, ف عايز بقى يحط ال Linux Kernel ده في مكان ما بحيث يكون `shared` والناس كلها ت connect عليه و تعدل كمان وت contribute و يرفع تعديلات. 
ف لجأ لواحده من الVersion control systems اللي موجودين و اختار واحد من اللي كانو متاحين واللي بيقدم خدمة for free. وكان اسمه **<mark>bit keepers</mark>**
كان خايف انهم ييجوا في يوم ويقولك مفيش حاجه free.
و قد كان سنه 2001 لغوا الخدمه الfree, قام المعلم يسكت لا راح عمل version control system سنه 2005
وعمل`Git`
________________________________
## 1.Getting started 
ال version control في منه 3 انواع 
>1-**Local Version Control Systems** (***LVC***) 
 2-**Central Version Control** (***CVC***) 
 3-**Distributed Version Control** (***DVC***) 

##### **Local Version Control Systems** (***LVC***) 

حاجه ليك انت شخصيا. local عندك على الجهاز بتاعك الشغل بتاعك. انت بتعمل الVersion control لنفسك والحاجات اللي انت بتعدلها. لا حد بيشوفه ولا هترفعه ف حته 
![Pasted%20image%2020250402152422.png](images/Pasted%20image%2020250402152422.png)

________
#### **Central Version Control** (***CVC***) 

 مثلا كلنا كprogrammers team شغالين على project للشركه,  وال source code بتاع الproject ده موجود على server في الdata center فالشركه
 و كلنا بن Accessعلى ال server ده عشان نعمل التعديلات اللي عايزينها والتعديلات بتاعتنا بتبقى`live`. 
 ![Pasted%20image%2020250402152851.png](images/Pasted%20image%2020250402152851.png)
 
وعشان ندخل ل الserver لازم طبعاََ تكون موجوده فالشركه او في communication شغاله live والcommunication بتكون upper running بينك و بين ال server زي ال `SSH` مثلا. 
لو في اي وقت او لأي سبب فقدت ال communication  بينك وبين ال server ده مش هتعرف تعمل اي حاحه على ال project.
>معندكش local copy انت شغال live على الserver`

_______
#### **Distributed Version Control** (***DVC***) 

شبه ال central ولكن في فرق 
بحيث ان ال source code بيكون shared بشكل متاح للناس على حسب رغبتي ممكن اعمله public او private مثلا, او احدد مجموعه من الناس بس اللي تقدر توصله. 
اللي بي connect على ال server عشان يشتغل على ال source code مبيشتغلش live على ال server.
اللي بيعمله هى انه بي`clone copy` من على ال project ده.

ايه بيclone دي؟!
هي مش download Copy؟ **لأ** لأن في فرق بين انك تdownload او تclone.
لما اعمل cloning من الserver بيشتغل زي Local Version Control بالظبط. الفرق بقى انه بعد ما يخلص الشغل بتاعه locally يقدر يجيب التعديلات او الdifferences بس اللي حصلت على الoriginal اثناء ماهو كان شغال. ما يمكن حد تاني دخل ظبط شويه حاجات او الauthor نفسه دخل ظبط شويه حاجات على server اللي خدت منه ال clone ده.
ف اقدر اجيب التعديلات اللي حصلت ف يبقى في **down stream communication** بيني وبين الServer. 
انا بعدل شويه تعديلات وبعدين أ`push` التعديلات دي وال author يعجبه الشخبطه بتاعتي ف يعمل incorporation او يmerge التعديلات بتاعتي في المشروع الرئيسي.
ف اه هو فعلا Download بس انا مش عملت download وفقدت الصله بال server خلاص. لأ ده انا عملت download ولسه في Relationship بين النسخه اللي على الserver والنسخه اللي موجوده Local معايا. بحيث تسهل عمليه ال ` communication UP and Down stream`
ف عدلت شويه حاجات ف اقدر أupload او أpush التعديلات اللي عملتها <mark>بس</mark>, اتعدل حاجات فال Server اقدر اخد الحاجات اللي اتعدلت <mark>بس</mark>.


>note 
ان اغلب الحاجات اللي بعملها بعملها والserver بيكون offline اعدل تعديلات واشخبط شخابيط والعب عالحيط ما انا عندي Local copy ووقت ما يكون في internet connection ابقى أconncetو  ابقى أpush واعمل كل حاجه. 

حاجه كمان انا مش بس بconnect على الdistributed version اللي على الServer, لا ده انا ممكن أconnect فنفس الوقت ولنفس الproject على واحده تاني او PC تاني. 
ف كده انا باخد التعديلات من ال Server الاصلي اللي عملت منه الClone ومن واحد تاني شغال على نفس ال Project. ف اشوف التعديلات من ده ومن ده أpush تعديلاتي هنا وهنا.
![Pasted%20image%2020250402160100.png](images/Pasted%20image%2020250402160100.png)

عشان كده اسمه **distributed version control**. حيث انه مش Local ومش Central.
>**GIT is a Distributed Version Control.**

ينفع يبقى local عادي

# GIT Basics 
ايه اللي يميز *<mark>Git</mark>* عن غيره, ايه المختلف بينه وبين الباقي.
في حاجات كتير تفرقه عن الباقي اهمهم مثلا : 
انه git لما بتعمل التعديلات بتاعتي, بيسجل التعديلات دي ازاي؟؟ ازاي بيtrack الversioning عندي فالfiles.  
اول حاجه باقي الversion control systems التانيين بيعملوا ايه؟؟
اول حاجه بتاخد snapshots من كل حاجه موجوده عندي في الProject بتاعي فالاصطباحه كده, جيت انت مثلا فتحت python file، وجيت زوّدت فيه سطر جديد، وعملت **commit** عشان تقول "دي نسخة جديدة".
في نظام زي **Subversion**، مش هيخزن الملف كله تاني. هياخد بس **الفرق**، يعني السطر اللي زوّدته ده بس، ويحتفظ بيه. دي اسمها **incremental differences** أو الدلتا (<mark>delta</mark>).
بعد كده، جيت تاني يوم وزوّدت سطر جديد تاني وعملت **commit** كمان.
هنا version control هيخزن السطر الجديد ده بس كمان، مش هيخزن الملف كله من الأول. يعني كل مرة بيضيف الاختلاف الجديد للي قبله.
كده معايا ال first snapshot والdelta اللي هي الdifference السطر اللي زاد فالاول وبعد كده ال Version التاني  سطر كمان زاد.

> - **Initial Commit**: You have a Python file in your project, and you commit it. The VCS stores the entire file as the baseline (e.g., Revision 1).
> - **First Modification**: You open the Python file, add a single line of code, and commit this change as a new version (e.g., Revision 2). The VCS doesn’t store the entire file again; it records only the **incremental difference**—the added line—along with metadata indicating where it was inserted.
> - **Second Modification**: The next day, you add another line to the same file and commit it (e.g., Revision 3). Again, the VCS stores just the new line as a delta, referencing the previous version (Revision 2).
> 
> - Revision 1: Full file.
> - Revision 2: Revision 1 + delta (first added line).
> - Revision 3: Revision 2 + delta (second added line).

بحيث ان لو الدنيا فرقعت خلاص وانا هbuild الproject من الversion control  اللي موجود عندي.
اللي هيحصل ان الversion control بيinstall اول snapshot خدها زمان و يعمل replay لكل delta اخدها.
ف لازم عشان يوصل لversion معين لازم يعدي على كل ال versions اللي قبله.
that what is called **<mark>incremental or differential version control</mark>**.

_______________________
 اومال git بيعمل ايه؟؟
  لو غيرت حرف من File هياخد snapshot تاني من الfile كله. ف في كل تعديل هياخد snapshot من كل ال file.
  طبعاً ده احسن كتير. زمان مكنش في disk space تكفي انك تعمل حاجه زي كده.  لكن محدش دلوقتي بي consider ان الspace مشكلة يعني. 

![Pasted%20image%2020250402220237.png](images/Pasted%20image%2020250402220237.png)


# Git Architecture 
اي Architecture فالدنيا  بيبدأ ب requirements, انت عايز ايه سواء عامله عشانك زي لينوس مثلا "عشان يحط Linux kernel عليه" او عشان الشركه طالبه حاجه معينه, فالاول لازم اكون عارف المشاكل اللي عند الcustomer اللي بيحاول يحلها بالsolution بتاعي. 
ايه الحاجات اللي اساسي لازم تكون موجوده و الحاجات اللي مش لازم تكون موجوده واللي برضو nice to have و هكذا.  وبنقسم ال requirements ل 
1-`function requirements`
الfunctions او الحاجات اللي الproduct هيعملها.
2-`nonfunction requirements`
مثلا صفات الproduct سواء speed, performance, security, etc.

عندي file اسمه A.txt هو `version 1`  موجود جوه ال**working Directory or tree** بتاعي.
فكره الversion control انه مثلا الfile ده عدلت فيه حاجه ف مبقاش ال version بتاع زمان بقى `version 1.1` مثلا. ف انا عايز الversion control بتاعي يtrack الحاجات دي, انه كان في file اسمه A.txt و فلان الفلاني عدل فيه في وقت ما و اصبح version 1.1 بدل version 1. ف انا عايزه يسجل ال versions وكل الكلام ده.
ف هيبقى عندي الA.txt جوه ال version control.
في git مش بيتقال عليه version control بنقول عليه **repository**  وعشان ندلعه <mark>git repo</mark>.
ف انا عايز ال`repo` بتاعي يبقى فيه Version 1 و version 1.1, خد بالك ان دايما اللي انت شايفه فال working directory و بتتعامل معاه على الOS هو version واحد بس اللي هو اخر version, انت مش شايف 100 file مثلا.
لكن اللي عليه كل ال copies الversions القديمه هو ال `git repo`.

#### Requirements
1-<mark>**Track Everything**</mark>
بمعني Everything كل ال files كل ال Folders اللي موجوده عندي, ومش أtrack ال content بتاع الfile بس لا كل حاجه سواء content, MetaData, etc.
2-<mark>**OS Independent**</mark>
يكون portable مش اروح اعمل الكلام ده على windows مثلا واجي انقله في OS تاني ميشتغلش.
لازم يكون contained اقدر انقله من windows ل Linux ل mac ويشتغل عادي جدا واشوف كل الhistory, وكمان لما اجي اعمل update لو اصلا الsource code شغال على windows وانا شغال على Linux يشتغل عادي برضو.
3-<mark>**Unique ID**</mark>
كل object -"اي حاجه بتtrack it اياً كان .Folder, file ,etc "- لازم يكون ليه `Unique ID`
4-<mark>**Track History**</mark>
مش بس اعرف ال versions القديمه لا اشوف مين حصل قبل مين, ومين بعد مين و ايه اللي حصل بعد كذا, ومين عدل وبعدين رجع ف كلامه.
5-<mark>**No content change**</mark>
لما تيجي تtrack مثلا file متكتبش حاجه جوه الfile, ت track الfile من غير ما تلمسه. متجيش ناحية الfiles اللي شغال فيها. ولا حتى ال metadata متعدلش مثلا فالProperties بتاعة ال file.
عشان لو عملت space حتى هيعتبر ده تعديل.
__________________________________________________________________________

**How can we apply these requirements?**

![Pasted%20image%2020250402225503.png](images/Pasted%20image%2020250402225503.png)

معرفش أtrack everything كده, افرض ال file ده غير اسمه ل b.txt مثلا ف مش هعرف اوصله, 
محتاج انه الحاجه اللي بتعرف او بتميز الobject اللي بعمله tracking ده متكونش جزء من الحاجات اللي بعملها tracking, مبتتغيرش يعني مفيش مجال للتعديل فيها. 
اسم الfile مميزه ليه ماشي, لكن افرض انا مسحت الfile ده و عملت واحد تاني اسمه برضو A.txt هنلغبط بعض بقى. اصلا الاسم ده من الحاجات اللي انت بتtrack it ف مينفعش تبقى هي الID بتاعك.

الحاجه اللي انت هتعملها tracking سواء كان .file, folders, etc مينفعش تبقى بالformat القديمه بتاعتها لأن كل حاجه موجوده قبل كده انا اصلا محتاج اعملها tracking, يبقى شكلها لازم يتغير يتحول من الشكل المعروف تتحول الى object. 

>اذا الfiles وال Folders بتتحول ل objects جوه git

**what is git object?**
<mark>**هي الحاجات اللي git بيعملها tracking, في 4 حاجات بيعملها tracking.**</mark>
1-**blob**
ببساطه هو الfile ,هو مش بالظبط. 
بس الفكره في `tracking everything`,الfile هنعمله tracking هو وال metadata بتاعته, غير الcontent هنtrack ال metadata.
الmetadata هي نوع الfile, الpermissions, الsize, الname بتاع الfile. ف انا عايز أtrack كل ده, ف مبقاش file زي ما معروف,  فاتغير اسمه ل `blob`.

2-**tree**
هي الfolder بس نفس الفكره زي الblob. اللي هو عشان بتtrack الcontent and metadata فمبقاش الfolder زي ما معروف بقى اسمه `tree`.
مبقاش folder بقى object فيه الcontent and metadata.

3-**commit**
4-**Tagged annotation**

***____________________________________________________________________________________________***
عشان ن apply فكره ال <mark>**OS Independent**</mark>, الحل الوحيد ان Git ده يبقى عباره ده **simple folder structure** ان git يبقى عباره عن **folder**, احطه فأي حته يتقري و يشتغل. طب والcontent؟ يكون معظمها **simple files** مش Database بقى والكلام ده ممكن نقلل الencryption لأن Already عندي ال security بتاعة ال project و ممكن نعمل compression بس عشان السرعه مش اكتر .
الrepo ده كله يبقى عباره عن Folder. هيساعدني ابقى portable كل الupdates والmodifications والversions كلها في folder واحد بس, احطه فأي حته اشوف اللي موجود فيه وكل الsnapshots وكل ده.

نعمل ده ازاي؟
 نروح للworking directory اللي فيه ال files وال folders اللي بتtrack it, الgit repo بقى اللي جواه كل الsnapshots وال objects, هيبقى جوه الWorking tree ده شخصياً. بيبقى `hidden folder`, اسمه <mark>git.</mark> ده هيحول لي الproject folder كمان ويسميه `repo`.
الrepo = الproject folder بتاعي اللي جواه ال`git.`. الrepo ده لما انقله من مكان ل مكان, من server ل server, من Linux ل windows  اياً كان ف كله شايف نفس الحاجه ونفس الversions و بيستعمل نفس ال commands, ايوه identical.
***____________________________________________________________________________________________***
**how can we apply Unique ID?**
دلوقتي مش هيبقى عندنا file و folder لا, ده عندنا blob و tree. واسماء الfiles والfolders مش هتنفع تبقى identifier. 
ف احنا محتاجين identifier, محتاج اعرف الobject ده انهي object, وهو Related بأنهي file او folder.
محتاج حاجه أ unique identify بيها الobject.
في طرق كتير عشان اعمل ده. 
1-في module في git اقدر أgenerate بيه `hash function`, 
>or built-in mechanism that uses a hash function, It is seamlessly integrated into Git's core architecture and automatically generates unique identifiers

![Pasted%20image%2020250403122821.png](images/Pasted%20image%2020250403122821.png)

ال$X$ ممكن تكون مثلا repo ,character, file, folder اي حاجه, وعلى حسب الالجوريزم اللي بتستخمه الhash function ,بيكون شكل ال$F(x)$, ممكن مثلا تستخدم Algorithm معين فالhashing ف تطلعلي شويهhexadecimal characters وتبقى unique.
>The output **F(X)** is a **160-bit** hash value, commonly displayed as a **40-character hexadecimal string** (e.g., a1b2c3d4...). This string serves as a unique identifier for the input data **X** within the Git repository, such as a commit, file, or directory.
 .The specific algorithm used in **Git** is **SHA-1** (`Secure Hash Algorithm 1`), a cryptographic hash function.

بناءاً على الحاجه اللي موجوده في $X$ و الالجوريزم المستخدم في الhash function, الناتج بتاعها بيبقى Unique.
لكن بشرط انها تبقى Deterministic, يعني نفس ال$X$ بتطلع نفس ال$F(x)$ في كل مره هدخل$X$ على الhash function. 
من الhashing Algorithms المشهوره **SHA,MD5** وال SHA في منه SHA1 و SHA256. 
تذكر ان احنا بنعمل كل ده عشان نخلي كل الobjects في git يبقى ليها Unique ID. 


![Pasted%20image%2020250403130628.png](images/Pasted%20image%2020250403130628.png)
ال**stdin--** عشان ياخد input من الpipeing.
الcommand اللي بيعمل نفس الكلام ده في Linux اسمه`shasum`.
![Pasted%20image%2020250403130935.png](images/Pasted%20image%2020250403130935.png)

طب ليه الاختلاف مع ان الاتنين بيستخدموا SHA1؟؟
زي ما احنا عارفين ان git مش بس بياخد الContent بتاع الObject كمان بياخد الmetadata, اللي بيحصل ان git مش بيشوف `Hello, Git` كده لا ده هو بيزود عليها حاجات  هو بيزود 3 حاجات 
1- type
2-size
3-null character
ف لما تديله `Hello, Git` مش هياخدها كده اللي هو حته text وخلاص لا هو بيجود من عنده الاول بعد كده ياخد كله على بعضه ويعمل الhash ل الobject ده.  
ف هو بيشوفها كده 
![Pasted%20image%2020250403132411.png](images/Pasted%20image%2020250403132411.png)
الtype بعدين الsize اللي هو `11` مش 10 عشان في line break فالاخر مش ظاهر بس الterminal بتحطه. ثم null  character بعدين يحط الtext. 
اي تغير ولو ايه هيفرق لأن الAlgorithm شغال اصلا على ال ASCII وال binary format.

عشان Linux يشوف ال`0\` انه escape character مش مجرد text عادي بنضيف option `-e` على الecho command.
![Pasted%20image%2020250403133207.png](images/Pasted%20image%2020250403133207.png)

لو جربت ت pass الformat اللي git بيشوفها وبيعملها ل`shasum`  هيطلعلك نفس ال$f(x)$ او نفس الhexadecimal characters.
وgit بيعمل الsha1 عشان يتأكد ان مفيش اي تغيير. وهي الRequierment الجايه.

***____________________________________________________________________________________________***

**how can we apply track history?**
هي الطريقه اللي git بيعرف بيها الfile ده اتغير ولا لا. هيعرف منين انك غيرت الfile؟ هيعرف من ال Sha1 ده.
هيعرف ان في تعديل في تغيير حصل, لو زودت space واحده حتى, هيطلعلك sha1 تانيه خالص.
اللي بيحصل ان gitبيعمل sha1 على الfile ويقارنه بال sha1 اللي مخزنه عنده فالrepo. لو زي بعض يبقى انت معدلتش حاجه لكن لو مختلفين يبقى حصل تعديل.

____________________________________________________________________________________________

الversion control systems اللي كانوا موجودين قبل كده قبل git يعني واللي منهم لسه موجودين لحد دلوقتي. 
كانوا بيعتمودا حاجه اسمه `two-tree architecture`
اللي هو يبقى عندي الworking tree والRepo, انا اشتغل فالworking tree وبعدين اعمل التعديلات  بتاعتي و ا push التعديلات دي على الrepo و الrepo بيخزنها. جيت وقت تاني عملت تعديلات وبعدين أpush اللي عملته ف يخزن version جديد ويشيل.
ف كده انا عندي 2trees واحد الWorking tree اللي بفتح اشوف فيه الfiles واعدل فيه او الOS يعني , والتاني اللي متخزن فيه الversion control والobjects. 

![Pasted%20image%2020250403143540.png](images/Pasted%20image%2020250403143540.png)
That is what is called a **two-tree architecture**.

________________________________________________________________________________

ومش ده الgit بيعمله. git عنده***three-tree architecture***, 
in Git architecture introduced 
اكيد عندي الworking directory و الrepo ,في النص مابينهم بقى موجود tree تانيه اسمها `staging Area` او الindex. هو يبان tree لكن هو physically عباره عن file.
مثلا عندي File و عدلت فيه بدل ما اوديه مره واحده على الRepo زي ال `two-tree architecture` لا بعمله staging الاول, staging اللي هو بهيأه وبظبطه عشان يتعمله commit والخطوه اللي بعد كده اني اعمله commit ل الrepo.
طب ايه الCommit دي؟
معناها هو تrecord ألتعديل بتاع الobject فالrepo. اللي هو بعتمد التعديل ده فالversion control repo بتاعي.
![Pasted%20image%2020250403150600.png](images/Pasted%20image%2020250403150600.png)

هل هو مجرد Step ملهاش لازمه؟
الstaging area او موضوع الcommit او انك ت save الobject او الversion الجديد ده على خطوتين بيserve اكتر من حاجه, اول حاجه انه بيserve الworkflow بتاعك. بدل ما يبقى عندي 20000 Version اتوه منهم, لا يبقى عندي فرصه اراجع اللي عملته وابص عليه واشوف الفرق بينه وبين اللي فات فالrepo و اقرر قرار نهائي هل اعتمد الكلام ده ولا لا.

وبرضو من اللي بتوفرهولي 
لو مثلا عايز اعدل حاجه ف مثلا web project والحاجه دي موجوده يعتبر في كل صفحات الweb project.
ف هعدل كده في ييجي 100page ولا حاجه, ولكن كل ده تعديل related ل request واحد ,هو حاجه واحده اللي بعدلها مثلا بعدل ارقام الشركه في كل الpages. هما related بس بعدلها ف files كتير.
ف هعدل كل file واعمله staging وكلهم related لحاجه واحده. that is what is called `batch` 
بعد ما اعمل staging  لكل واحد واخلصهم, هعمل commit مره واحده واعتمد التعديل اللي حصل في كل الpages دي مره واحده, ف يبقى تعديل واحد ل كذا File. فينزل فالRepo ك version واحد بس. 

ودي من الحاجات اللي ممكن استعمل فيها الindex, وممكن برضو استعملها فالTrouble shooting لو حبيت ارجع فالversion أو أrestore. الstaging area هي المنطقه اللي براجع فيها, قبل ماتبقى عندي فالworking tree لازم تاخد بالك ان الworking tree مش folder عمال تلعب فيه وخلاص ده ممكن يكون ال live project بتاعك اللي بيserve فالشركه والناس هتستخدمه, ف مش مكان لعب اعملcommit على طول او أrestore على طول على الworking tree بتاعي لازم اشوف هينفع ولا لا ,لازم اراجع و اقارن واقرر اه او لا وأ harden, finalize or solidify my changes فالworking tree عشان يعدل فالproject. 
ال**three-tree architecture** بيديني Work Flow افضل واحسن واشيك كتير.  
![Pasted%20image%2020250404191354.png](images/Pasted%20image%2020250404191354.png)

وفي command واحد بس اكتبه هيعمله الstaging والcommit في مره واحده بس, مش بيskip الstaging هو بيعملهم الاتنين في مره واحده.
_____

# Git File States
**الindex و ايه اللي بيحصل فيه؟**
الindex او الstaging area ده هو مجرد file. 
لو لأول مره بintialize الrepo بتاعي 
![Pasted%20image%2020250403155527.png](images/Pasted%20image%2020250403155527.png)

فgit هنا ميعرفش اي حاجه عن الFile اللي فالworking tree بتاعي,  الState او الحاله بتاعة الfile ده دلوقتي اسمها `UNtracked`. يعني git شايفه بس مش متابع فيه اي حاجه, عدل زي ما انت عايز واصلا Git مش متابع الversions بتاعته معندوش منه objects او snapshots او اي حاجه ليها علاقه بيه.

اول حاجه طبيعي بعملها فالWork Flow بتاعي اني بstage الfile ده بضيفه ل الindex. هي اني بحول الfile ده من`untracked` ل `tracked`. وده عن طريق الstaging. هنا بقى ييجي يدور الstaging area 
ايه اللي بيحصل لما اجي احوله من untracked ل tracked؟
اول حاجه بتحصل انه بيتعمله `SHA`,ثم بنعمله tracking عن طريق Command اسمه `git add`. اللي بيحصل لما اعمل `git add` لuntracked file, انه بيتسجل فالindex  او الstaging area, ال`SHA` بتاعه بيتكتب فالindex. بعد ما يتسجل فالindex, بييجي git يقوم ي initialize object ليه فالrepo, يintialize blob ليه فالrepo بنفس الSHA1 بتاعه اللي موجود فالindex. 
كل ده ولسه git معملوش version1. هو عمله tracking بس. الversion بيتعمل فالخطوه التانيه لما اعمل `git commit`  لما اعتمد.

>note 
> ال`git commit` هي الstep اللي بيتعمل فيها اول snapshot. اومال الblob اللي الgit عمله ده ايه؟ده يا معلم لزوم الtracking بس عشان يقولي اه حصل تغير هنا وهكذا لكن عشان اخد snapshots منه لازم أ`git commit`. 

![Pasted%20image%2020250403171557.png](images/Pasted%20image%2020250403171557.png)

>التسلسل الطبيعي
1-`git add` : stage files for old files, if new file convert it form untracked to tracked.
لو الfile مش جديد وalready عدلت فيه قبل كده وعملتله 1000 commit قبل كده وجيت عدلت فيه ف  الfile بيبقى `modified`. عدلت ولسه معملتش commit.
2-`git commit` :
تعتمد التغيرات ك version جديد فال repo. او ال file جديد بتعملي اول version.

***____________________________________________________________________________________________***
**file states**

بالنسبه ل git بيشوف الfiles ازاي؟ 
الكلام ده جوه الrepo
![Pasted%20image%2020250403174710.png](images/Pasted%20image%2020250403174710.png)

اي file عندي بيبقى ليه حاله من اتنين. Either `untracked(U)` or `tracked`.
الtracked بقى بيبقى `(M)modified` او `unmodified`
1-`modified(M)`
يعني اخر version من الfile فالrepo اتغيرت, انت عدلت فالworking tree ف كده الfile اللي قدامك فالworking tree مش هو هو اخر version فالrepo.
ف git بيقولك اخر version عندي من الobject ده غير اللي عندك فالworking tree فظبط نفسك بقى.
2-`unmodified`
يعني بعد ما عدلت فيه وعملت `git commit` وبقى في نسخه. ف اصبح ان اخر version عندي فالrepo  هو هو نفس الversion اللي قدامي فالworking tree.
____________________________________________________

# git installation
ممكن تنزله على Linux عن طريق الcommand ده `sudo apt install git `
![Pasted%20image%2020250404191310.png](images/Pasted%20image%2020250404191310.png)

>"The first step is to create a directory that will serve as the project folder, which will later be initialized as a Git repo."
the project folder is like a home for both your current work and the record of all past versions. The `.git` folder inside it is what makes version control possible—it’s where Git stores everything it needs to let you go back to older versions or track your changes.


بس قبل ما اعمل الinitialization والfolder بتاع git وكل ده في configuration مهم لازم اعمله لgit.
هو اني بس اكتب اسمي والemail بتاعي, ده  اقل Configuration ممكن يحصل, في configurations كتير ممكن تحصل, ممكن اشوف الlist بتاعة الconfiguration  اللي في git. هو فالاول وفالاخر مجرد file  اسمه `config file` واقدر اعدل فيه manual عاي.
![Pasted%20image%2020250404185128.png](images/Pasted%20image%2020250404185128.png)

ده عشان لما اجي اعمل الstaging بتاع الfile او الcommit و ابعت الversion على الrepo بتاعي لازم يسجل ويقول مين اللي عمل التعديل ده مين اللي اعتمد الكلام ده. ده distributed version control فلازم يسجل ان فالوقت كذا فلان الفلاني عمل كذا كذا. يعني بيtrack history بي track everything. 

note 
حتى الحاجات دي ممكن اعدلها, ال`global--` معناها هي global بالنسبه للuser, يعني كل الprojects بتاعتك انت او اي folder تاني انت هتعمله initialization git repo على نفس الجهاز هياخد نفس الname والemail ده. وده بيعدل في file اسمه <mark>**gitconfig./~**</mark>.
لكن لو عايز اعمله global بجد اللي هو على الSystem كله لكل الusers  فبنستخدم option تاني اللي 
هو `system--` وده بيعدل في file اسمه <mark>**etc/.gitconfig/**</mark>.
وممكن اعمله على الlevel بتاع الproject ده بس من غير `global--` ولا `system--` وده بيعدل في file اسمه 
<mark>**/.git/config**</mark> 
![Pasted%20image%2020250404194808.png](images/Pasted%20image%2020250404194808.png)

لو عايز اشوف الConfiguratio هستعمل
![Pasted%20image%2020250404195540.png](images/Pasted%20image%2020250404195540.png)
كده انا جاهز اني استعمل Git.  فهروح ل الproject folder و أinitialize الgit repo,
![Pasted%20image%2020250404202102.png](images/Pasted%20image%2020250404202102.png)

خلاص عملت ألproject Folder وعملت file جواه, اشتغلت فيه يعني. عايز بقى أinitialize git جواه و احول الproject Folder ده الى Repository ,ف هعمل ده عن طريق اني اقوله `git init` لاحظ انك لازم تexecute ألcommand ده من جوه الproject folder. اول ما تexecute الCommand ده, بيتعمل folder مخفي إسمه `git.`، وده اللي بيخزن كل الـ versions والتاريخ بتاع الproject.
![Pasted%20image%2020250404202848.png](images/Pasted%20image%2020250404202848.png)

وحتلاقيه عمل ال folder اللي اسمه`git.` 
![Pasted%20image%2020250404203233.png](images/Pasted%20image%2020250404203233.png)

كده تَحول الproject بتاعك الى repo.
![Pasted%20image%2020250404203913.png](images/Pasted%20image%2020250404203913.png)

الconfig file هو الfile اللي فيه الconfiguration زي ما قولنا. الobjects directory هنا بقى في الgit objects كله بقى الblob والtree والcommits والtagged annotation.
لو دخلت جوه الobjects directory مش هنلاقي objects خالص, which is make sense.

طبعاً الfile اللي عملناه فالproject folder دلوقتي الstate بتاعته `untracked`.
ولذلك عشان اشوف الFiles اللي عندي واشوف الحاله بتاعتهم هنستخدم command اسمه `git status` بيوريني حاله الfile اللي عندي سواء tracked او untracked او modified او unmodified و الوضع ايه فالworking tree. ولازم ت execute الcommad ده في الworking tree. 
![Pasted%20image%2020250404205503.png](images/Pasted%20image%2020250404205503.png)

No commits yet:
يعني مفيش اي Snapshots بأي شكل, مفيش اي version من الcode بتاعك.
Untracked file:
بيوريلي الuntracked file, بيقولك اهو في untracked file اسمه `file.txt`
حلاوه `git status`  انه بيقترح عليا اعمل ايه. 

____________________________________________________________________



# Explore Git Objects and Trees
احنا عندنا three-trees ال<mark>working tree</mark> وال<mark>staging tree</mark> اللي هو الindex وال<mark>repo tree</mark> اللي هو فيه الversions والcommits و الobjects وكل ده. عشان ال**three-tree architecture**.

طب لو انا عايز اشوف اللي في ده وفي ده, مثلا ابسط حاجه هاشوف اللي فالworking tree بالcommand `ls`.
![Pasted%20image%2020250404232116.png](images/Pasted%20image%2020250404232116.png)

زي كده بقى انا عايز اشوف الحاجات اللي فالindex اللي هو فالStaging areaوالحاجات اللي فالrepo, اعمل ايه؟
الحاجات اللي فالindex ليها Command هيوريني كل حاجه فالstaging area اللي هو `git ls-files`.
![Pasted%20image%2020250404232413.png](images/Pasted%20image%2020250404232413.png)

هنا لاقيناه فاضي وده معناه ان الrepo بتاعي مش بيtrack اي files خالص وده معناه إن الـ staging area عندك خالية تمامًا من أي ملفات أو تغييرات متظبطة للتسجيل. ماهو الindex هو اللي بيعرف git يتابع انهي Versions وانهي files عشان git يقارن بيه. وده اللي الindex بيعرفه لما تعمل `git add` عشان يضيف تعديلاتك على الindex ولو file جديد يبدأ الtracking. 

بالنسه للrepo مفيش command مباشر, بس في طريقه في technique من Linux نفسه.
ممكن استخدم find command عشان اشوف حاجه معينه بدور عليها مثلا بدور على الobjects اللي من نوع file
![Pasted%20image%2020250404234348.png](images/Pasted%20image%2020250404234348.png)

يبقى كده عندي file واحد فالworking tree والrepo والindex فاضيين.
![Pasted%20image%2020250404234603.png](images/Pasted%20image%2020250404234603.png)

ف اول خطوه عندي اني أstaged الfiles اللي عندي عن طريق `git add`. في الحاله دي `git add` بيحول الfile من `(U)untracked` الى `tracked`. و بيجهزوا لأول commit.  
الطبيعي اني هكتب `git add` وبعدها اسم الfile.
![Pasted%20image%2020250405000851.png](images/Pasted%20image%2020250405000851.png)

يعني لو 100 file فالproject هقعد اضيفهم file file ?!!
اقدر استعمل الregular expressions وال glob patterns بتاع الfile names 
![Pasted%20image%2020250405001108.png](images/Pasted%20image%2020250405001108.png)
أو اقوله ضيفلي كل حاجه موجوده عن طريق `*` او `.`"current directory" .
والطبيعي فالامر اني مش محتاج اعمل الكلام ده اللي هو مش محتاج أtrack كل files اللي عندي, ماهو في files مابتتغيرش اصلا ف مش محتاجه وجع دماغ كل مره هتبقى فالsnapshots بلا سبب زي ال OS generated files. 
كل حاجه بتبدأ ب `git add`.
نعمل `git status` نشوف ايه الدنيا دلوقتي.
![Pasted%20image%2020250405001919.png](images/Pasted%20image%2020250405001919.png)

هنا اتغير و بيقولك ان `file.txt` هو new file و من الfiles عايزه تcommit, ال`changes to be committed`. و برضو بيديك نصيحه لو عايز ترجع في كلامك عملت Staging بالغلط مثلا اعمل كذا فيرجعه من الStaging ل الunstage.

هانشوفه بقى فالindex لما نعمل `git ls-files`
![Pasted%20image%2020250405002532.png](images/Pasted%20image%2020250405002532.png)
في برضو حاجه احسن شويه هو option `-s`  مش بس بيعرض الfiles, لا ده بيوريني ال`SHA1` بتاعهم. و بيوريني حاجه اسمها الcreate mode بعرف منها نوع الfile والpermissions بتاعته.والStaging state `0`

![Pasted%20image%2020250405002833.png](images/Pasted%20image%2020250405002833.png)
كده انا عرفت ايه اللي عندي فالindex, في file عندي فالindex والfile ده بقى tracked و عن طريق ال`SHA1` بعرف state الFile دلوقتي modified ولا unmodified.

نشوفه في الRepo tree عن طريق الfind 
![Pasted%20image%2020250405003635.png](images/Pasted%20image%2020250405003635.png)
اها اختلف اهو, بقى في عندي object مش object بس ده في folder اسمه `b7` كمان. 
![Pasted%20image%2020250405012347.png](images/Pasted%20image%2020250405012347.png)

لو ركزت شويه هتلاقي ان `b7` هما اول 2characters من ال`SHA1` بتاع الfile, وهتلاقي ان اسم الFile اللي جوه  `b7` هو باقي ال`SHA1`
![Pasted%20image%2020250405012718.png](images/Pasted%20image%2020250405012718.png)

دي الطريقه الليgit بيsave بيها ال objects بيستعمل  `Folder structure`, مبيرميش كل objects كده على الroot بتاع الobjects directory,  تنظيم مش اكتر, وبيستعمل ال `SHA1` عشان يدي اسم للfolder والfile.
الobject او الblob هنا يعني ,هو الfile اللي جوه `b7`.

طب هنا عرفت انه blob عشان انا عارف ان ده file, طب لو عندي عشروميت file و folders اتصرف ازاي؟ ,هعرف منين؟ كل واحد هلاقيه 40 decimal characters هعرف ازاي ان ده اصله tree وده واصله file الى اخره.
في command اسمه `git cat-file` نفس الcat العادي بس ده بيخليني اقرأ أل content بتاع الcompressed files بتاعة git وهستخدم option`-t` بعد كده ال`SHA1` بتاع الobject.
![Pasted%20image%2020250405014651.png](images/Pasted%20image%2020250405014651.png)

هو بيقرأ الcontent بس مش بيقرأ كله ال`t-`  بتخليه يقرأ الtype. عشان اشوف الsize هستخدم option`-s`.
لو تفتكر الshasum كان فيه size, type, and content .
وعشان الcontent هستخدم option `-p`
![Pasted%20image%2020250405015315.png](images/Pasted%20image%2020250405015315.png)

ده مش snapshot ده مجرد what is called `base blob` المعلم git بيستخدمه عشان يtrack الاختلافات.
كل ده جزء من ال indexing.
![Pasted%20image%2020250405015609.png](images/Pasted%20image%2020250405015609.png)
***___________________________________________________________________________________________***
طب اعمل الversioning ازاي و ازاي أapply موضوع الtrack history واعرف مين قبل مين وكل ده, و اجيب version قديم والحوارات دي كلها؟؟!

بعد ال `git add` في ال `git commit`. 
![Pasted%20image%2020250405021011.png](images/Pasted%20image%2020250405021011.png)

`-m` 
دي اني بقوله انا ب initialize اول Version عندك فالrepo.
وبنحط زي comment او رساله اعرَّف بيها غيري ايه اللي حصل في الversion ده ايه اللي بيميزه وايه الجديد فيه  بدل ما الحوار كله بقى sha sha كده.

دلوقتي بقى عندي اول version من الproject بتاعي. 
![Pasted%20image%2020250405021410.png](images/Pasted%20image%2020250405021410.png)

لو تلاحظ ان مفيش اي حروف جمب اسم الfile "ده لو بتستخدم IDE زي VS Code هما فاهمين git ماشي اذاي"وده معناه ان الfile ده unmodified, اذاً النسخه اللي قدامي دي هي هي اللي فالgit repo.

دلوقتي نشوف الobjects بعد ما عملنا `git commit`, 
![Pasted%20image%2020250405134335.png](images/Pasted%20image%2020250405134335.png)
ايه ده 3objects!! ده انا معنديش غير blob واحده بس.

احنا اتفقنا اننا لازم ن apply فكره `track everything` و`track history` و `Unique ID
الfile للي عملتله tracking ده, مش موجود في folder صح كده, طب افرض اني مسحت الFile او افرض ان الfile عشان اوصله ادخل foldersكتير وجيت مسحت الfile ده, مش لازم ابقى انا عارف ال tree hierarchy بتاع الfile وهو في انهي folder.
لذلك لما باجي أcommit الfile مش بcommit ألcontent بس لا, ده انا ب commit ألmetadata بتاع الfile اللي من ضمنها الpath بتاعه.

ف كده في كل مره بعمل فيها commit هكون واخد الblob وكمان واخد الtree بتاعه اللي هو الfolder او  موجموعه الfolders اللي فيها الfile ده. 
![Pasted%20image%2020250405150247.png](images/Pasted%20image%2020250405150247.png)

لو جيت عدلت فيه تاني او عملت file او عملت folder جديد مثلا, وعملت `git add` و `git commit` تاني, فكده في Version جديد ونفس الكلام تاني عدلت تاني فأصبح في 3versiosns كل واحد فيه 3 او 4 blob مع كام tree. فالحوار هيرخم منين بيودي على فين. ف اعرف منين ان مثلا ال4 blobs دول تبع الversion الفلاني.
مثال تاني مثلا عندي فالworking tree موجودfolder  فيه 2files ف انا عدلت في واحد منهم, قصاد ده في الrepo هيحصل تعديل في الobject والtree. في الrepo بقى عرفت ازاي ان ال2files دول مع بعض ماهو الobjects في git متفرطين "كله على بعضه", كل object ليه file مستقل عن الباقي, اعرف منين انهم related لبعض و مع بعض في نفس الcommit .
اعرف منين انهم `batch` واحد, انه الobjects دول اتعملو كversion وحده واحده. 

**to solve this problem--->**
ف git عمل object تالت غير الـ blob والـ tree, اسمه ال`commit object`, عباره عن wrapper,  فيه بيانات بيقولك ان الbatch ده او الcommit ده كان فيها اي من trees و blobs ومين اللي عملها واتعملت امتى. و pointer بيشاور على أول تعديله اتعلدت `root tree`  ومنها اوصل للباقي.

> و pointer بيشاور على ال`parent commit`,   الcommit اللي قبل ده يعني. وكل commit كده بيشاور على اللي اتعمل قبله.
> اول commit خالص ما عندوش parent (يعني ما فيش commit قبله). كل الـ commits اللي بعده بتبقى مرتبطة بيه بشكل غير مباشر عن طريق سلسلة الـ pointers.
>  "دي من عندي لكن النقطه دي البروف شرحها قدام عند $02:07:00$ "

![Pasted%20image%2020250405152424.png](images/Pasted%20image%2020250405152424.png)

عباره عن `wrapper` بيحدد مين اللي عمل الcommit نفسها `Committer Information` واللي عمل التغييرات (الـ `author`) وامتى اتعملت (`timestamp`) والتعديل اللي اتعمل، وكمان بيديك `pointer` للـ `parent commit` اللي قبله، ومنه تقدر تتابع باقي الـ history. و فيه الـ `commit message` اللي بتشرح التغييرات دي عشان يوصفلي التعديل, زي comment كده. و بيوريني فين الtree اللي حصل فيها الكلام ده, عن طريق انه بيوريني اول[^2] root tree اتعدل فيها لو انت عندك اكتر من File عدلت فيهم ف من الـ root tree دي، بقدر أوصل للـ blobs والtrees اللي جوه.

اذاً الcommit هي الwrapper اللي بيقولي ان الblobs او الtrees دول اتعدلت كده مع بعض في مره واحده 
.![%20Pasted%20image%2020250405153305.png](images/%20Pasted%20image%2020250405153305.png)

و بما ان هو object ف بيبقى ليه `sha1`.

اذا التلاته اللي ظهروا فالاول لما اجيت اشوف الobjects هما الblob اللي هو file.txt والtree واللي هو الdirectory `gitwork`  اللي جواه file.txt واخر حاجه الcommit, اللي اتcreate لما عملت `git commit`.

عشان اشوف الhistory بتاعي, فهستخدم `git log`
![Pasted%20image%2020250405181152.png](images/Pasted%20image%2020250405181152.png)
ده بيوريك سلسلة الـ commits كلها، مع الـ SHA-1 hash بتاع كل commit، الـ author، الـ timestamp، والـ commit message.
لو ركزت هتلاقي ان `SHA1` بتاع الcommit هو اخر  `SHA1` فال stdout بتاع find command.

عشان اوصل لأي object لازم اشوف الاساس "رأس الافعى". الcommit هو بدايه كل شيء وهو اللي بيوصلني لباقي الproject. 

>**note** 
مش كل مره هحتاج أrefer لأي object  هاقعد اعمل copy paste ل خرطوشه الcharacters دي, اقدر اكتبله اول كام character  وهو هيفهم, غالبا اقل عدد من الcharacters اقدر استخدمه اختزالاً ل ال`SHA1` هو 4characters. ممكن بالصدفه يتشابه 2objects فال`SHA1` ف ممكن نخليها 5 ونجرب يعني.  حتى git بيختصرها ب 7. ![Pasted%20image%2020250405182214.png](images/Pasted%20image%2020250405182214.png)

عرفت انه commit خلاص نشوف الcontent بتاعه بقى ممكن نستخدم `cat-file -p` ![Pasted%20image%2020250405182511.png](images/Pasted%20image%2020250405182511.png)

هتلاقيه يعتبر نقس اللي ظهر فالstdout بتاع ال`git log`. و بيعرض الtimestamp بعدد الثواني اللي عدت.

من ضمن الcontent بتاع الcommit object ,هو الtree وجمبه ال`SHA1` بتاعه
and that `represents the top-level directory of the project at the time of the commit.` 

فانا عايز أtrack الbatch واعرف ايه الfiles والfolders اللي اتغيروا. ف التسلسل كده اني ببدأ بالcommit بعدين اروح للroot tree ده واشوف ايه اللي موجود فيه
![Pasted%20image%2020250405185802.png](images/Pasted%20image%2020250405185802.png)
ف بيعرضلي الfiles اللي عندو, اللي اتغيرت بس, هنا انا لسه معملتش حاجه خالص ف هيعرضلي الcontent بتاعه اللي هو الfile ده. 

![Pasted%20image%2020250405190623.png](images/Pasted%20image%2020250405190623.png)
 وده التسلسل الطبيعي حيث اني هبدأ منcommit object بعد كده الroot tree ثم ال trees وال blobs اللي جوه الtrees. واشوف الcontent نفسه اللي موجود فالsnapshots.
 اقل commit هعملها هتعمل على 3 objects. 
 مثلا لو عدلت في file, هيتعمل blob للfile ده و tree للfolder اللي شايل الfile وcommit object للbatch كله فيكون الباب لcommit دي.
 
 >**note** 
 الcommit object هو ده اللي بعد كده هنبدأ نشير ليه,  وكل Commit هعملها هنتكلم عن الcommit object بتاعها, ف هو ده الرأس والكبير بتاعهم مش هنقعد نقول trees و blobs <mark>**واللي مالوش كبير يشتريله كبير**</mark>.
 
____________________________________________________________

# Basic Git operations(add, commit, log, diff, and show)

هجرب بقى اعدل فالfile واكتب line جديد. بعد ما تعمل save(<mark>ctrl + s</mark>) لو بتستخدم IDE زي **VS** هتلاقي اسم الfile اتغير وبقى مكتوب `M` اللي هو`modified` بس بالاحمر.
نشوف `git status` رأيه ايه بعد التغيير
![Pasted%20image%2020250407155249.png](images/Pasted%20image%2020250407155249.png)

قال لي الfile modified وبيديني اقتراحات بما انه اتعدل فبيقولي اعمله staging وبعدين Commit. وبيقولك برضو لو انت غلط و عملت staging وعايز تعمل unstaging  اعمل `git restore`.
وممكن استخدم `s option-` مع `git status` عشان يلخص الكلام ده, مثلا عندي 50 file هيبقى موال بقى.
![Pasted%20image%2020250407155809.png](images/Pasted%20image%2020250407155809.png)

حتة انه modified بالاحمر دي يعني الfile اللي عندي فالWorking tree على الOS لا بيساوي اللي فالindex ولا بيساوي اللي موجود فالgit repo.
الline أللي زودته ده مش موجود فالstaging area ولا موجود فالgit repo.

الnext step الطبيعيه هي اني هعمله `git add` فيبقى modified بالاخضر ![Pasted%20image%2020250407160337.png](images/Pasted%20image%2020250407160337.png)

وده معناه الfile اللي فالworking tree على الOS هو نفسه اللي فالStaging area `index` لكن مش نفس اللي فالgit repo. 

نعمل `git commit` بقى عشان نعمل الgit object ونعمل version جديد منه فالRepo. هنستخدم معاها `m-` برضو ونغير بقى فالmessage وهتكون على حسب التغيير اللي انت عملته او حاجه انت عايز توضحها.
![Pasted%20image%2020250407160848.png](images/Pasted%20image%2020250407160848.png)

لو عملت `git log` عشان اشوف الدنيا ماشيه ازاي والcommits بتاعتي هلاقي عندي 2commit object وهتلاقي ان list الcommits فالlog مترتبه descending من الاخر للأول, اول واحد اتعمل يبقى اخر واحد خالص واحدث واحد يبقى اول واحد.
![Pasted%20image%2020250407161145.png](images/Pasted%20image%2020250407161145.png)


نبص على الobjects اللي موجوده عندي كلها بعد ماعملت commit كمان 
![Pasted%20image%2020250407161319.png](images/Pasted%20image%2020250407161319.png)

كله سايح ف بعضه, تخيل بقى عندك 5او6 commits, ف كان لازم يبقى فيه حاجه توريني انهي objects من دول Related مع بعض واتعملوا Commit واحده. 

نشوف المحتوى بتاع الcommit دي ونشوف الblobs وكل اللي موجود 
![Pasted%20image%2020250407161808.png](images/Pasted%20image%2020250407161808.png)

ايه ال
parent ده. ده جديد مكنش موجود فال commit اللي قبل  دي
![Pasted%20image%2020250407162128.png](images/Pasted%20image%2020250407162128.png)
وده جزء من ال**architecture**, نبص عليه 
لو عندي فالgit repo موجود commits كتير جداً وكل commit شايل الobjcts بتاعتها واللي اتعدلت فالbatch.
طب ازاي هقدر أtrack الhistory ازاي هعرف ايه هي اول commit و مين اللي بعدها ومين احدث واحده, فأكيد مش كل مره هاروح ادور فالtime stamp واقعد ادور او git ي scan كل الcommits و يعيد ترتيبهم على حسب الtime واشوف مين الcommit اللي قبلها واللي بعدها فالtime. ده شغل هواة يا حسين.

انا ميهمنيش بس اعرف مين قبل مين فالزمن, يهمني اعرف مين الversion اللي قبلها. 
>[!important]
>ف git بيرتب الcommit objects دي في `linked-List`, كل Commit بيشاور على الparent commit ,بيشاور على اللي قبله. 
وهو مش مسأله ان الcommit جه قبل الparent فالزمن لا,  هو قبله فالstate, هو التغير عن الparent commit وهي التعديل اللي حصل على الparent, مش منفصل عن ابوه خالص, بيكلمو بعض عادي, بس هو في شويه تعديلات حصلت على الparent ف نشأ الcommit فالcommit دي معتمده و مبنيه عالparent.

![Pasted%20image%2020250407165316.png](images/Pasted%20image%2020250407165316.png)
الاسهم بتشاور لورا عشان تشاور على الparent وده عكس التسلسل الزمني. هي تسلسل فالاحداث والتغييرات.
ف من جوه الcommit اقدر اعرف مين الparent بتاعه, مين هي الcommit اللي حصل عليها التغير و اتحولت الى الcommit الحاليه. ودي الطريقه اللي بtrack بيها الhistory.
اول commit خالص ملهاش parent واسمها ال`root commit`
.![Pasted%20image%2020250407170003.png](images/Pasted%20image%2020250407170003.png)
الشكل ال linear ده, that's what is called `branch`.
اذاً الbrach هو تسلسل linear ل commits.او مجموعه من الcommits كل واحد بيشاور على الparent بتاعه.

الbranch ده by default اسمه `master`, ممكن اغيره عادي.
________________________________________________________________________________
![Pasted%20image%2020250407215311.png](images/Pasted%20image%2020250407215311.png)
الcommits دي هي الversions بتاعة الbatches اللي عندي فالgit repo, ف أنا لما افتح الworking tree  الphysical files اللي قدامي دي بتreflect ده انهي version من دول, الطبيعي انه يبقى اخر واحد فالسلسله ,حيث ان اخر مره عملت git commit اتاخد version من الحاجات اللي عملتلها modification فأصبح ان اللي موجود عندي فالworking tree هو اللي فالrepo. 
طبعاً في وقت من الاوقات احتاج اعمل Roll back او اقارن حتى مثلا, 

المهم, git فيه طريقه يقولك الfiles اللي قدامك فالworking tree على الOS دي بتreflect انهي commit object, انهي version. ويtrack المقارنه بين الworking tree والcommit
ف git عنده pointer اسمه <mark>**HEAD**</mark>. 
![Pasted%20image%2020250407220631.png](images/Pasted%20image%2020250407220631.png)
لما الHEAD يشاور على commit معينه معناه ان اللي عندك فالworking tree هو الversion ده, هي الcommit دي.
![Pasted%20image%2020250407220803.png](images/Pasted%20image%2020250407220803.png)
 لو حصل ان الHEAD ده شاور على commit تانيه, ال Content بتاع الWorking tree والstate بتاع الfiles كله هيتغير وهيبقى نفس اللي موجود الcommit اللي بيشاور عليها الHEAD.
 ________________________________________________________________________________
**How can i see the modification?**
لو زودت line فالfile, وعملت `git status -s` هيقولي الfile ده `M` بالاحمر.
عشان اشوف الmodifications والفروق بين النسخه اللي عندي فالworking tree واللي فالindex او اللي فالrepo.
في command اسمه `git diff` بيوريني الفروق بين الthree-trees الworking والrepo والstaging لكل الfiles اللي فالproject بتاعي. 
بيديني list بكل الفروق في كل الFiles و الfolders أللي فالproject. 
![Pasted%20image%2020250407224024.png](images/Pasted%20image%2020250407224024.png)
هنا مثلا بيقولي في line اتضاق ملونه بالاخضر وعامل جمبه `+`. و بيعمل `-` للأسطر اللي اتمسحت.
 
هعمل الstep اللي بعد كده `git add` كده اللي عندي فالWorking tree هو هو اللي فالindex.
اجرب `git diff` تاني,
![Pasted%20image%2020250408012350.png](images/Pasted%20image%2020250408012350.png)

مطلعش حاجه!!
وده لأن `git diff` بتوريني الفرق بين الstaging area والworking tree, ف انا عملتله staging ب `git add`
فأصبح انهم بقوا نفس الversion.
طب لو عايز اشوف الفرق بين اللي فالRepo واللي فالindex. هستعمل برضو `git diff`,   بس اي operation بين الrepo والstaging area `index` لازم مع `git diff` نستخدم الoption `--staged`.
و  `staged--` معناها git command بين الrepo والindex. مالوش علاقه بالworking tree.
![Pasted%20image%2020250408013112.png](images/Pasted%20image%2020250408013112.png)

وهو كان اصلا نفس الفرق بين الindex والworking tree قبل ما اعمل `git add`.

الStep بعد كده اعمل commit.
بمناسبه `git commit` افرض مش عاجبني الحته اللي بكتب فيها الcommit message, ف من ضمن الConfiguration أللي ممكن اعملها في git اني أconfigure editor بحيث لما اعمل `git commit` مكتبش الmessage فالline يفتحلي editor اكتب فيه.
![Pasted%20image%2020250408014257.png](images/Pasted%20image%2020250408014257.png)

هكتب بس git commit هيفتحلي على طول الeditor.
![Pasted%20image%2020250408014344.png](images/Pasted%20image%2020250408014344.png)

بعد الsubject لو عايز ازد ممكن انزل line اضيف description بس حاول مايزيدش عن 70 characters.
![Pasted%20image%2020250408014623.png](images/Pasted%20image%2020250408014623.png) 

و أsave عادي زي اي editor.
وهاشوف الsubject والdescription عادي لما اعمل `git log`
![Pasted%20image%2020250408014807.png](images/Pasted%20image%2020250408014807.png)

ترويشه على `git log`
1- <mark>**--oneline**</mark>
![Pasted%20image%2020250408014910.png](images/Pasted%20image%2020250408014910.png)
مختصر في كله حتى ال`SHA1`.
نفهم من هنا ان الmaster ده هو الbranch اللي احنا شغالين عليه  والhead بيقول ان النسخه او الversion اللي فالworking tree دلوقتي ده, هو النسخه او الversion  صاحب ال`SHA1` ده على الmaster branch ده.    
لو نقلت الhead ده لاب بأي طريقه لأي version تاني هيبقى هو اللي على الworking tree.
اذاً الhead بيشاور على الversion او الcommit اللي بيreflect اللي موجود فالworking tree دلوقتي.
لو عندي commits كتير اوي اقدر أعمل filtering للكلام ده, وهعمل ده ب`git log`.

مثلاُ عايز اقوله اعملي filtering لل commits اللي فيها الblobs بتاعة  `file.txt`![Pasted%20image%2020250411210401.png](images/Pasted%20image%2020250411210401.png)

بحيث لما يكون عندي عدد commits كتير جدا اقدر أfilter اللي انا عايزه بس, مثلا انا شغال في الحاجات اللي ليها علاقه بالdatabase او json files بس. ماليش دعوه بالباقي مثلا 

2- <mark>**-n**</mark>
بحيث اقوله عايز اخر كام `n` دول بس.
![Pasted%20image%2020250411210734.png](images/Pasted%20image%2020250411210734.png) 
ولو عايز الcommits بتاعة حد معين 
 و اقدر اقوله عايز الcommits اللي على branch معين.
   
>**Variations**:
> Add options like `-p` for diffs `--oneline` for summaries, or `--all` to include all branches if needed.
![Pasted%20image%2020250411211707.png](images/Pasted%20image%2020250411211707.png)
![Pasted%20image%2020250411212237.png](images/Pasted%20image%2020250411212237.png)

لو عايز اشوف كل الbranches اللي عندي ممكن استخدم الcommand `git branch` ممكن استخدم معاها option `-a` عشان يعرض كله حتى الremote.
![Pasted%20image%2020250411212345.png](images/Pasted%20image%2020250411212345.png)

________________________________________________________________________________
ممكن اعمل graph لما استخدم `graph--`
![Pasted%20image%2020250411212718.png](images/Pasted%20image%2020250411212718.png)

________________________________________________________________________________
احنا شوفنا الفروق او الmodifications ب`git diff`, ازاي اقدر اقوله يوريني وريني الحاجه اللي جوه وشكل الcommit بدل ما انا بدني الف على commit ثم الroot الroot tree لحد ما اوصل للblobs والTrees.
مفيش طريقه اشيك تعمل لي هي الtraverse ده. 
اه فيه هو اني استخدم `git show` بتاخد الobject عن طريق ال `SHA1` وتعرض اللي جواه.
![Pasted%20image%2020250412002627.png](images/Pasted%20image%2020250412002627.png)
بيبدأ من الcommit لحد الblob و يوريني التعديلات اللي حصلت عليه, هنا بيقولي في file اتضاف.

لو عايز اعرف الفروقات مابين 2commits, فكك بقى من اللي فالworking tree. لو قولته `git diff`  بس هيجيب الفرق بين الworking tree والindex ولو عملت  `staged--` هيقارن بين الRepo والindex مش هيبقى في فروقات فالحالتين لأن الfile حالته modified.
طب لو عايز اقارن بين 2commits مثلا الworking tree و commit قديمه.  هعمل ده بنفس ال`git diff` 
`git diff SHA1..SHA1`
![Pasted%20image%2020250412003653.png](images/Pasted%20image%2020250412003653.png)
هنا بيقولك ان الفرق بينهم ان في 2files اتضافوا.
![Pasted%20image%2020250412003823.png](images/Pasted%20image%2020250412003823.png)
وهنا Line واحد اتضاف.
## removing file 
مسح file في حد ذاته يعتبر تغيير او modification في الtree, محتاج اعمله staging واعمله commit.
مش معنى اني مسحته خلاص لا, ان اهم مزايا git أن مفيش بتتمسح لو مسحت حاجه مش هيتشال وخلاص ده هيتكتب انك مسحت الline ده.
 لو جيت مسحت File سواء بgit command او من الoperating system لازم اعمله staging و commit.
  ![Pasted%20image%2020250412005538.png](images/Pasted%20image%2020250412005538.png)
  
## moving or rename files 
احياناُ git بيهيس لما اعمل Rename او move من الOS, فالاحسن ان انا اعمل كده ب`git mv`
![Pasted%20image%2020250412014334.png](images/Pasted%20image%2020250412014334.png)

## viewing the commit history 
![Pasted%20image%2020250412014440.png](images/Pasted%20image%2020250412014440.png)

  [^2]: commit contains a pointer to a single **tree object**, referred to as the root tree. This tree represents the top-level directory of the project at the time of the commit. The root tree recursively references other tree objects (for subdirectories) and **blob objects** (for file contents), thereby providing a `complete hierarchical representation of the project's state`.

# Undoing things

لو عايز أ delete الrepo بسهوله خالص,هعمل delete الfolder بتاع الrepo.
![Pasted%20image%2020250412021856.png](images/Pasted%20image%2020250412021856.png) 
كده خلاص مبقاش في repo, نبتدي على نضافه بقى.
نعمل `git init` و `git add` لو جيت بعد كده عملت `git status` هلاقيه بيقولي لو عايز تعمل unstage عشان ت untrack اعمل `<git rm --cached <file`
وهي بتشيل الملف من الـ Staging Area والـ Repository (يعني تخلّيه untracked) بس تبقّيه موجود في الـ Working Directory.
![Pasted%20image%2020250412022344.png](images/Pasted%20image%2020250412022344.png)

لو جيت عملت تعديلات على File, ف لو عملت `git status`  هلاقيه بيقولي ان الfile ده modified بالاحمر. طب لو عايز أdiscard الchanges دي 
هلاقيه بيقولي في `git status` لو الmodifications والتغيرات مش عجباك اعمل `git restore` واسم الfile. الcommand  `git restore` كل اللي بيعمله هو انه بيrestore الfile من الstaged, بيشوف اخر State فالindex كانت ايه ويرجعها. 
ف بكده الmodifications اللي عملتها هتdiscard. ف يبقى الFile modified.

لو رجعت عملت تعديلات تاني بس المره دي عملت `git add` فأصبح ان اللي فالindex هو هو اللي فالworking tree بس مش هو اللي فالrepo, ف `git restore` هنا متنفعش لأني هاrestore منين ما الindex هو هو الworking tree. طب ايه الحل؟

لو جربت اعمل `git status`
![Pasted%20image%2020250412075829.png](images/Pasted%20image%2020250412075829.png)

مديني برضو option ازاي اعمل `unstage`, انا عملتله staging ب `git add` ف عشان اعمله unstage بيقول استخدم `stage--` مع `git restore`
لو عملت `git restore --staged file.txt` هيحصل ان الfile هيتحول من staged الى unstaged بس التعديلات زي ماهي وعشان أ discard اعمل `git restore` بس.
________________________________________________________________________________
![Pasted%20image%2020250412081125.png](images/Pasted%20image%2020250412081125.png)

عشان اعمل `git add` و `git commit` في نفس الوقت.
الoption `-a` بيضيف التعديلات على الملفات اللي **tracked** بس، يعني:
الملفات اللي عدّلتها أو مسحتها وكانت موجودة في الـ Repository. لكن الملفات الجديدة (new files) اللي لسه **untracked** (ما عملتهاش git add قبل كده) مش هتتضاف تلقائيً
________________________________________________________________________________
من ضمن الحاجات اللي اقدر اعملها ان انا اعدل الcommit message, في اخر Commit message. 
عشان اعدل فيها في option اسمه `amend--` مع `git commit`, بيديني فرصه اني اعدل في اخر رساله Commit, بيفتحلي editor واعدل زي ما انا عايز بقى.
واقدر اشوف التعديل ده لما اعمل `git log`.
________________________________________________________________________________
في الغالب اللي بحتاجه هو اني أتنقل بين الVersions, مثلا عايز ارجع لversion قديم سواء Roll back او roll forward, اعمل  ده ازاي؟
نبدأ بالHEAD 
![Pasted%20image%2020250412084451.png](images/Pasted%20image%2020250412084451.png)

ده الوضع دلوقتي 
الHEAD بيشاور على الcommit object اللي انا شايفه قدامي فالworking treeو بيشاور على انهي branch, مش موجود عندي غير واحد دلوقتي وهو الmaster.

لو عايز ارجع لversion قديم مثلا, بحيث يكون الworking tree تكون بنفس الstate بتاعه الversion القديم ده.
عشان اعمل ده مش محتاج بقى اعمل backups وكل ده. انا عندي snapshots هي already موجوده في Git.
نستغل ده بإننا نحرك الHEAD ده. 
مثلا لو نقلت الHEAD على C3 هلاقي الfile عندي فالworking tree اصبح في نفس الstate بتاعة الfile بعد ماعملت الCommit التالته. 
اذا هي الطريقه ببساطه ان انا احرك الHEAD ده.

الarchitecture دلوقتي
![Pasted%20image%2020250412085833.png](images/Pasted%20image%2020250412085833.png)
لما اجي احرك الhead من الcommit الحاليه مثلا ل الcommit C3, في عندي اختيار من اتنين 
1-ممكن بعد ما انقل الHEAD اخليه يسمَّع فالworking tree.
2-وممكن اخليه يسمَّع فالstaging بس.
لأن حته انه يسمَّع على الworking tree ده قرار خطير, ممكن الworking tree ده يكون live project.
ف من الاحسن لما احاول ارجع لcommit قديم, اني ارجعه في الstaging الاول, حتى ياعم اشوف الdifferences لأني هكون اقدر اقوله `git diff`. واقرر اقول اه او لا.
وبعدين من الstaging ارجعه ل الworking tree, اعمله `unstage`. وبعدين أdiscard الmodifications.

او او متأكد يبقى مره واحده وخلاص اجيبه من الrepo على طول على الworking tree.
![Pasted%20image%2020250412090951.png](images/Pasted%20image%2020250412090951.png)

فالحالتين هستعمل Command اسمه `git reset HEAD`, معناه اني بحرك الHEAD. لوحدها كده بتوديه على الstaging area.
لو عايزه ي reflect على طول على الworking tree هديله option `--hard` بيعدل physically فالworking tree.
اذا `git reset` هي دي الطريقه اللي بنقدر نعملها بيها undoing بعد ما نعمل `git commit` وعملت commit و version جديد.
________________________________________________________________________________
![Pasted%20image%2020250412092628.png](images/Pasted%20image%2020250412092628.png)

الHEAd ده عباره عن file جواه Pointer بيشاور على `SHA1`. لو روحت ل `git.` وعملت ls هلاقي في file اسمه `HEAD`
.![Pasted%20image%2020250412092822.png](images/Pasted%20image%2020250412092822.png)

هلاقي جواه زي لينك كده 
![Pasted%20image%2020250412092938.png](images/Pasted%20image%2020250412092938.png)

وكل ما اعمل Commit الFile ده هيتعمله update ب اخر  commit احنا واقفين عليه اللي هو نفس اللي موجود في الworking tree.

لو عايز بقى انقل الHEAD وارجع revision 
لو عايز ارجع commit واحده ل ورا, هستعمل الanotation ده `1~` يعني خطوه ل ورا. لو عايز ارجع 2revisions هاقوله `2~` وهكذا.

ممكن مثلا لو عايز اقارن بين الHEAD واي commit تانيه بس انا مش عارف الSHA1 بتاع الHEAD.
![Pasted%20image%2020250412094728.png](images/Pasted%20image%2020250412094728.png)

المفروض لو رجعت للcommit دي ال2lines الفرق دول هيتشالوا.
![Pasted%20image%2020250412095739.png](images/Pasted%20image%2020250412095739.png)

رجعت commit ل ورا, بس الlog بقى فيها 3commits بس, هل ده معناه ان الرابعه اتمسحت؟ لا الobject موجود.
طب انا ندمان وحزنان في حاجه تخليني أ roll forward, هي basically مسمهاش roll forward في git اسمها `fast forward`. ف اقدر اعمل fast forward عادي.

لكن قبل ده نشوف `git reflog`, كونك اتحركت بالHEAD دي operation انت عملتها المفرةض تبقى logged لكن مش object ف عشان كده مش هاتعرف تشوفها ب`git log`, بس تقدر تشوفها ب`git reflog`
و reflog هي short for `refrences log`, فهي بتوريني الlog بتاع الrefrences, الRefrences هنا زي ال`SHA1` كده.
![Pasted%20image%2020250412102139.png](images/Pasted%20image%2020250412102139.png)

كل حاجه معروفه و مرصوده 

طب اعمل fast forward ازاي؟ برضو بنفس الCommand `git reset head` هو اللي هيفسحنا يروح يمين وشمال او ي replay نفس الcommit عادي جداً. طب `~` بترجعني ورا,  فهنستعمل الannotation ده `{n}@`.

الobject 3c183d4 اختفى من git log, ممكن اتأكد انه موجود عن طريق `git show`
![Pasted%20image%2020250412133745.png](images/Pasted%20image%2020250412133745.png)

لو عايز ارجع تاني مش هسنخدم `1~` بقى هشوف الrefrence بتاع اللي عايزه فين مثلا هنا الForth line added, هلاقي جمبه `{1}@` فهستخدم دي.
![Pasted%20image%2020250412134006.png](images/Pasted%20image%2020250412134006.png)


واقدر اشوف النتيجه من `git log` وايه اللي حصل من `git reflog`
![Pasted%20image%2020250412134247.png](images/Pasted%20image%2020250412134247.png)
![Pasted%20image%2020250413101226.png](images/Pasted%20image%2020250413101226.png)
________________________________________________________________________________
![Pasted%20image%2020250413102320.png](images/Pasted%20image%2020250413102320.png)

`git revert`
Given one or more existing commits, revert the changes that the related patches introduce, and record some new commits that record them. This requires your working tree to be clean (no modifications from the HEAD commit).

Note: `git revert` is used to <mark>_record_</mark> some new commits to reverse the effect of some earlier commits (often only a faulty one).it help undo commits that have already been pushed and shared with the team, we cannot use the git reset command. Instead, we have to use `git revert`. git revert will create a new commit that will undo all of the work that was done in the commit you want to revert.

If you want to throw away all uncommitted changes in your working directory, you should see `git-reset`, particularly the `--hard` option. If you want to extract specific files as they were in another commit, you should see `git-restore`, specifically the `--source` option. Take care with these alternatives as both will discard uncommitted changes in your working directory.
__________________________________________________________________
**OPTIONS**
- ​`<commit>`
     Commits to revert.

- `-e` , `--edit`
    With this option, _git revert_ will let you edit the commit message prior to committing the revert. This is the default if you run the command from a terminal.

`-n` , `--no-commit`
Usually the command automatically creates some commits with commit log messages stating which commits were reverted. This flag applies the changes necessary to revert the named commits to your working tree and the index, but does not make the commits. In addition, when this option is used, your index does not have to match the HEAD commit. The revert is done against the beginning state of your index.
__________________________________________________________________
 **EXAMPLES**
`git revert HEAD~3`
Revert the changes specified by the fourth last commit in HEAD and create a new commit with the reverted changes.

`git revert -n master~5..master~2`
Revert the changes done by commits from the fifth last commit in master (included) to the third last commit in master (included), but do not create any commit with the reverted changes. The revert only modifies the working tree and the index.
__________________________________________________________________
**SEQUENCER SUBCOMMANDS** 
`--continue`
Continue the operation in progress using the information in `.git/sequencer`. Can be used to continue after resolving conflicts in a failed cherry-pick or revert.

`--skip`
Skip the current commit and continue with the rest of the sequence.

`--quit`
Forget about the current operation in progress. Can be used to clear the sequencer state after a failed cherry-pick or revert.

`--abort`
Cancel the operation and return to the pre-sequence state.
***__________________________________________________________________________***

`git checkout` 
it can "update files in the working tree to match the version in the index or the specified tree." Since `HEAD` refers to the last commit, using `git checkout HEAD <filename> `correctly restores the file from that commit to the working directory.
and This restores a file that was deleted in the working directory but not yet committed, bringing it back to the state it was in at the last commit (HEAD).

`git checkout` has many uses, but the main one is to switch between branches.  
For example, to switch from master branch to dev branch, I would type `git checkout dev`. After that, if I do a git commit, notice where it goes. Try it.
In addition to checking out branches, you can also checkout individual commits. Try it.  Make a new commit and then type` git checkout bb92e0e` and see what happens.

Type git commit, git branch, and git checkout commands to your hearts desire until you understand this concept.
# Tags
اخر object من الgit objects هو ال`Tags annotation`.
احنا عمالين نقول versionsنتحرك بين ال versions وبتاع, احنا بنستخدمها بس لمجرد التسهيل انما فالحقيقه ممكن نقعد نعمل تعديلات و commit كتير  جدا بس مش دي الversions دي مجرد تعديلات بس.  لحد ما اوصل لcommit معين بالنسبالي ده version جديد بجد, مش كل ما اعدل line في file يبقى ده version هو مجرد تعديل.
بوصل لحته ان في كام commit عايز اعلمهم احطلهم bookmark بقول ان الcommit دي مهم جداً.
ف من ضمن الحاجات اللي اقدر اعملها اني اعمل tagging ل الcommits, اعلم على Commit اقوله ده version 2 و ده Version 2.5.
>[!note]
>we have 2types of tags.
**Lightweight**:
very much like a branch that doesn't change it's just a pointer to a specific commit.
**Annotated**:
stored as full objects in the git objects.

لو عايز أعمل tagging ل commit معين هستخدم `git tag`
![Pasted%20image%2020250413122746.png](images/Pasted%20image%2020250413122746.png)


السهوله وحلاوه الموضوع لو قولتله 
![Pasted%20image%2020250413122822.png](images/Pasted%20image%2020250413122822.png)

مش هاروح بقى اشوف الcommits وال`SHA1` والmessages عشان اعرف انهي واحده هي, بيخليني انط على طول فالversions. 
لو تلاحظ الtag ده ليه tagger و Date والmessage لذلك<mark>_هو object_</mark>.
>[!important]
If you have some previous commits and you forgot to tag, you can later on tag a previous commit by referring to its checksum `SHA1`.![Pasted%20image%2020250413123437.png](images/Pasted%20image%2020250413123437.png)
By default `git push` doesn't push tags. You mush specify
![Pasted%20image%2020250413123537.png](images/Pasted%20image%2020250413123537.png)
**Lightweight Tags**
Just a commit checksum added to a file, no more info stored.
![Pasted%20image%2020250413123302.png](images/Pasted%20image%2020250413123302.png)

_______

# Git Aliases
note: <mark>this topic from _ProGit_ book copy-paste.</mark>

Before we move on to the next chapter, we want to introduce a feature that can make your Git experience simpler, easier, and more familiar: aliases. For clarity’s sake, we won’t be using them anywhere else in this book, but if you go on to use Git with any regularity, aliases are something

you should know about.
Git doesn’t automatically infer your command if you type it in partially. If you don’t want to type
the entire text of each of the Git commands, you can easily set up an alias for each command using
`git config`. Here are a couple of examples you may want to set up:
![Pasted%20image%2020250413104545.png](images/Pasted%20image%2020250413104545.png)
This means that, for example, instead of typing `git commit`, you just need to type `git ci`. As you go
on using Git, you’ll probably use other commands frequently as well; don’t hesitate to create new
aliases.

This technique can also be very useful in creating commands that you think should exist. For
example, to correct the usability problem you encountered with `unstaging` a file, you can add your
own `unstage` alias to Git:
![Pasted%20image%2020250413104647.png](images/Pasted%20image%2020250413104647.png)

_________________________________________________________________________________
This makes the following two commands equivalent:
![Pasted%20image%2020250413104713.png](images/Pasted%20image%2020250413104713.png)


________________________________________________________________________________
This seems a bit clearer. It’s also common to add a last command, like this:![Pasted%20image%2020250413104823.png](images/Pasted%20image%2020250413104823.png)

This way, you can see the last commit easily:![Pasted%20image%2020250413104856.png](images/Pasted%20image%2020250413104856.png)

_________________________________________________________________________________
As you can tell, Git simply replaces the new command with whatever you alias it for. 
However, maybe you want to run an external command, rather than a Git subcommand. In that case, you start the command with a `!` character. This is useful if you write your own tools that work with a
Git repository. We can demonstrate by aliasing `git visual` to run `gitk`:
![Pasted%20image%2020250413105029.png](images/Pasted%20image%2020250413105029.png)

**Summary**
At this point, you can do all the basic local Git operations — creating or cloning a repository, making
changes, staging and committing those changes, and viewing the history of all the changes the
repository has been through. Next, we’ll cover Git’s killer feature: its branching model.
# Git Branching 
الBranches هي من ضمن الحاجات المهمه في git ودايما هنستعملها, Git بيسهل التعامل معاها خالص.

>هعمل الalias كده 
>`git config --global alias.graph 'log --oneline --decorate --graph --all'`,and run it with <mark>git graph</mark>.
 or `alias Graph='git log --oneline --decorate --graph --all'`, and run it with <mark>Graph</mark>.

![Pasted%20image%2020250414010317.png](images/Pasted%20image%2020250414010317.png)

زي ما احنا عرفين ان Git بيstore الdata, الcommits بتاعته يعني عن طريق انه بيجمع كل الblobs والtrees تحت الroot tree بتعاهم ويwrap ألكلام ده في Commit بحيث الcommit يبقى فيه الparent commit والroot tree والcommiter وإلى اخره.  
![Pasted%20image%2020250413161803.png](images/Pasted%20image%2020250413161803.png)
***___________________________________________________________________________________________***
![Pasted%20image%2020250413162043.png](images/Pasted%20image%2020250413162043.png) [^3]

ده الوضع الحالي ل الCommits عندي.
الbranch هو مجموعه من الCommit objects وبيكونو connected لبعض عن طريق اول parent خالص.
<mark>_so branch is a linear layout of commits._</mark>
![Pasted%20image%2020250413162853.png](images/Pasted%20image%2020250413162853.png)

في اوقات كتير بيحصل اني ببقى عايز اني  اتفرع منه `forking` و اعمل revision تاني و أTest حاجه ازود feature أجرب أو احل issue و فنفس الوقت مش عايز اغير اي حاجه في اخر Commit او revision فالmaster.
عشان اعمل ده هحتاج اني اعمل Branch جديد هسميه مثلا testing, بعد كده اقدر احول على الtesting اعدل فيه واي تعديل هعمله هيكون مبني على الparent بتاعه اللي خدت منه الbranch.
![Pasted%20image%2020250413171903.png](images/Pasted%20image%2020250413171903.png)
واي تعديل هعمله ل الcommit هيتعمله revision فالrepo عادي بس هيبقى متعلم انه تبع الbranch اللي اسمه testing بقى.
خلصت ورجعت لل master عادي اقدر اكمل اعمل commits عادي جدا. 
![Pasted%20image%2020250413172244.png](images/Pasted%20image%2020250413172244.png)

ده بيخلي الdevelopment بتاعي `non-linear`, كل branch لوحده هو linear بس لما اعمل اكتر من branch وكذا تفريعه واعدل فيهم فأصبح **non-linear development**.
>[!important]
>to create new branch we can use `git branch <branch-name>`, and to list my branches we can use `git branch`.![Pasted%20image%2020250414010620.png](images/Pasted%20image%2020250414010620.png)

هنا **<mark>master</mark>** ده بالاخضر يعني هو ده ال`current branch` , يعني لو جيت عدلت حاجه فالfile وعملت الcommit. الcommit دي هتبقى امتداد للmaster branch ده. و<mark>_النجمه اللي هي الHEAD_</mark>.
يعني اللي قدامي على الworking tree على الOS هو اللي فالmaster branch.

ف كده دلوقتي الmaster والtesting branch فيهم نفس الcontent, واتأكد من ده لما اعمل `git log` او graph زي فوق. وانا لسه معملتش حاجه مجرد ان انا خدت branch من الmaster.![Pasted%20image%2020250414010900.png](images/Pasted%20image%2020250414010900.png)

الHEAD بيشاور على الMaster. والMaster وال testing واقفين على الCommit صاحب ال`SHA1` ده.
![Pasted%20image%2020250414011915.png](images/Pasted%20image%2020250414011915.png)

لو عايز اعمل switch ل الtesting branch هستخدم `git switch testing`, قبل كده كان اسمه `checkout` هو مازال موجود برضو.  ![Pasted%20image%2020250414012118.png](images/Pasted%20image%2020250414012118.png)

و غير الbranch لما شوفنا الstatus و قالك احنا على الtesting branch , كده عملنا switch ل الtesting, فأصبح الtesting هو الcurrent والHEAD بيشاور عليه. ![Pasted%20image%2020250414012355.png](images/Pasted%20image%2020250414012355.png)

والMaster وال testing واقفين على الrevision صاحب ال`SHA1` ده.بس الHEAD بيشاور على الtesting ف اذا الtesting هو الcurrent.

ف دلوقتي لو عملت اي تعديل فالfile وعملت commit ده هيعمل revision جديد.
الrevision دي هتبقى في ال`testing branch`
![Pasted%20image%2020250414013007.png](images/Pasted%20image%2020250414013007.png)
الmaster دي اللي كنا واقفين عليها لما عملنا الtesting branch.
بعد كده عملنا switch ل الtesting branch. ,وعملت تعديل ثم عملت commit فحصل `Divergent`.
ألmaster وقف زي ماهو على اخر revision كان موجود عليها و أتحركت انا خطوه بتعديل جديد عملتله commit وعملت  revision جديد ولكن فالtesting branch.

![Pasted%20image%2020250414015042.png](images/Pasted%20image%2020250414015042.png)
دلوقتي عندي 2branches واقدر أswitch مابينهم. لو جيت عملت switch ل الmaster ايه اللي هيحصل؟
لما أswitch لل master branch هي هي اكني عملت Reset ل الHEAD.
يعني لما اعمل Switch ,تلقائي الHEAD هيشاور على الcommit بتاعة الmaster.![Pasted%20image%2020250426125835.png](images/Pasted%20image%2020250426125835.png)

و ده هيخلي اللي فالworking tree يبقى هو هو أللي فالcommit بتاعة الmaster. 
فأصبح ان الHEAD بيشاور على commit قبل اللي كانت موجوده 
![Pasted%20image%2020250426130414.png](images/Pasted%20image%2020250426130414.png)


لما اعمل Switch يعتبر `اكني` عملت reset لأن يعتبر كلهم على خط واحد ف اقدر ارجع Linearly.
![Pasted%20image%2020250426130705.png](images/Pasted%20image%2020250426130705.png)
>[!IMPORTANT]
>switching to a different branch not only moves the HEAD pointer to that branch but also reverts the contents of the working tree to that point in time. Moving the HEAD is like rewinding

 >the **master branch** is the default primary branch in a repository. It serves as the main line of development, typically containing the most stable and production-ready version of a project’s codebase. The master branch is created automatically when a repository is initialized and is often used as the reference point for integrating changes from other branches

# Merging Branches
التعدبلات اللي عملتها فالtesting دي لو انا راضي عنها ممكن اعملها `merging`.
to merge branches we can use `git merge`.
![Pasted%20image%2020250426133052.png](images/Pasted%20image%2020250426133052.png)
<mark>__merging testing branch into master branch__</mark>
بعمل الmerge وانا واقف في الbranch اللي هيحصل فيه الmerging.
___<mark>المعلم git بيختار طريقة الـ merge بناءً على شكل الـ commit history بتاعك.</mark>___
هو بيقول fast forward لأن ده اللي حصل, الmerge هنا عباره عن اني نقلت الmaster والhead خطوه قدام ل الcommit اللي testing بيشاور عليها. عشان كده اسمه fast forward. 
الfast forward حصل لأن مفيش اي commits زياده فالmaster, بالتالي كلهم على خط واحد, ف هنقل الpointer وخلاص.
![Pasted%20image%2020250426172423.png](images/Pasted%20image%2020250426172423.png)
لو تلاحظ مفيش كوميت جديد اتعمل للـ merge، المعلم git بيبص على الhistory ويلاقي إن كل اللي محتاج يعمله هو إنه ينقل ألmaster (والـ**HEAD** معاه) للكوميت اللي testing بيشاور عليها.

في option اسمه `merged--` مع `git branch` بيوريني الbranches اللي اتعملها merge في الmaster.![Pasted%20image%2020250426172624.png](images/Pasted%20image%2020250426172624.png)
خلاص وظيفه الtesting branch ممكن امسحه عادي كده. <mark>d = delete-</mark>![Pasted%20image%2020250426172709.png](images/Pasted%20image%2020250426172709.png)
_____________________________
مش ده دايما الcase اللي موجود مش لازم الdevelopment يكون linear.
اللي بيحصل مثلا اني بعمل branch والعب فيه وفي نفس الوقت انا بعدل  اصلا فالmaster واعمل commits.![Pasted%20image%2020250426174525.png](images/Pasted%20image%2020250426174525.png)
>that's what is called `Divergent History`.

![Pasted%20image%2020250426183330.png](images/Pasted%20image%2020250426183330.png)
خلصت انا كده وعايز اعمل merge,  هيختلف هنا الmerging مش هينفع الfast forward لأن الhistory مش عباره عن خط من الCommits اقدر اروح واجي عليه لا.

الmerge هنا اسمه `three-way merge` وده بيعتمد على التلاته دول![Pasted%20image%2020250426183854.png](images/Pasted%20image%2020250426183854.png) عشان يعمل الmerge, بيعمل COMMIT جديد revision رابع ولا واحد منهم.

![Pasted%20image%2020250426184439.png](images/Pasted%20image%2020250426184439.png) 
هعمل بقى merge للtesting into master, فلما اعمل ده هيفتحلي text editor يقولي اكتب message عشان ال`merge commit` بقى.

ف ده اللي هيحصل
![Pasted%20image%2020250426184833.png](images/Pasted%20image%2020250426184833.png)
![Pasted%20image%2020250426184857.png](images/Pasted%20image%2020250426184857.png)

مكنش فيه خط linear بين الbranches فGit ااضطر يعمل revision جديد عشان يقدر يعملهم merge وادالها commit message. 

![Pasted%20image%2020250426185128.png](images/Pasted%20image%2020250426185128.png)
كده خلاص Testing اتعلمه merge في الmaster, ف مش محتاجه ممكن امسحه عادي.
________________________
لو شوفت الHEAD  ![Pasted%20image%2020250426185321.png](images/Pasted%20image%2020250426185321.png) هتلاقيه بيقولك انه merge بين الcommits. و هما دول أللي كان بيشاور عليهم ال2branches.
____________

ساعات ممكن اجي اعمل merge ف يحصل `conflict`  ده بيحصل مثلا لما اكون انا معدل في نفس الfile فال2 branches.  
**how can we solve this?**

هيعدل فالfile ده و هيقولي في تعديل فالmaster شكله كده وفي تعديل فالTesting شكله كده انت عايز تسيب انهي واحده فيهم 
هبص على الstatus واشوف الconflicts فين واحلها.  لما اعمل `git status`  هلاقي جمب الfile اللي فيه الconflict مكتوب انه  `both modified` .
ف هعدل فالfile واعمل اللي انا عايزه.و بعد ما اعدل الملف وامسح العلامات، هحفظ التغييرات.ف هاعمل <mark>_git add_</mark> ثم <mark>__git commit__</mark> ف يتعمل الmerge commit.
لما بيحصل الconflict ف git بيعدل الfile عن طريق انه ويحط علامات (`<<<<<<<`, `<mark>=</mark>===`, `>>>>>>>`) عشان يوضح التغييرات من الفرعين:
- التغييرات من master هتبقى تحت <mark>_<<<<<<< HEAD_</mark>.
- التغييرات من testing هتبقى تحت <mark>_>>>>>>> testing_</mark>.
- بينهم فاصل (`<mark>=</mark>==`).
- ![Pasted%20image%2020250426234859.png](images/Pasted%20image%2020250426234859.png)
 **Merge Conflicts**
If you try to do merge commit with conflicting files in both branches git will notify you and abort the process. To check the conflicting portions of the file use `git status` then resolve the conflict then commit then merge again

**<mark>git branch</mark> important options**
![Pasted%20image%2020250426233219.png](images/Pasted%20image%2020250426233219.png)

**git rebase**
الrebase هو شكل اخر من الmerge.
هو عباره عن merge عادي جدا بتعمل branches وفالاخر بتعمل `git rebase`. 
Rebase is one of two Git utilities that specializes in integrating changes from one branch onto another. Merge is always a forward moving change record. Alternatively, rebase has powerful history rewriting features.
الفرق انه لما تستخدم الmerge بتلاقي الcommits لسه موجوده عادي. لكن الrebase بيخلي الموضوع يرجع linear history تاني كأن محصلش branching قبل كده.
![Pasted%20image%2020250426235631.png](images/Pasted%20image%2020250426235631.png)

Rebasing is the process of moving or combining a sequence of commits to a new base commit. Rebasing is most useful and easily visualized in the context of a feature branching workflow.
![Pasted%20image%2020250426235950.png](images/Pasted%20image%2020250426235950.png)
***___________________________________________________________________________________________***

# working with remotes 
بما ان git هو **distribute version control** ف بالتالي اقدر أclone repo واشتغل عليه local عادي. مش لازم دايما يبقى الconnection شغال. واقدر لما اخلص التعديلات بتاعتي اعملها `push`. ولو حصل اي تعديل من الناس اللي بتcontribute فالrepo دي أقدر أpull الmodifications او الupdates دي.

**working with remotes Architecture**
![Pasted%20image%2020250427002711.png](images/Pasted%20image%2020250427002711.png)

لما اعمل Clone لأول مره ل الremote repo ده. هيبقى عندي نسخه طبقه الاصل من الrepo وقت ما عملت clone. بالbranches والcommits كل حاجه حتى نفس ال `SHA1` و نفس الrefernces بتاعهم. 
`identical copy`.
بعد كده يأما اعمل push للmodifications او الupdates بتاعتي او اعمل pull ل الupdates ` Synchronize` ب fetch او pull.
![Pasted%20image%2020250427003106.png](images/Pasted%20image%2020250427003106.png)
___________________

اقدر أconnect على اكتر من remote. 
![Pasted%20image%2020250427003259.png](images/Pasted%20image%2020250427003259.png)

مثلا في اكتر من شخص على مستوى العالم شغلاين على نفس الrepo وكل واحد عنده النسخه بتاعته بيعدل فيها فأقدر اخد دايما الupdates او أpush التعديلات بتاعتي.
to deal with remotes we can use `git remote`.
ف typically بنعمل الكلام ده على `hosting service`, مثلا repo موجود على hosting service زي git-lab او git-hub مثلا.

عشان اعلم cloning هستخدم `git clone` واديله الlocation بتاع الrepo دي. هو تلقائي بيدي الlocal repo  نفس الاسم بتاع الremote لو لسبب ما كنت عايز اغير الاسم بتاع الlocal repo عندي هاكتب الاسم اللي انا عايزه بعد الlocation.
![Pasted%20image%2020250427004919.png](images/Pasted%20image%2020250427004919.png)

عشان اشوف كل الreomte repos اللي عندي هستخدم `git remote`.
![Pasted%20image%2020250427005439.png](images/Pasted%20image%2020250427005439.png)

ال<mark>_origin_</mark> ده اسمه الshort name. لما اشوف origin دي كده ده معناه ان الrepo أللي شغال عليه ده متاخد من remote repo. 
الorigin ده  اسمه الshort name او ال`alias` بتاع الremote repo. لو عايز اعرف details عن الremote repo ده.  
هستخدم `git remote -v`
![Pasted%20image%2020250427010213.png](images/Pasted%20image%2020250427010213.png)

هلاقي فيه اتنين origin والorigin دي زي alias كده عن الURL بدل ما كل مره  هكتب الURL كله.
في السطرين دول بيقولي انه فالrepo ده اقدر اعمل حاجتين اقدر اعمل fetch و push.

لو جيت عدلت فالRemote وعملت Commit والدنيا تمام. 
ده الremote:
![Pasted%20image%2020250427040606.png](images/Pasted%20image%2020250427040606.png)

وده الlocal:
![Pasted%20image%2020250427040609.png](images/Pasted%20image%2020250427040609.png)

هاجي اشوف ده فالlocal مثلا اجرب `git status` مش هيحس بيه 
![Pasted%20image%2020250427033103.png](images/Pasted%20image%2020250427033103.png)

وده مش صح. ازاي انا up to date مع الremote.
لكن ده طبيعي لأنك لسه مجبتش الupdates اللي حصلت فالremote. هي دي اخر حاجه يعرفها الlocal repo انك up to date.

ف by the way, عشان اعرف الbranches اللي جايه من الremote. هنستخدم `git branch -r`.
![Pasted%20image%2020250427033502.png](images/Pasted%20image%2020250427033502.png)

لو انا عايز اضيف اكتر من remote, هنستخدم `<git remote add <short> <URL`.

عشان اجيب و اعرف التغيرات  اللي حصلت فالremote repo من اخر مره عملت Cloning,  عشان اعمل ده في طريقه من 2.
الطبيعي اني بعمل `<اسم الريبو> git fetch`  اللي بيعمله هو انه بيجيب كل الobjects وال References وكل الحاجات أللي اتغيرت من الremote ل الlocal repo بتاعي.
![Pasted%20image%2020250427034650.png](images/Pasted%20image%2020250427034650.png)

بعد `git fetch` هو عرف ان  في commit جديده اتعملت فالremote بس ليه مطبهاش فالWorking tree عندي فالlocal repo.
حتى لما عملت cat-file عندي فالlocal Repo ل الrevision اللي اتضاف فالremote repo لاقيته موجود.
![Pasted%20image%2020250427035757.png](images/Pasted%20image%2020250427035757.png)

اللي بيحصل ان `git fetch` بتعمل download لكل الupdates والrevisions ألمختلفه عن الlocal لكن مبتعملهاش `merge` مع الlocal repo والworking tree عندي.
بحيث يبقى في Work flow حتى اعمل `git show` واشوف ايه الدنيا. لو تمام خلاص اعمل `git merge`. 

ف by the way لو جربت اعمل `git status` بعد ما عرف updates لما عملت `git fetch` هلاقيه جابلي الرساله التمام.
![Pasted%20image%2020250427040353.png](images/Pasted%20image%2020250427040353.png)

لما اعمل `git merge` هيعمل update ل الworking tree.
![Pasted%20image%2020250427041027.png](images/Pasted%20image%2020250427041027.png)

و git status خلاص مفيش حاجه انت up to date وتمام.
![Pasted%20image%2020250427041327.png](images/Pasted%20image%2020250427041327.png)

طب لو جربت اعمل تعديل فالlocal. ألlocal repo عارف كل حاجه, هيقولك انت اللي متقدم Commit عن الremote.
![Pasted%20image%2020250427041522.png](images/Pasted%20image%2020250427041522.png)
![Pasted%20image%2020250427041646.png](images/Pasted%20image%2020250427041646.png)
هنا الCommit التانيه دي هي اخر حاجه git عارف انها تبع الorigin و عليها الorigin/head والorigin/master.
و الHEAD على local branch, تعرف انه local لما متلاقيش جمبه `origin` دي. 

حتى اهو الremote معندوش غير 2commits
![Pasted%20image%2020250427042340.png](images/Pasted%20image%2020250427042340.png)

بعد كده خطوه ال`git push`. 

 **typical work flow.**
  الطبيعي اني لما بعمل cloning ل الremote repo مش عشان اعدل فالmaster. ممكن اعمل branch خاص بيا انا و بشغلي. وبعدين اعمل ال push. عشان أ synchronize ال branch ده مع الremote repo. وده الطبيعي فالشغل.
  والشخص اللي شغال على الremote repo ده بيrevise الكلام بتاعك. 

  <mark>اغلب الremote repos بتبقى لمجرد الdevelopment ف ملهاش working tree من الاساس.</mark>
__________

لو جيت عملت branch في الLocal وعملتله switch  ثم عملتله commit.
![Pasted%20image%2020250427045351.png](images/Pasted%20image%2020250427045351.png)

هلاقي ان Git مش شايف ومش فاهم ايه علاقه branch feature بالremote. 
هو basically, مفيش اي branch زيه او قصاده فالRrmote عشان يقدر يقارن بينهم, git مش tracking اي feature branch في الremote.
لما تيجي تعمل `git status` بيقارن الlocal branch بالtracked remote branch اللي قصاده.

كده عندي branch كامل مش موجود فالRemote. ف هعمل بقى <mark>up stream</mark> عن طريق
`<اسم البرانش> git push`. <اسم البرانش> اللي ه push عليه.
![Pasted%20image%2020250427123638.png](images/Pasted%20image%2020250427123638.png)

جابلي الerror ده `the current branch feature has no upstream branch.`.
اللي هو الbranch feature اللي بتقولي اعمله push ده اعمله push على ايه.  مفيش قصاده branch تاني عشان يعمل معاه synchronization. 
ف git مش عارف يعمل synchronize للbranch ده مع اي branch فالremote.

بيقترح انك تعمل `git push --set-upstream origin feature`.
ف هعمل ده مره واحده لأن الbranch كله مش موجود فالremote.
<mark>__--set-upstream__</mark> = <mark>_-u_</mark>.
so we can type `git push -u origin feature`
بقوله وانت بتpush اعمل branch اسمه feature فالorigin. اذا الcommand ده هيعمل feature branch وي synchronize الupdates بتاعته.
![Pasted%20image%2020250427125047.png](images/Pasted%20image%2020250427125047.png)

![Pasted%20image%2020250427125013.png](images/Pasted%20image%2020250427125013.png)

واتأكد من ده لما اعمل `git branch` فالremote.
![Pasted%20image%2020250427125202.png](images/Pasted%20image%2020250427125202.png)

كده تمام بالنسبه `git status`
![Pasted%20image%2020250427125425.png](images/Pasted%20image%2020250427125425.png)
 هتلاحظ انه المره دي اداني tracking information بين الlocal والremote عن الfeature branch.
  في الاول كان بيجيب عن الmaster بس. 
  ___________
  عشان ن synchronize من الremote ل الlocal, عملنا `git fetch` ثم `git merge` الخطوتين دول اقدر اعملهم ب command واحد بس اللي هو `git pull` ![Pasted%20image%2020250427130543.png](images/Pasted%20image%2020250427130543.png)

![Pasted%20image%2020250427130545.png](images/Pasted%20image%2020250427130545.png)
  ___________
  
![Pasted%20image%2020250427130832.png](images/Pasted%20image%2020250427130832.png) 
بيlist كل الbranches اللي عندي والlatest commit بتاعتهم و بيحددلي ب `*` ان ده الHEAD.

![Pasted%20image%2020250427130933.png](images/Pasted%20image%2020250427130933.png) 
هنا بيقولي ان ال feature في قدامه `origin/feature` و  ال master في قدامه `origin/master`. ده what is called `tracking`.
خلاص انت مش محتاج كل مره اقوله synchronize الbranch الفلاني مع الbranch ده. هو عارف.

***___________________________________________________________________________________________***
# points in vs code chapter 

الاصل فGit-Hub انه hosting service ل git.
اكنه مكان انا ب host فيه الremote repos بتاعتي.
في حاجات تقدر تعملها على git ماقدرش تعملها على git hub والعكس صحيح.

عشان أclone repo من GitHub
![Pasted%20image%2020250427143550.png](images/Pasted%20image%2020250427143550.png)

لو نزلت الzip file هاتروح تعمله extract عادي لو فتحته من الterminal هتلاقي في hidden directory اسمه `github.`
![Pasted%20image%2020250427143849.png](images/Pasted%20image%2020250427143849.png)

بس مفيش `git.` الrepo يعني.
حتى لو فتحت الdirectory ده جوه الVS code كده `. code` هتلاقي انه مش شايف ان هو repo.
وده معناه اني لما عملت download  ل الzip file ده, هو عمل download بجد مش clone.

لو عايز اعمل clone, هلاقيه مديني الURL بتاعه ف ممكن اعمل `<git clone <URL> <name`
![Pasted%20image%2020250427144515.png](images/Pasted%20image%2020250427144515.png)

ولما اخش الdirectry هلاقيه عرف انه repo
![Pasted%20image%2020250427144548.png](images/Pasted%20image%2020250427144548.png)
________________________________________________
# Introduction to GitHub
ممكن نعتبر الgithub زي web hosting ب host عليه الrepos بتاعتي. او أaccess hosted repos من حد تاني.
هو من الحاجات اللي بتخلي git يحقق فكره انه**distributed version control**. 

ممكن انا اعمل repository عادي عن طريق اني أclick على <mark>__New__</mark>.
![Pasted%20image%2020250427195920.png](images/Pasted%20image%2020250427195920.png)

وبيكون اسم الrepo او الURL بتاعه عباره عن `owner-name/repository-name`. والrepository-name ده اللي انت بتحطه ف حاول تعمله Unique بالنسبه للaccount بتاعك.

ممكن اضيف `README` file وهو عباره عن markup file. ممكن اضيفه لو عايز اول ما حد يفتح الrepo الاقي زي description موجود جوه الfile وتكون حاجه descriptive تعرفه الRepo ده عباره عن ايه وبيعمل ايه.
`README` file: <mark>_acts as an introduction and guide._</mark> It outlines how others can contribute, such as submitting bug reports or code. It shows how to use the project, often with examples .It gives a quick overview of what the project is and what it does. 

ال`gitignore.` ده file بحط فيه الpatterns بتاعة الfile اللي مش عايزها تبقى موجوده فالrepo.
بحيث يبقى في files هو مبيبصلهاش اصلا, مهما تعملها add او staging مش هتنضاف و مش هيعمل tracking لل files دي.
It uses patterns (like `*`, `?`, or` /`) to specify what to exclude.
Always double-check your `.gitignore` file before committing to make sure you’re not accidentally uploading files you meant to ignore.

وادوس `create repository`
______
![Pasted%20image%2020250427201611.png](images/Pasted%20image%2020250427201611.png)

***__________________________________________________________________________________________***

# basic GitHub Repo Operation 
>الmian هو الmaster.

اقدر اعدل واعمل كل حاجه.
ممكن اضيف file عن طريق `Add file`. ممكن أupload file زي ما انا عايز.
وعلى حسب الextesion اللي هتضيفه ل الfile فGitHub بيrecognise الfile ده.
![Pasted%20image%2020250427203301.png](images/Pasted%20image%2020250427203301.png)
و بيقولك اعمل commit وبيقترح عليك الcommit message.

![Pasted%20image%2020250427203419.png](images/Pasted%20image%2020250427203419.png)

وهلاقي تأثير ده حصل هنا اهو
![Pasted%20image%2020250427203505.png](images/Pasted%20image%2020250427203505.png)

قالك عندك 2 commits وضاف الfile اهو, وال`SHA1` بتاع الlatest commit.
لو دوست على Commits هيظهرلي الcommits اللي عندي كده
![Pasted%20image%2020250427203803.png](images/Pasted%20image%2020250427203803.png)

لو دوست على ال`SHA1` بتاع اي واحده هايقولي ايه اللي حصل فيها.
![Pasted%20image%2020250427203906.png](images/Pasted%20image%2020250427203906.png)

ممكن ابدأ اconverse مع الناس اللي بتشوف الrepo بتاعي. كل واحد يقدر يسيب comment.
و موجود ده برضو فالissues
![Pasted%20image%2020250427205704.png](images/Pasted%20image%2020250427205704.png)

مثلا يقولي في issue فالحته الفلانيه او الcode بيجيب معايا error مثلا. بعدين هو يقترح عليا حلول او أpass ده ل واحد من الcollaborators عشان يعدل.

الطبيعي عندي فالworkflow ان الrepo بتاعي بحضره locally عندي و بعدين أpush ل الGitHub account بتاعي.
اقدر اعدل في حاجات كتير في GitHub عن طريق الsetting
1-احدد مين الcollaborators معايا او بيcontribute ل الrepo ده.
2-اعدل ال visibility بتاعته
3-امسح الrepo خالص
4-etc
5- أقدر اعمل protected branches محدش يقدر يوصلها, ودي Features مش موجوده في Git.

موجود desktop version ل GitHub لكن ل mac و windows فقط.
_________
لو عايز أcreate Branch هاروح عند كلمه `main` و اكتب اسم الbranch ده.
![Pasted%20image%2020250427211543.png](images/Pasted%20image%2020250427211543.png)

و أclick على `create branch: feature`.
الbranch اللي اسمه بيبقى مكان الmain كده هو ده ال<mark>_current branch_</mark>.

![Pasted%20image%2020250427211825.png](images/Pasted%20image%2020250427211825.png)

ف انا هنا على الfeature branch واي تعديل هعمله هيبقى committed على ال feature branch ده.

![Pasted%20image%2020250427212144.png](images/Pasted%20image%2020250427212144.png)

بعد ماتعمل الcommit 
من ضمن الoptions اللي هيديهالك <mark>__Compare & pull request__</mark> ده اللي بيوديني فالاخر ل ال`merge`.
أ click على __<mark>Compare & pull request</mark>__  
هلاقيه مقترح الmessage عادي. و بيقولي انها <mark>able to merge</mark> الfeature branch  ده into الmain branch. ف أclick على __<mark>create pull request</mark>__!
[Pasted%20image%2020250427214249.png](images/Pasted%20image%2020250427214249.png)

ثم __<mark>merge pull request</mark>__
![Pasted%20image%2020250427214628.png](images/Pasted%20image%2020250427214628.png) 

ثم  اكتبله ال`commit merge message` و أclick على __<mark>confirm merge</mark>__.
![Pasted%20image%2020250427214642.png](images/Pasted%20image%2020250427214642.png)

وأقدر في كل مره اسيب Comment كده.
بس كده الmerge خلص خلاص. 
![Pasted%20image%2020250427214915.png](images/Pasted%20image%2020250427214915.png)

ممكن اdelete الbranch عادي لو خلصت اللي انا عايزه.
***___________________________________________________________________________________________***
# Basic GitHub Workflow  
لو عايز اعمل connection على الrepo ده و يبقى ده الremote repo بتاعي. هعمله clone عادي زي ماعملنا قبل كده
زي ما قولنا ان الطريقه الصح هو اني ب initiate الrepo ده locally وبعدين أpush من الCLI نفسه اياً كان بس من عندي انا. 
لأن وانا بعمل ده locally انا بكون مجهز already الfiles والcommits وكل حاجه عايزها.
ف مش منطقي اني اروح كل شويه اعمل add file والحوارات دي.

من الطرق المستخدمه 
اننا ن<mark>_create empty repo_</mark>. من الحاجات الحلوه في GitHub انه لما بcreate empty repo هو بيعرف انك هت populate الrepo ده من الdown stream ف بيديني شويه options لكل case. !
[Pasted%20image%2020250427222347.png](images/Pasted%20image%2020250427222347.png)

حتى لو تلاحظ دي مظهرتش قبل كده لما خليناه يadd الREADME file واحنا بنcreate الrepo.

 <mark>_push an existing repository from the command line_</mark> 
 لما يكون already عندي repo ,هو ده ال**typical workflow**. انه يكون already عندي repo وانا على الrepo ده locally اعرفله remote.
حتى لو الrepo ده مكنش cloned, لو انت عامله from scratch اقدر اعرفله remote, يعني حته لو مش cloned من حاجه اقدر اعرفله upstream او remote.

ف هعمل repo عندي locally واعمل اللي انا عايزه والcommits وكل حاجه. وبعدين اسمع كلام عمه GitHub واكتب `git remote add origin https://github.com/Mikhanagy55/rrepoooo.git`
اهو ونتأكد وكل حاجه
![Pasted%20image%2020250427224956.png](images/Pasted%20image%2020250427224956.png)

عادي نعمل upstream لو اسامي الbranches مختلفه بس ده مش كويس. ف نسمع كلامه تاني ونغير اسم الmaster ل main.
![Pasted%20image%2020250427225144.png](images/Pasted%20image%2020250427225144.png)
خلاص كله تمام نعمل اخر حاجه بقى اللي هو نعمل push. عن طريق `git push -u origin main`

![Pasted%20image%2020250427225326.png](images/Pasted%20image%2020250427225326.png)

# Authenticating to Push to GitHub

انت عايز تعمل push upstream. هي سايبه؟ عشان عملتلك كام Commit بقى.
لازم يكون عندك permissions عشان تقدر انك تpush وتعدل في GitHub. 
عندي طريقه من اتنين في موضوع الpermissions ده.

لو تاخد بالك بما ان VS code عنده الsupport لgit والGitHub, ف هو بيديك options. بيقولك sign in `authenticate`. 
حتى هتلاقي ده لما تجرب تpush من الCLI.
و ده المنطقي والطبيعي هتلاقيه بيقولك اكتبلي username و password.
![Pasted%20image%2020250428015802.png](images/Pasted%20image%2020250428015802.png)

كأني عملت authentication على GitHub. حتى هو طالب الusername بتاعة `htts://github.com`. 
دي واحده من الطرق اللي ممكن أauthenticate بيها.

note 
![Pasted%20image%2020250428020226.png](images/Pasted%20image%2020250428020226.png)

لو تلاحظ هتلاقي ان origin ده بيستعمل `https` protocol.  
لو تفتكر كان واحنا بنعمل الrepo كان في اختيارين `SSH` و `HTTPS` اعرَّف عن طريقهم الremote repo واحنا عرفنا الremote عن طريق ال`https`.

![Pasted%20image%2020250428020438.png](images/Pasted%20image%2020250428020438.png)

الHTPPS هو اللي فات اللي كنا بنتعامل معاه نكتب الusername والpassword خلاص خلص الauthentication والكلام ده هيخش ال cash memory وكل مره هعمل push مش هيطلبه تاني.


الطريقه التانيه هي المستعلمه اكتر لأكتر من سبب
1-for security reasons
2-مش دايما هتكون بتpush على Account بتاعك اصلا. وممكن تكون بتpush على حاجه مفتوحه مؤقتاً لل contribution او حاجه ملكش ليها access. الى اخره.

#### SSH 
![Pasted%20image%2020250428021418.png](images/Pasted%20image%2020250428021418.png)
![Pasted%20image%2020250428021546.png](images/Pasted%20image%2020250428021546.png)

هنستعمل الURL بتاع الSSH ده. وعملنا الshort name بتاع الremote اسمه `ssh-origin`.
لما اعمل `git remote -v`,  ظهر 2 remotes واحد اسمه origin والURL بتاعه https و ده الprotocol اللي شغال بيه. 
والتاني اسمه ssh-origin. هو نفس المكان ونفس كل حاجه لكن الprotocol المستعمل مختلف. ده شغال ب `SSH`.

لو جرب اعملت push بالURL بتاع الSSH.
![Pasted%20image%2020250428022154.png](images/Pasted%20image%2020250428022154.png)

هو جاب error `permission denied` بس مش هيطلب مني username و password.
وهي دي الفكره اللي عايزينها. لو هتعمل push وهستعتمل الSSH او هستعمل remote بكَلِمُه بالSSH.
اذا لازم يبقى فيه الprivate والpublic keys.

الpublic key ده hash كبير المفروض انا بعمله locally عندي على الmachnie. والkey ده يكون already copied او staged او موجود في الsettings بتاعة الGitHub account.

ف اللي بيحصل ان GitHub account بيقارن بين الkey اللي متخزن عنده واللي متخزن عندي locally على الmachine. لو الاتنين متطابقين, اذا الراجل ده من حقه يpush ويcontribute على الrepo دي.

so, The next step is to generate an SSH public key and add it to your GitHub account’s SSH settings.

![Pasted%20image%2020250428023733.png](images/Pasted%20image%2020250428023733.png)

حتى هو بيوريني ازاي اعمل generate ل الkey.

هgenerate ألkey عن طريق الcommand ده
![Pasted%20image%2020250428023833.png](images/Pasted%20image%2020250428023833.png)

لازم تتأكد ان الايميل اللي هتكتبه هنا اللي هو على اساسه هيتعمل الkey, يكون هو نفس الemail اللي انت عملت بيه ال configuration ل الgit repo locally عندي.

![Pasted%20image%2020250428025816.png](images/Pasted%20image%2020250428025816.png)

هيعمل 2files اهم حاجه بالنسبالنا هي الpublic key file, هناخد الcontent بتاعته copy ونحطها على الGitHub account عشان اقدر اعمل push.


before adding a new SSH key to the `ssh-agent` to manage your keys, you should have checked for existing SSH keys and generates a new key.

![Pasted%20image%2020250428031416.png](images/Pasted%20image%2020250428031416.png)
![Pasted%20image%2020250428031444.png](images/Pasted%20image%2020250428031444.png)

بيقولي تقدر كمان تعمل evaluation تتأكد ان الkey اتعمل صح. 
![Pasted%20image%2020250428133037.png](images/Pasted%20image%2020250428133037.png)

الPID بيظهر عشان يأكد إن الـ Agent شغال, وتقدر تستخدم الرقم ده لو عايز تتحكم في العملية (مثلاً توقّفها أو تشوفها).
الـ SSH Agent نفسه بيستخدم الـ PID ده داخليًا عشان يحمل الprivate key (زي id_ed25519) في الmemory، ويوفّرها لما تتصل بسيرفر زي GitHub (مثلاً لما تعمل git push).

و بعدين اضيف الprivate key لو انا عايز اضيف بس مش محتاج.

بعدين اشوف الcontent بتاع الpublic key 
![Pasted%20image%2020250428133856.png](images/Pasted%20image%2020250428133856.png)

وهاخد الcontent كله copy وارجع ل GitHub و اخش على الssh key setting و أclick على <mark>__New SSH Key__</mark>.
اديله اي اسم ,واحط الkey.
![Pasted%20image%2020250428134116.png](images/Pasted%20image%2020250428134116.png)

وأclick على <mark>__Add SSH key__</mark>.

نعمل push بقى.
![Pasted%20image%2020250428134950.png](images/Pasted%20image%2020250428134950.png)

الpush المره دي نجح.

اتأكد برضو لما تلاقي الlocal والremote عندهم نفس الcommits بلا`SHA1` بتاعهم.
![Pasted%20image%2020250428140237.png](images/Pasted%20image%2020250428140237.png)

![Pasted%20image%2020250428140252.png](images/Pasted%20image%2020250428140252.png)

كده الpush successful.

![Pasted%20image%2020250428140612.png](images/Pasted%20image%2020250428140612.png)

وهنا بيقولك ان تم استعماله بالفعل.

اقدر اخش على الseeting وبتاعه الrepo واعملله delete.

![Pasted%20image%2020250428030442.png](images/Pasted%20image%2020250428030442.png)

ده هيأكدلك إن GitHub عارف المفتاح بتاعك من غير ما تحتاج تعمل push.

**What is the SSH Agent?**
 The **SSH Agent** is a background process that runs on your system to manage your SSH **private keys**. Its main job is to securely handle these keys and facilitate authentication with remote servers (e.g., GitHub) without requiring you to manually enter a passphrase or credentials every time you connect.

 Think of the SSH Agent as a "key manager" that holds your private keys in memory and automatically provides them to servers when needed, making your SSH interactions seamless.
 you can start it with `eval "$(ssh-agent -s)"`, add keys with `ssh-add`, and use it in VS Code’s terminal for seamless Git operations. 
 If you have multiple keys or issues with your old key tied to an IP, configure <mark>_~/.ssh/config_</mark> to ensure the correct key is used.

نعمل pull والfetch 
لو جيت على الorigin من GitHub وعلمت file وعملت commit. كده اصبح ان عندي 2file.
لو جيت على الlocal repo مش هلاقي عندي فالmain branch غير file واحده.
ف محتاج اني اعمل `fetch` عشان اقدر اشوف التعديلات. 
![Pasted%20image%2020250428142718.png](images/Pasted%20image%2020250428142718.png)

كده عملت fetch لو عملت git log 
![Pasted%20image%2020250428143222.png](images/Pasted%20image%2020250428143222.png)

ممكن استخدم `all--` عشان يوريني كل الcommits الموجوده سواء remote او local.
![Pasted%20image%2020250428142836.png](images/Pasted%20image%2020250428142836.png)

هيقولي في واحده ذياده 
عشان الذياده دي اشوفها عندي فالlocal هعمل `git merge`
![Pasted%20image%2020250428143408.png](images/Pasted%20image%2020250428143408.png)


لو عملت git log هلاقي ال4commits الموجوده.
![%20Pasted%20image%2020250428143446.png](images/%20Pasted%20image%2020250428143446.png)
أقدر اpublish من على الVS code 
![Pasted%20image%2020250428145326.png](images/Pasted%20image%2020250428145326.png)

ده واحد من الworkflows انه اكون شغال على الrepo بتاعتي انا. الremote على GitHub والlocal على الmachine.

# Forking GitHub Repos
اغلب الشغل الشغل مش على الrepo بتاعتي, بيبقى على repos بتاعة ناس تانيه.

ف ازاي أContribute في repo زي hello world. اذاً هنا الworkflow هيختلف. مش الpush والpull المباشر اصل الrepo ده مش بتاعي.
اول حاجه هعملها هو اني اعمل `fork` ل الrepo ده. ده معناه اني بعمل copy من الrepo ده من على GitHub ل GitHub account بتاعي. 
ف هيتعمل repo عندي على الGitHub account بتاعي. هيكون نسخه من ده ويبقى `forked` منه بنفس الاسم والcontent وكل حاجه.
عشان اعمل fork. هاروح أclick على `fork`
![Pasted%20image%2020250428150922.png](images/Pasted%20image%2020250428150922.png)

هتلاحظ ان في 1500 واحد عاملين ل الrepo ده fork.

_______

![Pasted%20image%2020250428151135.png](images/Pasted%20image%2020250428151135.png)


وهتلاقي كل settings والcommits وال configuration كلها موجوده عندك.

من ضمن الحاجات اللي اقدر اعملها بعد الfork اني أ`Fetch upstream` او أ`contribute`
![Pasted%20image%2020250428151806.png](images/Pasted%20image%2020250428151806.png)

طب عايز ابدأ إني أcontribute مع الناس دي, عايز أpush انا كمان.
عشان اعمل ده بعد ما اعملت الfork. إما انك تعدل في GitHub اعمل add file وكل الكلام ده.   
او الطبيعي والمنطقي <mark>_اني اعمل cloning من الforked repo بتاعي_</mark> ده. 
![Pasted%20image%2020250428152203.png](images/Pasted%20image%2020250428152203.png)

![Pasted%20image%2020250428152232.png](images/Pasted%20image%2020250428152232.png)

ولو عملت `git remote -v`
![Pasted%20image%2020250428152356.png](images/Pasted%20image%2020250428152356.png)

هلاقي ان الremote بتاع الrepo ده هو من الaccount بتاعي. مش الoriginal اللي واخد منه الfork.

وممكن اضيف remote تاني اللي هو الشخص اللي واخد منه الfork.
![Pasted%20image%2020250428152744.png](images/Pasted%20image%2020250428152744.png)

عشان ابقى قادر اشوف الupdates دايما وابقىup to date مع الrepo الاصلي. واعدلها و أpush التعديلات دي عندي.
ما انا مش هعرف اعمل push عند الoriginal file.

لو عدلت انا فالforked عندي فالLocal ف هعمل push عادي للmodifications أللي عملتها ل الremote forked repo.  ف انا شايف ان الكلام ده مهم وكده عايز اقول ل صاحب الRepo انه يضيف تعديلاتي فهيحصل ده ازاي؟؟

هنا يظهر ييجي مفهوم جديد في `GitHub` اسمه `pull request`.  بطلب منه يعمل pull ل الforked repo بتاعي بعد ما ضفت تعديلاتي. 
عشان اعمل ده هاروح ل<mark>pull request</mark>
![Pasted%20image%2020250428153905.png](images/Pasted%20image%2020250428153905.png) 
و أclick على <mark>__Create pull request__</mark> 
ف هيشوف التعديلات اللي انا عدلتها ومش موجوده فالoriginal
![Pasted%20image%2020250428154009.png](images/Pasted%20image%2020250428154009.png)

و أclick على <mark>__Create pull request__</mark>

واحط الmessage وابدأ اديله تفاصيل عن اللي عملته, و أclick على <mark>__Create pull request__</mark>.
عند الراجل هناك بقى هيفتح الpull request هيلاقي في request جايله منahmed sami 

![Pasted%20image%2020250428154309.png](images/Pasted%20image%2020250428154309.png)
و يا اما يقبله او ي close انه ي ignore يعني.
ويحط comment 
![Pasted%20image%2020250428154601.png](images/Pasted%20image%2020250428154601.png)


من ضمن الحاجات اللي اقدر اعملها على GitHub  انه احط policies و restrictions بحيث مين يقدر يcontribute او يقبل الpull requests في branches معينه. اقدر احدد ده والprotected branches ومين يقبل pull request كل pull request محتاج له كام approval. من الحاجات اللي موجوده في GitHub ومش موجوده في git.

**made by [Mikhail Nagy](https://www.linkedin.com/in/mikhail-nagy-99620718a)**
