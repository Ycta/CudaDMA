#  Copyright 2010 NVIDIA Corporation
#
#  Licensed under the Apache License, Version 2.0 (the "License");
#  you may not use this file except in compliance with the License.
#  You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
#  Unless required by applicable law or agreed to in writing, software
#  distributed under the License is distributed on an "AS IS" BASIS,
#  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#  See the License for the specific language governing permissions and
#  limitations under the License.

all: test_sequential

test_sequential: ../../../include/cudaDMA.h cudaDMA_test_sequential.cu
	nvcc -I../../../include -o test_sequential -O2 -arch=compute_20 cudaDMA_test_sequential.cu 

ts2: ../../../include/cudaDMAv2.h cudaDMA_test_sequential_v2.cu
	nvcc -I ../../../include -o test_sequential -O2 -arch=compute_20 cudaDMA_test_sequential_v2.cu

ts2_k20: ../../../include/cudaDMAv2.h cudaDMA_test_sequential_v2.cu
	nvcc -I ../../../include -o test_sequential -O2 -arch=compute_35 cudaDMA_test_sequential_v2.cu

clean:
	rm -f *.o test_sequential
