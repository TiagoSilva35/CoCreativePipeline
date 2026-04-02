FAST_MODE = False
Using data directory: ..\data\ml-100k
Top-level contents: [WindowsPath('../data/ml-100k'), WindowsPath('../data/README.md')]
n_users: 943 n_items: 1682
Train size: 80000 Test size: 20000
Global-mean baseline RMSE: 1.1331379413604736
SGD params: {'d': 81, 'lam_biases': 0.0005274432500432459, 'lam_factors': 0.11381526595226511, 'eta': 0.011638537448331186, 'epochs': 75}
ALS params: {'d': 131, 'lam': 9.71633075356387, 'iters': 15}
Epoch 01 | train RMSE=0.9513 | val RMSE=0.9868
Epoch 02 | train RMSE=0.9186 | val RMSE=0.9672
Epoch 03 | train RMSE=0.9028 | val RMSE=0.9593
Epoch 04 | train RMSE=0.8929 | val RMSE=0.9554
Epoch 05 | train RMSE=0.8859 | val RMSE=0.9527
Epoch 06 | train RMSE=0.8802 | val RMSE=0.9512
Epoch 07 | train RMSE=0.8753 | val RMSE=0.9500
Epoch 08 | train RMSE=0.8704 | val RMSE=0.9493
Epoch 09 | train RMSE=0.8657 | val RMSE=0.9471
Epoch 10 | train RMSE=0.8608 | val RMSE=0.9463
Epoch 11 | train RMSE=0.8556 | val RMSE=0.9453
Epoch 12 | train RMSE=0.8500 | val RMSE=0.9447
Epoch 13 | train RMSE=0.8441 | val RMSE=0.9431
Epoch 14 | train RMSE=0.8379 | val RMSE=0.9414
Epoch 15 | train RMSE=0.8316 | val RMSE=0.9400
Epoch 16 | train RMSE=0.8246 | val RMSE=0.9389
Epoch 17 | train RMSE=0.8179 | val RMSE=0.9377
Epoch 18 | train RMSE=0.8109 | val RMSE=0.9367
Epoch 19 | train RMSE=0.8039 | val RMSE=0.9355
Epoch 20 | train RMSE=0.7968 | val RMSE=0.9341
Epoch 21 | train RMSE=0.7901 | val RMSE=0.9335
Epoch 22 | train RMSE=0.7833 | val RMSE=0.9327
Epoch 23 | train RMSE=0.7765 | val RMSE=0.9316
...
ALS iter 14 | train RMSE=0.6109 | val RMSE=0.9303
ALS iter 15 | train RMSE=0.6109 | val RMSE=0.9304
SGD val RMSE: 0.9246
ALS val RMSE: 0.9296
Output is truncated. View as a scrollable element or open in a text editor. Adjust cell output settings...
Total preference pairs: 37358
delta_F shape: (37358, 5)
Features: [s_MF, b_u, b_i, pop, bias]
Epoch  20 | loss=0.4257 | phi=[0.48559434 0.         0.18734543 0.02416756 0.        ]
Epoch  40 | loss=0.3192 | phi=[0.78976675 0.         0.28358055 0.03537465 0.        ]
Epoch  60 | loss=0.2655 | phi=[1.01103369 0.         0.34059503 0.04117926 0.        ]
Epoch  80 | loss=0.2328 | phi=[1.1863413  0.         0.37707975 0.04424145 0.        ]
Epoch 100 | loss=0.2105 | phi=[1.33245771 0.         0.40119543 0.04569729 0.        ]

Learned weights phi: [1.33245771 0.         0.40119543 0.04569729 0.        ]
Feature names:       [mf_score, user_bias, item_bias, log_pop]
Users with >= 1 relevant test item: 922
Evaluating on 300 users

=== E1: Baseline Comparison ===
              Recall@10  NDCG@10
