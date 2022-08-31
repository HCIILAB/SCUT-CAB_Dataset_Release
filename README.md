# SCUT-CAB_Dataset_Release
The SCUT-CAB Dataset for the research of document layout analysis in Chinese ancient books is now released by Deep Leaning and Visual Computing Lab of South China University of Technology. The dataset can be downloaded through the following link:

- [Baidu Cloud](https://pan.baidu.com/s/1xxgt3olnC3nh4-nf7K9Nvg)(Password: dlvc)
- [OneDrive](https://1drv.ms/u/s!AkXauEAZ68NKoQoaUccK7MjVetNq?e=RcQD8t) 


Note: The SCUT-CAB dataset can only be used for non-commercial research purpose. For scholars or organization who wants to use the SCUT-CAB database, please first fill in this [Application Form](Application_Form/Application_Form_for_Using_SCUT-CAB_2022.doc) and send it via email to us ([eelwjin@scut.edu.cn](mailto:eelwjin@scut.edu.cn)). When submiting the application form to us, please list or attached 1-2 of your publications in recent 6 years to indicate that you (or your team) do research in the related research fields of OCR, handwriting analysis and recognition, document image processing, and so on. We will give you the decompression password after your letter has been received and approved. 

## Description

The SCUT-CAB Dataset contains 4000  images of Chinese ancient books, including 31,931 layout element
annotations, which contains different binding forms, fonts, and preservation conditions. To facilitate multiple tasks
of layout analysis, the dataset is divided into two parts: CAB-Physical for physical layout analysis and CAB-Logical for logical layout analysis. 
CAB-Physical contains 4 classes including 31,931 layout elements annotations, CAB-Logical contains 27 classes including 31,931 layout
elements annotations. The SCUT-CAB dataset also contains the labeling of the reading order.

## Examples of SCUT-CAB
Data source:
  + Buddhist scriptures. The dataset of MTHv2 [14] contains Buddhist scripture
datasets of various layouts, which are suitable for layout analysis tasks. Bud-
dhist scriptures are rich in content, including political, ethical, philosophical,
literature, art, customs etc.
+ Chinese Remade Rare Book. Rare books are the essence of ancient book
culture. Selected and representative precious classics in the history of books
and editions.
+ Others. Includes a variety of ancient books including local county histories
and poetry scriptures.

![sample_distribution](images/sample_distribution.png)

## Statistics of SCUT-CAB



 
![five subset](images/five_subsets_com.png)

The following are some page/text level images of SCUT-HCCDoc:

![page_samples](images/page_exmaples.png)

![text lines1](images/weixin_7053_3.jpg)

![text lines2](images/multiA_1197_14.jpg)

![text lines4](images/weixin_7120_9.jpg)

![text lines3](images/multiB_5439_12.jpg)



The diversity of SCUT-HCCDoc can be described in three levels: 
1) **Image-level diversity:** image appearance and geometric variances caused by camera-captured settings (such as perspective, background, and resolution) and  different applications (such as note-taking, test papers, and homework); 
2) **Text-level diversity:** variances of text line length, rotation, etc.; 
3) **Character-level diversity:** variances of character categories (up to 6,109 classes with additional English letters, and digits), character size, individual writing style, etc.

For example, the following image shows the number of character instances for the 50 most frequently observed character categories in the SCUT-HCCDoc.

![top50_chars](images/top_50_chars.png)

## Text recognition baseline (updated)

Here, we give the **latest baseline results**, which are different from those in the paper. In the paper, the input images of the recognizers are resize to 576 x 126 directly. However, we found that it is appropriate, because it will cause huge  deformations in the long text images. So when training, we keep the aspect ratio of input image, and pad the image with zero pixels to a size of 2304 x 126. The network structure and  other training parameter settings are unchanged. The experiments have shown that it does lead to significant improvements, as shown in the tables below.

![updated_rec_result](images/updated_rec_result.jpg)

## Citation and Contact
Please consider to cite our paper when you use our dataset:
```
@article{zhang2020scut,
  title={SCUT-HCCDoc: A New Benchmark Dataset of Handwritten Chinese Text in Unconstrained Camera-captured Documents},
  author={Zhang, Hesuo and Liang, Lingyu and Jin, Lianwen},
  journal={Pattern Recognition},
  pages={107559},
  year={2020},
  publisher={Elsevier}
}
```
For any quetions about the dataset please contact the authors by sending email to Prof. Jin
([eelwjin@scut.edu.cn](mailto:eelwjin@scut.edu.cn)), Prof. Lingyu Liang
([lianglysky@gmail.com](mailto:lianglysky@gmail.com)) or Hesuo Zhang 
([eehesuo.zhang@mail.scut.edu.cn](mailto:eehesuo.zhang@mail.scut.edu.cn)).

## Statement
Many images of SCUT-HCCDoc are searched and downloaded from the Internet, we do not own the copyright of the images. For researchers and developers who wish to use the images for non-commercial research and/or education purpose, we provide the access to images and the corresponding annotations.The url of the web images are given in the dataset. 

If you believe that any images or text in SCUT-HCCDoc violated your rights, please let us know, and we will remove the images.
