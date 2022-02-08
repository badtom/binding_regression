# binding_regression
In the 'data' folder, files ligand_activities.pckl and ligand_activity_deltas.pckl
are pickled sparse matrices of type csr_matrix from scipy.sparse.
The value in the *i*th row and *j*th column of the matrix from ligand_activity_deltas.pckl
is equal to *delta = pActivity - threshold* for the *i*th ligand and *j*th target,
while such value for the matrix in ligand_activities.pckl is *1* if *delta >= 0*
and *-1* if *delta < 0*. The file ligand_smiles.txt contains ligand smileses
corresponding to the consecutive rows of the above matrices and 
target_chembl_ids.txt contains ChEMBL ids for targets in columns of these matrices. 

The folder 'data/train_valid_test_splits' contains information about 
the training-validation-test splits used. In each of its subfolders, 
target_indices.pckl is a pickled numpy array containing column indices of the above 
sparse matrices corresponding to targets used in a given split, while 
train_ligand_indices.pckl, valid_ligand_indices.pckl, and test_ligand_indices.pckl 
are pickled numpy arrays with row indices of the above matrices corresponding to ligands used in the train, 
validation, and test set of the split respectively.


