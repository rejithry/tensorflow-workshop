# Copyright 2016 Google Inc. All Rights Reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
FROM gcr.io/tensorflow/tensorflow:latest-devel

RUN pip install --upgrade pip
RUN apt-get update
RUN apt-get install -y python-scipy
RUN pip install sklearn

ADD download_git_repo.py download_git_repo.py

# TensorBoard
EXPOSE 6006
# IPython
EXPOSE 8888

CMD ["sh", "-c", "python download_git_repo.py ; /bin/bash"]