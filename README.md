Datasets
---------
Datasets currently used in this repo is the Human brain pharmacome and a modified version of it with causal-only relations.


Data Availability
------------------
The data in this repository were collected from open source databases, thereby there is no restriction on its reusal to reproduce the results

Repository Structure
---------------------
The repo contains a main folder ([SynDRep_results](/SynDRep_results)) containing 2 Datasets (pharmacomes) that were used for drug repurposing using
 [SynDRep](https://github.com/SynDRep/SynDRep) framework for each dataset.

The data and results for each pharmacome are available in their respective folders, within each dataset's folder,

1) [Causal-only pharmacome](SynDRep_results/Causal_only_pharmacome) - Experiments run on causal only pharmacome using [embedding only](SynDRep_results/Causal_only_pharmacome/EM_only) or [embedding then ML](SynDRep_results/Causal_only_pharmacome/EM_then_ML).
2) [Human Brain Pharmacome](SynDRep_results/Human_Brain_Pharmacome) - Experiments run on original Human Brain Pharmacome using [embedding only](SynDRep_results/Human_Brain_Pharmacome/Embedding) or [ ML only](SynDRep_results/Human_Brain_Pharmacome/ML) using graph topology and phaysicochemical properities of drugs.

Each experiment folder contains the data and results of experiment.

