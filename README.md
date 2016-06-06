# When Truth is Efficient: Analysing Concurrency

This repo houses most of the benchmarks (148 out of 175) used in the evaluation section of the ISSTA '15 paper titled, "When Truth is Efficient: Analysing Concurrency". We were able to run ISP with required number of processes on 160 benchmarks; and, the repo has those benchmarks for which both DEFINDER and MPI2CSP were able to generate correct intermediate files.

In case there is a problem with git-lfs, a snapshot of the repo is available for download at https://www.dropbox.com/s/qdwbl6u3v9miqhh/definder.tar.lrz?dl=0.

The benchmarks.list file lists the names and number of processes for which the benchmarks were run under ISP. The repo has three compressed files that contain the outputs of ISP, MPI2CSP, and DEFINDER, respectively. The datafiles in the tarball are named after the entries in benchmarks.list.

To download the benchmark files, you will need the git lfs extension [https://git-lfs.github.com/]. After installing the lfs extension, please do:

                        git clone https://github.com/gan237/definder
                        cd definder
                        git lfs pull
    
You will need the `lrzip` tool [https://github.com/ckolivas/lrzip] to extract the downloaded files. To untar a tarball, just do `lrzuntar <file.lrz>`. This should generate a directory containing the ISP / MPI2CSP / DEFINDER output.

The output files of DEFINDER serve as inputs to **lingeling** [http://fmv.jku.at/lingeling/]. The output files of MPI2CSP serve as inputs to `FDR3` [https://www.cs.ox.ac.uk/projects/fdr/]. We also found the runsolver tool [http://www.cril.univ-artois.fr/~roussel/runsolver/] handy when running the benchmarks.

The (modified) ISP output we generated is given as reference: it serves as a easily parseable inteermediate form that can be used to compare DEFINDER with other/future tools from the community.


