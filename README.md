总结用于测试大语言模型医学性能的Benchmark

## 自然语言
### MedMCQA
[MedMCQA Homepage](https://medmcqa.github.io/)
- **医学领域**
	- 21个学科/亚专科
	- 药理学，耳鼻喉科，预防和社会医学，牙科，外科，儿科，眼科，皮肤科，骨科，生物化学，解剖学，放射学，妇产科，内科，微生物学，生理学，精神病学，病理学，麻醉学。
- **任务类型**
	- 多选问答题
- **数据来源**
	- 全印度医学科学研究所（AIIMS）和国家资格入学考试（NEET）PG入学考试的真题和模拟题，包含自1991年至今的AIIMS PG考试题和2001年至今的NEET PG考试题​。
- **样本数量**
	- 193,155道医学多选题，其中训练集182,822道，验证集4,183道，测试集6,150道
- **评估指标**
	- 回答准确率（accuracy）
### MedQA
[jind11/MedQA: Code and data for MedQA](https://github.com/jind11/MedQA)
- **医学领域**
	- 美国、中国大陆、中国台湾的执业医师考试题
- **任务类型**
	- 多选问答题
- **数据来源**
	- USMLE，MCMLE，TWMLE
	- 同时提供18本英文教科书和33本简体中文教科书的文档
- **样本数量**
	- 英文：12,723道
	- 简体中文：34, 251道
	- 繁体中文：14, 123道
- **评估指标**
	- 回答准确率（accuracy）
### PubMedQA
[PubMedQA Homepage](https://pubmedqa.github.io/)
- **医学领域**
	- PubMed中的临床研究，包括回顾性研究、前瞻性研究、队列研究，以及与治疗结果、预后、风险因素等主题
- **任务类型**
	- 根据提供的上下文回答研究性问题，答案为“是”“否”或“可能”。
- **数据来源**
	- 从PubMed中收集的医学文献摘要。
- **样本数量**
	- 总计273,500个QA实例，包括三个子集：
		- **PQA-L (Labeled)**：1,000个专家标注的QA实例，带有答案。
	    - **PQA-U (Unlabeled)**：61,200个未标注的实例。
	    - **PQA-A (Artificial)**：211,300个人工生成的问题-答案对。
- **评估指标**
	- 准确率（accuracy）与 macro-F1
### MedBench（Mianxin Liu）
https://medbench.opencompass.org.cn/
- **医学领域**
	-涵盖43个临床专科亚专科，包括肿瘤学，传染病学，康复医学，临床营养学，麻醉学，内科学，皮肤科，疼痛医学，外科，儿科，妇产科，急诊医学，结核病学，口腔科，儿童外科，儿童保健，精神病学，妇女健康科，眼科，耳鼻喉科，重症医学，公共卫生，普通内科，内分泌学，肾脏病学，神经科，胃肠病学，心脏科，免疫学，性传播疾病诊所，血液学，胃肠感染科，肝病学，小儿肺科，小儿传染病科，小儿神经科，新生儿科，妇科，生殖健康与不育，口腔黏膜病科，小儿神经外科，儿童生长发育科，临床心理学，青少年健康，更年期健康，鼻科，普外科，肝胆外科，结直肠外科，骨科，泌尿科，烧伤外科，神经外科，心血管与胸外科，胸外科。
- **任务类型**
	- 多选问答、填空问答、开放式问答、信息提取。
- **数据来源**
	- 数据集包括8个公开数据集和12个自建数据集，公开数据集来源包括CMeEE、CMeIE、CHIP-CDEE、CHIP-CDN、CHIP-CTC、MedDG、IMCS-V2-MRG、CMB-Clin；自建数据集包括SMDoc、DBMHG、Med-Exam、MedHC、MedMC、MedSpeQA、MedHG、DDx-basic、DDx-advanced、MedTreat、MedSafety、DrugCA。
- **样本数量**
	- 共计300,901道
- **评估指标**
	- 准确率（Accuracy）用于多选问答
	- BLEU和ROUGE-L用于开放式问答
	- Micro-F1用于信息提取和文本分类任务。
### MMedBench
[Henrychur/MMedBench · Datasets at Hugging Face](https://huggingface.co/datasets/Henrychur/MMedBench)
- **医学领域**
    - 21个医学学科，包括内科、生物化学、药理学、精神病学、微生物学、生理学、病理学、免疫学、妇产科、公共卫生、血液学、外科、急诊医学、骨科、神经病学、解剖学、医学遗传学、放射学、皮肤病学、内分泌学等。
- **任务类型**
    - 多选问答
- **数据来源**
    - 汇集了现有的多语种医学多选问答数据集，包括MedQA（英语和简体中文）、IgakuQA（日语）、FrenchMedMCQA（法语）、RuMedDaNet（俄语）、Head-QA（西班牙语）。
    - 使用GPT-4生成解释性内容，并经过临床专家验证，以确保准确性和广泛的医学知识覆盖。
- **样本数量**
    - 总共53,566道问答对，训练集包含45,048对，测试集8,518对。
- **评估指标**
    - 准确率（accuracy）
    - BLEU-1、ROUGE-1，BERT-score
### MedicationQA
[abachaa/Medication_QA_MedInfo2019: The gold standard corpus for medication question answering introduced in the MedInfo 2019 paper (Bridging the Gap between Consumers’ Medication Questions and Trusted Answers)](https://github.com/abachaa/Medication_QA_MedInfo2019)
- **医学领域**
    - 消费者关于药物的常见问题，例如剂量、副作用、使用时长、停药方法等。
- **任务类型**
    - 问答匹配任务，主要识别问题的聚焦点（如药物名称）和问题类型（如剂量、相互作用、副作用等）并提供对应的答案。
- **数据来源**
    - 来源于MedlinePlus的匿名消费者问题，主要参考了FDA推荐的可信药物信息资源，包括MedlinePlus、DailyMed、Mayo Clinic、PubMed等。
- **样本数量**
    - 674个QA对，涵盖25种问题类型，例如剂量、使用方法、副作用、适应症等。
- **评估指标**
    - 问题焦点识别的F1分数，问题类型识别准确率。
### LiveQA TREC 2017
[abachaa/LiveQA_MedicalTask_TREC2017: Medical Question-Answering datasets prepared for the TREC 2017 LiveQA challenge (Medical Task)](https://github.com/abachaa/LiveQA_MedicalTask_TREC2017)
- **医学领域**
    - 消费者健康问题，涉及疾病、药物和医疗程序。
- **任务类型**
    - 自动问答任务，旨在回答消费者健康问题，包括问题的实体识别和子问题分类。
- **数据来源**
    - 来自美国国家医学图书馆（NLM）的消费者健康问题。
- **样本数量**
    - 训练集：634个问答对（分为388个和246个问答对的两个子集）。
    - 测试集：104个NLM问题。
- **评估指标**
    - 平均得分（avgScore），量化系统回答的质量，评分范围为0-3。
    - 成功率（succ@i+）：统计达到特定评分等级（如2或4分）及以上的问题比例。
    - 准确率（prec@i+）：统计系统回答中达到特定评分的比例

### CMB
[FreedomIntelligence/CMB: CMB, A Comprehensive Medical Benchmark in Chinese](https://github.com/FreedomIntelligence/CMB)
- **医学领域**
    - 个主类别和28个子类别，包括住院医师、护士、医技、药师、基础医学、临床医学、中医及中药学、预防医学与公共卫生等学科。
- **任务类型**
	- 多选问答
	- 临床诊断问答，多轮问答
- **数据来源**
	- 主要来自公开的考试题库和专家整理的医疗教材案例，特别是Medtiku提供的考试真题，并经过专业人员审校与清理​。
- **样本数量**
    - **CMB-Exam**：280,839道选择题
    - **CMB-Clin**：包含74个复杂病例，共208个问答对​
- **评估指标**
	- 选择题准确率（accuracy）
	- 人工或GPT-4对CMB-Clin部分的流畅性、相关性、完整性、专业性评估
### CLUE
[TIO-IKIM/CLUE: CLUE: A Clinical Language Understanding Evaluation for LLMs](https://github.com/TIO-IKIM/CLUE)
- **医学领域**
	- 患者咨询，临床推理，信息提取，病历摘要等
- **任务类型**
	- **MeDiSumQA**：开放式问答任务，要求模型根据MIMIC-IV病历出院总结生成符合患者视角的问题和答案。
	- **MeDiSumCode**：ICD-10编码任务。
	- **MedNLI**：自然语言推理任务。
	- **MeQSum**：患者咨询摘要任务。
	- **Problem Summary**：基于SOAP格式的病历概要提取任务。
	- **LongHealth**：长文本问答任务。
- **数据来源**
	- **MIMIC-III和MIMIC-IV**：使用出院小结和病历记录中的数据。
	- **U.S. National Library of Medicine**：用于MeQSum的患者查询数据集。
	- **LongHealth数据集**
- **样本数量**
	- **MeDiSumQA**：453个样本，平均1451.79词/样本。
	- **MeDiSumCode**：500个样本，平均1515.32词/样本
	- **MedNLI**：1425个样本，平均20.81词/样本。
	- **MeQSum**：1000个样本，平均60.77词/样本。
	- **Problem Summary**：237个样本，平均123.5词/样本。
	- **LongHealth**：400个样本，平均5536.82词/样本。
- **评估指标**
	- **MeDiSumQA**：R-L, R-1, R-2, BERT F1, UMLS F1
	- **MeDiSumCode**：EM F1, AP F1, Valid Code
	- **MedNLI**：accuracy
	- **MeQSum**：R-L，R-1， R-2，BERT F1
	- **Problem Summary**：R-L，R-1，R-2，BERT F1，UMLS F1
	- **LongHealth**：accuracy

## 多模态
### GMAI-MMBench
[GMAI-MMBench](https://uni-medical.github.io/GMAI-MMBench.github.io/)
- **医学领域**
	- 眼科学，耳鼻喉科，头颈外科，呼吸内科，消化科，肝病，泌尿科，手术器械，皮肤科，运动医学，骨科学，血液科，医学检验与病理科。
- **任务类型**
	- 成像质量评估，神经组织识别，胸部、腹部、盆腔和泌尿系统器官识别，血管识别，疾病诊断，血液图像细胞计数，头颈部解剖结构识别，手术动作识别，外科手术流程识别，外科手术器械识别，肌肉识别，骨结构识别，微生物识别。
- **数据来源**
	- 284个来自全球的公开医疗数据集，共38个模态。
- **样本数量**
	- 约26k
- **评估指标**
	- 单项选择题的macro accuracy
	- 多项选择题的命中率（$ACC_{mcq}$）与召回率($Recall_{mcq}$)

### OmniMedVQA
[foreverbeliever/OmniMedVQA · Datasets at Hugging Face](https://huggingface.co/datasets/foreverbeliever/OmniMedVQA)
- **医学领域**
	- 按解剖位置包括肺、乳腺、手、上肢、眼睛、子宫、肠、皮肤、肩部、肾脏、胆囊、胰腺、脾脏、肝脏、盆腔、卵巢、血管、脊柱、泌尿系统、脂肪组织、肌肉组织、口腔、膝盖、足部、下肢。
- **任务类型**
	- 视觉问答（VQA），题目分为五类：成像模态识别、解剖部位识别、疾病诊断、病变分级、其他生物学属性分析。
- **数据来源**
	- 73个医学分类数据集，转化为VQA形式，其中包含12种成像模态：阴道镜检查、CT、数字摄影、眼底摄影、红外反射成像、MRI、光学相干断层成像（OCT）、皮肤镜、内窥镜、显微图像、X光、超声。
- **样本数量**
	- 118,010张医学图像，共127,995个问答对。
- **评估指标**
	- Question-answering Score 与 Prefix-based Score

## 参考
1. Abacha, A. B., Agichtein, E., Pinter, Y., & Demner-Fushman, D. (2017). Overview of the medical question answering task at TREC 2017 LiveQA. _Text Retrieval Conference_. [https://api.semanticscholar.org/CorpusID:3902472](https://api.semanticscholar.org/CorpusID:3902472)
2. Abacha, A. B., Mrabet, Y., Sharp, M., Goodwin, T. R., Shooshan, S. E., & Demner-Fushman, D. (2019). Bridging the Gap Between Consumers’ Medication Questions and Trusted Answers. In _MEDINFO 2019: Health and Wellbeing e-Networks for All_ (pp. 25–29). IOS Press. [https://doi.org/10.3233/SHTI190176](https://doi.org/10.3233/SHTI190176)
3. Bedi, S., Liu, Y., Orr-Ewing, L., Dash, D., Koyejo, S., Callahan, A., Fries, J. A., Wornow, M., Swaminathan, A., Lehmann, L. S., Hong, H. J., Kashyap, M., Chaurasia, A. R., Shah, N. R., Singh, K., Tazbaz, T., Milstein, A., Pfeffer, M. A., & Shah, N. H. (2024). Testing and Evaluation of Health Care Applications of Large Language Models: A Systematic Review. _JAMA_. [https://doi.org/10.1001/jama.2024.21700](https://doi.org/10.1001/jama.2024.21700)
4. Chen, P., Ye, J., Wang, G., Li, Y., Deng, Z., Li, W., Li, T., Duan, H., Huang, Z., Su, Y., Wang, B., Zhang, S., Fu, B., Cai, J., Zhuang, B., Seibel, E. J., He, J., & Qiao, Y. (2024). _GMAI-MMBench: A Comprehensive Multimodal Evaluation Benchmark Towards General Medical AI_ (No. arXiv:2408.03361). arXiv. [http://arxiv.org/abs/2408.03361](http://arxiv.org/abs/2408.03361)
5. Dada, A., Bauer, M., Contreras, A. B., Koraş, O. A., Seibold, C. M., Smith, K. E., & Kleesiek, J. (2024). _CLUE: A Clinical Language Understanding Evaluation for LLMs_ (No. arXiv:2404.04067). arXiv. [http://arxiv.org/abs/2404.04067](http://arxiv.org/abs/2404.04067)
6. Hendrycks, D., Burns, C., Basart, S., Zou, A., Mazeika, M., Song, D., & Steinhardt, J. (2021). _Measuring Massive Multitask Language Understanding_ (No. arXiv:2009.03300). arXiv. [http://arxiv.org/abs/2009.03300](http://arxiv.org/abs/2009.03300)
7. Hu, Y., Li, T., Lu, Q., Shao, W., He, J., Qiao, Y., & Luo, P. (2024). _OmniMedVQA: A New Large-Scale Comprehensive Evaluation Benchmark for Medical LVLM_. 22170–22183. [https://openaccess.thecvf.com/content/CVPR2024/html/Hu_OmniMedVQA_A_New_Large-Scale_Comprehensive_Evaluation_Benchmark_for_Medical_LVLM_CVPR_2024_paper.html](https://openaccess.thecvf.com/content/CVPR2024/html/Hu_OmniMedVQA_A_New_Large-Scale_Comprehensive_Evaluation_Benchmark_for_Medical_LVLM_CVPR_2024_paper.html)
8. Jin, Q., Dhingra, B., Liu, Z., Cohen, W. W., & Lu, X. (2019). _PubMedQA: A Dataset for Biomedical Research Question Answering_. [https://doi.org/10.48550/ARXIV.1909.06146](https://doi.org/10.48550/ARXIV.1909.06146)
9. Pal, A., Umapathi, L. K., & Sankarasubbu, M. (2022). MedMCQA: A Large-scale Multi-Subject Multi-Choice Dataset for Medical domain Question Answering. _Proceedings of the Conference on Health, Inference, and Learning_, 248–260. [https://proceedings.mlr.press/v174/pal22a.html](https://proceedings.mlr.press/v174/pal22a.html)
10. Qiu, P., Wu, C., Zhang, X., Lin, W., Wang, H., Zhang, Y., Wang, Y., & Xie, W. (2024). Towards building multilingual language model for medicine. _Nature Communications_, _15_(1), 8384. [https://doi.org/10.1038/s41467-024-52417-z](https://doi.org/10.1038/s41467-024-52417-z)
11. Singhal, K., Azizi, S., Tu, T., Mahdavi, S. S., Wei, J., Chung, H. W., Scales, N., Tanwani, A., Cole-Lewis, H., Pfohl, S., Payne, P., Seneviratne, M., Gamble, P., Kelly, C., Babiker, A., Schärli, N., Chowdhery, A., Mansfield, P., Demner-Fushman, D., … Natarajan, V. (2023). Large language models encode clinical knowledge. _Nature_, _620_(7972), 172–180. [https://doi.org/10.1038/s41586-023-06291-2](https://doi.org/10.1038/s41586-023-06291-2)
12. Xie, Y., Wu, J., Tu, H., Yang, S., Zhao, B., Zong, Y., Jin, Q., Xie, C., & Zhou, Y. (2024). _A Preliminary Study of o1 in Medicine: Are We Closer to an AI Doctor?_ (No. arXiv:2409.15277). arXiv. [http://arxiv.org/abs/2409.15277](http://arxiv.org/abs/2409.15277)
13. Jin, D., Pan, E., Oufattole, N., Weng, W.-H., Fang, H., & Szolovits, P. (2020). _What Disease does this Patient Have? A Large-scale Open Domain Question Answering Dataset from Medical Exams_. [https://doi.org/10.48550/ARXIV.2009.13081](https://doi.org/10.48550/ARXIV.2009.13081)