Popularity       0.0917   0.1768
MF-SGD           0.0453   0.0799
MF-ALS           0.0816   0.1725
Pairwise LTR     0.0457   0.0823
Genre matrix: (1682, 19), non-zero rows: 1682
MMR helpers defined (genre-vector cosine similarity).
alpha | NDCG@10 | Diversity@10
------+---------+-------------
0.0   | 0.0817  | 0.7370
0.1   | 0.0804  | 0.7964
0.4   | 0.0688  | 0.9312
0.7   | 0.0667  | 0.9615
1.0   | 0.0667  | 0.9695
=== Ablation A: Effect of MMR (on Pairwise LTR) ===
                             NDCG@10  Recall@10  Diversity@10
LTR (no MMR)                  0.0823     0.0457        0.7539
LTR + MMR (λ=0.4)             0.0682     0.0375        0.9359

=== Ablation B: Effect of Popularity Feature ===
                          NDCG@10  Recall@10
LTR (full, 5 features)     0.0823     0.0457
LTR (no pop, 4 features)   0.0785     0.0441

Full phi (5 feats):   [1.33245771 0.         0.40119543 0.04569729 0.        ]
No-pop phi (4 feats): [1.33362896 0.         0.4025163  0.        ]  (s_MF, b_u, b_i, bias)
Loaded 1682 item titles
Selected users for sessions:
  [active  ] user  449  — 95 relevant test items
  [median  ] user  387  — 8 relevant test items
  [marginal] user  432  — 2 relevant test items

============================================================
Session: active user (u=449, 95 relevant items)
============================================================
Turn 1: picked [602] Rear Window (1954)  (5/5)
         NDCG@10=0.2588  Recall@10=0.0316  Diversity@10=0.9208
Turn 2: picked [317] Schindler's List (1993)  (5/5)
         NDCG@10=0.2985  Recall@10=0.0211  Diversity@10=0.8526
Turn 3: picked [184] Psycho (1960)  (5/5)
         NDCG@10=0.1428  Recall@10=0.0211  Diversity@10=0.8165
Turn 4: picked [190] Amadeus (1984)  (5/5)
         NDCG@10=0.1396  Recall@10=0.0211  Diversity@10=0.7085
Turn 5: picked [196] Graduate, The (1967)  (5/5)
         NDCG@10=0.2934  Recall@10=0.0316  Diversity@10=0.8640

============================================================
Session: median user (u=387, 8 relevant items)
============================================================
Turn 1: picked [482] Casablanca (1942)  (not in test)
         NDCG@10=0.0000  Recall@10=0.0000  Diversity@10=0.9320
Turn 2: picked [312] Titanic (1997)  (5/5)
         NDCG@10=0.0761  Recall@10=0.1250  Diversity@10=0.8984
Turn 3: picked [511] Wings of Desire (1987)  (not in test)
         NDCG@10=0.0000  Recall@10=0.0000  Diversity@10=0.7412
Turn 4: picked [189] Henry V (1989)  (not in test)
         NDCG@10=0.0000  Recall@10=0.0000  Diversity@10=0.8057
Turn 5: picked [315] As Good As It Gets (1997)  (not in test)
         NDCG@10=0.0000  Recall@10=0.0000  Diversity@10=0.8743

============================================================
Session: marginal user (u=432, 2 relevant items)
============================================================
Turn 1: picked [11] Usual Suspects, The (1995)  (5/5)
         NDCG@10=0.1934  Recall@10=0.5000  Diversity@10=0.8940
Turn 2: picked [512] Third Man, The (1949)  (not in test)
         NDCG@10=0.0000  Recall@10=0.0000  Diversity@10=0.9464
Turn 3: picked [497] African Queen, The (1951)  (not in test)
         NDCG@10=0.0000  Recall@10=0.0000  Diversity@10=0.8041
Turn 4: picked [612] My Man Godfrey (1936)  (not in test)
         NDCG@10=0.0000  Recall@10=0.0000  Diversity@10=0.7697
Turn 5: picked [658] Arsenic and Old Lace (1944)  (not in test)
         NDCG@10=0.0000  Recall@10=0.0000  Diversity@10=0.8114

JSONL log written to: session_log.jsonl (5783 bytes)    