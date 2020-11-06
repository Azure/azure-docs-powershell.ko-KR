---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: b209c706a8da88cfc5188b11302166469749c33f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536224"
---
# <span data-ttu-id="b8560-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b8560-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="b8560-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8560-102">SYNOPSIS</span></span>
<span data-ttu-id="b8560-103">ASR 보호 컨테이너에서 보호 가능한 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8560-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8560-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8560-104">SYNTAX</span></span>

### <span data-ttu-id="b8560-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="b8560-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="b8560-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="b8560-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="b8560-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b8560-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="b8560-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b8560-108">DESCRIPTION</span></span>
<span data-ttu-id="b8560-109">**AzureRmRecoveryServicesAsrProtectableItem** Cmdlet은 Azure Site Recovery 보호 컨테이너에서 보호 가능한 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8560-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="b8560-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b8560-110">EXAMPLES</span></span>

### <span data-ttu-id="b8560-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8560-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="b8560-112">지정 된 ASR 보호 컨테이너의 보호 가능한 모든 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8560-112">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="b8560-113">변수</span><span class="sxs-lookup"><span data-stu-id="b8560-113">PARAMETERS</span></span>

### <span data-ttu-id="b8560-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b8560-114">-FriendlyName</span></span>
<span data-ttu-id="b8560-115">ASR 보호 가능한 항목의 대화명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8560-115">Specifies the friendly name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8560-116">-이름</span><span class="sxs-lookup"><span data-stu-id="b8560-116">-Name</span></span>
<span data-ttu-id="b8560-117">ASR 보호 가능한 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8560-117">Specifies the name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8560-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b8560-118">-ProtectionContainer</span></span>
<span data-ttu-id="b8560-119">Azure Site Recovery 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8560-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8560-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8560-120">CommonParameters</span></span>
<span data-ttu-id="b8560-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8560-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8560-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8560-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8560-123">입력</span><span class="sxs-lookup"><span data-stu-id="b8560-123">INPUTS</span></span>

### <span data-ttu-id="b8560-124">SiteRecovery. ASRProtectionContainer에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="b8560-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="b8560-125">출력</span><span class="sxs-lookup"><span data-stu-id="b8560-125">OUTPUTS</span></span>

### <span data-ttu-id="b8560-126">System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRProtectableItem, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="b8560-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b8560-127">상속자</span><span class="sxs-lookup"><span data-stu-id="b8560-127">NOTES</span></span>

## <span data-ttu-id="b8560-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8560-128">RELATED LINKS</span></span>

[<span data-ttu-id="b8560-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b8560-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="b8560-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b8560-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)
