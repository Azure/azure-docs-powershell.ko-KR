---
title: Docker에서 Azure PowerShell 사용
description: Docker 이미지에 미리 설치된 Azure PowerShell을 사용하는 방법입니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 48935f15241ec965adf4c34d2c17aa670110585a
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715868"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="46170-103">Docker에서 Azure PowerShell 사용</span><span class="sxs-lookup"><span data-stu-id="46170-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="46170-104">Azure PowerShell이 미리 설치된 Docker 이미지를 게시하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46170-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="46170-105">이 문서에서는 Docker 컨테이너에서 Azure PowerShell을 사용하여 시작하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="46170-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="46170-106">사용 가능한 이미지 찾기</span><span class="sxs-lookup"><span data-stu-id="46170-106">Finding available images</span></span>

<span data-ttu-id="46170-107">릴리스된 이미지에는 Docker 17.05 이상 버전이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="46170-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="46170-108">또한 `sudo` 또는 로컬 관리자 권한 없이 Docker를 실행할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46170-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="46170-109">Docker의 공식 [지침][install]에 따라 `docker`를 올바르게 설치하세요.</span><span class="sxs-lookup"><span data-stu-id="46170-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="46170-110">최신 컨테이너 이미지에는 최신 버전의 PowerShell과 Az 모듈에서 지원되는 최신 Azure PowerShell 모듈이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46170-110">The latest container image contains the latest version of PowerShell and the latest Azure PowerShell modules supported with the Az module.</span></span>

<span data-ttu-id="46170-111">Az 모듈이 새로 릴리스될 때마다 다음 운영 체제에 대한 이미지가 릴리스됩니다.</span><span class="sxs-lookup"><span data-stu-id="46170-111">For each new release of the Az module we are releasing an image for the following operating systems:</span></span>

- <span data-ttu-id="46170-112">Ubuntu 18.04(기본값)</span><span class="sxs-lookup"><span data-stu-id="46170-112">Ubuntu 18.04 (default)</span></span>
- <span data-ttu-id="46170-113">Debian 9</span><span class="sxs-lookup"><span data-stu-id="46170-113">Debian 9</span></span>
- <span data-ttu-id="46170-114">CentOs 7</span><span class="sxs-lookup"><span data-stu-id="46170-114">CentOs 7</span></span>

<span data-ttu-id="46170-115">사용 가능한 이미지의 전체 목록은 [Docker 이미지][az image] 페이지에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46170-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="46170-116">컨테이너에서 Azure PowerShell 사용</span><span class="sxs-lookup"><span data-stu-id="46170-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="46170-117">다음 단계에서는 이미지를 다운로드하고 대화형 PowerShell 세션을 시작하는 데 필요한 Docker 명령을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="46170-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="46170-118">최신 azure-powershell 이미지를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="46170-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="46170-119">azure-powershell 컨테이너를 대화형 모드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="46170-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

<span data-ttu-id="46170-120">Windows Docker 호스트의 경우 Windows의 로컬 드라이브를 Linux 컨테이너와 공유할 수 있도록 Docker 파일 공유를 활성화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46170-120">For Windows Docker hosts, you must enable Docker File Sharing to allow local drives on Windows to be shared with Linux containers.</span></span> <span data-ttu-id="46170-121">자세한 내용은 [Windows용 Docker 시작][file-sharing]을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="46170-121">For more information see [Get started with Docker for Windows][file-sharing].</span></span>

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="46170-122">호스트 인증을 사용하여 azure-powershell 컨테이너를 대화형으로 실행</span><span class="sxs-lookup"><span data-stu-id="46170-122">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="46170-123">Azure PowerShell이 Docker를 호스팅하는 시스템에 이미 설치되어 있으면 Azure 자격 증명을 캐시했을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46170-123">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="46170-124">이러한 자격 증명은 Docker 컨테이너에서 실행되는 PowerShell 세션에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46170-124">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="46170-125">캐시된 자격 증명은 기본적으로 호스트의 `$HOME/.Azure` 디렉터리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46170-125">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="46170-126">자격 증명에 액세스하려면 Docker 서비스에서 이 위치에 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46170-126">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="46170-127">다음 명령은 자격 증명 캐시가 탑재된 상태에서 컨테이너를 시작하고 대화형 PowerShell 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="46170-127">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="46170-128">더 이상 필요하지 않은 이미지 제거</span><span class="sxs-lookup"><span data-stu-id="46170-128">Remove the image when no longer needed</span></span>

<span data-ttu-id="46170-129">더 이상 필요하지 않은 경우 다음 명령이 Docker 컨테이너를 삭제하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="46170-129">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="46170-130">다음 단계</span><span class="sxs-lookup"><span data-stu-id="46170-130">Next steps</span></span>

<span data-ttu-id="46170-131">Azure PowerShell 모듈 및 모듈의 기능에 대해 자세히 알아보려면, [Azure PowerShell 시작](get-started-azureps.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="46170-131">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