The tree structure looks like as given below,
```
SynDRep_results
├── Causal_only_pharmacome
│  ├── EM_only
│  │  ├── Data_EM
│  │  │  ├── CSV
│  │  │  │  ├── drug_combos_not_ph.csv
│  │  │  │  ├── drug_combos_ph.csv
│  │  │  │  ├── drugs.csv
│  │  │  │  ├── final_combos.csv
│  │  │  │  └── has_combination_with_CYPHER.csv
│  │  │  ├── JSON
│  │  │  │  └── cid_name_dict.json
│  │  │  ├── TSV
│  │  │  │  ├── new_training_splits
│  │  │  │  │  ├── test_data_ns.tsv
│  │  │  │  │  ├── train_data_ns.tsv
│  │  │  │  │  └── validation_data_ns.tsv
│  │  │  │  ├── pharmacome_detailed.tsv
│  │  │  │  ├── pharmacome_detailed_names.tsv
│  │  │  │  ├── test_data.tsv
│  │  │  │  ├── testval_all.tsv
│  │  │  │  ├── testval_d.tsv
│  │  │  │  ├── testval_d_p.tsv
│  │  │  │  ├── train_data.tsv
│  │  │  │  └── validation_data.tsv
│  │  │  └── TXT
│  │  │     ├── final_results.txt
│  │  │     └── results.txt
│  │  └── Embedding_EM
│  │     ├── CompGCN
│  │     │  ├── CompGCN_hpo_results
│  │     │  │  ├── best_pipeline
│  │     │  │  │  └── pipeline_config.json
│  │     │  │  ├── study.json
│  │     │  │  └── trials.tsv
│  │     │  ├── CompGCN_model_results
│  │     │  │  ├── training_triples
│  │     │  │  │  ├── base.pth
│  │     │  │  │  ├── entity_to_id.tsv.gz
│  │     │  │  │  ├── numeric_triples.tsv.gz
│  │     │  │  │  └── relation_to_id.tsv.gz
│  │     │  │  ├── metadata.json
│  │     │  │  ├── results.json
│  │     │  │  └── trained_model.pkl
│  │     │  ├── CompGCN_config_hpo.json
│  │     │  └── CompGCN_config_model.json
│  │     ├── ComplEx
│  │     │  ├── ComplEx_hpo_results
│  │     │  │  ├── best_pipeline
│  │     │  │  │  └── pipeline_config.json
│  │     │  │  ├── study.json
│  │     │  │  └── trials.tsv
│  │     │  ├── ComplEx_model_results
│  │     │  │  ├── training_triples
│  │     │  │  │  ├── base.pth
│  │     │  │  │  ├── entity_to_id.tsv.gz
│  │     │  │  │  ├── numeric_triples.tsv.gz
│  │     │  │  │  └── relation_to_id.tsv.gz
│  │     │  │  ├── metadata.json
│  │     │  │  ├── results.json
│  │     │  │  └── trained_model.pkl
│  │     │  ├── ComplEx_config_hpo.json
│  │     │  └── ComplEx_config_model.json
│  │     ├── HolE
│  │     │  ├── HolE_hpo_results
│  │     │  │  ├── best_pipeline
│  │     │  │  │  └── pipeline_config.json
│  │     │  │  ├── study.json
│  │     │  │  └── trials.tsv
│  │     │  ├── HolE_model_results
│  │     │  │  ├── training_triples
│  │     │  │  │  ├── base.pth
│  │     │  │  │  ├── entity_to_id.tsv.gz
│  │     │  │  │  ├── numeric_triples.tsv.gz
│  │     │  │  │  └── relation_to_id.tsv.gz
│  │     │  │  ├── metadata.json
│  │     │  │  ├── results.json
│  │     │  │  └── trained_model.pkl
│  │     │  ├── HolE_config_hpo.json
│  │     │  └── HolE_config_model.json
│  │     ├── RotatE
│  │     │  ├── RotatE_hpo_results
│  │     │  │  ├── best_pipeline
│  │     │  │  │  └── pipeline_config.json
│  │     │  │  ├── study.json
│  │     │  │  └── trials.tsv
│  │     │  ├── RotatE_model_results
│  │     │  │  ├── training_triples
│  │     │  │  │  ├── base.pth
│  │     │  │  │  ├── entity_to_id.tsv.gz
│  │     │  │  │  ├── numeric_triples.tsv.gz
│  │     │  │  │  └── relation_to_id.tsv.gz
│  │     │  │  ├── metadata.json
│  │     │  │  ├── results.json
│  │     │  │  └── trained_model.pkl
│  │     │  ├── RotatE_config_hpo.json
│  │     │  └── RotatE_config_model.json
│  │     ├── TransE
│  │     │  ├── TransE_hpo_results
│  │     │  │  ├── best_pipeline
│  │     │  │  │  └── pipeline_config.json
│  │     │  │  ├── study.json
│  │     │  │  └── trials.tsv
│  │     │  ├── TransE_model_results
│  │     │  │  ├── training_triples
│  │     │  │  │  ├── base.pth
│  │     │  │  │  ├── entity_to_id.tsv.gz
│  │     │  │  │  ├── numeric_triples.tsv.gz
│  │     │  │  │  └── relation_to_id.tsv.gz
│  │     │  │  ├── metadata.json
│  │     │  │  ├── results.json
│  │     │  │  └── trained_model.pkl
│  │     │  ├── TransE_config_hpo.json
│  │     │  └── TransE_config_model.json
│  │     ├── TransR
│  │     │  ├── TransR_hpo_results
│  │     │  │  ├── best_pipeline
│  │     │  │  │  └── pipeline_config.json
│  │     │  │  ├── study.json
│  │     │  │  └── trials.tsv
│  │     │  ├── TransR_model_results
│  │     │  │  ├── training_triples
│  │     │  │  │  ├── base.pth
│  │     │  │  │  ├── entity_to_id.tsv.gz
│  │     │  │  │  ├── numeric_triples.tsv.gz
│  │     │  │  │  └── relation_to_id.tsv.gz
│  │     │  │  ├── metadata.json
│  │     │  │  ├── results.json
│  │     │  │  └── trained_model.pkl
│  │     │  ├── TransR_config_hpo.json
│  │     │  └── TransR_config_model.json
│  │     ├── Model_summary_EM.csv
│  │     ├── ROC-AUC for Different Models.png
│  │     ├── percent_true_all_relations.png
│  │     └── percent_true_drug_drug.png
│  └── EM_then_ML
│     ├── Data_EMML
│     │  ├── CSV
│     │  │  ├── drug_combos_not_ph.csv
│     │  │  ├── drug_combos_ph.csv
│     │  │  ├── drugs.csv
│     │  │  └── final_combos.csv
│     │  ├── JSON
│     │  │  └── cid_name_dict.json
│     │  ├── TSV
│     │  │  ├── new_training_splits
│     │  │  │  ├── test_data_ns.tsv
│     │  │  │  ├── train_data_ns.tsv
│     │  │  │  └── validation_data_ns.tsv
│     │  │  ├── pharmacome_detailed.tsv
│     │  │  ├── pharmacome_detailed_names.tsv
│     │  │  ├── test_data.tsv
│     │  │  ├── testval_all.tsv
│     │  │  ├── testval_d.tsv
│     │  │  ├── testval_d_p.tsv
│     │  │  ├── train_data.tsv
│     │  │  └── validation_data.tsv
│     │  └── TXT
│     │     └── results.txt
│     ├── Embedding_EMML
│     │  ├── CompGCN
│     │  │  ├── CompGCN_hpo_results
│     │  │  │  ├── best_pipeline
│     │  │  │  │  └── pipeline_config.json
│     │  │  │  ├── study.json
│     │  │  │  └── trials.tsv
│     │  │  ├── CompGCN_model_results
│     │  │  │  ├── training_triples
│     │  │  │  │  ├── base.pth
│     │  │  │  │  ├── entity_to_id.tsv.gz
│     │  │  │  │  ├── numeric_triples.tsv.gz
│     │  │  │  │  └── relation_to_id.tsv.gz
│     │  │  │  ├── metadata.json
│     │  │  │  ├── results.json
│     │  │  │  └── trained_model.pkl
│     │  │  ├── CompGCN_config_hpo.json
│     │  │  └── CompGCN_config_model.json
│     │  ├── ComplEx
│     │  │  ├── ComplEx_hpo_results
│     │  │  │  ├── best_pipeline
│     │  │  │  │  └── pipeline_config.json
│     │  │  │  ├── study.json
│     │  │  │  └── trials.tsv
│     │  │  ├── ComplEx_model_results
│     │  │  │  ├── training_triples
│     │  │  │  │  ├── base.pth
│     │  │  │  │  ├── entity_to_id.tsv.gz
│     │  │  │  │  ├── numeric_triples.tsv.gz
│     │  │  │  │  └── relation_to_id.tsv.gz
│     │  │  │  ├── metadata.json
│     │  │  │  ├── results.json
│     │  │  │  └── trained_model.pkl
│     │  │  ├── ComplEx_config_hpo.json
│     │  │  └── ComplEx_config_model.json
│     │  ├── HolE
│     │  │  ├── HolE_hpo_results
│     │  │  │  ├── best_pipeline
│     │  │  │  │  └── pipeline_config.json
│     │  │  │  ├── study.json
│     │  │  │  └── trials.tsv
│     │  │  ├── HolE_model_results
│     │  │  │  ├── training_triples
│     │  │  │  │  ├── base.pth
│     │  │  │  │  ├── entity_to_id.tsv.gz
│     │  │  │  │  ├── numeric_triples.tsv.gz
│     │  │  │  │  └── relation_to_id.tsv.gz
│     │  │  │  ├── metadata.json
│     │  │  │  ├── results.json
│     │  │  │  └── trained_model.pkl
│     │  │  ├── HolE_Embeddings_all.csv
│     │  │  ├── HolE_Embeddings_drugs.csv
│     │  │  ├── HolE_config_hpo.json
│     │  │  └── HolE_config_model.json
│     │  ├── RotatE
│     │  │  ├── RotatE_hpo_results
│     │  │  │  ├── best_pipeline
│     │  │  │  │  └── pipeline_config.json
│     │  │  │  ├── study.json
│     │  │  │  └── trials.tsv
│     │  │  ├── RotatE_model_results
│     │  │  │  ├── training_triples
│     │  │  │  │  ├── base.pth
│     │  │  │  │  ├── entity_to_id.tsv.gz
│     │  │  │  │  ├── numeric_triples.tsv.gz
│     │  │  │  │  └── relation_to_id.tsv.gz
│     │  │  │  ├── metadata.json
│     │  │  │  ├── results.json
│     │  │  │  └── trained_model.pkl
│     │  │  ├── RotatE_config_hpo.json
│     │  │  └── RotatE_config_model.json
│     │  ├── TransE
│     │  │  ├── TransE_hpo_results
│     │  │  │  ├── best_pipeline
│     │  │  │  │  └── pipeline_config.json
│     │  │  │  ├── study.json
│     │  │  │  └── trials.tsv
│     │  │  ├── TransE_model_results
│     │  │  │  ├── training_triples
│     │  │  │  │  ├── base.pth
│     │  │  │  │  ├── entity_to_id.tsv.gz
│     │  │  │  │  ├── numeric_triples.tsv.gz
│     │  │  │  │  └── relation_to_id.tsv.gz
│     │  │  │  ├── metadata.json
│     │  │  │  ├── results.json
│     │  │  │  └── trained_model.pkl
│     │  │  ├── TransE_config_hpo.json
│     │  │  └── TransE_config_model.json
│     │  ├── TransR
│     │  │  ├── TransR_hpo_results
│     │  │  │  ├── best_pipeline
│     │  │  │  │  └── pipeline_config.json
│     │  │  │  ├── study.json
│     │  │  │  └── trials.tsv
│     │  │  ├── TransR_model_results
│     │  │  │  ├── training_triples
│     │  │  │  │  ├── base.pth
│     │  │  │  │  ├── entity_to_id.tsv.gz
│     │  │  │  │  ├── numeric_triples.tsv.gz
│     │  │  │  │  └── relation_to_id.tsv.gz
│     │  │  │  ├── metadata.json
│     │  │  │  ├── results.json
│     │  │  │  └── trained_model.pkl
│     │  │  ├── TransR_config_hpo.json
│     │  │  └── TransR_config_model.json
│     │  ├── Model_summary_EMML.csv
│     │  ├── ROC-AUC for Different Models.png
│     │  └── percent_true_all_relations.png
│     └── ML_EMML
│        ├── elastic_net
│        │  └── cross_validation_results.json
│        ├── gradient_boost
│        │  └── cross_validation_results.json
│        ├── logistic_regression
│        │  └── cross_validation_results.json
│        ├── pathway_check
│        │  ├── pharmacome_detailed.tsv
│        │  └── pharmacome_detailed_names.tsv
│        ├── random_forest
│        │  └── cross_validation_results.json
│        ├── svm
│        │  └── cross_validation_results.json
│        ├── ROC-AUC.png
│        ├── antagonism_pred_EMML.csv
│        ├── synergy_pred_EMML.csv
│        └── train_test_data.csv
└── Human_Brain_Pharmacome
   ├── Embedding
   │  ├── CompGCN
   │  │  ├── CompGCN_hpo_results
   │  │  │  ├── best_pipeline
   │  │  │  │  └── pipeline_config.json
   │  │  │  ├── study.json
   │  │  │  └── trials.tsv
   │  │  ├── CompGCN_config_hpo.json
   │  │  └── CompGCN_config_model.json
   │  ├── ComplEx
   │  │  ├── ComplEx_hpo_results
   │  │  │  ├── best_pipeline
   │  │  │  │  └── pipeline_config.json
   │  │  │  ├── study.json
   │  │  │  └── trials.tsv
   │  │  ├── ComplEx_model_results
   │  │  │  ├── training_triples
   │  │  │  │  ├── base.pth
   │  │  │  │  ├── entity_to_id.tsv.gz
   │  │  │  │  ├── numeric_triples.tsv.gz
   │  │  │  │  └── relation_to_id.tsv.gz
   │  │  │  ├── metadata.json
   │  │  │  ├── results.json
   │  │  │  └── trained_model.pkl
   │  │  ├── ComplEx_config_hpo.json
   │  │  └── ComplEx_config_model.json
   │  ├── Data
   │  │  ├── CSV
   │  │  │  ├── drug_combos_not_ph.csv
   │  │  │  ├── drug_combos_ph.csv
   │  │  │  ├── drugs.csv
   │  │  │  ├── final_combos.csv
   │  │  │  └── has_combination_with_CYPHER.csv
   │  │  ├── JSON
   │  │  │  └── cid_name_dict.json
   │  │  ├── TSV
   │  │  │  ├── new_training_splits
   │  │  │  │  ├── test_data_ns.tsv
   │  │  │  │  ├── train_data_ns.tsv
   │  │  │  │  └── validation_data_ns.tsv
   │  │  │  ├── pharmacome.tsv
   │  │  │  ├── pharmacome_names.tsv
   │  │  │  ├── test_data.tsv
   │  │  │  ├── testval_all.tsv
   │  │  │  ├── testval_d.tsv
   │  │  │  ├── testval_d_p.tsv
   │  │  │  ├── train_data.tsv
   │  │  │  └── validation_data.tsv
   │  │  └── TXT
   │  │     ├── final_results.txt
   │  │     └── results.txt
   │  ├── HolE
   │  │  ├── HolE_hpo_results
   │  │  │  ├── best_pipeline
   │  │  │  │  └── pipeline_config.json
   │  │  │  ├── study.json
   │  │  │  └── trials.tsv
   │  │  ├── HolE_model_results
   │  │  │  ├── training_triples
   │  │  │  │  ├── base.pth
   │  │  │  │  ├── entity_to_id.tsv.gz
   │  │  │  │  ├── numeric_triples.tsv.gz
   │  │  │  │  └── relation_to_id.tsv.gz
   │  │  │  ├── metadata.json
   │  │  │  ├── results.json
   │  │  │  └── trained_model.pkl
   │  │  ├── HolE_config_hpo.json
   │  │  └── HolE_config_model.json
   │  ├── RotatE
   │  │  ├── RotatE_hpo_results
   │  │  │  ├── best_pipeline
   │  │  │  │  └── pipeline_config.json
   │  │  │  ├── study.json
   │  │  │  └── trials.tsv
   │  │  ├── RotatE_model_results
   │  │  │  ├── training_triples
   │  │  │  │  ├── base.pth
   │  │  │  │  ├── entity_to_id.tsv.gz
   │  │  │  │  ├── numeric_triples.tsv.gz
   │  │  │  │  └── relation_to_id.tsv.gz
   │  │  │  ├── metadata.json
   │  │  │  ├── results.json
   │  │  │  └── trained_model.pkl
   │  │  ├── RotatE_config_hpo.json
   │  │  ├── RotatE_config_model.json
   │  │  ├── antagonism_pred.csv
   │  │  └── synergy_pred.csv
   │  ├── TransE
   │  │  ├── TransE_hpo_results
   │  │  │  ├── best_pipeline
   │  │  │  │  └── pipeline_config.json
   │  │  │  ├── study.json
   │  │  │  └── trials.tsv
   │  │  ├── TransE_model_results
   │  │  │  ├── training_triples
   │  │  │  │  ├── base.pth
   │  │  │  │  ├── entity_to_id.tsv.gz
   │  │  │  │  ├── numeric_triples.tsv.gz
   │  │  │  │  └── relation_to_id.tsv.gz
   │  │  │  ├── metadata.json
   │  │  │  ├── results.json
   │  │  │  └── trained_model.pkl
   │  │  ├── TransE_config_hpo.json
   │  │  └── TransE_config_model.json
   │  ├── TransR
   │  │  ├── TransR_hpo_results
   │  │  │  ├── best_pipeline
   │  │  │  │  └── pipeline_config.json
   │  │  │  ├── study.json
   │  │  │  └── trials.tsv
   │  │  ├── TransR_model_results
   │  │  │  ├── training_triples
   │  │  │  │  ├── base.pth
   │  │  │  │  ├── entity_to_id.tsv.gz
   │  │  │  │  ├── numeric_triples.tsv.gz
   │  │  │  │  └── relation_to_id.tsv.gz
   │  │  │  ├── metadata.json
   │  │  │  ├── results.json
   │  │  │  └── trained_model.pkl
   │  │  ├── TransR_config_hpo.json
   │  │  └── TransR_config_model.json
   │  ├── Model_summary.csv
   │  ├── ROC-AUC for Different Models.png
   │  ├── percent_true_all_relations.png
   │  └── percent_true_drug_drug.png
   └── ML
      ├── elastic_net
      │  └── cross_validation_results.json
      ├── gradient_boost
      │  └── cross_validation_results.json
      ├── logistic_regression
      │  └── cross_validation_results.json
      ├── random_forest
      │  └── cross_validation_results.json
      ├── Antagonism_pred_ML.csv
      ├── ROC-AUC.png
      ├── cid_name_dict.json
      ├── cid_properties_dic.json
      ├── final_dataset_detailed.csv
      └── synergy_pred_ML.csv

```

