---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 3a28545958e353c5a5523e24baf20ac6bff21ef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703661"
---
# <span data-ttu-id="a3082-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="a3082-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="a3082-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3082-102">SYNOPSIS</span></span>
<span data-ttu-id="a3082-103">현재 자격 증명 모음의 사이트 복구에서 관리 되는 네트워크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3082-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3082-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a3082-104">SYNTAX</span></span>

### <span data-ttu-id="a3082-105">ByFabricObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="a3082-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="a3082-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a3082-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="a3082-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a3082-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="a3082-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a3082-108">DESCRIPTION</span></span>
<span data-ttu-id="a3082-109">**AzureRmRecoveryServicesAsrNetwork** cmdlet은 현재 Azure site recovery 자격 증명 모음에 대 한 Azure site recovery 네트워크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3082-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="a3082-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a3082-110">EXAMPLES</span></span>

### <span data-ttu-id="a3082-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3082-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="a3082-112">지정 된 패브릭의 알려진 모든 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3082-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="a3082-113">변수</span><span class="sxs-lookup"><span data-stu-id="a3082-113">PARAMETERS</span></span>

### <span data-ttu-id="a3082-114">-패브릭</span><span class="sxs-lookup"><span data-stu-id="a3082-114">-Fabric</span></span>
<span data-ttu-id="a3082-115">ASR fabric 개체</span><span class="sxs-lookup"><span data-stu-id="a3082-115">ASR fabric object</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3082-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a3082-116">-FriendlyName</span></span>
<span data-ttu-id="a3082-117">네트워크 ASR 개체의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3082-117">Friendly name of network ASR object.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3082-118">-이름</span><span class="sxs-lookup"><span data-stu-id="a3082-118">-Name</span></span>
<span data-ttu-id="a3082-119">네트워크 ASR 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3082-119">Name of network ASR object.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3082-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3082-120">CommonParameters</span></span>
<span data-ttu-id="a3082-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3082-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3082-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3082-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3082-123">입력</span><span class="sxs-lookup"><span data-stu-id="a3082-123">INPUTS</span></span>

### <span data-ttu-id="a3082-124">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="a3082-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="a3082-125">출력</span><span class="sxs-lookup"><span data-stu-id="a3082-125">OUTPUTS</span></span>

### <span data-ttu-id="a3082-126">System.webserver. t e r ' 1 [[SiteRecovery], [[Microsoft Azure. SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]],,.</span><span class="sxs-lookup"><span data-stu-id="a3082-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a3082-127">상속자</span><span class="sxs-lookup"><span data-stu-id="a3082-127">NOTES</span></span>

## <span data-ttu-id="a3082-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3082-128">RELATED LINKS</span></span>

