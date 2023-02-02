To preprocessed raw text resumes,

First, change the path to the output_dir in the file preprocessor.py (edit the property output_dir of the class Preprocessor)

Then run the command :

python process_data.py

This operation creates subdatasets corresponding to the resume length in the directory <output_dir>

The operation creates two additional files :

resumes_refs.py : which associates a sample data id to the path of the original resume.
resumes_words.py : which represents a dictionary where keys are hashed words'vectors and values are corresponding words
The resulting dataset is in form of a matrix :

The first column of the matrix is an integer representing the id of the resume.

The last 10 columns represent the classes of the resumes.

The columns between the id and the classes represent the flatten form of a resume matrix.

By default, each resume is encoded into a matrix of shape (500,100).