# Digital Image Processing Summary for License Plate Recognition and Vehicle Counting

A report on two applications of digital image processing in transportation:
license plate recognition and vehicle counting. It discusses the processing
stages, relevant image features, reported results, and limitations of each
application.

The report is written in LaTeX using the IEEE conference format.

## Overview

The report focuses on how image features are selected according to the
information required by each task:

| Aspect | License Plate Recognition | Vehicle Counting |
| --- | --- | --- |
| Input | Vehicle image | Road video frames |
| Main object | License plate and its characters | Vehicle regions |
| Relevant features | Edge density and connected character regions | Foreground regions, contours, position, and size |
| Output | Recognized plate characters | Number of vehicles |

### License Plate Recognition

The main case study discusses a framework by Arafat et al. that uses
edge-based detection and connected component analysis.

The processing flow is:

```text
Vehicle image
    → Preprocessing
    → Edge detection and energy mapping
    → Plate localization
    → Character segmentation
    → Character recognition
    → Recognized plate text
```

Vertical and horizontal edge information helps identify candidate plate
regions. After localization, connected component analysis helps separate
character candidates, which are then compared with stored templates.

### Vehicle Counting

The main case study discusses a video-based system by Liu et al. that adapts
its counting method to traffic conditions.

The processing flow is:

```text
Road video
    → Background subtraction
    → Vehicle segmentation
    → Contour extraction
    → Virtual detection line or area
    → Vehicle count
```

The system uses foreground regions and contours to represent vehicles. It
considers their position or occupancy within a virtual detection area to
update the count.

## Report Structure

1. **Introduction**: The problems and objectives of both applications.
2. **Background**: Image features and relevant processing techniques.
3. **Case Studies**: Methods, features, reported results, and limitations.
4. **Comparison and Discussion**: Differences between the two applications.
5. **Conclusion**: The relationship between feature selection and task needs.
6. **References**: Five international journal articles.

## Repository Contents

| File | Description |
| --- | --- |
| `PCD_Assignment4 \|.tex` | LaTeX source of the report |
| `PCD_Assignment4 \|.pdf` | Compiled report |
| `fig1.png` | Image file included in the repository |
| `README.md` | Project overview and instructions |

The repository also contains auxiliary files produced during LaTeX
compilation, such as `.aux` and `.log` files.

## Build the Report

### Requirements

- A LaTeX distribution, such as MacTeX, TeX Live, or MiKTeX.
- The `IEEEtran`, `cite`, and `url` LaTeX packages.
- `pdflatex` available from your terminal.

### Compile

Run the following command from the repository directory:

```bash
pdflatex 'PCD_Assignment4 |.tex'
pdflatex 'PCD_Assignment4 |.tex'
```

Running the command twice allows LaTeX to resolve references and citations.
The output is saved as `PCD_Assignment4 |.pdf`.

## References

The report draws on the following articles:

1. M. Y. Arafat, A. S. M. Khairuddin, and R. Paramesran, “Connected component
   analysis integrated edge based technique for automatic vehicular license
   plate recognition framework,” *IET Intelligent Transport Systems*, 2020.
   [DOI](https://doi.org/10.1049/iet-its.2019.0006)
2. F. Liu, Z. Zeng, and R. Jiang, “A video-based real-time adaptive
   vehicle-counting system for urban roads,” *PLOS ONE*, 2017.
   [DOI](https://doi.org/10.1371/journal.pone.0186098)
3. J. Yepez and S.-B. Ko, “Improved license plate localisation algorithm based
   on morphological operations,” *IET Intelligent Transport Systems*, 2018.
   [DOI](https://doi.org/10.1049/iet-its.2017.0224)
4. J. Kim, “Automatic vehicle license plate extraction using region-based
   convolutional neural networks and morphological operations,” *Symmetry*,
   2019. [DOI](https://doi.org/10.3390/sym11070882)
5. L. Rosas-Arias et al., “Vehicle counting in video sequences: An incremental
   subspace learning approach,” *Sensors*, 2019.
   [DOI](https://doi.org/10.3390/s19132848)

## Author

**Muhammad Fathan Romiza**  
Digital Image Processing Course  
Gadjah Mada University