# hdrvideoreader
This repository is used to read numpy array image direct from HDR and SDR video


### requirements

scikit-video==1.1.11

### example

      from hdrreader import FFmpegReader as hdrffm
      from sdrreader import FFmpegReader as sdrffm
      outputdict = {
            '-pix_fmt': 'rgb48'
        }
      hdrt = hdrffm(videopath,outputdict = outputdict)
      hdrv = hdrt.nextFrame()
      for i in range(hdrt.inputframenum):
        hdrframe = next(hdrv)  # RGB image

    sdrt = sdrffm(videopath)
    sdrv = sdrt.nextFrame()
    for i in range(sdrt.inputframenum):
        sdrframe = next(sdrv)
    

## Citation
If our work is helpful to you, please cite our paper:


      @inbook{HDCFMMM,
      author = {Gang He and Kepeng Xu* and Li Xu and Chang Wu and Ming Sun and Xing Wen and Yu-Wing Tai},
      title = {SDRTV-to-HDRTV via Hierarchical Dynamic Context Feature Mapping},
      year = {2022},
      isbn = {9781450392037},
      publisher = {Association for Computing Machinery},
      address = {New York, NY, USA},
      url = {https://doi.org/10.1145/3503161.3548043},
      booktitle = {Proceedings of the 30th ACM International Conference on Multimedia},
      numpages = {9}
      }
