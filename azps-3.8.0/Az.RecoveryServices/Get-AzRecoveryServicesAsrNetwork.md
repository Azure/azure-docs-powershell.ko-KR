---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877437"
---
# <span data-ttu-id="6af85-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="6af85-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="6af85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6af85-102">SYNOPSIS</span></span>
<span data-ttu-id="6af85-103">현재 자격 증명 모음의 사이트 복구에서 관리 되는 네트워크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6af85-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="6af85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6af85-104">SYNTAX</span></span>

### <span data-ttu-id="6af85-105">ByFabricObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="6af85-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6af85-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6af85-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6af85-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6af85-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6af85-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6af85-108">DESCRIPTION</span></span>
<span data-ttu-id="6af85-109">**AzRecoveryServicesAsrNetwork** cmdlet은 현재 Azure site recovery 자격 증명 모음에 대 한 Azure site recovery 네트워크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6af85-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="6af85-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6af85-110">EXAMPLES</span></span>

### <span data-ttu-id="6af85-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6af85-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="6af85-112">지정 된 패브릭의 알려진 모든 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6af85-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="6af85-113">변수</span><span class="sxs-lookup"><span data-stu-id="6af85-113">PARAMETERS</span></span>

### <span data-ttu-id="6af85-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6af85-114">-DefaultProfile</span></span>
<span data-ttu-id="6af85-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6af85-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af85-116">-패브릭</span><span class="sxs-lookup"><span data-stu-id="6af85-116">-Fabric</span></span>
<span data-ttu-id="6af85-117">ASR fabric 개체</span><span class="sxs-lookup"><span data-stu-id="6af85-117">ASR fabric object</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6af85-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6af85-118">-FriendlyName</span></span>
<span data-ttu-id="6af85-119">네트워크 ASR 개체의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6af85-119">Friendly name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af85-120">-이름</span><span class="sxs-lookup"><span data-stu-id="6af85-120">-Name</span></span>
<span data-ttu-id="6af85-121">네트워크 ASR 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6af85-121">Name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af85-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6af85-122">CommonParameters</span></span>
<span data-ttu-id="6af85-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af85-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6af85-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6af85-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6af85-125">입력</span><span class="sxs-lookup"><span data-stu-id="6af85-125">INPUTS</span></span>

### <span data-ttu-id="6af85-126">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="6af85-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="6af85-127">출력</span><span class="sxs-lookup"><span data-stu-id="6af85-127">OUTPUTS</span></span>

### <span data-ttu-id="6af85-128">SiteRecovery. r m/. m g 네트워크</span><span class="sxs-lookup"><span data-stu-id="6af85-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="6af85-129">상속자</span><span class="sxs-lookup"><span data-stu-id="6af85-129">NOTES</span></span>

## <span data-ttu-id="6af85-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6af85-130">RELATED LINKS</span></span>
