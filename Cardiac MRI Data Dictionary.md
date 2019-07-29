| Column             | Data Type   | Description                                                                       | Comments                                      |
|:-------------------|:------------|:----------------------------------------------------------------------------------|:----------------------------------------------|
| Name               | Object      | Name of the MRI image                                                             |                                               |
| Age                | Boolean     | Age at time of the MRI                                                            |                                               |
| Sex                | Boolean     | Patient sex                                                                       | Simple Boolean                                |
| Hypertension       | Boolean     | Presence of hypertension                                                          | Does not include degree of hypertension       |
| Hyperlipidemia     | Boolean     | Presence of hyperlipidemia                                                        | Does not include degree of hyperlipidemia     |
| Diabetes           | Boolean     | Presence of diabetes                                                              | Simple Boolean                                |
| History Of Smoking | Nominal     | Whether or not an individual is a smoker, is not a smoker, or quit smoking        | Nominal categories                            |
| LVEDV              | Continuous  | Ventricular volume in the diastolic phase                                         | Measured in mL                                |
| LVESV              | Continuous  | Ventricular volume in the systolic phase                                          | Measured in mL                                |
| LV Wall Thickness  | Ordinal     | How hypertrophic the muscle wall of the left ventricle is                         | On a scale: 0 (normal) to 3 (severe)          |
| LVEF               | Continuous  | Ventricular ejection fraction: how much blood is move during contraction          | 60% to 70% is considered normal               |
| Aortic Stenosis    | Ordinal     | How stenosed (narrowed) the opening of the valve is                               | On a scale: 0 (not stenosed) to 4 (severe)    |
| Aortic Reg         | Ordinal     | Severity of aortic regurgitation: how much blood moves back through the valve     | On a scale: 0 is mild, 3 is severe            |
| Mitral Reg         | Ordinal     | Severity of mitral regurgitation: how much blood moves back through the valve     | On a scale: 0 is mild, 3 is severe            |
| Tricuscpid Reg     | Ordinal     | Severity of tricuspid regurgitation: how much blood moves bakc through the vavle  | On a scale: 0 is mild, 3 is severe            |
| BA_HE              | Ordinal     | Damage to the tissue on the basal anterior portion of the heart                   | On a scale: 1 (25%) to 4 (100%, tissue death) |
| BAS_HE             | Ordinal     | Damage to the tissue on the basal antero-septal portion of the heart              | On a scale: 1 (25%) to 4 (100%, tissue death) |
| BIS_HE             | Ordinal     | Damage to the tissue on the basal infero-septal portion of the heart              | On a scale: 1 (25%) to 4 (100%, tissue death) |
| BI_HE              | Ordinal     | Damage to the tissue on the basal inferior portion of the heart                   | On a scale: 1 (25%) to 4 (100%, tissue death) |
| BIL_HE             | Ordinal     | Damage to the tissue on the basal infero-lateral portion of the heart             | On a scale: 1 (25%) to 4 (100%, tissue death) |
| BAL_HE             | Ordinal     | Damage to the tissue on the basal antero-lateral portion of the heart             | On a scale: 1 (25%) to 4 (100%, tissue death) |
| MA_HE              | Ordinal     | Damage to the tissue on the mid-anterior portion of the heart                     | On a scale: 1 (25%) to 4 (100%, tissue death) |
| MAS_HE             | Ordinal     | Damage to the tissue on the mid antero-septal portion of the heart                | On a scale: 1 (25%) to 4 (100%, tissue death) |
| MIS_HE             | Ordinal     | Damage to the tissue on the mid infero-septal portion of the heart                | On a scale: 1 (25%) to 4 (100%, tissue death) |
| MI_HE              | Ordinal     | Damage to the mid interior portion of the heart                                   | On a scale: 1 (25%) to 4 (100%, tissue death) |
| MIL_HE             | Ordinal     | Damage to the mid infero-lateral portion of the heart                             | On a scale: 1 (25%) to 4 (100%, tissue death) |
| MAL_HE             | Ordinal     | Damage to the mid antero-lateral portion of the heart                             | On a scale: 1 (25%) to 4 (100%, tissue death) |
| AA_HE              | Ordinal     | Damage to the apical anterior portion of the heart                                | On a scale: 1 (25%) to 4 (100%, tissue death) |
| AS_HE              | Ordinal     | Damage to the apical septal portion of the heart                                  | On a scale: 1 (25%) to 4 (100%, tissue death) |
| AI_HE              | Ordinal     | Damage to the apical interior portion of the heart                                | On a scale: 1 (25%) to 4 (100%, tissue death) |
| Apex_HE            | Ordinal     | Damage to the apex of the heart                                                   | On a scale: 1 (25%) to 4 (100%, tissue death) |
| BA_Ischemia        | Boolean     | Loss of blood flow to the tissue on the basal anterior portion of the heart       | Simple Boolean                                |
| BAS_Ischemia       | Boolean     | Loss of blood flow to the tissue on the basal antero-septal portion of the heart  | Simple Boolean                                |
| BIS_Ischemia       | Boolean     | Loss of blood flow to the tissue on the basal intero-septal portion of the heart  | Simple Boolean                                |
| BI_Ischemia        | Boolean     | Loss of blood flow to the tissue on the basal interior portion of the heart       | Simple Boolean                                |
| BIL_Ischemia       | Boolean     | Loss of blood flow to the tissue on the basal intero-lateral portion of the heart | Simple Boolean                                |
| BAL_Ischemia       | Boolean     | Loss of blood flow to the tissue on the basal antero-lateral portion of the heart | Simple Boolean                                |
| MA_Ischemia        | Boolean     | Loss of blood flow to the tissue on the mid anterior portion of the heart         | Simple Boolean                                |
| MAS_Ischemia       | Boolean     | Loss of blood flow to the tissue on the mid antero-septal portion of the heart    | Simple Boolean                                |
| MIS_Ischemia       | Boolean     | Loss of blood flow to the tissue on the mid intero-septal portion of the heart    | Simple Boolean                                |
| MI_Ischemia        | Boolean     | Loss of blood flow to the tissue on the mid interor portion of the heart          | Simple Boolean                                |
| MIL_Ischemia       | Boolean     | Loss of blood flow to the tissue on the mid intero-lateral portion of the heart   | Simple Boolean                                |
| MAL_Ischemia       | Boolean     | Loss of blood flow to the tissue on the mid antero-lateral portion of the heart   | Simple Boolean                                |
| AA_Ischemia        | Boolean     | Loss of blood flow to the tissue on the apical anterior portion of the heart      | Simple Boolean                                |
| AS_Ischemia        | Boolean     | Loss of blood flow to the tissue on the apical antero-septal portion of the heart | Simple Boolean                                |
| AI_Ischemia        | Boolean     | Loss of blood flow to the tissue on the apical inferior portion of the heart      | Simple Boolean                                |
| AL_Ischemia        | Boolean     | Loss of blood flow to the tissue on the apical lateral portion of the heart       | Simple Boolean                                |