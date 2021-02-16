---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a5701fc6308f1884bbf0237887a223a62a58669
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411588"
---
# <span data-ttu-id="f5cd1-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="f5cd1-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="f5cd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="f5cd1-103">현재 자격 증명 모음에 대한 Site Recovery에서 관리하는 네트워크에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f5cd1-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="f5cd1-104">구문</span><span class="sxs-lookup"><span data-stu-id="f5cd1-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f5cd1-105">설명</span><span class="sxs-lookup"><span data-stu-id="f5cd1-105">DESCRIPTION</span></span>
<span data-ttu-id="f5cd1-106">**Get-AzureSiteRecoveryNetwork** cmdlet은 현재 Site Recovery 자격 증명 모음에 대한 Azure Site Recovery 네트워크에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f5cd1-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="f5cd1-107">예제</span><span class="sxs-lookup"><span data-stu-id="f5cd1-107">EXAMPLES</span></span>

### <span data-ttu-id="f5cd1-108">예제 1: 사이트 복구 네트워크 얻기</span><span class="sxs-lookup"><span data-stu-id="f5cd1-108">Example 1: Get site recovery networks</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetwork -Server $Servers[0]
Name                : phase2RecoveryVMNetwork
ID                  : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
FabricObjectID      : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}

Name                : phase2PrimaryVMNetwork
ID                  : d903e2c6-3141-4cef-bfe1-04616cd43cbb
FabricObjectID      : d903e2c6-3141-4cef-bfe1-04616cd43cbb
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}
```

<span data-ttu-id="f5cd1-109">첫 번째 명령 cmdlet은 **Get-AzureSiteRecoveryServer** cmdlet을 사용하여 현재 Azure Site Recovery 자격 증명 모음에 대한 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f5cd1-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="f5cd1-110">이 명령은 Site Recovery 서버를 $Servers 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cd1-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="f5cd1-111">두 번째 명령은 $Servers 배열의 첫 번째 서버에 대한 사이트 복구 네트워크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f5cd1-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="f5cd1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5cd1-112">PARAMETERS</span></span>

### <span data-ttu-id="f5cd1-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="f5cd1-113">-Profile</span></span>
<span data-ttu-id="f5cd1-114">이 cmdlet이 읽을 Azure 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cd1-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f5cd1-115">프로필을 지정하지 않으면 이 cmdlet은 로컬 기본 프로필에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f5cd1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5cd1-116">-Server</span><span class="sxs-lookup"><span data-stu-id="f5cd1-116">-Server</span></span>
<span data-ttu-id="f5cd1-117">Site Recovery 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cd1-117">Specifies a Site Recovery server.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5cd1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5cd1-118">CommonParameters</span></span>
<span data-ttu-id="f5cd1-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cd1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5cd1-120">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f5cd1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5cd1-121">입력</span><span class="sxs-lookup"><span data-stu-id="f5cd1-121">INPUTS</span></span>

## <span data-ttu-id="f5cd1-122">출력</span><span class="sxs-lookup"><span data-stu-id="f5cd1-122">OUTPUTS</span></span>

## <span data-ttu-id="f5cd1-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f5cd1-123">NOTES</span></span>

## <span data-ttu-id="f5cd1-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5cd1-124">RELATED LINKS</span></span>




