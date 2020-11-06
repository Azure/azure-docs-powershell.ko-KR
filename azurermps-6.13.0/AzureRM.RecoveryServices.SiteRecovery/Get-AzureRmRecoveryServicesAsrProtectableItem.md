---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 72f94dca73a1d99adf2d5cced50be9122ff2e7d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531953"
---
# <span data-ttu-id="6b8ec-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6b8ec-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="6b8ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b8ec-102">SYNOPSIS</span></span>
<span data-ttu-id="6b8ec-103">ASR 보호 컨테이너에서 보호 가능한 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b8ec-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b8ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b8ec-104">SYNTAX</span></span>

### <span data-ttu-id="6b8ec-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="6b8ec-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b8ec-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="6b8ec-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b8ec-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b8ec-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b8ec-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6b8ec-108">DESCRIPTION</span></span>
<span data-ttu-id="6b8ec-109">**AzureRmRecoveryServicesAsrProtectableItem** Cmdlet은 Azure Site Recovery 보호 컨테이너에서 보호 가능한 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b8ec-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="6b8ec-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6b8ec-110">EXAMPLES</span></span>

### <span data-ttu-id="6b8ec-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6b8ec-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="6b8ec-112">지정 된 ASR 보호 컨테이너의 보호 가능한 모든 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b8ec-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="6b8ec-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6b8ec-113">Example 2</span></span>
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

<span data-ttu-id="6b8ec-114">지정 된 ASR 보호 컨테이너에서 보호 되는 항목을 가져오고 제공 된 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b8ec-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="6b8ec-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="6b8ec-115">Example 3</span></span>
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

<span data-ttu-id="6b8ec-116">지정 된 ASR 보호 컨테이너의 보호 가능한 모든 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b8ec-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="6b8ec-117">변수</span><span class="sxs-lookup"><span data-stu-id="6b8ec-117">PARAMETERS</span></span>

### <span data-ttu-id="6b8ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b8ec-118">-DefaultProfile</span></span>
<span data-ttu-id="6b8ec-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b8ec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8ec-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b8ec-120">-FriendlyName</span></span>
<span data-ttu-id="6b8ec-121">ASR 보호 가능한 항목의 대화명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b8ec-121">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="6b8ec-122">-이름</span><span class="sxs-lookup"><span data-stu-id="6b8ec-122">-Name</span></span>
<span data-ttu-id="6b8ec-123">ASR 보호 가능한 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b8ec-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="6b8ec-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6b8ec-124">-ProtectionContainer</span></span>
<span data-ttu-id="6b8ec-125">Azure Site Recovery 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b8ec-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="6b8ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b8ec-126">CommonParameters</span></span>
<span data-ttu-id="6b8ec-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b8ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b8ec-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b8ec-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b8ec-129">입력</span><span class="sxs-lookup"><span data-stu-id="6b8ec-129">INPUTS</span></span>

### <span data-ttu-id="6b8ec-130">SiteRecovery. ASRProtectionContainer에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="6b8ec-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="6b8ec-131">출력</span><span class="sxs-lookup"><span data-stu-id="6b8ec-131">OUTPUTS</span></span>

### <span data-ttu-id="6b8ec-132">System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRProtectableItem, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="6b8ec-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6b8ec-133">상속자</span><span class="sxs-lookup"><span data-stu-id="6b8ec-133">NOTES</span></span>

## <span data-ttu-id="6b8ec-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b8ec-134">RELATED LINKS</span></span>

[<span data-ttu-id="6b8ec-135">Get-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="6b8ec-135">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="6b8ec-136">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="6b8ec-136">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)
