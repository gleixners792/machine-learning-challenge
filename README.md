##### Exoplanet Data Exploration
# 1)	Step One – Review Decision Tree and Random Forests
    a.	Decision Tree – Test Data - .85
    b.	Random Forest – Test Data - .90
    c.	Random Forest Importance & Features
*         (0.10925409228010884, 'koi_fpflag_co'),
*         (0.09563983042304605, 'koi_fpflag_nt'),
*         (0.0627642855318202, 'koi_fpflag_ss'),
*         (0.054822302245283644, 'koi_model_snr'),
*         (0.05204955946403267, 'koi_prad'),
*         (0.03700767695984468, 'koi_duration_err2'),
*         (0.03474923795144018, 'koi_prad_err2'),
*         (0.03273943975175016, 'koi_duration_err1'),
*         (0.03240966826442024, 'koi_steff_err1'),
*         (0.032094174521212826, 'koi_fpflag_ec'),
*         (0.030870703723820666, 'koi_prad_err1'),
*         (0.029724543410898373, 'koi_steff_err2'),
*         (0.02510227210186771, 'koi_time0bk_err2'),
*         (0.024148245731406413, 'koi_period'),
*         (0.023364726850349467, 'koi_time0bk_err1'),
*         (0.02216941580663501, 'koi_duration'),
*         (0.01946287485876426, 'koi_period_err1'),
*         (0.01890297293718455, 'koi_depth'),
*         (0.018583144675960204, 'koi_period_err2'),
*         (0.01758239795636518, 'koi_impact'),
*         (0.017087678514593908, 'koi_insol_err1'),
*         (0.016554755011250158, 'koi_insol'),
*         (0.015236790830303569, 'koi_teq'),
*         (0.013838475751767101, 'koi_insol_err2'),
*         (0.013833323375844553, 'koi_time0bk'),
*         (0.012984527227393974, 'koi_depth_err1'),
*         (0.012561465885304551, 'koi_depth_err2'),
*         (0.011957766195865664, 'ra'),
*         (0.011339320335258923, 'dec'),
*         (0.010943071870493341, 'koi_impact_err1'),
*         (0.010906692214365982, 'koi_impact_err2'),
*         (0.010860169079407643, 'koi_slogg_err2'),
*         (0.010527118078551567, 'koi_kepmag'),
*         (0.010444805524439642, 'koi_srad_err1'),
*         (0.009888621143480276, 'koi_steff'),
*         (0.009258156407369107, 'koi_srad'),
*         (0.008762724834036803, 'koi_slogg_err1'),
*         (0.008755679039085182, 'koi_slogg'),
*         (0.008176101663705115, 'koi_srad_err2'),
*         (0.00264119157127161, 'koi_tce_plnt_num')



# 2)	K Nearest Neighbors (KNN)
    a.	5 features – Test Accuracy - .79
    b.	25 features – Test Accuracy - .79
    c.	More features – Test Accuracy – Really Bad
    
# 3)	Support Vector Machine (SVN)
    a.	5 features – Test Accuracy – .77
    b.	25 features – Test Accuracy – .84
    c.	34 features – Test Accuracy - .83
    
# 4)	Grid Search & Hyper Tuning
    a.	5 features–Test Accuracy- .71 (best parameters{'C': 4.68, 'gamma': 1e-06})
    b.	16 features–Test Accuracy- .87 (best parameters{'C': 18.0, 'gamma': 1e-06})
    c.	25 features–Test Accuracy- .88 (best parameters{'C': 17.1, 'gamma': 1e-06})
    d.	34 features–Test Accuracy- .89 (best parameters{C': 450, 'gamma': 1e-07})

# Summary

It is very import to scale your data for the math intensive functions. I ran a Grid Search on five parameters on un-scaled data, it took twenty hours to run. The grid search method appears to be the most particle and reliable test method for this set of data. It was nice to have Random Forest output to help focus on which features were the most likely to positively impact the model. If I had more time, I would continue to model different features to eliminate the features that had little or no impact to the model or other features.







