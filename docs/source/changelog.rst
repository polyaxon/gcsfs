Changelog
=========

Note: in some releases, there are no changes, because we always guarantee
releasing in step with fsspec.

2026.10.0
---------

* upgrades google-cloud-storage (#1039)
* microbenchmarks: separate regional and zonal large file comparison configurations (#1032)
* fix(core): defer GCSFile finalizer cleanup during garbage collection (#1031)
* feat(macrobenchmarks): add Ray Data and Ray Train PyTorch workload (#1030)
* ci(macrobenchmarks): integrate Ray Train workload into Cloud Build automation and docs (#1029)
* feat(macrobenchmarks): add Ray Data and Ray Train metrics parsers and calculation engine (#1028)
* adds cache_type and cache_source for grpc client (#1019)
* fix(benchmarks): add engine and method fields to BigQuery benchmarks schema (#1026)
* Comment why internal write buffer is not needed for ZonalFile (#1027)
* fix(core): prevent deadlock in deferred file close during garbage collection (#1025)
* feat(microbenchmark): add comparison between gcsfs and cli (#1022)
* perf(microbenchmarks): accelerate fixture data prep (#1021)
* ci: add GitHub Actions workflow to mark and close stale issues (#1023)
* refactor(core.py): simplify split_range and _cat_file_concurrent implementations (#1016)
* fix(benchmark): precisely simulate Lightning checkpoint loading sequence (#1018)
* fix(subsystembenchmarks): make checkpoint_case prefix generation robust to bucket URIs (#1015)
* feat(subsystembenchmarks): add PyTorch Lightning checkpoint load benchmark (#1006)
* adds agent skills file (#1012)
* fix(subsystembenchmarks): enable finalize_on_close for datagen shard writes (#1011)
* fix: prevent NotImplementedError when closing GCSFile from event loop thread (#1009)
* refactor(subsystembenchmarks): switch datagen ingest pool to spawn-based ProcessPoolExecutor (#1010)
* perf(subsystembenchmarks): remove num_workers=0 variant from webdataset read benchmarks (#1008)
* chore: release 2026.8.0 (#995)
* feat(subsystembenchmarks): add webdataset image dataloading read benchmark (#1005)
* feat(subsystembenchmarks): generalize dataloading seam for multiple loaders (#1004)
* subsystembenchmarks: support model id substitution in checkpointing save (#1003)
* Track whether cache_type is explicitly set or defaulting in User-Agent header (#998)
* fix(benchmarks): force reinstall requirement overrides and wait for JobSet webhook (#1000)
* feat(subsystembenchmarks): add PyTorch Lightning checkpointing save benchmark (#994)
* fix(macrobenchmarks): enable autoupgrade on GKE clusters and node pools (#999)
* Update benchmarks to remove custom env for prefetcher (#996)
* Makes prefetcher none cache default (#992)
* fix(hns): cache root bucket properly in _get_dirs_and_update_cache (#990)
* test(microbenchmarking): adding walk operation to the microbenchmarking list suite (#989)
* docs(subsystembenchmarks): add benchmark guides (#985)
* fix(benchmark): use fsspec.open instead of shared IPC instance to avoid multiprocessing timeout (#988)
* perf: Update subsystem benchmark baseline num_workers to 4 (#986)
* feat(subsystembenchmarks): print markdown result table (#984)
* ci(subsystembenchmarks): harden stale VM cleanup (#983)
* perf(subsystembenchmarks): tune Hugging Face read benchmark cases (#982)
* Update delete microbenchmarks config for PyTorch Lightning FSDP checkpoint workloads (#971)
* ci(subsystembenchmarks): add Cloud Build execution pipeline and BigQuery ingestion (#976)
* fix(macrobenchmarks) Explicitly wrap FSDP1 units in Lightning macrobenchmark (#981)
* feat(subsystembenchmarks): add HuggingFace Datasets read subsystem benchmarks (#978)
* Update prefetcher.rst (#977)
* feat(perf): add dataloading subsystem benchmark suite and read-amplification scraping (#975)
* feat(subsystembenchmarks): add benchmark measurement framework (#974)
* Fix VM and bucket deletion logic in Cloud Build cleanup (#973)
* refactor(perf-tests): share process-tree resource monitor (#972)
* Updates prefetcher numbers for Standard Buckets (#970)
* Add epoch logging to StepTimeCallback and DatasetEpochCallback (#969)
* feat(macrobenchmarks): make llama_3_1_8b_cpu_sim a real-GPU drop-in (#968)
* feat(macrobenchmarks): add real-time data wait and dataset build metrics (#967)
* feat(macrobench): add dataloading knobs to HF workload (#966)
* docs(macrobenchmarks): add READMEs for cloudbuild and perf macrobenchmarks (#957)
* feat(macrobenchmarks): add support for ModelParallelStrategy (FSDP2) (#965)
* feat(macrobenchmarks): allow one canonical dataset for any bucket type (#963)
* fix(macrobenchmarks): honor full-pass mode in step validation and checkpoint interval (#962)
* Fix SQLite DB locking race condition in create_buckets.sh (#960)
* fix(macrobenchmarks): support empty string null marker in BigQuery schema (#959)
* Fix timer initialization in StepTimeCallback for LLaMA 3.1 8B training (#946)
* chore(macrobenchmarks): tidy up comments and docstrings (#956)
* feat(macrobenchmarks): add throughput and checkpoint size metrics (#958)
* ci: move build and release logic to reusable build-and-release workflow (#955)
* feat(macrobenchmarks): collect and report system metrics (#952)
* uses forkserver instead spawn in microbenchmarks (#950)
* feat(macrobenchmarks): add FSDP support for Llama 3.1 8B CPU simulation (#954)
* chore: release 2026.7.0 (#953)
* fix(macrobenchmarks): fix cloud build machine type networkPerformanceConfig error (#951)
* fix(macrobenchmarks): use random optimizer moments, not zeros, in CPU sim (#949)
* test(macrobench): use default DDP timeout in llama CPU simulation (#947)
* Update release process documentation (#945)
* Add permissions and path filters to release-on-merge workflow (#944)
* fix(cleanup): retry GKE cluster deletion on failure (#943)
* fix(macrobenchmarks): remove HNS validation and external model bucket check (#942)
* fix: seed timer at training start to avoid AttributeError (#941)
* Automate monthly release process (#916)
* refactor(macrobench): share helm args and update cloudbuild config (#940)
* test(perf): add microbenchmarks for put operations (#939)
* Update benchmarking tables schema and values under ReadAhead Cache (#934)
* support environment where ctypes.pythonapi is not available (#938)
* Enhance CPU simulator logging and throughput metrics (#937)
* ci: isolate macrobenchmark GKE cluster in a dedicated VPC network (#933)
* macrobenchmarks: parameterize macrobenchmarks (#936)
* macrobenchmarks: add checkpoint seeding and reduce emulator ranks to 4 (#935)
* Implement zero-cost local backward seeks in PrefetchConsumer (#930)
* Add cache_type in user-agent fo http client  (#908)
* Fix root cache invalidation (#931)
* Use memoryview to enable zero-copy in _pipe_file (#928)
* Fix ValueError message for invalid access in GCSFileSystem (#932)
* feat(macrobench): add BigQuery ingestion pipeline with dynamic schema evolution (#915)
* Fix silent truncation on short reads in zonal bucket downloads (#920)
* Fix generation threading in gcsfs url and concurrent fetches (#921)
* macrobenchmarks: Parameterize training strategy and simulated step compute; generalize requirements (#927)
* Implement makedirs for HNS buckets (#906)
* docs: update benchmarking sections with single-threaded data (#925)
* Optimize concurrent downloads by capping task count based on minimum chunk size (#926)
* ci: add macrobenchmark infrastructure unit tests (#924)
* prefetcher docs: update no cache benchmark tables for Standard buckets (#922)
* perf(benchmarks): increase pipe benchmark size and exclude setup overhead from write benchmark (#917)
* feat(macrobench): add metrics calculation and summary assembly engine (#913)
* feat(macrobench): add metrics extraction and storage engine (#912)
* feat(macrobench): add GKE orchestration scripts and Cloud Build pipeline (#914)
* feat(macrobench): add Llama 3.1 8B CPU simulator workload (hf-pytorch-lightning-cpu) (#911)
* Update prefetcher.rst with Rapid Buckets performance numbers (#909)
* fix: force schema recreation for staging external table in ingestion pipeline (#910)
* Implement zero-copy in write path of standard bucket (#907)
* updated latest fsspec version in pyproject.toml (#903)
* chore: update build configurations and database schema (#904)
* Remove GCE_METADATA_MTLS_MODE export from e2e pipeline (#905)
* chore(benchmarks): make create-vm wait for cleanup-leaked-resources (#902)
* Remove 48 process rapid read benchmark (#901)
* Fix order-independent assertion in test_read_block_zb (#897)
* Update changelog for 2026.6.0 (#899)
* Update changelog for 2026.5.0 release (#898)
* Check finalized state to optimize MRD pool initialization (#896)
* Add mixed pattern in gcsfs microbenchmarks (#822)
* Introduce async API in Prefetcher and Integrate it with Disk Reads (#877)
* Optimize E2E tests: parallelize resource creation and enable parallel test execution (#892)
* Refactor directory cache updates and optimize caching logic (#870)
* Optimize _rm batchsize and speed up tests (#893)
* Fix streaming upload alignment for non-final chunks (#894)
* Fix CPU and Memory monitoring aggregation logic (#891)
* Fix multi-process benchmark child process crash handling (#883)
* ci: Update Codecov config (#890)
* test: clean up zonal/HNS test markers and GHA exports (#876)
* Remove mrd_supports_multi_request and assume it's always true (#884)
* perf: cache metadata details from MRDPoolCache info lookup to avoid redundant network calls (#874)
* Fix ZonalFile generation parameter overwriting (#882)
* Fix `ResourceMonitor` thread shutdown latency affecting benchmark durations (#881)
* Fix generation parameter not forwarded to GCSFile in open() (#880)
* Fix: Route GCSMap through dynamically resolved GCSFileSystem (#879)
* Fix multiple `_info()` calls in `_process_limits_to_offset_and_length` (#878)
* Adds a comprehensive performance micro-benchmark suite targeting fs.glob() (#873) (#873)
* test: create flat bucket dynamically (#869)
* enable exp reads (#868)
* ci: block release pipeline on Google Cloud Build E2E integration tests (#866)
* fix: use conda-forge for docs to avoid Anaconda SSL error (#865)
* fix: clean up duplicate tests (#867)
* Adds log for download range for Rapid Bucket (#863)
* Implement zero-copy optimization for single-read operations (#840)
* Merge HNS and flat bucket deletion routing in rm (#858)
* Fix multiprocessing emulator _get_bucket_type calls (#859)
* Add open microbenchmark (#860)
* Update read performance microbenchmark config to use 1 file (#861)
* Refactor prefetcher code (#818)
* Refcount in-flight MRDs in MRDPool (#856)
* Fix teardown order in close_resources() (#857)
* Fix concurrent MRD reuse by tracking in-flight MRDs on close (#854)
* Fix off-by-one error in upload_chunk shortfall recursion (#855)
* Fix swapped arguments in _process_object inside inventory_report.py (#853)
* Optimize benchmarks pipeline, fix quota leaks and handle manual builds (#851)
* Update default value of mrd_pool_size in micro benchmark to None and add pool parameters to benchmark schema (#850)
* Fix BigQuery ingestion errors and improve Cloud Build robustness (#849)
* Document intentional non-caching and fallback behavior for UNKNOWN bucket layouts (#844)
* Add mrd pool cache (#846)
* Use pytest markers to gate Rapid/HNS tests (#848)
* Fix Storage Control endpoint resolution for TPC (#847)
* Run tests concurrently in CI (#845)
* Improve test speed and emulator compatibility (#843)
* add support for testing against fsspec HEAD (#841)
* Adds Pipe function in microbenchmark (#842)
* Pass trailing / to createFolder as per documentation (#839)
* Add multi-threaded fixed-duration read microbenchmarks (#838)
* Remove fsspec exclusion following prefix fix (#837)
* Add pypi environment to release workflow (#836)
* Update the benchmark config, and fix the block size propogation (#808)
* Integrate prefetcher engine with zonal buckets (#805)
* Merge pull request #835 from zhixiangli/fix-httperror-content-none
* Add workflow to automate PyPI package publishing on release (#824)
* fix: adjust fsspec dependency version constraint (#834)
* add more coverage
* fix issue with special characters in rm method
* Enable branch wise tracking (#819)
* include only directories that match the prefix in find()
* add support for partial prefixes in find method for HNS buckets
* update zonal doc (#828)
* changelog (#827)
* Enhance Retry Logic and Configuration for Storage Control API (#787)
* fix: add fallback for missing `_version.py` when running from a raw git clone (#826)
* fix: pass quota_project_id to AsyncGrpcClient in ExtendedGcsFileSystem (#825)
* Migrate from setuptools to hatch (#809)
* Fix location in _put_file (#821)
* Fix 'Task exception was never retrieved' in parallel_tasks_first_completed (#807)
* Fix the error message formatting in _rm_files (#820)
* benchmarks: implement cleanup-on-failure in Cloud Build (#813)
* Use moveTo API to move files for standard buckets (#800)
* Add benchmark type conditionals for VM creation (#810)
* Support for Requester Pays buckets in ExtendedGcsFileSystem (#817)
* chore: update google-cloud-storage git repository URL in benchmarks (#812)
* Skip cloud credential method when NO_GCE_CHECK=true (#803)
* Changes log level to warning instead of error storage layout API (#816)
* Update ptable to prettytable in microbenchmarks (#811)
* docs: add prefetcher to index to fix ci (#815)
* Add prefetcher reader for standard buckets. (#795)
* Microbenchmarks improvements and bug fixes (#799)
* Enhance _info method to check file and directory info in parallel (#786)
* adds speed diff in documentation for more clarity (#802)
* Update README.md (#801)
* Add documentation for retries in GCSFS (#789)
* Correct typos in comments (#774)
* Add tests for size, glob, tree, walk, expand_path and improve HNS integration coverage (#778)
* Rename read/write_fixed_duration to read/write (#782)
* fixes typos (#798)
* Update find cache and rm tests (#797)
* Support independent chunk and block sizes for both Read and Write FixedDuration microbenchmarks (#779)
* Update documentation (#794)
* fixes type, updates changelog (#796)
* changelog (#793)
* Refactor file range processing and update logging in mrd (#790)
* fixes doc build (#792)
* Update documentation for Rapid Storage (#788)
* support creation of zonal buckets using mkdir (#769)
* Zonal documentation (#781)
* Fix the failing unit and e2e tests in CI pipelines (#785)
* Make ExtendedGcsFileSystem the default implementation (#773)
* Update ZonalFile write operations with byte count and location tracking (#777)
* micro benchmarks ingestion automation (#775)
* ci: improve Cloud Build failure reporting (#772)
* Fix Race Condition in HNS Folder Rename (#771)
* Delete read and write non duration benchmark tests (#770)
* Update derived tests and add idempotency token for storage control API calls (#764)
* Implement ZonalFile AAOW lazy init, add core tests for Zonal buckets, and improve CI pipeline (#766)
* gracefully handle exceptions during MRD and AAOW close (#763)
* Add info microbenchmarks. (#767)
* Update coverage configuration to omit gcsfs/tests directory (#765)
* fixed duration read and write benchmarks (#762)
* Override mv_file to use atomic moveTo JSON API (#758)
* Add async support for HNS methods (#756)
* refactors list api to include only valid parameters (#759)
* Implement _cp_file for Zonal Buckets & support custom flush interval (#746)
* Perf micro benchmark automation using cloudbuild (#753)
* changelog (#757)
* Remove cache_type option from ExtendedGCSFSFileSystem._open (#754)
* Fix for recent breaking changes introduced in python sdk  (#755)
* Adds test coverage check in repo (#68) (#752)
* Add the new readahead_v2 cache (#750)
* rm override for HNS buckets (#742)
* Ignore benchmark folders (#748)
* adds info() integration tests for HNS (#749)
* change errors to warning in ZonalFile commit (#747)
* find Method Implementation for HNS Buckets (#735)
* Explicitly set the expiry time for raw token, and avoid retrying if it expires (#716)
* feat: support Zonal file download and add few fixes (#744)
* runs benchmark unit tests only when benchmark skip test is false (#745)
* Implement rmdir method for HNS buckets (#728)
* Include empty folders in ls (#733)
* seggregate unit tests and integration tests for rename (#740)
* Write, List, Rename & Delete Microbenchmarks (#738)
* changelog (#741)
* Implement async upload methods and support async mode in ExtendedGcsfs (#737)
* mkdir override for HNS buckets (#731)
* reformat benchmark readme
* Adds GCSFS Microbenchmarks (#722)
* ✨ Support alternative GCP Universes (#732)
* Override info for hns (#730)
* Update ci pipeline to run tests on HNS bucket (#729)
* feat(zb-write): Support write mode in Zonal File (#726)
* Adds mv/rename method implementation for HNS buckets (#727)
* Increased the ulimit temporarily for VM in CI pipeline to avoid too many open files error
* Add multi threaded read tests for Zonal buckets and bug fixes (#723)
* Prevent OS Login key accumulation in e2e tests (#725)
* fix the ls method to return max_results if specified (#724)
* capture generation after upload (#718)
* Enable tests on Zonal bucket as Rapid storage is now enabled (#721)
* Fix authentication issue with anon token and support block size/consistency options in ExtendedGcsFileSystem (#720)
* Add ci pipeline using CloudBuild to run integration tests against real GCS (#719)
* changelog (#717)
* Fixes for actual GCS bucket tests (#714)
* adds the logic to only run extended gcsfilesystem tests when experimental env variable is set (#712)
* Feat: Introduce ExtendedGcsFileSystem for Zonal Bucket gRPC Read Path (#707)
* Add support for Python 3.14 and drop EOL 3.9 (#709)
* changelog (#706)
* Fix for slower exists() and info() calls (#705)
* Add CoC (#703)
* Should not attempt to create bucket by default on mkdir (#701)
* Add goatcounter (#700)
* changelog (#698)
* Fix iterating over every entry (#697)
* Ensure right error type for get() on nonexistent (#695)
* changelog (#693)
* add support message (#691)
* remove addcidental inclusion
* less refresh in ci (#690)
* changelog (#689)
* Use correct timezone conversion for credentials expiry timestamp (#688)
* Fix timezone comparison (#683)
* changelog (#681)
* Create warning for appending mode 'a' operations (#675)
* Avoid deprecated `utcnow` (#680)
* Add support for specifying Cloud KMS keys when creating files (#679)
* Yet another fix for isdir (#676)
* add userProject to batch deletion query (#673)
* Changelog (#671)
* changelog (#670)
* Fix find with path not ending with "/" (#668)
* Remove caveat from doc (#666)
* Don't check expiry for creds that have none (#665)
* changelog (#662)
* Improvements for credentials refresh under high load (#658)
* changelog (#660)
* Try better shutdown cleanup behaviour (#657)
* Guess file content type when not specified (#655)
* changelog (#652)
* Add exclusive write (#651)
* avoid index error on whole second (#649)
* Added note about refresh and POSIX behavior (#648)
* Handle cache_timeout = 0 in GCSFileSystem (#646)
* changelog (#644)
* Update credentials.py to test removal of race condition in credentials (#643)
* Fix md5 hash logic. Make it order agnostic. (#640)
* changelog (#639)
* Handle case when error message is a string. (#631)
* changelog (#629)
* changelog (#626)
* Add seek(0) to request data to prevent issues on retries (#624)
* Changelog (#622)
* swap order of protocols to favor "gs" when unstripping protocol from URI (#620)
* _get_file: fix makedirs call when the lpath is relative and in the working directory (#618)
* changelog (#614)
* retry bulk rm (#608)
* Add options to `mkdir` (#610)
* fix(sign): use timedelta to pass proper expiration time (#613)
* Ensure dircache on ls (#612)
* Update docs about credentials (#609)
* close_session: clean up loop handling (#606)
* changelog (#605)
* Small clarification on dict and filepath GCP tokens (#603)
* req
* changelog (#596)
* Release (#594)
* Changelog (#592)
* Ensure consistent use of versions during pagination (#591)
* Fix double asterisk glob in tests (#589)
* changelog (#588)
* Fix small transaction (#586)
* cgangelog (#585)
* Remove CI warnings
* changelog (#581)
* Inventory report: fix nit and typo (#578)
* changelog (#579)
* Avoid copying files with same name prefix when copying folder (#576)
* Add test_move_recursive (#575)
* fix: use utcnow time to test ctime info (#577)
* added refresh flag to ls (#556)
* Better double asterisk support (#572)
* Asyncio Listing and Inventory Report Integration (#573)
* feat: update versioneer (#568)
* Add pickling support to `HttpError` class (#571)
* squash warnings (#569)
* Implement maxdepth in GCSFileSystem._find (#566)
* Invalidate dircache on gcs.cp (#564)
* Translate time metadata from GCS names to fsspec standard names. (#563)
* Faster cache in `find` (#561)
* changelog (#557)
* GCSFileSystem can accept a raw token (#554)
* updated async docs (#552)
* Expose fixed_key_metadata kwarg for put and pipe (#550)
* Cache expiry duplicated (#551)
* changelog (#549)
* Auto-prepend scheme prefix to STORAGE_EMULATOR_HOST (closes #547) (#548)
* Wrap BytesIO to prevent accidental closure when retrying (#540)
* changelog (#538)
* changelog (#532)
* remove stray print
* Don't let find() mess up dircache (#531)
* Add python 3.11, drop 3.7 (#529)
* Switch doc build to use Read the Docs version 2 (#528)
* Assume times as UTC (#527)
* What sent body bytes in io.BytesIO (#525)
* ls: Only append the generation to the entry's name if it exists
* Add cp, get and put recursive tests (#521)
* changelog (#520)
* timestamps without enough zeros (#518)
* feat: support created and modified methods in GCSFileSystem (#516)
* set a session (#515)
* Don't immediately make seesion in init (#514)
* Fixed issue in sign url function (#513)
* Update pre-commit, add python versions (#508)
* ls: support versions (#509)
* dep and changelog (#507)
* dep and changelog (#506)
* core: support object versioning (#504)
* deps: bump fsspec to 2022.10.0 (#503)
* Escape all special characters in URL paths (#502)
* Refresh credentials to check validity (#487)
* don't include parent in find(withdirs=True) (#499)
* Splitting remove files requests into 100-chunk batched requests. (#496)
* bump (#497)
* for release (#494)
* prevent find from corrupting dircache (#488)
* docs: add a note regarding aiohttp and proxy envvars (#491)
* Avoid aiohttp v4.0.0a0 and v4.0.0a1 (#490)
* changelog
* Fix failed tests `test_attrs()` and `test_mkdir_with_path()` (#479)
* Fix to also try `cloud` authentication method when `method=None` (#481)
* update release notes, dep (#475)
* Fix cache invalidation in put and pipe (#473) (#474)
* Add **kwargs parameters to _mkdir, _cat_file, adhere to fsspec API (#471)
* update release notes (#467)
* Alternate bucket info if cannot GET (#464)
* Pass `sign` kwargs to `generate_signed_url` (#460)
* Allow configuring bucket location (#455)
* Fix check connection (#457)
* Explicitly cope with dir+dirmarker combination (#459)
* Use local server for browser auth (#456)
* Fix endpoint_url docstring typo (#451)
* Close auth session (#452)
* Change pin of fsspec to 2022.2.0 (no leading zeros) (#450)
* changelog for release
* fix _list_buckets with disabled caching (#449)
* gcsfs: drop python 3.6 (#445)
* Update changelog, deps (#443)
* Make tarball creation more reproducible (#442)
* update deps, changelog (#438)
* Don't touch cache on find with prefix (#437)
* for release (#435)
* fixup references to dask/gcsfs (#434)
* Add support to additional 'fixed-key-metadata' (#429)
* feat(gcsfs/core): support storage_emulator_host for http requests (#424)
* update changelog
* feat: sign url using google-cloud-storage (#411)
* for release
* core: add default no-op callbacks (#422)
* update dep and changelog (#420)
* Update checks for 404 during retry (#419)
* Encode percent character, add test (#415)
* Workaround .details being a property upstream (#417)
* core: implement callbacks for put_file/get_file (#416)
* changelog and dep (#410)
* Fix link, spelling, pytest color (#409)
* Avoid retrying responses with 404 status code (#406)
* Add test to cover get/put with lists (#401)
* Fix typo in GCSFile docstring (#403)
* for release (#400)
* spec: fix find()/glob() calls with prefix on cache (#399)

2026.8.0
--------

**Adaptive Concurrent Prefetching is now the default read path**

**Enhanced read path via adaptive concurrent prefetching is now the default  in GCSFS.**
Starting with this version, GCSFS predicts the next byte range an application will read, fetches it in the background across several concurrent HTTP requests, and keeps the bytes in memory before next read() is called. Network round-trips overlap with application compute instead of blocking calls where compute has to wait for data to be fetched. We are also enabling read concurrency, so a single reader is no longer limited by the bandwidth of a single HTTP connection.

GCSFS prefetcher adapts to workload read IO patterns. It tracks the rolling average of recent read sizes and scales the prefetch window linearly with the detected sequential streak, rather than using a fixed block size or exponential doubling. This is inline to what modern Linux kernels will do to balance prefetch and memory footprint. When the pattern turns random read i.e. we are not able to leverage the prefetched buffer to answer the next read() call, it drains the buffer to zero, so that random-access workloads pay no bandwidth or memory penalty.

**Why this matters for AI/ML workloads**

* **Model loading and checkpoint restore are typically large sequential reads - and prefetcher shines there.** In our benchmarking, a single-stream sequential throughput improved from 23.69 MB/s to 658.71 MB/s for 1 MB I/O, and from 156 MB/s to 736 MB/s for 16 MB I/O.
* **Training data pipelines stay fed.** Parquet and sharded dataset reads issue small-to-medium sequential ranges that previously suffered from low throughput, but now achieve significantly more; at 16 MB I/O throughput rises from 150 MB/s to 730 MB/s. Reducing the wait time for data loading improves accelerator goodput(amount of time accelerator is utilised for training than waiting).
* **Multi-worker dataloader scaling.** The prefetcher manufactures its own parallelism per worker instead of relying on process count alone.
* **Accelerate the throughput even further with Rapid Buckets.** With Rapid Buckets single node throughput reaches 21 GiB/s with  16-process sequentially reading at 16 MiB I/O compared to standard buckets with 48processes.

**Adaptive prefetcher is enabled by default** when cache_type is not explicitly set and concurrency value is set at 4(DEFAULT_GCSFS_CONCURRENCY=4) for both Standard and Rapid buckets. You can disable adaptive prefetcher by setting an explicit cache_type, or by setting  USE_EXPERIMENTAL_ADAPTIVE_PREFETCHING='false', or by passing use_experimental_adaptive_prefetching=False to open() call.

**(Warning) Impact on memory:** Prefetching trades memory for throughput. Peak memory rises from ~170 MB to 600 MB on single-stream reads for 16 MB IO size and varies with requested IO sizes, and would be materially more under high process counts. Please ensure that   application memory  limits accordingly to use prefetcher without any Out of Memory(OOM) issues. To put hard limit, you can also use [user_max_prefetch_size](https://github.com/fsspec/gcsfs/blob/main/gcsfs/prefetcher.py#L154)

For  details on architecture, tuning, full benchmark tables, along with known limitations please refer to : https://github.com/fsspec/gcsfs/blob/main/docs/source/prefetcher.rst

(#795, #805, #818, #877)

**Bug Fixes & Improvements**

* Zero-cost local backward seeks in PrefetchConsumer - Parquet footer and ZIP directory reads are served from the existing buffer instead of re-issuing a network request. (#930)
* Concurrent downloads cap task count against a minimum chunk size, removing per-task overhead on small ranges. (#926)
* Generation consistency across parallel fetches, guaranteeing every chunk comes from the same object version. (#921)
* Fixed silent truncation on short reads in zonal bucket downloads. (#920)
* Zero-copy read and write paths via memoryview, cutting CPU and transient memory in the hot path. (#840, #907, #928)
* Graceful fallback where ctypes.pythonapi is unavailable. (#938)


2026.7.0
--------

* fix(macrobenchmarks): fix cloud build machine type networkPerformanceConfig error (#951)
* fix(macrobenchmarks): use random optimizer moments, not zeros, in CPU sim (#949)
* test(macrobench): use default DDP timeout in llama CPU simulation (#947)
* Update release process documentation (#945)
* Add permissions and path filters to release-on-merge workflow (#944)
* fix(cleanup): retry GKE cluster deletion on failure (#943)
* fix(macrobenchmarks): remove HNS validation and external model bucket check (#942)
* fix: seed timer at training start to avoid AttributeError (#941)
* Automate monthly release process (#916)
* refactor(macrobench): share helm args and update cloudbuild config (#940)
* test(perf): add microbenchmarks for put operations (#939)
* Update benchmarking tables schema and values under ReadAhead Cache (#934)
* support environment where ctypes.pythonapi is not available (#938)
* Enhance CPU simulator logging and throughput metrics (#937)
* ci: isolate macrobenchmark GKE cluster in a dedicated VPC network (#933)
* macrobenchmarks: parameterize macrobenchmarks (#936)
* macrobenchmarks: add checkpoint seeding and reduce emulator ranks to 4 (#935)
* Implement zero-cost local backward seeks in PrefetchConsumer (#930)
* Add cache_type in user-agent fo http client  (#908)
* Fix root cache invalidation (#931)
* Use memoryview to enable zero-copy in _pipe_file (#928)
* Fix ValueError message for invalid access in GCSFileSystem (#932)
* feat(macrobench): add BigQuery ingestion pipeline with dynamic schema evolution (#915)
* Fix silent truncation on short reads in zonal bucket downloads (#920)
* Fix generation threading in gcsfs url and concurrent fetches (#921)
* macrobenchmarks: Parameterize training strategy and simulated step compute; generalize requirements (#927)
* Implement makedirs for HNS buckets (#906)
* docs: update benchmarking sections with single-threaded data (#925)
* Optimize concurrent downloads by capping task count based on minimum chunk size (#926)
* ci: add macrobenchmark infrastructure unit tests (#924)
* prefetcher docs: update no cache benchmark tables for Standard buckets (#922)
* perf(benchmarks): increase pipe benchmark size and exclude setup overhead from write benchmark (#917)
* feat(macrobench): add metrics calculation and summary assembly engine (#913)
* feat(macrobench): add metrics extraction and storage engine (#912)
* feat(macrobench): add GKE orchestration scripts and Cloud Build pipeline (#914)
* feat(macrobench): add Llama 3.1 8B CPU simulator workload (hf-pytorch-lightning-cpu) (#911)
* Update prefetcher.rst with Rapid Buckets performance numbers (#909)
* fix: force schema recreation for staging external table in ingestion pipeline (#910)
* Implement zero-copy in write path of standard bucket (#907)
* updated latest fsspec version in pyproject.toml (#903)
* chore: update build configurations and database schema (#904)
* Remove GCE_METADATA_MTLS_MODE export from e2e pipeline (#905)
* chore(benchmarks): make create-vm wait for cleanup-leaked-resources (#902)
* Remove 48 process rapid read benchmark (#901)
* Fix order-independent assertion in test_read_block_zb (#897)

2026.6.0
--------

* check finalized state to optimize MRD pool initialization (#896)
* fix streaming upload alignment for non-final chunks (#894)
* optimize _rm batchsize and speed up tests (#893)
* optimize E2E tests: parallelize resource creation and enable parallel test execution (#892)
* fix CPU and Memory monitoring aggregation logic (#891)
* update Codecov config (#890)
* remove mrd_supports_multi_request and assume it's always true (#884)
* fix multi-process benchmark child process crash handling (#883)
* fix ZonalFile generation parameter overwriting (#882)
* fix ResourceMonitor thread shutdown latency affecting benchmark durations (#881)
* fix generation parameter not forwarded to GCSFile in open() (#880)
* route GCSMap through dynamically resolved GCSFileSystem (#879)
* fix multiple _info() calls in _process_limits_to_offset_and_length (#878)
* introduce async API in Prefetcher and integrate it with disk reads (#877)
* clean up zonal/HNS test markers and GHA exports (#876)
* cache metadata details from MRDPoolCache info lookup to avoid redundant network calls (#874)
* add a comprehensive performance micro-benchmark suite targeting fs.glob() (#873)
* refactor directory cache updates and optimize caching logic (#870)
* create flat bucket dynamically (#869)
* enable exp reads (#868)
* clean up duplicate tests (#867)
* block release pipeline on Google Cloud Build E2E integration tests (#866)
* use conda-forge for docs to avoid Anaconda SSL error (#865)
* add log for download range for Rapid Bucket (#863)
* update read performance microbenchmark config to use 1 file (#861)
* add open microbenchmark (#860)
* fix multiprocessing emulator _get_bucket_type calls (#859)
* merge HNS and flat bucket deletion routing in rm (#858)
* fix teardown order in close_resources() (#857)
* refcount in-flight MRDs in MRDPool (#856)
* fix off-by-one error in upload_chunk shortfall recursion (#855)
* fix concurrent MRD reuse by tracking in-flight MRDs on close (#854)
* fix swapped arguments in _process_object inside inventory_report.py (#853)
* optimize benchmarks pipeline, fix quota leaks and handle manual builds (#851)
* update default value of mrd_pool_size in micro benchmark to None and add pool parameters to benchmark schema (#850)
* fix BigQuery ingestion errors and improve Cloud Build robustness (#849)
* use pytest markers to gate Rapid/HNS tests (#848)
* fix Storage Control endpoint resolution for TPC (#847)
* add mrd pool cache (#846)
* run tests concurrently in CI (#845)
* document intentional non-caching and fallback behavior for UNKNOWN bucket layouts (#844)
* improve test speed and emulator compatibility (#843)
* add Pipe function in microbenchmark (#842)
* add support for testing against fsspec HEAD (#841)
* implement zero-copy optimization for single-read operations (#840)
* pass trailing / to createFolder as per documentation (#839)
* add multi-threaded fixed-duration read microbenchmarks (#838)
* remove fsspec exclusion following prefix fix (#837)
* add mixed pattern in gcsfs microbenchmarks (#822)
* refactor prefetcher code (#818)

2026.5.0
--------

* add pypi environment to release workflow (#836)
* fix HttpError message formatting and handle None content in validate_response (#835)
* adjust fsspec dependency version constraint (#834)
* add support for partial prefixes in find method for HNS buckets (#831)
* fix issue with special characters in rm method (#831)
* update zonal doc (#828)
* add workflow to automate PyPI package publishing on release (#824)
* enable branch-wise tracking in benchmarks (#819)
* update the benchmark config, and fix the block size propagation (#808)
* integrate prefetcher engine with zonal buckets (#805)

2026.4.0
--------

* add fallback when missing __version__ (#826)
* use project ID in gRPC, if set (#825)
* fix location lookup in put_file (#821)
* error message formatting in rm_files (#820)
* requestor pays in ExtendedGcs (#817)
* logging error->warning in storage layout API (#816)
* fix prefetcher docs (#815)
* cleanup on failure in cloud build benchmarks (#812)
* benchmark updates (#812, 811, 810, 802)
* migrate setuptools to hatch (#809)
* retreive coroutine exceptions (#807)
* honour NO_GCE_CHECK (#803)
* update README (#801)
* use moveTo in standard buckets (#800)
* typos (#798, 796, 794)
* prefetcher for standard buckets (#795)

2026.3.0
--------

**Support for Rapid and hierarchical buckets is moved from opt-in to default.**
**The default implementation is now ExtendedGcsFileSystem**. This still
defers to GCSFileSystem for operations on "normal" buckets (i.e., not
zonal, rapid, hierarchical). Set GCSFS_EXPERIMENTAL_ZB_HNS_SUPPORT to
disable.

* docs for zonal/rapid storage support (#792, 788, 781)
* test/ci/cov fixes (#785, 772, 766, 765, 764)
* fix zonalfile writes to track byte count (#777)
* benchmarks (#775, 770, 767, 762)
* fix folder rename race (HNS) (#771)
* create zonal buckets (#769)
* graceful close (#763)
* list: pass only valid kwargs (#759)
* make mv_file atomic (#758)

2026.2.0
--------

* New readahead-chunks cacher (#754, 750)
* test coverage (#752)
* info() integration tests for hierarchical (#749)
* more benchmark work (#748, 745)
* zonal file downloads (#744)
* rm for hierarchical (#742)

2026.1.0
--------

New opt-in support for hierarchical buckets.

* Support alternative GCP Universes (#732)
* overrides for HNS buckets (#731, 730, 727
* CI for HNS and zonal buckets (#729, 721, 719)
* Zonal bucket write mode (#726)
* CI auth fixes (#720, 725
* Microbenchmarks framework (#722)
* capture generation value after upload (#718)


2025.12.0
---------

* Fix CI when run against rela SGC buckets (#71)
* Run extended rests when env var is set (#712)
* Support py3.14 and drop 3.9 (#709)
* Introduce ExtendedGcsFileSystem for Zonal Bucket gRPC Read Path (#707)

2025.10.0
---------

* fix info() performance regression (#705)
* add CoC (#703)
* mkdir should not create bucket by default (#701)
* add anonymous tracker to docs (#700)

2025.9.0
--------

* fix slow ls iterations (#697)
* Ensure right error type for get() on nonexistent (#695)

2025.7.0
--------

* acknowledge Anaconda support (#691)
* less refreshing for CI (#690)

2025.5.1
--------

* Fix token timezone comparison (#683, 688)

2025.5.0
--------

* Avoid deprecated utcnow (#680)
* Add support for specifying Cloud KMS keys when creating files (#679)
* Yet another fix for isdir (#676)
* Create warning for appending mode 'a' operations (#675)
* add userProject to batch deletion query (#673)

2025.3.2
--------

no changes

2025.3.1
--------

* Fix find with path not ending with "/" (#668)
* remove "beta" note from doc (#666)
* don't check expiry of creds that don't expire (#665)

2025.3.0
--------

* Improvements for credentials refresh under high load (#658)

2025.2.0
--------

* guess upload file MIME types (#655)
* better shutdown cleanup (#657)

2024.12.0
---------

* Exclusive write (#651)
* Avoid IndexError on integer seconds (#649)
* note on non-posixness (#648)
* handle chache_timeout=0 (#646)

2024.10.0
---------

* Remove race condition in credentials (#643)
* fix md5 hash order logic (#640)

2024.9.0
--------

* In case error in a pure string (#631)

2024.6.1
--------

no changes

2024.6.0
--------

* Add seek(0) to request data to prevent issues on retries (#624)

2024.5.0
--------

* swap order of "gcs", "gs" protocols (#620)
* fix get_file for relative lpath (#618)

2024.3.1
--------

* fix expiration= for sign() (#613)
* do populate dircache in ls() (#612)
* allow passing extra options to mkdir (#610)
* credentials docs (#609)
* retry in bulk rm (#608)
* clean up loop on close (#606)

2024.2.0
--------

* doc for passing tokens (#603)

2023.12.2
---------

no changes

2023.12.1
---------

no changes

2023.12.0
---------

* use same version when paginating list (#591)
* fix double asterisk glob test (#589)

2023.10.0
---------

* Fix for transactions of small files (#586)

2023.9.2
--------

* CI updates (#582)

2023.9.1
--------

* small fixes following #573 (#578)

2023.9.0
--------

* bulk operations edge cases (#576, 572)
* inventory report based file listing (#573)
* pickle HttpError (#571)
* avoid warnings (#569)
* maxdepth in find() (#566)
* invalidate dircache (#564)
* standard metadata field names (#563)
* performance of building cache in find() (#561)


2023.6.0
--------

* allow raw/session token for auth (#554)
* fix listings_expiry_time kwargs (#551)
* allow setting fixed metadata on put/pipe (#550)

2023.5.0
--------

* Allow emulator host without protocol (#548)
* Prevent upload retry from closing the file being sent (#540)

2023.4.0
--------

No changes

2023.3.0
--------

* Don't let find() mess up dircache (#531)
* Drop py3.7 (#529)
* Update docs (#528)
* Make times UTC (#527)
* Use BytesIO for large bodies (#525)
* Fix: Don't append generation when it is absent (#523)
* get/put/cp consistency tests (#521)

2023.1.0
--------

* Support create time (#516, 518)
* defer async session creation (#513, 514)
* support listing of file versions (#509)
* fix ``sign`` following versioned split protocol (#513)

2022.11.0
---------

* implement object versioning (#504)

2022.10.0
---------

* bump fsspec to 2022.10.0 (#503)

2022.8.1
--------

* don't install prerelease aiohttp (#490)

2022.7.1
--------

* Try cloud auth by default (#479)

2022.5.0
--------

* invalidate listings cache for simple put/pipe (#474)
* conform _mkdir and _cat_file to upstream (#471)

2022.3.0
--------

(note that this release happened in 2022.4, but we label as 2022.3 to match
fsspec)

* bucket exists workaround (#464)
* dirmarkers (#459)
* check connection (#457)
* browser connection now uses local server (#456)
* bucket location (#455)
* ensure auth is closed (#452)

2022.02.0
---------

* fix list_buckets without cache (#449)
* drop py36 (#445)

2022.01.0
---------

* update refname for versions (#442)

2021.11.1
---------

* don't touch cache when doing find with a prefix (#437)

2021.11.0
---------

* move to fsspec org
* add support for google fixed_key_metadata (#429)
* deprecate `content_encoding` parameter of setxattrs method (#429)
* use emulator for resting instead of vcrpy (#424)

2021.10.1
---------

* url signing (#411)
* default callback (#422)

2021.10.0
---------

* min version for decorator
* default callback in get (#422)

2021.09.0
---------

* correctly recognise 404 (#419)
* fix for .details due to upstream (#417)
* callbacks in get/put (#416)
* "%" in paths (#415)

2021.08.1
---------

* don't retry 404s (#406)

2021.07.0
---------

* fix find/glob with a prefix (#399)

2021.06.1
---------

* kwargs to aiohttpClient session
* graceful timeout when disconnecting at finalise (#397)

2021.06.0
---------

* negative ranges in cat_file (#394)

2021.05.0
---------

* no credentials bug fix (#390)
* use googleapis.com (#388)
* more retries (#387, 385, 380)
* Code cleanup (#381)
* license to match stated one (#378)
* deps updated (#376)

Version 2021.04.0
-----------------

* switch to calver and fsspec pin

Version 0.8.0
-------------

* keep up with fsspec 0.9.0 async
* one-shot find
* consistency checkers
* retries for intermittent issues
* timeouts
* partial cat
* http error status
* CI to GHA

Version 0.7.0
-------------

* async operations via aiohttp


Version 0.6.0
-------------

* **API-breaking**: Changed requester-pays handling for ``GCSFileSystem``.

  The ``user_project`` keyword has been removed, and has been replaced with
  the ``requester_pays`` keyword. If you're working with a ``requester_pays`` bucket
  you will need to explicitly pass ``requester_pays-True``. This will include your
  ``project`` ID in requests made to GCS.

Version 0.5.3
-------------

* ``GCSFileSystem`` now validates that the ``project`` provided, if any, matches the
  Google default project when using ``token-'google_default'`` to authenticate (:pr:`219`).
* Fixed bug in ``GCSFileSystem.cat`` on objects in requester-pays buckets (:pr:`217`).

Version 0.5.2
-------------

* Fixed bug in ``user_project`` fallback for default Google authentication (:pr:`213`)

Version 0.5.1
-------------

* ``user_project`` now falls back to the ``project`` if provided (:pr:`208`)

Version 0.5.0
-------------

* Added the ability to make requester-pays requests with the ``user_project`` parameter (:pr:`206`)

Version 0.4.0
-------------

* Improved performance when serializing filesystem objects (:pr:`182`)
* Fixed authorization errors when using ``gcsfs`` within multithreaded code (:pr:`183`, :pr:`192`)
* Added contributing instructions (:pr:`185`)
* Improved performance for :meth:`gcsfs.GCSFileSystem.info` (:pr:`187`)
* Fixed bug in :meth:`gcsfs.GCSFileSystem.info` raising an error (:pr:`190`)

.. raw:: html

    <script data-goatcounter="https://gcsfs.goatcounter.com/count"
        async src="//gc.zgo.at/count.js"></script>
