# Podcastfy Advanced Configuration Guide

Podcastfy uses a `config.yaml` file to manage various settings and parameters. This guide explains each configuration option available in the file.

## Content Extractor

- `youtube_url_patterns`:
  - Patterns to identify YouTube URLs.
  - Current patterns: "youtube.com", "youtu.be"

## Website Extractor

- `markdown_cleaning`:
  - `remove_patterns`:
    - Patterns to remove from extracted markdown content.
    - Current patterns remove image links, hyperlinks, and URLs.

## YouTube Transcriber

- `remove_phrases`:
  - Phrases to remove from YouTube transcriptions.
  - Current phrase: "[music]"

## Logging

- `level`: "INFO"
  - Default logging level.
- `format`: "%(asctime)s - %(name)s - %(levelname)s - %(message)s"
  - Format string for log messages.

## Website Extractor

- `markdown_cleaning`:
	- `remove_patterns`:
		- Additional patterns to remove from extracted markdown content:
		- '\[.*?\]': Remove square brackets and their contents
		- '\(.*?\)': Remove parentheses and their contents
		- '^\s*[-*]\s': Remove list item markers
		- '^\s*\d+\.\s': Remove numbered list markers
		- '^\s*#+': Remove markdown headers
- `unwanted_tags`:
	- HTML tags to be removed during extraction:
		- 'script', 'style', 'nav', 'footer', 'header', 'aside', 'noscript'
- `user_agent`: 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.124 Safari/537.36'
	- User agent string to be used for web requests
- `timeout`: 10
	- Request timeout in seconds for web scraping


