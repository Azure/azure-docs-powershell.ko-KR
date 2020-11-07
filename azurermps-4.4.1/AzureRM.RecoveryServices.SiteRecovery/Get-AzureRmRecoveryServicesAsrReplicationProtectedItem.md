---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fbd2f518d3bdcf64599e32b55cdb9f416c29be21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537020"
---
# <span data-ttu-id="6d7ec-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6d7ec-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="6d7ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="6d7ec-103">Azure Site Recovery 복제 보호 항목의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6d7ec-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d7ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d7ec-104">SYNTAX</span></span>

### <span data-ttu-id="6d7ec-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="6d7ec-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="6d7ec-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="6d7ec-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="6d7ec-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6d7ec-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="6d7ec-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="6d7ec-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [<CommonParameters>]
```

## <span data-ttu-id="6d7ec-109">설명은</span><span class="sxs-lookup"><span data-stu-id="6d7ec-109">DESCRIPTION</span></span>
<span data-ttu-id="6d7ec-110">**AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet은 지정 된 asr 보호 컨테이너에서 모든 또는 지정 된 asr 복제 보호 항목의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6d7ec-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="6d7ec-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6d7ec-111">EXAMPLES</span></span>

### <span data-ttu-id="6d7ec-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d7ec-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="6d7ec-113">지정 된 ASR 보호 컨테이너에서 모든 복제 보호 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d7ec-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="6d7ec-114">변수</span><span class="sxs-lookup"><span data-stu-id="6d7ec-114">PARAMETERS</span></span>

### <span data-ttu-id="6d7ec-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6d7ec-115">-FriendlyName</span></span>
<span data-ttu-id="6d7ec-116">가져올 복제 보호 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d7ec-116">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="6d7ec-117">-이름</span><span class="sxs-lookup"><span data-stu-id="6d7ec-117">-Name</span></span>
<span data-ttu-id="6d7ec-118">가져올 복제 보호 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d7ec-118">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="6d7ec-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6d7ec-119">-ProtectableItem</span></span>
<span data-ttu-id="6d7ec-120">ASR 보호 가능한 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d7ec-120">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="6d7ec-121">Cmdlet은 항목이 보호 되는 경우 지정 된 ASR 보호 가능한 항목에 해당 하는 ASR 복제 보호 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6d7ec-121">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d7ec-122">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6d7ec-122">-ProtectionContainer</span></span>
<span data-ttu-id="6d7ec-123">복제 보호 항목에 해당 하는 ASR 보호 컨테이너의 ASR 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d7ec-123">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d7ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d7ec-124">CommonParameters</span></span>
<span data-ttu-id="6d7ec-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d7ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d7ec-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d7ec-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d7ec-127">입력</span><span class="sxs-lookup"><span data-stu-id="6d7ec-127">INPUTS</span></span>

### <span data-ttu-id="6d7ec-128">SiteRecovery. ASRProtectionContainer에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="6d7ec-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="6d7ec-129">SiteRecovery. ASRProtectableItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="6d7ec-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="6d7ec-130">출력</span><span class="sxs-lookup"><span data-stu-id="6d7ec-130">OUTPUTS</span></span>

### <span data-ttu-id="6d7ec-131">System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRReplicationProtectedItem, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="6d7ec-131">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6d7ec-132">상속자</span><span class="sxs-lookup"><span data-stu-id="6d7ec-132">NOTES</span></span>

## <span data-ttu-id="6d7ec-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d7ec-133">RELATED LINKS</span></span>

[<span data-ttu-id="6d7ec-134">새로운 AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6d7ec-134">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="6d7ec-135">제거-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6d7ec-135">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="6d7ec-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6d7ec-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)