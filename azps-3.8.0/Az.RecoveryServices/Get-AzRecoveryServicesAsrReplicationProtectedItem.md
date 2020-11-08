---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 3c89133b18f1425f65ab9430765f0a2a9a7cfafe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034363"
---
# <span data-ttu-id="95f77-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="95f77-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="95f77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95f77-102">SYNOPSIS</span></span>
<span data-ttu-id="95f77-103">Azure Site Recovery 복제 보호 항목의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95f77-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

## <span data-ttu-id="95f77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95f77-104">SYNTAX</span></span>

### <span data-ttu-id="95f77-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="95f77-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f77-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="95f77-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f77-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="95f77-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f77-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="95f77-108">ByProtectableItemObject</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95f77-109">설명은</span><span class="sxs-lookup"><span data-stu-id="95f77-109">DESCRIPTION</span></span>
<span data-ttu-id="95f77-110">**AzRecoveryServicesAsrReplicationProtectedItem** cmdlet은 지정 된 asr 보호 컨테이너에서 모든 또는 지정 된 asr 복제 보호 항목의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95f77-110">The **Get-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="95f77-111">예제의</span><span class="sxs-lookup"><span data-stu-id="95f77-111">EXAMPLES</span></span>

### <span data-ttu-id="95f77-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="95f77-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="95f77-113">지정 된 ASR 보호 컨테이너에서 모든 복제 보호 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="95f77-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="95f77-114">변수</span><span class="sxs-lookup"><span data-stu-id="95f77-114">PARAMETERS</span></span>

### <span data-ttu-id="95f77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f77-115">-DefaultProfile</span></span>
<span data-ttu-id="95f77-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95f77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="95f77-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="95f77-117">-FriendlyName</span></span>
<span data-ttu-id="95f77-118">가져올 복제 보호 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95f77-118">Specifies the friendly name of the replication protected item to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f77-119">-이름</span><span class="sxs-lookup"><span data-stu-id="95f77-119">-Name</span></span>
<span data-ttu-id="95f77-120">가져올 복제 보호 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95f77-120">Specifies the name of the replication protected item to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f77-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="95f77-121">-ProtectableItem</span></span>
<span data-ttu-id="95f77-122">ASR 보호 가능한 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95f77-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="95f77-123">Cmdlet은 항목이 보호 되는 경우 지정 된 ASR 보호 가능한 항목에 해당 하는 ASR 복제 보호 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95f77-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95f77-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="95f77-124">-ProtectionContainer</span></span>
<span data-ttu-id="95f77-125">복제 보호 항목에 해당 하는 ASR 보호 컨테이너의 ASR 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95f77-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95f77-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f77-126">CommonParameters</span></span>
<span data-ttu-id="95f77-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95f77-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f77-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95f77-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f77-129">입력</span><span class="sxs-lookup"><span data-stu-id="95f77-129">INPUTS</span></span>

### <span data-ttu-id="95f77-130">SiteRecovery. ASRProtectionContainer에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="95f77-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

### <span data-ttu-id="95f77-131">SiteRecovery. ASRProtectableItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="95f77-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="95f77-132">출력</span><span class="sxs-lookup"><span data-stu-id="95f77-132">OUTPUTS</span></span>

### <span data-ttu-id="95f77-133">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="95f77-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="95f77-134">상속자</span><span class="sxs-lookup"><span data-stu-id="95f77-134">NOTES</span></span>

## <span data-ttu-id="95f77-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95f77-135">RELATED LINKS</span></span>

[<span data-ttu-id="95f77-136">새로운 AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="95f77-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="95f77-137">제거-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="95f77-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="95f77-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="95f77-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
