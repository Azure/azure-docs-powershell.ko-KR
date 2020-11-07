---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 4ea8bcb0e27c9ca44cc30f36005bdcccdbd20d61
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699732"
---
# <span data-ttu-id="bed8e-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="bed8e-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="bed8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bed8e-102">SYNOPSIS</span></span>
<span data-ttu-id="bed8e-103">ASR 보호 컨테이너에서 보호 가능한 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="bed8e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bed8e-104">SYNTAX</span></span>

### <span data-ttu-id="bed8e-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="bed8e-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bed8e-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="bed8e-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bed8e-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="bed8e-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bed8e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bed8e-108">DESCRIPTION</span></span>
<span data-ttu-id="bed8e-109">**AzRecoveryServicesAsrProtectableItem** Cmdlet은 Azure Site Recovery 보호 컨테이너에서 보호 가능한 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="bed8e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bed8e-110">EXAMPLES</span></span>

### <span data-ttu-id="bed8e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bed8e-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="bed8e-112">지정 된 ASR 보호 컨테이너의 보호 가능한 모든 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="bed8e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="bed8e-113">Example 2</span></span>
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

<span data-ttu-id="bed8e-114">지정 된 ASR 보호 컨테이너에서 보호 되는 항목을 가져오고 제공 된 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="bed8e-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="bed8e-115">Example 3</span></span>
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

<span data-ttu-id="bed8e-116">지정 된 ASR 보호 컨테이너의 보호 가능한 모든 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="bed8e-117">변수</span><span class="sxs-lookup"><span data-stu-id="bed8e-117">PARAMETERS</span></span>

### <span data-ttu-id="bed8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed8e-118">-DefaultProfile</span></span>
<span data-ttu-id="bed8e-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bed8e-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="bed8e-120">-FriendlyName</span></span>
<span data-ttu-id="bed8e-121">ASR 보호 가능한 항목의 대화명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-121">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="bed8e-122">-이름</span><span class="sxs-lookup"><span data-stu-id="bed8e-122">-Name</span></span>
<span data-ttu-id="bed8e-123">ASR 보호 가능한 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="bed8e-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="bed8e-124">-ProtectionContainer</span></span>
<span data-ttu-id="bed8e-125">Azure Site Recovery 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="bed8e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed8e-126">CommonParameters</span></span>
<span data-ttu-id="bed8e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed8e-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bed8e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed8e-129">입력</span><span class="sxs-lookup"><span data-stu-id="bed8e-129">INPUTS</span></span>

### <span data-ttu-id="bed8e-130">SiteRecovery. ASRProtectionContainer에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="bed8e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="bed8e-131">출력</span><span class="sxs-lookup"><span data-stu-id="bed8e-131">OUTPUTS</span></span>

### <span data-ttu-id="bed8e-132">SiteRecovery. ASRProtectableItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="bed8e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="bed8e-133">상속자</span><span class="sxs-lookup"><span data-stu-id="bed8e-133">NOTES</span></span>

## <span data-ttu-id="bed8e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bed8e-134">RELATED LINKS</span></span>

[<span data-ttu-id="bed8e-135">Get-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="bed8e-135">Get-AzRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="bed8e-136">Set-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="bed8e-136">Set-AzRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzRecoveryServicesAsrProtectionEntity.md)
