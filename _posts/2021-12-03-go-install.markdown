
---
layout: post
title:  "Go를 알고! 설치하고! 설정 하자!"
date:   2021-12-03 21:34:14 +0900
categories: Go
---
새로운 프로젝트를 시작할때 고려해야 할 많은 요소들이 있지만 개발 언어 선택은 그 중에서도 매우 중요한 결정입니다.
급속도로 발전하는 IT 트랜드에 맞춰 빠르게 진화하고 이에 따라 이전 기술에 보안점을 더하면서도 자신의 특기를 명확하게 뽐내는 새로운 언어들 또한 등장 하고 있습니다.
이러한 상황에서 수많은 언어들중 어떤 언어를 선택 하느냐는 심히 고민에 빠지게 합니다.
자신의 필살기 언어도 중요하지만 트랜디함을 놓쳐서는 결국 도퇴할 수 밖에 없다고 생각합니다.

그런 의미에서 오늘 제가 소개시켜 드릴 언어는 `Go언어` 입니다.
저에게 Go란 어느 순간부터 채용 공고, 신규 프로젝트에 자주 등장하는 언어였는데요. 벌써 Go를 사용하여 프로젝트를 진행한지 언 1년 가까이 되어가네요.
늦었지만 지금 부터 `Go`를 소개 하겠습니다. Let's `Go` :)

``` 
[What is Golang]
고(Go) 는 2009년에 구글에서 처음 발표된 후 2012년 3월에 정식 발표된 프로그래밍 언어 입니다. 
C++의 복잡함이 싫어서 만들어진 언어로서 특징으로 compile언어지만 컴파일러의 컴파일 속도가 빨라 인터프리터 언어처럼 사용 할 수 있다는 점입니다. 
단순함과 실용성을 지향하고 있어 언어에서 사용하는 키워드도 25개 밖에 되지 않습니다. 
가장 큰 단점으로는 bytecode를 생성하여 실행하는 언어가 아니므로, 바이너리를 배포할 경우 C/C++ 처럼 각각의 플랫폼에 맞게 컴파일을 해줘야 합니다.
```

Go 설치 하기
============= 

Go는 다수의 OS를 지원합니다. 해당 되는 OS에 맞춰 설치하고 버전 정보를 통해 잘 설치 되었는지 확인 해 보도록 하겠습니다.

Windows 설치
------------

1. https://go.dev/dl/ 링크로 이동하여 `Featured downloads` 항목에 `Microsoft Windows` 설치 파일을 다운로드 합니다.

> ![windows_download](../assets/go_windows_down.png)

2. 다운받은 설치 파일을 실행하여 설치 합니다.

> ![windows_download](../assets/go_window_msi.png)
3. 설치가 완료 되었으면 명령 프롬프트를 실행하여 버전 정보를 통해 제대로 설치 되었는지 확인합니다. 

> ``` 
>  > go version
>  > go evn 


MacOS
------

1. Go 설치
> ``` 
>  $ brew install go

2. 버전 및 환경변수 확인
> ``` 
> $ go version
> $ go env


Linux
------

1. Linux는 Go설치와 동시에 환경 설정을 같이 진행 하였습니다. 
> ```
> $ GO_VERSION=1.17.1
> $ curl -LO https://dl.google.com/go/go${GO_VERSION}.linux-amd64.tar.gz
> $ rm -rf /usr/local/go && tar -C /usr/local -xzf go${GO_VERSION}.linux-amd64.tar.gz
> $ cat ~/.profile | grep /usr/local/go/bin || echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.profile
> $ cat ~/.profile | grep GOPATH= || echo 'export GOPATH=$(go env GOPATH)' >> ~/.profile
> $ cat ~/.profile | grep GOPATH/bin || echo 'export PATH=$PATH:$GOPATH/bin' >> ~/.profile
> $ source ~/.profile
> $ echo $GOPATH
> $ go version

2. 이대로만 하면 Go설치와 설정이 동시에 환경설정도 되었습니다. 확인 해볼까요?
> ```
> $ go env


이렇게 `Go` 설치를 해봤는데요. 이제 Go를 설치 하였으니 프로젝트에 Go를 사용하여 어떤 개발을 하였는지 알아볼께요. 
다음 글로 Let's `Go` :)
