# YouTube Chapters (YTC) Dataset

The YouTube Chapters (YTC) dataset is specially curated for long tutorial videos. This dataset focuses on the annotations for YouTube chapters, which provide structured segmentations of the video content.

## Data Splits

All the data splits (`train.json`, `test.json`, and `val.json`) contain chapter annotations. These annotations are extracted directly from YouTube and have been manually annotated by the video creators themselves, ensuring the authenticity and relevance of each chapter.

## Pretraining Data

For those interested in pretraining models, this dataset also includes a file named `pretrain_bmd.jsonl`. This file contains data used for the pretraining phase. For a comprehensive understanding of how this data was sourced and processed, please refer to the ```Behance Moment Detection (BMD) dataset```.

## Video Links Association

To correlate the `video_id` from the annotations with the actual video link, you can refer to the `ytc_links.jsonl` file.

## Annotation File Structure

The dataset annotations are formatted in the `jsonl` (JSON Lines) format. Each line in the annotation file is a standalone JSON object, detailing a specific moment in a video.

Here's an example of how the annotations look:

```json
{"vid": "-IXKOGg_Vos", "query": " \u2013 Introduction", "qid": "youtube_-IXKOGg_Vos_1", "relevant_windows": [[34, 109]]}
```

### Attributes:

- **qid**: The unique query identifier.
- **query**: The actual query described in natural language, summarizing the video segment's content.
- **vid**: The video identifier, which can be used to reference the specific video.
- **relevant_windows**: An array containing the start and end times (in seconds) of the relevant video segment for the described query.

