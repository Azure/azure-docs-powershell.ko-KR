---
title: Docker에서 Azure PowerShell 사용
description: Docker 이미지에 미리 설치된 Azure PowerShell을 사용하는 방법입니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a5746b71cfc41f7c6283b0e95b0940ca4b594ec7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402683"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="87004-103">Docker에서 Azure PowerShell 사용</span><span class="sxs-lookup"><span data-stu-id="87004-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="87004-104">Azure PowerShell이 미리 설치된 Docker 이미지를 게시하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87004-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="87004-105">이 문서에서는 Docker 컨테이너에서 Azure PowerShell을 사용하여 시작하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="87004-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="87004-106">사용 가능한 이미지 찾기</span><span class="sxs-lookup"><span data-stu-id="87004-106">Finding available images</span></span>

<span data-ttu-id="87004-107">릴리스된 이미지에는 Docker 17.05 이상 버전이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="87004-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="87004-108">또한 `sudo` 또는 로컬 관리자 권한 없이 Docker를 실행할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="87004-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="87004-109">Docker의 공식 [지침][install]에 따라 `docker`를 올바르게 설치하세요.</span><span class="sxs-lookup"><span data-stu-id="87004-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="87004-110">릴리스된 컨테이너는 공식 PowerShell 컨테이너에서 빌드된 다음, Az 모듈이 계층으로 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="87004-110">The released containers are built from the official PowerShell containers, then the Az module added as a layer.</span></span>

<span data-ttu-id="87004-111">안정적인 최신 이미지에 포함된 항목은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="87004-111">The latest stable image includes:</span></span>

- <span data-ttu-id="87004-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="87004-112">Ubuntu 18.04</span></span>
- <span data-ttu-id="87004-113">PowerShell 버전 6.2.4</span><span class="sxs-lookup"><span data-stu-id="87004-113">PowerShell version 6.2.4</span></span>
- <span data-ttu-id="87004-114">Azure PowerShell 최신 Az 모듈</span><span class="sxs-lookup"><span data-stu-id="87004-114">Azure PowerShell most current Az module</span></span>

<span data-ttu-id="87004-115">사용 가능한 이미지의 전체 목록은 [Docker 이미지][az image] 페이지에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87004-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="87004-116">컨테이너에서 Azure PowerShell 사용</span><span class="sxs-lookup"><span data-stu-id="87004-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="87004-117">다음 단계에서는 이미지를 다운로드하고 대화형 PowerShell 세션을 시작하는 데 필요한 Docker 명령을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="87004-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="87004-118">최신 azure-powershell 이미지를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="87004-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="87004-119">azure-powershell 컨테이너를 대화형 모드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="87004-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="87004-120">호스트 인증을 사용하여 azure-powershell 컨테이너를 대화형으로 실행</span><span class="sxs-lookup"><span data-stu-id="87004-120">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="87004-121">Azure PowerShell이 Docker를 호스팅하는 시스템에 이미 설치되어 있으면 Azure 자격 증명을 캐시했을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87004-121">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="87004-122">이러한 자격 증명은 Docker 컨테이너에서 실행되는 PowerShell 세션에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87004-122">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="87004-123">캐시된 자격 증명은 기본적으로 호스트의 `$HOME/.Azure` 디렉터리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87004-123">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="87004-124">자격 증명에 액세스하려면 Docker 서비스에서 이 위치에 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="87004-124">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="87004-125">다음 명령은 자격 증명 캐시가 탑재된 상태에서 컨테이너를 시작하고 대화형 PowerShell 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="87004-125">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="87004-126">더 이상 필요하지 않은 이미지 제거</span><span class="sxs-lookup"><span data-stu-id="87004-126">Remove the image when no longer needed</span></span>

<span data-ttu-id="87004-127">더 이상 필요하지 않은 경우 다음 명령이 Docker 컨테이너를 삭제하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="87004-127">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="87004-128">다음 단계</span><span class="sxs-lookup"><span data-stu-id="87004-128">Next steps</span></span>

<span data-ttu-id="87004-129">Azure PowerShell 모듈 및 모듈의 기능에 대해 자세히 알아보려면, [Azure PowerShell 시작](get-started-azureps.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="87004-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell