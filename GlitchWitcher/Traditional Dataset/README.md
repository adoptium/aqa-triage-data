# Traditional Dataset

This folder contains resources for extracting traditional software metrics from C/C++ files in a GitHub repository, as described in [aqa-test-tools issue #1076](https://github.com/adoptium/aqa-test-tools/issues/1076).

## Contents

- **ExtractTraditionalFeatures.sh**: A general-purpose shell script to extract traditional features (Halstead, McCabe, line counts, etc.) from all C/C++ files in any input repository.
- **OpenJ9_Traditional_Dataset.csv**: Cleaned dataset generated for the [OpenJ9](https://github.com/eclipse-openj9/openj9) repository, containing metrics for all C/C++ files.

## Dataset Details

- Only C/C++ files from the repository are included.
- The dataset has 2764 entries (files), of which 749 are labeled as defective (~27%), and the rest are non-defective.
- The dataset is cleaned and ready for analysis.

## Usage

To extract traditional features for C/C++ files from any repository:

```bash
./ExtractTraditionalFeatures.sh <github_repo_url>
```

This will generate a summary CSV file with metrics for each C/C++ file in the specified repository.

## Notes

- The script is general and can be used for any GitHub repository containing C/C++ code.
- The metrics include Halstead and McCabe complexity measures, line counts, and defect labels based on commit history.
