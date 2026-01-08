# Notes

## Containers and Codecs

Information has to be encoded to stored. For media files this requires encoding the content itself and information about the content. For audio and video, the scheme used for the content is called a codec (COmpressor DECompressor algorithm), and the structure used to record that encoded content as well as contextual information is the container, also known as a file format. One container can include multiple pieces of content with different encodings, like an MP4 container with AVC-encoded video and AAC-encoded audio.

These terms can be used in other domains as well, since the ideas and technologies are the same. Since 2019, Apple has stored digital photography as HEIC containers with HEVC-encoded images. HEIC is derived from the MP4 file format, and HEVC is a codec developed for video.

## Standards

In the 1980s and 1990s, there was immense variety in the diversity and quirks of the computing platforms. Manufacturers had no guarantee that a given container or codec could be rendered by a user's computer. And camera manufacturers were constantly pushing the boundaries of what their hardware could process and record. As a result, many used very basic pixel mapping formats like BMP.

Manufacturers wanted to offer users the ability to fit more content onto their devices digital storage. A compressing codec enables this, but creating your own codec means creating software to render that image as well. A shared standard would socialize those costs. It would also increase interoperability for consumers.

JPEG began its work in 1985, and published its first standard in 1992. That standard is also titled JPEG, but to avoid some confusion, it's referred to here as JPEG-1. The release of a standard does not mean immediate adoptions. The first JPEG-1 capable cameras came out in xxx, but cameras were released up until 2000 without JPEG-1 support. Since then, it's been the standard.

The story is similar for video. The MPEG group began in 199x and published MPEG-1 in 1994 and MPEG-2 in 199x. Neither had widespread uptake in cameras. MPEG-4 contained the standards for MP4/H263/AAC. While some cameras adopted this, major manufactures like Nikon didn't start using it until 2010.

Once a standard is widespread, it's hard to dislodge it. JPEG-1 has broadly met the needs of digital photography. More efficient compression algorithms have been created and standardized by the JPEG group, but they do not have the near universal support of JPEG-1. Space is still a concern for video, and manufacturers have added MPEG-4 Part  14 (HEVC) as an option, but MP4 and AAC remain the container and audio codec of choice.

Standards bodies don't have as strong of an influence on the professional market. Most major camera manufacturers offer the option to record relatively raw sensor data that allows for further photographic processing. The process to encode this data is often proprietary and the container is often standard. For example, Canon mirrorless cameras can create CR3s, a proprietary encoding of the image sensor data in a an MP4-based container.

## Images

### Lossy Compression - JPEG

The files are referred to as JPEGs. This is both an accurate and misleading name.

JPEG is the Joint Photographic Experts Group. Their first published standard was called JPEG. It specifies how to use a Discrete Cosine Transform to reduce detail in an image while reducing image size further, lossy compression. In Annex B, it specifies the JPEG Interchange Format (JIF), a container for JPEG 1-encoded data.

In 1991, a group of companies agreed on the JPEG File Interchange Format (JFIF), a further refinement of the JIF format. This is the container for most JPEG-1 images.

In 1995, a group of camera companies published the Extensible Image File Format (Exif) through JEITDA. Exif defines a set of metadata tags and how to implement them in three formats: JIF for compressed images, TIFF for uncompressed images, and WAVE for audio. The JIF-based standard is the one implemented by most camera manufacturers.

Due to a requirement in how JFIF and Exif require metadata to be ordered within the file, they are incompatible. However, it has become common practice to write a least-invalid version of the combination when software wants to use features from both formats.

So a JPEG file is JPEG-1 encoded image data in Exif, JFIF, or JFIF/Exif container. It may be easier to use JPEG sometimes, and know the full complexity at others.

### RAW formats



## Video

### Lossy

MP4/AVC/AAC became common by about 2010. Prior to this, manufacturers used other container and codecs.

Hitach MP-EG1 first digital video recorder in 1997 mpeg-1 formats

Sharp VN EZ1 first MPEG 4 1999

For example, initially Nikon began with QuickTime/MotionJPEG/PCM in 2006. The MP4/H264/AAC standards already existed and were in use by manufacturers like Flip video, but the hardware and software support was not as widespread.

Quicktime (MOV) was originally developed by Apple in 1999 and became the basis of MPEG-4 in 2001. MPEG-4 allows manufacturers to create subtypes of the formats, which Apple did to create a new version of Quicktime, sometimes identified as MP4 with a Quicktime profile.

Another option for a container was Audio Video Interlace (1991). This had  much broader support, but did not offer the same extensible feature set as MOV/MP4 for metadata, multiple media tracks, and indexing.

MotionJPEG treats video as a series of images, each compressed with the JPEG DCT algorithm. This can take advantage of the existing JPEG creation pathways in a camera, but it can not achieve the same compression performance as more dedicated video codecs.

Pulse Code Modulation (PCM) is an uncompressed audio codec that samples the electrical signal at defined intervals. Storing the data is relatively simple compared to the processing needed for AAC.

The theme is that increasing camera sensors resolution required increasing computational power to encode the data. Manufacturers tended to prefer solutions that required less computation and would be compatible with more computers.