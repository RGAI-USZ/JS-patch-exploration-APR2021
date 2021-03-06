# Data for patch correctness study presented at APR 2021 @ICSE

This repository contains open science data used in the paper **Exploring Plausible Patches Using Source Code Embeddings in JavaScript**.

If you use this data for academic purposes, please cite the appropriate publication:
Viktor Csuvik, Dániel Horváth, Márk Lajkó, László Vidács, [Exploring Plausible Patches Using Source Code Embeddings in JavaScript](https://arxiv.org/abs/2103.16846)

Candidate patches can be found under the `candidate_patches` folder. The `eslint_i` subfolder contains the candidate patches for the `i`-th bug. In these subfolders 3 different naming conventions are used:
 - `Eslint_i_buggy.js`: the original (buggy) program of Eslint_i
 - `Eslint_i_dev.js`: the developer fix
 - `Eslint_i_p.js`: the p-th generated patch candidate
 
 The annotated data for each bug is stored in the `categorizations.csv` file and also displayed in a table format at the bottom of this file. The columns of the csv file are the following:
 >`bug_id, patch_id, rel_1, rel_2, res`

Where:
 - `bug_id` is the identifier of the bug
 - `patch_id` is the identifier of the generated patch
 - `rel_1, rel_2` are the relevance scores given by each expert
 - `res` is the resolution where individual scores differed
 
 
 The relevance score is a real number ranging between -1 to 2. -1 would mean that a patch is clearly incorrect, while 2 annotates that a patch syntactically matches the developer fix. We marked with 0, where we were uncertain about the patch and with 1 if the patch is semantically identical to the developer fix. Intermediate categories are also conceivable: e.g. -0.5 would mean that a patch is probably incorrect, but we were not sure about that, because the lack of domain knowledge about the system examined.
 
 
 |bug_id    |patch_id|rel_1|rel_2|res |
|----------|--------|-----|-----|----|
|Eslint_1  |0       |0    |0    |0   |
|Eslint_1  |1       |0    |0    |0   |
|Eslint_1  |2       |0    |0    |0   |
|Eslint_1  |3       |-0.5 |0    |-0.5|
|Eslint_100|0       |0    |0.5  |0.5 |
|Eslint_100|1       |-1   |-1   |-1  |
|Eslint_100|10      |-1   |-1   |-1  |
|Eslint_100|11      |-1   |-1   |-1  |
|Eslint_100|2       |-1   |-1   |-1  |
|Eslint_100|3       |-1   |-1   |-1  |
|Eslint_100|4       |-1   |-1   |-1  |
|Eslint_100|5       |-1   |-1   |-1  |
|Eslint_100|6       |-1   |-1   |-1  |
|Eslint_100|7       |-1   |-1   |-1  |
|Eslint_100|8       |-1   |-1   |-1  |
|Eslint_100|9       |-1   |-1   |-1  |
|Eslint_217|0       |0.5  |1    |1   |
|Eslint_217|1       |0.5  |1    |1   |
|Eslint_217|2       |0.5  |1    |1   |
|Eslint_217|3       |0.5  |1    |1   |
|Eslint_221|0       |-0.5 |-1   |-1  |
|Eslint_221|1       |-0.5 |-1   |-1  |
|Eslint_221|10      |-0.5 |-0.5 |-0.5|
|Eslint_221|100     |-1   |0.5  |0.5 |
|Eslint_221|101     |1    |1    |1   |
|Eslint_221|102     |0.5  |1    |1   |
|Eslint_221|103     |-1   |1    |1   |
|Eslint_221|104     |0.5  |1    |1   |
|Eslint_221|105     |0.5  |1    |1   |
|Eslint_221|106     |-1   |1    |1   |
|Eslint_221|107     |-0.5 |1    |1   |
|Eslint_221|108     |0.5  |0.5  |0.5 |
|Eslint_221|109     |0    |0.5  |0.5 |
|Eslint_221|11      |-0.5 |0    |-0.5|
|Eslint_221|110     |-0.5 |1    |1   |
|Eslint_221|111     |0    |0.5  |0.5 |
|Eslint_221|112     |0    |0.5  |0.5 |
|Eslint_221|113     |0    |1    |1   |
|Eslint_221|114     |0    |1    |1   |
|Eslint_221|115     |-0.5 |-1   |-1  |
|Eslint_221|116     |0    |-1   |-1  |
|Eslint_221|117     |0    |-1   |-1  |
|Eslint_221|118     |1    |1    |1   |
|Eslint_221|119     |0.9  |1    |1   |
|Eslint_221|12      |-1   |1    |1   |
|Eslint_221|120     |1    |1    |1   |
|Eslint_221|121     |-1   |1    |1   |
|Eslint_221|122     |0    |1    |1   |
|Eslint_221|123     |0    |1    |1   |
|Eslint_221|124     |0    |1    |1   |
|Eslint_221|125     |0    |1    |1   |
|Eslint_221|126     |1    |1    |1   |
|Eslint_221|127     |1    |1    |1   |
|Eslint_221|128     |0.5  |1    |1   |
|Eslint_221|129     |1    |1    |1   |
|Eslint_221|13      |0    |0.5  |0.5 |
|Eslint_221|130     |0    |-1   |-1  |
|Eslint_221|131     |0    |-1   |-1  |
|Eslint_221|132     |-0.5 |1    |1   |
|Eslint_221|133     |0    |-1   |-1  |
|Eslint_221|134     |0    |-1   |-1  |
|Eslint_221|135     |0    |1    |1   |
|Eslint_221|136     |0    |-1   |-1  |
|Eslint_221|137     |-0.5 |1    |1   |
|Eslint_221|138     |0    |1    |1   |
|Eslint_221|139     |1    |1    |1   |
|Eslint_221|14      |0    |1    |1   |
|Eslint_221|140     |0    |-1   |-1  |
|Eslint_221|141     |1    |1    |1   |
|Eslint_221|142     |1    |1    |1   |
|Eslint_221|143     |1    |1    |1   |
|Eslint_221|144     |0    |1    |1   |
|Eslint_221|145     |0    |1    |1   |
|Eslint_221|146     |0    |0    |0   |
|Eslint_221|147     |1    |1    |1   |
|Eslint_221|148     |0    |-1   |-1  |
|Eslint_221|149     |0    |-1   |-1  |
|Eslint_221|15      |0    |-1   |-1  |
|Eslint_221|150     |0    |-1   |-1  |
|Eslint_221|151     |1    |1    |1   |
|Eslint_221|152     |-1   |1    |1   |
|Eslint_221|153     |-1   |1    |1   |
|Eslint_221|154     |0    |1    |1   |
|Eslint_221|155     |1    |1    |1   |
|Eslint_221|156     |1    |1    |1   |
|Eslint_221|157     |1    |1    |1   |
|Eslint_221|158     |0    |-1   |-1  |
|Eslint_221|159     |0    |-1   |-1  |
|Eslint_221|16      |0    |-1   |-1  |
|Eslint_221|160     |1    |1    |1   |
|Eslint_221|161     |0    |1    |1   |
|Eslint_221|162     |0    |1    |1   |
|Eslint_221|163     |0    |1    |1   |
|Eslint_221|164     |0    |1    |1   |
|Eslint_221|165     |1    |1    |1   |
|Eslint_221|166     |1    |1    |1   |
|Eslint_221|167     |0    |-1   |-1  |
|Eslint_221|168     |0    |-1   |-1  |
|Eslint_221|169     |1    |1    |1   |
|Eslint_221|17      |0    |-1   |-1  |
|Eslint_221|170     |0    |1    |1   |
|Eslint_221|171     |0    |-1   |-1  |
|Eslint_221|172     |1    |1    |1   |
|Eslint_221|173     |1    |1    |1   |
|Eslint_221|174     |1    |1    |1   |
|Eslint_221|175     |1    |1    |1   |
|Eslint_221|176     |0    |1    |1   |
|Eslint_221|177     |1    |1    |1   |
|Eslint_221|178     |0.9  |1    |1   |
|Eslint_221|179     |0.9  |1    |1   |
|Eslint_221|18      |0    |-1   |-1  |
|Eslint_221|180     |0    |1    |1   |
|Eslint_221|181     |-1   |1    |1   |
|Eslint_221|182     |1    |1    |1   |
|Eslint_221|183     |0    |-1   |-1  |
|Eslint_221|184     |0.9  |1    |1   |
|Eslint_221|185     |1    |1    |1   |
|Eslint_221|186     |0    |0    |0   |
|Eslint_221|187     |0    |-1   |-1  |
|Eslint_221|188     |0    |1    |1   |
|Eslint_221|189     |1    |1    |1   |
|Eslint_221|19      |1    |1    |1   |
|Eslint_221|190     |1    |1    |1   |
|Eslint_221|191     |1    |1    |1   |
|Eslint_221|192     |1    |1    |1   |
|Eslint_221|193     |1    |1    |1   |
|Eslint_221|194     |1    |1    |1   |
|Eslint_221|195     |0.9  |1    |1   |
|Eslint_221|196     |0    |-1   |-1  |
|Eslint_221|197     |0    |-1   |-1  |
|Eslint_221|198     |-1   |1    |1   |
|Eslint_221|199     |1    |1    |1   |
|Eslint_221|2       |0    |-1   |-1  |
|Eslint_221|20      |0    |-1   |-1  |
|Eslint_221|200     |1    |1    |1   |
|Eslint_221|201     |0.5  |1    |1   |
|Eslint_221|202     |1    |1    |1   |
|Eslint_221|203     |1    |1    |1   |
|Eslint_221|204     |0    |1    |1   |
|Eslint_221|205     |0    |1    |1   |
|Eslint_221|206     |0    |1    |1   |
|Eslint_221|207     |0    |1    |1   |
|Eslint_221|208     |0    |1    |1   |
|Eslint_221|209     |0    |1    |1   |
|Eslint_221|21      |0    |-1   |-1  |
|Eslint_221|210     |0    |1    |1   |
|Eslint_221|211     |0.5  |1    |1   |
|Eslint_221|212     |0    |1    |1   |
|Eslint_221|213     |0    |1    |1   |
|Eslint_221|214     |0    |1    |1   |
|Eslint_221|215     |0    |1    |1   |
|Eslint_221|216     |0    |1    |1   |
|Eslint_221|217     |0    |1    |1   |
|Eslint_221|218     |0    |1    |1   |
|Eslint_221|219     |-0.5 |1    |1   |
|Eslint_221|22      |0.5  |1    |1   |
|Eslint_221|220     |0    |1    |1   |
|Eslint_221|23      |1    |1    |1   |
|Eslint_221|24      |0.5  |0    |0.5 |
|Eslint_221|25      |0    |-1   |-1  |
|Eslint_221|26      |0    |-1   |-1  |
|Eslint_221|27      |0    |-1   |-1  |
|Eslint_221|28      |1    |1    |1   |
|Eslint_221|29      |-1   |1    |1   |
|Eslint_221|3       |0    |-1   |-1  |
|Eslint_221|30      |0    |1    |1   |
|Eslint_221|31      |0    |-1   |-1  |
|Eslint_221|32      |0    |-1   |-1  |
|Eslint_221|33      |0    |-1   |-1  |
|Eslint_221|34      |0    |0    |0   |
|Eslint_221|35      |0    |-1   |-1  |
|Eslint_221|36      |0    |-1   |-1  |
|Eslint_221|37      |0    |-1   |-1  |
|Eslint_221|38      |0    |-1   |-1  |
|Eslint_221|39      |-1   |1    |0   |
|Eslint_221|4       |0    |-1   |-1  |
|Eslint_221|40      |-1   |1    |0   |
|Eslint_221|41      |1    |1    |1   |
|Eslint_221|42      |0    |1    |1   |
|Eslint_221|43      |1    |1    |1   |
|Eslint_221|44      |1    |1    |1   |
|Eslint_221|45      |0    |-1   |-1  |
|Eslint_221|46      |0    |1    |1   |
|Eslint_221|47      |0    |1    |1   |
|Eslint_221|48      |1    |1    |1   |
|Eslint_221|49      |1    |1    |1   |
|Eslint_221|5       |0.5  |1    |1   |
|Eslint_221|50      |0    |-1   |-1  |
|Eslint_221|51      |0    |1    |1   |
|Eslint_221|52      |1    |1    |1   |
|Eslint_221|53      |0.5  |1    |1   |
|Eslint_221|54      |0    |-1   |-1  |
|Eslint_221|55      |0    |-1   |-1  |
|Eslint_221|56      |0    |1    |1   |
|Eslint_221|57      |0    |1    |1   |
|Eslint_221|58      |-0.5 |-1   |-1  |
|Eslint_221|59      |0    |-1   |-1  |
|Eslint_221|6       |1    |1    |1   |
|Eslint_221|60      |0    |1    |1   |
|Eslint_221|61      |-1   |1    |1   |
|Eslint_221|62      |0    |1    |1   |
|Eslint_221|63      |0    |-1   |-1  |
|Eslint_221|64      |0    |1    |1   |
|Eslint_221|65      |-0.5 |1    |1   |
|Eslint_221|66      |1    |1    |1   |
|Eslint_221|67      |1    |1    |1   |
|Eslint_221|68      |0    |1    |1   |
|Eslint_221|69      |0.5  |1    |1   |
|Eslint_221|7       |0    |-1   |-1  |
|Eslint_221|70      |1    |1    |1   |
|Eslint_221|71      |1    |-1   |1   |
|Eslint_221|72      |-0.5 |-1   |-1  |
|Eslint_221|73      |0    |-1   |-1  |
|Eslint_221|74      |0    |-1   |-1  |
|Eslint_221|75      |0    |-1   |-1  |
|Eslint_221|76      |0    |-1   |-1  |
|Eslint_221|77      |0    |1    |1   |
|Eslint_221|78      |0    |-1   |-1  |
|Eslint_221|79      |0    |-1   |-1  |
|Eslint_221|8       |0    |-1   |-1  |
|Eslint_221|80      |0    |-1   |-1  |
|Eslint_221|81      |1    |1    |1   |
|Eslint_221|82      |0    |1    |1   |
|Eslint_221|83      |1    |-1   |1   |
|Eslint_221|84      |0    |1    |1   |
|Eslint_221|85      |1    |1    |1   |
|Eslint_221|86      |0    |-1   |-1  |
|Eslint_221|87      |0    |-1   |-1  |
|Eslint_221|88      |0    |-1   |-1  |
|Eslint_221|89      |1    |1    |1   |
|Eslint_221|9       |0    |-1   |-1  |
|Eslint_221|90      |0    |1    |1   |
|Eslint_221|91      |1    |1    |1   |
|Eslint_221|92      |0.5  |-1   |1   |
|Eslint_221|93      |0    |1    |1   |
|Eslint_221|94      |0    |-1   |-1  |
|Eslint_221|95      |1    |1    |1   |
|Eslint_221|96      |1    |1    |1   |
|Eslint_221|97      |0    |-1   |-1  |
|Eslint_221|98      |0    |1    |1   |
|Eslint_221|99      |0    |-1   |-1  |
|Eslint_321|0       |0.5  |-1   |0.5 |
|Eslint_321|1       |1    |1    |1   |
|Eslint_321|2       |-1   |-1   |-1  |
|Eslint_321|3       |-1   |-1   |-1  |
|Eslint_321|4       |-1   |-1   |-1  |
|Eslint_323|0       |-1   |-1   |-1  |
|Eslint_323|1       |-1   |1    |0   |
|Eslint_323|10      |0.5  |0.5  |0.5 |
|Eslint_323|100     |0.5  |-1   |0   |
|Eslint_323|101     |-1   |1    |-1  |
|Eslint_323|102     |0.9  |1    |1   |
|Eslint_323|103     |-1   |-1   |-1  |
|Eslint_323|104     |-1   |-1   |-1  |
|Eslint_323|105     |-1   |0    |-1  |
|Eslint_323|106     |0    |0    |0   |
|Eslint_323|107     |-1   |1    |-1  |
|Eslint_323|108     |-1   |1    |0   |
|Eslint_323|109     |0.5  |-1   |-1  |
|Eslint_323|11      |0.5  |1    |1   |
|Eslint_323|110     |-1   |-1   |-1  |
|Eslint_323|111     |-1   |0    |-1  |
|Eslint_323|112     |-1   |1    |-1  |
|Eslint_323|113     |-1   |1    |-1  |
|Eslint_323|114     |-1   |-1   |-1  |
|Eslint_323|115     |0.5  |-1   |-1  |
|Eslint_323|116     |-1   |1    |-1  |
|Eslint_323|117     |0    |-1   |-1  |
|Eslint_323|118     |-1   |-1   |-1  |
|Eslint_323|119     |-1   |-1   |-1  |
|Eslint_323|12      |-1   |-1   |-1  |
|Eslint_323|120     |0    |-1   |-1  |
|Eslint_323|121     |-1   |-1   |-1  |
|Eslint_323|122     |-1   |1    |-1  |
|Eslint_323|123     |0    |-1   |-1  |
|Eslint_323|124     |-1   |-1   |-1  |
|Eslint_323|125     |-1   |-1   |-1  |
|Eslint_323|126     |-1   |-1   |-1  |
|Eslint_323|127     |-1   |-1   |-1  |
|Eslint_323|128     |-1   |-1   |-1  |
|Eslint_323|129     |-1   |-1   |-1  |
|Eslint_323|13      |0.9  |-1   |-1  |
|Eslint_323|130     |-1   |-1   |-1  |
|Eslint_323|131     |-1   |-1   |-1  |
|Eslint_323|132     |0.9  |-1   |-1  |
|Eslint_323|133     |0.5  |-1   |-1  |
|Eslint_323|134     |-1   |1    |0   |
|Eslint_323|135     |-1   |0    |-1  |
|Eslint_323|136     |0    |-1   |-1  |
|Eslint_323|137     |0    |-1   |-1  |
|Eslint_323|138     |0    |-1   |-1  |
|Eslint_323|139     |-1   |-1   |-1  |
|Eslint_323|14      |0    |-1   |-1  |
|Eslint_323|140     |-1   |-1   |-1  |
|Eslint_323|141     |-1   |-1   |-1  |
|Eslint_323|142     |-1   |-1   |-1  |
|Eslint_323|143     |-1   |0    |-1  |
|Eslint_323|144     |-1   |-1   |-1  |
|Eslint_323|145     |-1   |-1   |-1  |
|Eslint_323|146     |-1   |-1   |-1  |
|Eslint_323|147     |0    |-1   |-1  |
|Eslint_323|148     |-1   |-1   |-1  |
|Eslint_323|149     |-1   |-1   |-1  |
|Eslint_323|15      |0    |-1   |-1  |
|Eslint_323|150     |-1   |-1   |-1  |
|Eslint_323|151     |-1   |-1   |-1  |
|Eslint_323|152     |0    |-1   |-1  |
|Eslint_323|153     |0    |-1   |-1  |
|Eslint_323|154     |-1   |0    |-1  |
|Eslint_323|155     |-1   |-1   |-1  |
|Eslint_323|156     |-1   |-1   |-1  |
|Eslint_323|157     |-1   |-1   |-1  |
|Eslint_323|158     |-1   |-1   |-1  |
|Eslint_323|159     |-1   |-1   |-1  |
|Eslint_323|16      |0.5  |-1   |-1  |
|Eslint_323|160     |-1   |0    |-1  |
|Eslint_323|161     |-1   |0    |-1  |
|Eslint_323|162     |-1   |-1   |-1  |
|Eslint_323|163     |-1   |-1   |-1  |
|Eslint_323|164     |-1   |-1   |-1  |
|Eslint_323|165     |-1   |-1   |-1  |
|Eslint_323|166     |-1   |-1   |-1  |
|Eslint_323|167     |-1   |-1   |-1  |
|Eslint_323|168     |-1   |-1   |-1  |
|Eslint_323|169     |-1   |1    |1   |
|Eslint_323|17      |1    |1    |1   |
|Eslint_323|170     |-1   |-1   |-1  |
|Eslint_323|171     |-1   |-1   |-1  |
|Eslint_323|172     |-1   |-1   |-1  |
|Eslint_323|173     |-1   |-1   |-1  |
|Eslint_323|174     |-1   |-1   |-1  |
|Eslint_323|175     |-1   |-1   |-1  |
|Eslint_323|176     |-1   |-1   |-1  |
|Eslint_323|177     |-1   |-1   |-1  |
|Eslint_323|178     |-1   |-1   |-1  |
|Eslint_323|179     |-1   |-1   |-1  |
|Eslint_323|18      |0    |-1   |-1  |
|Eslint_323|180     |-1   |-1   |-1  |
|Eslint_323|181     |-1   |-1   |-1  |
|Eslint_323|182     |-1   |-1   |-1  |
|Eslint_323|183     |-1   |-1   |-1  |
|Eslint_323|184     |-1   |-1   |-1  |
|Eslint_323|185     |-1   |-1   |-1  |
|Eslint_323|186     |-1   |-1   |-1  |
|Eslint_323|187     |-1   |-1   |-1  |
|Eslint_323|188     |-1   |-1   |-1  |
|Eslint_323|189     |-1   |-1   |-1  |
|Eslint_323|19      |-1   |1    |1   |
|Eslint_323|190     |-1   |-1   |-1  |
|Eslint_323|191     |-1   |-1   |-1  |
|Eslint_323|2       |0    |-1   |-1  |
|Eslint_323|20      |0    |1    |1   |
|Eslint_323|21      |-1   |-1   |-1  |
|Eslint_323|22      |-1   |-1   |-1  |
|Eslint_323|23      |-1   |0    |-1  |
|Eslint_323|24      |-1   |1    |1   |
|Eslint_323|25      |0.5  |1    |1   |
|Eslint_323|26      |-1   |1    |1   |
|Eslint_323|27      |1    |-1   |1   |
|Eslint_323|28      |-0.5 |-1   |-1  |
|Eslint_323|29      |-1   |-1   |-1  |
|Eslint_323|3       |1    |1.5  |1.5 |
|Eslint_323|30      |-1   |-1   |-1  |
|Eslint_323|31      |-1   |1    |1   |
|Eslint_323|32      |0    |-1   |-1  |
|Eslint_323|33      |0.5  |-1   |-1  |
|Eslint_323|34      |0.5  |1    |1   |
|Eslint_323|35      |0    |1    |1   |
|Eslint_323|36      |-1   |-1   |-1  |
|Eslint_323|37      |0    |-1   |-1  |
|Eslint_323|38      |0    |-1   |-1  |
|Eslint_323|39      |0.9  |-1   |1   |
|Eslint_323|4       |-1   |1    |1   |
|Eslint_323|40      |0.9  |-1   |1   |
|Eslint_323|41      |0    |-1   |-1  |
|Eslint_323|42      |0    |-1   |-1  |
|Eslint_323|43      |0    |-1   |-1  |
|Eslint_323|44      |-1   |-1   |-1  |
|Eslint_323|45      |-1   |-1   |-1  |
|Eslint_323|46      |1    |-1   |1   |
|Eslint_323|47      |0    |-1   |-1  |
|Eslint_323|48      |0    |-1   |-1  |
|Eslint_323|49      |-1   |-1   |-1  |
|Eslint_323|5       |0.9  |-1   |1   |
|Eslint_323|50      |0    |1    |1   |
|Eslint_323|51      |0    |1    |1   |
|Eslint_323|52      |0    |1    |1   |
|Eslint_323|53      |0.5  |1    |1   |
|Eslint_323|54      |0.9  |-1   |1   |
|Eslint_323|55      |0.5  |-1   |0.5 |
|Eslint_323|56      |0.5  |-1   |0.5 |
|Eslint_323|57      |0.5  |-1   |0.5 |
|Eslint_323|58      |0.9  |-1   |1   |
|Eslint_323|59      |-1   |-1   |-1  |
|Eslint_323|6       |2    |2    |2   |
|Eslint_323|60      |0    |-1   |-1  |
|Eslint_323|61      |0    |-1   |-1  |
|Eslint_323|62      |-1   |-1   |-1  |
|Eslint_323|63      |0.5  |1    |1   |
|Eslint_323|64      |0    |1    |1   |
|Eslint_323|65      |-1   |1    |0   |
|Eslint_323|66      |0    |-1   |-1  |
|Eslint_323|67      |0    |-1   |-1  |
|Eslint_323|68      |-1   |1    |1   |
|Eslint_323|69      |1    |1    |1   |
|Eslint_323|7       |0    |1    |1   |
|Eslint_323|70      |0.9  |1.5  |1   |
|Eslint_323|71      |0.5  |1    |1   |
|Eslint_323|72      |-0.5 |1    |1   |
|Eslint_323|73      |-1   |-1   |-1  |
|Eslint_323|74      |0    |1    |1   |
|Eslint_323|75      |0    |1    |1   |
|Eslint_323|76      |-1   |1    |1   |
|Eslint_323|77      |-1   |-1   |-1  |
|Eslint_323|78      |1    |1    |1   |
|Eslint_323|79      |1    |1    |1   |
|Eslint_323|8       |0    |1    |1   |
|Eslint_323|80      |-1   |-1   |-1  |
|Eslint_323|81      |-1   |-1   |-1  |
|Eslint_323|82      |0    |-1   |-1  |
|Eslint_323|83      |-1   |-1   |-1  |
|Eslint_323|84      |0.5  |1    |1   |
|Eslint_323|85      |-1   |1    |0   |
|Eslint_323|86      |-1   |1    |0   |
|Eslint_323|87      |-1   |-1   |-1  |
|Eslint_323|88      |0.5  |1    |1   |
|Eslint_323|89      |0.9  |1    |1   |
|Eslint_323|9       |0.5  |1    |1   |
|Eslint_323|90      |1    |1    |1   |
|Eslint_323|91      |1    |1    |1   |
|Eslint_323|92      |0    |-1   |-1  |
|Eslint_323|93      |-0.5 |-1   |-1  |
|Eslint_323|94      |0    |-1   |-1  |
|Eslint_323|95      |-1   |-1   |-1  |
|Eslint_323|96      |-1   |1    |1   |
|Eslint_323|97      |0    |0    |0   |
|Eslint_323|98      |0    |1    |1   |
|Eslint_323|99      |-1   |-1   |-1  |
|Eslint_41 |0       |-1   |-1   |-1  |
|Eslint_41 |1       |-1   |-1   |-1  |
|Eslint_41 |2       |-1   |-1   |-1  |
|Eslint_47 |0       |2    |2    |2   |
|Eslint_47 |1       |0    |-1   |-1  |
|Eslint_47 |2       |1    |-1   |-1  |
|Eslint_72 |0       |2    |2    |2   |
|Eslint_72 |1       |-1   |0    |-1  |
|Eslint_72 |2       |-1   |0    |-1  |
|Eslint_72 |3       |-1   |-1   |-1  |
|Eslint_72 |4       |-1   |0.5  |0.5 |
|Eslint_72 |5       |-1   |0.5  |0.5 |
|Eslint_72 |6       |-1   |0.5  |0.5 |
|Eslint_94 |0       |-1   |-1   |-1  |
|Eslint_94 |1       |0    |0.5  |0.5 |
|Eslint_94 |10      |-1   |-1   |-1  |
|Eslint_94 |11      |-1   |-1   |-1  |
|Eslint_94 |12      |-1   |-1   |-1  |
|Eslint_94 |13      |-1   |-1   |-1  |
|Eslint_94 |2       |-1   |-1   |-1  |
|Eslint_94 |3       |0    |0.5  |0.5 |
|Eslint_94 |4       |-1   |-1   |-1  |
|Eslint_94 |5       |-1   |-1   |-1  |
|Eslint_94 |6       |-1   |-1   |-1  |
|Eslint_94 |7       |-1   |-1   |-1  |
|Eslint_94 |8       |-1   |-1   |-1  |
|Eslint_94 |9       |-1   |-1   |-1  |

# Acknowledgement
The research presented in this paper was supported in part by the ÚNKP-20-3-SZTE and ÚNKP-20-5-SZTE New National Excellence Programs, by grant NKFIH-1279-2/2020 and by the Artificial Intelligence National Laboratory Programme of the Ministry of Innovation and the National Research, Development and Innovation Office. László Vidács was also funded by the János Bolyai Scholarship of the Hungarian Academy of Sciences.
