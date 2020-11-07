---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: af4dbdbb2741850cdb01eb88e321f80a4844919a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699722"
---
# <span data-ttu-id="e47b7-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e47b7-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="e47b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e47b7-102">SYNOPSIS</span></span>
<span data-ttu-id="e47b7-103">Azure Site Recovery 복제 보호 항목의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e47b7-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

## <span data-ttu-id="e47b7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e47b7-104">SYNTAX</span></span>

### <span data-ttu-id="e47b7-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="e47b7-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e47b7-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e47b7-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e47b7-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e47b7-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e47b7-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="e47b7-108">ByProtectableItemObject</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e47b7-109">설명은</span><span class="sxs-lookup"><span data-stu-id="e47b7-109">DESCRIPTION</span></span>
<span data-ttu-id="e47b7-110">**AzRecoveryServicesAsrReplicationProtectedItem** cmdlet은 지정 된 asr 보호 컨테이너에서 모든 또는 지정 된 asr 복제 보호 항목의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e47b7-110">The **Get-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="e47b7-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e47b7-111">EXAMPLES</span></span>

### <span data-ttu-id="e47b7-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e47b7-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="e47b7-113">지정 된 ASR 보호 컨테이너에서 모든 복제 보호 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="e47b7-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="e47b7-114">변수</span><span class="sxs-lookup"><span data-stu-id="e47b7-114">PARAMETERS</span></span>

### <span data-ttu-id="e47b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e47b7-115">-DefaultProfile</span></span>
<span data-ttu-id="e47b7-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e47b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e47b7-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e47b7-117">-FriendlyName</span></span>
<span data-ttu-id="e47b7-118">가져올 복제 보호 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e47b7-118">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="e47b7-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e47b7-119">-Name</span></span>
<span data-ttu-id="e47b7-120">가져올 복제 보호 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e47b7-120">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="e47b7-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e47b7-121">-ProtectableItem</span></span>
<span data-ttu-id="e47b7-122">ASR 보호 가능한 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e47b7-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="e47b7-123">Cmdlet은 항목이 보호 되는 경우 지정 된 ASR 보호 가능한 항목에 해당 하는 ASR 복제 보호 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e47b7-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

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

### <span data-ttu-id="e47b7-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e47b7-124">-ProtectionContainer</span></span>
<span data-ttu-id="e47b7-125">복제 보호 항목에 해당 하는 ASR 보호 컨테이너의 ASR 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e47b7-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

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

### <span data-ttu-id="e47b7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e47b7-126">CommonParameters</span></span>
<span data-ttu-id="e47b7-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e47b7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e47b7-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e47b7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e47b7-129">입력</span><span class="sxs-lookup"><span data-stu-id="e47b7-129">INPUTS</span></span>

### <span data-ttu-id="e47b7-130">SiteRecovery. ASRProtectionContainer에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="e47b7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

### <span data-ttu-id="e47b7-131">SiteRecovery. ASRProtectableItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="e47b7-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="e47b7-132">출력</span><span class="sxs-lookup"><span data-stu-id="e47b7-132">OUTPUTS</span></span>

### <span data-ttu-id="e47b7-133">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="e47b7-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e47b7-134">상속자</span><span class="sxs-lookup"><span data-stu-id="e47b7-134">NOTES</span></span>

## <span data-ttu-id="e47b7-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e47b7-135">RELATED LINKS</span></span>

[<span data-ttu-id="e47b7-136">새로운 AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e47b7-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="e47b7-137">제거-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e47b7-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="e47b7-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e47b7-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
