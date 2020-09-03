---
title: Docker에서 Azure PowerShell 사용
description: Docker 이미지에 미리 설치된 Azure PowerShell을 사용하는 방법입니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2b487abeecbffa6cd8b7b64276ab301619348385
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239862"
---
# <a name="using-azure-powershell-in-docker"></a>Docker에서 Azure PowerShell 사용

Azure PowerShell이 미리 설치된 Docker 이미지를 게시하고 있습니다. 이 문서에서는 Docker 컨테이너에서 Azure PowerShell을 사용하여 시작하는 방법을 보여 줍니다.

## <a name="finding-available-images"></a>사용 가능한 이미지 찾기

릴리스된 이미지에는 Docker 17.05 이상 버전이 필요합니다. 또한 `sudo` 또는 로컬 관리자 권한 없이 Docker를 실행할 수 있어야 합니다. Docker의 공식 [지침][install]에 따라 `docker`를 올바르게 설치하세요.

최신 컨테이너 이미지에는 최신 버전의 PowerShell과 Az 모듈에서 지원되는 최신 Azure PowerShell 모듈이 포함되어 있습니다.

Az 모듈이 새로 릴리스될 때마다 다음 운영 체제에 대한 이미지가 릴리스됩니다.

- Ubuntu 18.04(기본값)
- Debian 9
- CentOs 7

사용 가능한 이미지의 전체 목록은 [Docker 이미지][az image] 페이지에서 찾을 수 있습니다.

## <a name="using-azure-powershell-in-a-container"></a>컨테이너에서 Azure PowerShell 사용

다음 단계는 이미지를 다운로드하고 대화형 PowerShell 세션을 시작하는 데 필요한 Docker 명령을 보여 줍니다.

1. 최신 azure-powershell 이미지를 다운로드합니다.

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. azure-powershell 컨테이너를 대화형 모드에서 실행합니다.

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

Windows Docker 호스트의 경우 Windows의 로컬 드라이브를 Linux 컨테이너와 공유할 수 있도록 Docker 파일 공유를 활성화해야 합니다. 자세한 내용은 [Windows용 Docker 시작][file-sharing]을 참조하세요.

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a>호스트 인증을 사용하여 azure-powershell 컨테이너를 대화형으로 실행

Azure PowerShell이 Docker를 호스팅하는 시스템에 이미 설치되어 있으면 Azure 자격 증명을 캐시했을 수 있습니다. 이러한 자격 증명은 Docker 컨테이너에서 실행되는 PowerShell 세션에서 사용할 수 있습니다.

캐시된 자격 증명은 기본적으로 호스트의 `$HOME/.Azure` 디렉터리에 있습니다. 자격 증명에 액세스하려면 Docker 서비스에서 이 위치에 액세스할 수 있어야 합니다. 다음 명령은 자격 증명 캐시가 탑재된 상태에서 컨테이너를 시작하고 대화형 PowerShell 세션을 시작합니다.

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a>더 이상 필요하지 않은 이미지 제거

다음 명령은 더 이상 필요하지 않을 경우 Docker 컨테이너를 삭제하는 데 사용됩니다.

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a>다음 단계

Azure PowerShell 모듈 및 모듈의 기능에 대해 자세히 알아보려면, [Azure PowerShell 시작](get-started-azureps.md)을 참조하세요.

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
