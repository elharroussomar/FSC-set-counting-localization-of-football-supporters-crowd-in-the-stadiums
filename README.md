
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FSC-Set Dataset Documentation</title>
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom font import for a clean look */
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap');
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8fafc; /* Tailwind slate-50 */
        }
        .code-block {
            background-color: #0f172a; /* Tailwind slate-900 */
            color: #f1f5f9; /* Tailwind slate-100 */
            padding: 1rem;
            border-radius: 0.5rem;
            overflow-x: auto;
            font-family: monospace;
        }
    </style>
</head>
<body class="p-4 sm:p-8">
    <div class="max-w-4xl mx-auto bg-white shadow-xl rounded-xl p-6 md:p-10 border border-slate-200">

        <!-- Header and Title -->
        <header class="mb-8 border-b pb-4">
            <h1 class="text-4xl sm:text-5xl font-extrabold text-slate-900 leading-tight">
                FSC-set-counting-localization-of-football-supporters-crowd-in-the-stadiums
            </h1>
            <p class="mt-4 text-lg text-slate-700">
                This repository contains the datasets of football supporters crowd in the stadium for the paper:
            </p>
            <p class="text-xl font-semibold text-indigo-700 mt-2">
                "Refined Edge Detection With Cascaded and High-Resolution Convolutional Network"
            </p>
            <p class="text-sm text-slate-500 mt-1">
                Based on the code in <a href="https://github.com/zhuoinoulu/pidinet" class="text-indigo-500 hover:text-indigo-600 underline" target="_blank">https://github.com/zhuoinoulu/pidinet</a>
            </p>
        </header>

        <!-- Image -->
        <div class="my-8 flex justify-center">
            <img src="https://github.com/elharroussomar/chrnet/blob/main/Model.jpg" alt="CH-RNet Model Architecture Diagram" class="w-full max-w-xl h-auto rounded-lg shadow-lg border border-slate-200" loading="lazy">
        </div>

        <!-- Section 1: Dataset Overview -->
        <section class="mt-10">
            <h2 class="text-3xl font-bold text-slate-800 border-b-2 border-indigo-400 pb-2 mb-6">
                📝 Dataset Overview
            </h2>
            <p class="text-slate-700 leading-relaxed">
                The <strong>FSC-Set (Football Supporters Crowd Dataset)</strong> is a large-scale collection of images designed for <strong>crowd counting</strong> and <strong>individual localization</strong> in highly dense stadium environments. The annotations provide precise ground truth data for developing and evaluating advanced computer vision models, particularly those involved in edge detection and high-resolution feature analysis. This dataset is a resource for projects related to the cited code repository.
            </p>
        </section>

        <!-- Section 2: Dataset Statistics -->
        <section class="mt-10">
            <h2 class="text-3xl font-bold text-slate-800 border-b-2 border-indigo-400 pb-2 mb-6">
                📊 Dataset Statistics
            </h2>
            <div class="overflow-x-auto rounded-lg shadow-md">
                <table class="min-w-full divide-y divide-slate-300">
                    <thead class="bg-indigo-500 text-white">
                        <tr>
                            <th scope="col" class="py-3.5 pl-4 pr-3 text-left text-sm font-semibold sm:pl-6">Feature</th>
                            <th scope="col" class="px-3 py-3.5 text-left text-sm font-semibold">Value</th>
                        </tr>
                    </thead>
                    <tbody class="divide-y divide-slate-200 bg-white">
                        <tr class="hover:bg-indigo-50/50">
                            <td class="whitespace-nowrap py-4 pl-4 pr-3 text-sm font-medium text-slate-900 sm:pl-6">Total Number of Images</td>
                            <td class="whitespace-nowrap px-3 py-4 text-sm text-slate-600 font-semibold">6,000</td>
                        </tr>
                        <tr class="hover:bg-indigo-50/50">
                            <td class="whitespace-nowrap py-4 pl-4 pr-3 text-sm font-medium text-slate-900 sm:pl-6">Total Annotated Individuals</td>
                            <td class="whitespace-nowrap px-3 py-4 text-sm text-slate-600 font-semibold">Over 1.5 Million</td>
                        </tr>
                        <tr class="hover:bg-indigo-50/50">
                            <td class="whitespace-nowrap py-4 pl-4 pr-3 text-sm font-medium text-slate-900 sm:pl-6">Annotation Method</td>
                            <td class="whitespace-nowrap px-3 py-4 text-sm text-slate-600">Manual Point Annotation (Head Coordinates)</td>
                        </tr>
                        <tr class="hover:bg-indigo-50/50">
                            <td class="whitespace-nowrap py-4 pl-4 pr-3 text-sm font-medium text-slate-900 sm:pl-6">Image Diversity</td>
                            <td class="whitespace-nowrap px-3 py-4 text-sm text-slate-600">Varying FOV, illumination, resolution, and scale</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <!-- Section 3: File Structure -->
        <section class="mt-10">
            <h2 class="text-3xl font-bold text-slate-800 border-b-2 border-indigo-400 pb-2 mb-6">
                📁 File Structure
            </h2>
            <p class="text-slate-700 mb-4">
                The dataset is organized to separate the visual data from the ground truth coordinates:
            </p>
            <div class="code-block">
