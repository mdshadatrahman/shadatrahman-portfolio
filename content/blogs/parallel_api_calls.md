+++
title = 'Parallel api calls'
date = 2023-10-06T23:27:39+06:00
+++

## What is Parallel api calls?

Parallel API calls allow your app to fetch data from multiple endpoints simultaneously. Parallel API calls can significantly improve app performance, especially when dealing with multiple data sources or large datasets, while traditional API calls in Flutter are sequential.

## Why use Parallel api calls?

Parallel API calls are a great way to improve app performance. They allow your app to fetch data from multiple endpoints simultaneously, which can significantly improve app performance, especially when dealing with multiple data sources or large datasets.

## How to use Parallel api calls?

```dart
	Future<void> fetchParallelRequests() async {
		final responses = await Future.wait([
			http.get(Uri.parse('https://xyz.com/api/endpoint1')),
			http.get(Uri.parse('https://xyz.com/api/endpoint2')),
			http.get(Uri.parse('https://xyz.com/api/endpoint3')),
			http.get(Uri.parse('https://xyz.com/api/endpoint4')),
			http.get(Uri.parse('https://xyz.com/api/endpoint5')),
			http.get(Uri.parse('https://xyz.com/api/endpoint6')),
		]);
	}

```