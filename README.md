# Data Processing Pipeline with Temporal and Apache Arrow

[![Build and Test](https://github.com/TFMV/temporal-flight/actions/workflows/build-test.yml/badge.svg)](https://github.com/TFMV/temporal-flight/actions/workflows/build-test.yml)
[![Go Report Card](https://goreportcard.com/badge/github.com/TFMV/temporal)](https://goreportcard.com/report/github.com/TFMV/temporal)

A high-performance data processing pipeline using Temporal for workflow orchestration and Apache Arrow for efficient data handling.

## Features

- **Streaming Record Batch Processing**: Process data in batches for optimal throughput
- **Zero-Copy Operations**: Minimize memory overhead with Arrow's zero-copy operations
- **Vectorized Execution**: Leverage Arrow's columnar format for vectorized processing
- **Fault Tolerance**: Utilize Temporal's reliability features for resilient workflows
- **Memory Efficiency**: Optimize memory usage with Arrow's columnar data structures
- **Scalability**: Scale horizontally with Temporal workers
- **Arrow Flight Integration**: Direct memory sharing between activities using Arrow Flight

## Architecture

The pipeline consists of several key components:

### System Architecture Diagram

![Architecture](art/temporal.png)

### Arrow Flight Server

Enables direct memory sharing between activities, minimizing serialization overhead.

### Streaming Workflow

Orchestrates the data processing pipeline with Temporal, managing the flow of data between activities.

### Data Processing Activities

- **Generate Batch Activity**: Creates Arrow RecordBatches with sample data
- **Process Batch Activity**: Filters and transforms the data using vectorized operations
- **Store Batch Activity**: Stores the processed data (simulated in this example)

### Batch Processors

Implements vectorized operations on Arrow data for efficient processing.

### Command-line Interface

Provides a flexible interface for configuring and running the pipeline.

## License

[MIT](LICENSE)