<pre>
FSC-set-counting-localization/
├── images/
│   ├── scene_0001.jpg
│   └── ... (6000 total images)
└── annotations/
    ├── scene_0001.txt
    └── ... (6000 total annotation files)
</pre>
            </div>
            <h3 class="text-xl font-semibold text-slate-800 mt-6 mb-2">Annotation Details</h3>
            <ul class="list-disc list-inside space-y-1 text-slate-700 pl-4">
                <li><strong>Format:</strong> Typically a <code>.txt</code> or equivalent file.</li>
                <li><strong>Content:</strong> The $$(x, y)$$ coordinates of the person's head or center point within the image.</li>
            </ul>
        </section>

        <!-- Section 4: Usage -->
        <section class="mt-10">
            <h2 class="text-3xl font-bold text-slate-800 border-b-2 border-indigo-400 pb-2 mb-6">
                🚀 Usage
            </h2>
            <h3 class="text-xl font-semibold text-slate-800 mt-4 mb-2">Integration with CH-RNet/PIDiNet</h3>
            <p class="text-slate-700 leading-relaxed">
                This dataset is used to train and validate crowd localization techniques, which often rely on highly refined edge or density maps. The dense point annotations can be converted into <strong>density maps</strong> for model training, aligning with the methods utilized in networks like those referenced above.
            </p>
            <div class="mt-4 p-4 bg-yellow-50 border-l-4 border-yellow-500 text-yellow-800 rounded-md">
                <span class="font-bold">❗ Note:</span> Due to the large volume of images and annotations, the full data files may be hosted externally. Please <strong>[Specify how users can download the dataset, e.g., Visit the project website for download links]</strong> to obtain the complete data package.
            </div>
        </section>

        <!-- Section 5: Citation -->
        <section class="mt-10">
            <h2 class="text-3xl font-bold text-slate-800 border-b-2 border-indigo-400 pb-2 mb-6">
                📜 Citation
            </h2>
            <p class="text-slate-700 mb-4">
                If this dataset is used in your academic work, please cite the corresponding paper:
            </p>
            <div class="code-block text-sm">
<pre>
@article{Elharrouss2022FSCSet,
  title={FSC-Set: Counting, Localization of Football Supporters Crowd in the Stadiums},
  author={Elharrouss, Omar and Almaadeed, Noora and Abualsaud, Khalid and Al-Maadeed, Somaya and Al-Ali, Aisha and Al-Maadeed, Alaa},
  journal={IEEE Access},
  volume={10},
  pages={10446--10457},
  year={2022},
  doi={10.1109/ACCESS.2022.3144607}
}
</pre>
            </div>
        </section>

        <!-- Section 6: License -->
        <section class="mt-10">
            <h2 class="text-3xl font-bold text-slate-800 border-b-2 border-indigo-400 pb-2 mb-6">
                ⚖️ License
            </h2>
            <p class="text-slate-700 leading-relaxed">
                This dataset is released under the <strong>[LICENSE NAME, e.g., Creative Commons Attribution 4.0 International License (CC BY 4.0)]</strong>. Please refer to the <code>LICENSE</code> file in the repository for specific usage terms.
            </p>
        </section>

        <footer class="mt-12 pt-6 border-t text-center text-sm text-slate-500">
            &copy; 2024 Research Project Documentation. All rights reserved.
        </footer>

    </div>
</body>
</html>
