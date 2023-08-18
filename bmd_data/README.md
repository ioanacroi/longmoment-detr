# Behance Moment Detection (BMD) Dataset

The Behance Moment Detection (BMD) dataset is curated for the task of moment detection in long tutorial videos.

## Data Splits

- **Evaluation Splits**: The `val.json` and `test.json` splits have been manually annotated.
  
- **Training Split**: This contains automatic annotations.

## Automatic Annotation Procedure

1. **Video Segmentation**: Videos are initially divided into segments using the tool available at [ivi-ru/video-scene-detection](https://github.com/ivi-ru/video-scene-detection).
   
2. **Summarization**: For every video segment, a Large Language Model (LLM) - specifically GPT-3 - is used to produce a summarization derived from the transcript of that segment.

## Additional Annotations

- **Alternative LLMs**: Annotations produced using different LLMs are housed in the `different_llms_query_generation/` directory or file.

## Video Links Association

To correlate the `video_id` from the annotations with the actual video link, you can refer to the `bmd_links.jsonl` file.

## Transcripts for Training Split

For those interested in the raw transcripts from which the annotations in the training split were derived, the transcripts can be accessed at the following link:
[Training Split Transcripts](https://drive.google.com/file/d/18GvWd7xWht2YBDdn6ixau8HYYPgKrr3x/view?usp=sharing)

## Annotation File Structure

The dataset annotations (including the transcript) are formatted in the `jsonl` (JSON Lines) format. Each line in the annotation file is a standalone JSON object, detailing a specific moment in a video.

Here's an example of how the annotations look:

```json
{"qid": 3978, "query": "the host starts the stream with the face cam on and greets the viewers. and talks about the random topics and shares the screen with a car image on the canvas. and sets off to get started with the sketch.", "vid": "06175b95-ae49-4ae8-9b6e-532d2e2f8789", "relevant_windows": [[0, 657]]}
```

### Attributes:

- **qid**: The unique query identifier.
- **query**: The actual query described in natural language, summarizing the video segment's content.
- **vid**: The video identifier, which can be used to reference the specific video.
- **duration**: Duration of the whole video in seconds.
- **relevant_windows**: An array containing the start and end times (in seconds) of the relevant video segment for the described query.

## Features

We will provide the extracted SlowFast features for the dataset. Stay tuned!

