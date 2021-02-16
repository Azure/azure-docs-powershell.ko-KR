---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: da9dd3d7b1ed0a54a34fdf5c8a0c9d65b507a07b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411843"
---
# <span data-ttu-id="8aed2-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8aed2-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="8aed2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aed2-102">SYNOPSIS</span></span>
<span data-ttu-id="8aed2-103">ASR 보호 컨테이너에서 보호 가능한 항목을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aed2-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="8aed2-104">구문</span><span class="sxs-lookup"><span data-stu-id="8aed2-104">SYNTAX</span></span>

### <span data-ttu-id="8aed2-105">ByObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="8aed2-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aed2-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="8aed2-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aed2-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8aed2-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8aed2-108">설명</span><span class="sxs-lookup"><span data-stu-id="8aed2-108">DESCRIPTION</span></span>
<span data-ttu-id="8aed2-109">**Get-AzRecoveryServicesAsrProtectableItem** cmdlet은 Azure Site Recovery Protection 컨테이너에서 보호 가능한 항목을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aed2-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="8aed2-110">예제</span><span class="sxs-lookup"><span data-stu-id="8aed2-110">EXAMPLES</span></span>

### <span data-ttu-id="8aed2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8aed2-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="8aed2-112">지정된 ASR 보호 컨테이너에 있는 보호 가능한 모든 항목을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aed2-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="8aed2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="8aed2-113">Example 2</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -FriendlyName $piFriendlyName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="8aed2-114">지정된 ASR 보호 컨테이너 및 지정된 친숙한 이름으로 보호 가능한 항목을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aed2-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="8aed2-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="8aed2-115">Example 3</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -Name $piName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="8aed2-116">지정된 ASR 보호 컨테이너에 있는 보호 가능한 모든 항목을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aed2-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="8aed2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8aed2-117">PARAMETERS</span></span>

### <span data-ttu-id="8aed2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aed2-118">-DefaultProfile</span></span>
<span data-ttu-id="8aed2-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8aed2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8aed2-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8aed2-120">-FriendlyName</span></span>
<span data-ttu-id="8aed2-121">ASR 보호 가능한 항목의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8aed2-121">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="8aed2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8aed2-122">-Name</span></span>
<span data-ttu-id="8aed2-123">ASR 보호 가능한 항목의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8aed2-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="8aed2-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8aed2-124">-ProtectionContainer</span></span>
<span data-ttu-id="8aed2-125">Azure Site Recovery Protection 컨테이너 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8aed2-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8aed2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aed2-126">CommonParameters</span></span>
<span data-ttu-id="8aed2-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8aed2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aed2-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8aed2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aed2-129">입력</span><span class="sxs-lookup"><span data-stu-id="8aed2-129">INPUTS</span></span>

### <span data-ttu-id="8aed2-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8aed2-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="8aed2-131">출력</span><span class="sxs-lookup"><span data-stu-id="8aed2-131">OUTPUTS</span></span>

### <span data-ttu-id="8aed2-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8aed2-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="8aed2-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8aed2-133">NOTES</span></span>

## <span data-ttu-id="8aed2-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8aed2-134">RELATED LINKS</span></span>


