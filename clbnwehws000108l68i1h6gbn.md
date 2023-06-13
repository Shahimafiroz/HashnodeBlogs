---
title: "Chrome DEV Tools."
seoTitle: "Chrome DEV Tools."
seoDescription: "How to improve web page speed by analysing page code using Chrome dev tools"
datePublished: Wed Dec 14 2022 16:59:57 GMT+0000 (Coordinated Universal Time)
cuid: clbnwehws000108l68i1h6gbn
slug: chrome-dev-tools
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1671036960412/cM4yBsP8X.jpeg
tags: pagespeed, javascript, webdev, quality, chromedevtools

---

Let's Analyse some random page performance using Chrome dev Tools. Our main aim is to improve page performance through the following analysis.

*Tools Used*

*   *Chrome dev Tools*
    
*   *Google page insights*
    

 *Overall Analysis*

*   The page made 100 requests, and the total time for loading was 14.17s
    
    ![](https://lh5.googleusercontent.com/7S8YuCfUEMr-JvNPkmkn4nUw04v_g9QTXoMrlrn__IBNVyIoWe6KkZu8RfrrTqQimaubKeQfzrlrk0FQxROy-cHlnBc9hwAoQRDMqbH2V0fvzHPb9vZ-unRhVGISxiEfT7mlGIvwyf2BuvrQrG4VylnVLE5ZaPngu2slKGdccspdz_TovPf7RUsMHF1A6w align="left")
    

*Site Audit*

For auditing, the site performance the following parameters were selected

![](https://lh5.googleusercontent.com/fWLh9YvbbfEm6awEbtET6GlA_srOGtH5y7HkO_QvoCj6ug9A3t2_UvVyBDPsuSSOU7Ns0EM6Ta0vqQT8Z-gY8_6yg3IMyKaghTPNO9jl4tPVe6_cRbgl0ogIV9jjd4kF1ltQYrmU3UNC1Fm8-vA9-YFmEcaxtogValxC0n7LRg7EHlSDLA7ohsfFrZX8mA align="left")

*   Parameters that require improvement :
    

1.  Defer offscreen images
    
2.  Does not use HTTP/2
    
3.  Reduce unused JavaScript
    
4.  Serve images in next-gen formats
    
5.  Eliminate render-blocking resources
    
6.  Properly size images
    
7.  Reduce unused CSS
    
8.  Efficiently encode images
    
    ![](https://lh3.googleusercontent.com/Ho_P5KW7RxGxPfH5oH5opVQXcm30966dlDm9xtm5yphKMUnfxqwETJvsSSAP3ReC96IGdx9xclDAxXZc0tPr5afSzqppnVBKMcUuDZpseILaAsX62PEmX1gTlCsxKTMWq4J7YRk4uIv7CHRr8-nw22e2yiLfJueGZv4hmBW6_7-UndyuaCEnZERG0FmGhA align="left")
    

*   *Parameters that passed the Audit*
    

1.  CSS is minified
    
2.  Java Script is minified
    
3.  Text compression Enabled
    
4.  Prior connection to required origins established
    
5.  Short initial server response time
    
6.  Multiple pages redirects avoided
    
7.  Video formats used for animated content
    
8.  Duplicate modules from java-script bundles removed
    
9.  Largest contentful paint image preloaded
    
10.   Enormous network payloads avoided
    
11.   JavaScript execution timeless
    
12.   Minimal 3rd party usage
    
13.  The largest Contentful Paint image was not lazily loaded
    
14.  Avoids document. write() 
    
15.  Has a &lt;meta name="viewport"&gt; tag with width or initial-scale 
    
16.  Avoids unloading event listeners
    

  
SOLUTIONS:-

1.  Defer offscreen images
    

If we observe the initial performance analysis of our web page we see Time to interact is not in a good range. Deferring offscreen images is one of the factors which is directly influencing this performance parameter. And in order to fix this we need to enable the images to lazy-load and load the important contents 1st. The solution can be basically summarised as “load it as you need it”

This lazy load can be applied simply by using a **loading** attribute in your **img html tag** and set the value as **lazy.** 

&lt;img src=”Shahima.png” loading = “lazy” alt = “shahima” width = “100%” height = “100%”&gt;

  

2.  Does not use HTTP/2
    

The resources requested by the website do not use HTTP/2. Using HTTP/2 offers more performance and optimization to the website than HTTP 1.1 . And leading to further improvement in the page load and overall performance.HTTP/2 offers many benefits over HTTP/1.1, including binary headers and multiplexing

To pass this audit we would have to enable HTTP/2 on our server. 

1.  You can use CloudFlare to get HTTP/2 without touching your backend at all.
    
2.   Alternatively, you can use KeyCDN’s HTTP/2 test tool, which visits any URL for you and tells you if HTTP/2 has been set up correctly.
    
3.  According to [w3techs.com](http://w3techs.com), Apache is still the most used web server today with over 55% of the websites using it.  For HTTP/2, you need Apache &gt;= 2.4. If you are running Ubuntu LTS (16.04), the default apt sources won’t bring you very far. 
    
4.  AWS added support for HTTP/2 to CloudFront. Source
    
5.  Google Cloud Storage If you use a non-custom domain you will get HTTP/2 automatically. For custom domains, there is no HTTP/2 support just yet 
    

3.  Reduce unused JavaScript
    

Java script can slow down the page load speed as the browser needs to download and compile before it can proceed with rendering work. JavaScript is asynchronous (not render-blocking), and the code competes for bandwidth with other resources while it's downloading, which has significant performance implications.

**your website has the following JavaScript file with more than 20 kibibytes of unused code:**

![](https://lh4.googleusercontent.com/lGfhHU_96G5vXqcS_c_H-RZJGBHdaMEfR_ksMqn635p67XwfBKwBZY02Sb9N5lYaMaqTeullHZzEn__80etaZI-3E0r4PTat7JE290rZRaTwJaImFFl34fpZ3tggRkIQE688aDqVko50SxIDIbLTLXz5-_-JYE0zFzQ8jkdICb8TU8K8ibULCXIVADIczg align="left")

You can see the unused code in the coverage tools: as u see only 49% used it so far

![](https://lh5.googleusercontent.com/6Um6J-8AP4QZV2fVJmUX8-GHwDDUPaKQy3kpGN1gHLWODwivZfNWJ6z4SsbhQ7qhrt6JlMghlrtwbKaPxc550FHBUii8TEor4Q7k5_qhx25Ns6Dn15hrNp25CzFX_WrW0Lj-X5w6KfaZI164rsw0N7EhhMfgUOv0Qf-IQX7HK70qtwJrLUeq8a0vmvhujw align="left")

If we analyse the 1st file then all the red bar section shows the unused code that can be removed for this web page. Similarly, other files can also be analysed and unused code can be removed.

![](https://lh6.googleusercontent.com/Oiia4kpeuzXWmxaBiYtf1qUxAyEC23NV2L4u-nUz-7d2DoF56mg6XEThwm4ZscxY5kLqv1qpICaLqP86EyLbIrgzduPmrCstwYtZ_PZkZaVtTHXcrSQqnTmrxsYBuKLos9uoUAIQcObjnhK_WZ1wjE0HgSh8MQHOUT0HPmQNzDp1hVhfSkgQ5RJDOuHIig align="left")

4.  Serve images in next-gen formats
    

The Opportunities section of your Lighthouse report lists all images in older image formats, showing potential savings gained by serving AVIF versions of those images. AVIF and WebP are image formats that have superior compression and quality characteristics compared to their older JPEG and PNG counterparts. Encoding your images in these formats rather than JPEG or PNG means that they will load faster and consume less cellular data.

5.  Properly size images
    

Images can be handled in the following ways:

1.  Resize during the build process
    
2.  Create multiple sizes and use srcset
    
3.  Use img CDN
    

6.  Eliminate render-blocking resources
    

Check for the following resources in the coverage tools and decide which is the most unused.

![](https://lh4.googleusercontent.com/t6eNLeheZ8SyBciihRgHL8kKMUIBvRJlb-8iJlYe5KMTEnAcYVr3KFyl3Hah8zQKJ1J6GmyvDXjTtqB1swcPifn7Nn7REbIgspHHbQGgPmKyZAkDF7wTAPCJ-kLRGIdVgHado4EDozcW3VnrsYEaUHk__g-rEVBoKJINOk5_9pG6kh_V0SMbxnI_7u6tUQ align="left")

Coverage tools will show a waterfall graph and %age of each URL used and hence the elimination can be decided based on that

![](https://lh6.googleusercontent.com/29MxO424P-5_VSFzEcKjzfqoMVs4WR95FiA9uq4lwexyvGKSUgAdpu4icynf7J622KZzAGviJWAG0OzCa5JwMCmmunM9-Sz8QTHtEbdee1hX7A5FQ0X44tYY7GHMZXF0PObof1BdHwwp8RYyUsx6aV4DksglC2E7KJ1H1inV2nzLWvHVTPMeGqDlUYTwXw align="left")

Instead of directly removing the files, libraries and URLs you can test them in the **block tool.**

![](https://lh6.googleusercontent.com/U26fDU_9MY1QnbJtd9zqvPCdRSTTXtlfxBKF_CDmbPa1DC2-OSWtY3FHoepWN8zinPQJk5ltf5xIGg_eiknDxpjDJBGwquoTtnLBOIcV4Sph245MQOoGIyGlSh91MsqBSRXXKI01RhGTwFbCLeh9zkP8zbQN4QtyUWzbhpSB61sTjwHGgePrIUz_aDXKXg align="left")

  
8\. Efficiently encode images

lists all unoptimized images, with potential savings in kibibytes (KiB). Optimise these images so that the page loads faster and consumes less data:

![](https://lh3.googleusercontent.com/wyPcWXQ7jZoLlaeMWz9zfN7jjT5oWQYsp4WRmCy5zCfTqz2D1N74oJzvPNUVk2fhFqffqJHqpPQ4oRqLF727ap8b0wOaWAra8GLy1PJ5D6KDPgbzA6CsqkydGrN4I2Dhnj2-fQxAsSmM9RPEGiclSGSm4D69SWmXLPwtwOBMyd7FoNVfLuMLzdu0TL3O9Q align="left")

9.  Reduce unused CSS
    

Reduce unused rules from stylesheets and defer CSS not used for above-the-fold content to decrease bytes consumed by network activity. Again you can detect the unused css using coverage tool and block and see it if no changes detected then remove the unused CSS from the page.