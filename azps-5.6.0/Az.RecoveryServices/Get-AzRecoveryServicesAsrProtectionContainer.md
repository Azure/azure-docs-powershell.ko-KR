---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 1d7f8adfa0db67d66c65c5ac7f3df7c64b665fda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992502"
---
# <span data-ttu-id="c974b-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c974b-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="c974b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c974b-102">SYNOPSIS</span></span>
<span data-ttu-id="c974b-103">Recovery Services 자격 증명 모음에서 ASR 보호 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c974b-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="c974b-104">구문</span><span class="sxs-lookup"><span data-stu-id="c974b-104">SYNTAX</span></span>

### <span data-ttu-id="c974b-105">ByFabricObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="c974b-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c974b-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c974b-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c974b-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c974b-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c974b-108">설명</span><span class="sxs-lookup"><span data-stu-id="c974b-108">DESCRIPTION</span></span>
<span data-ttu-id="c974b-109">**Get-AzRecoveryServicesAsrProtectionContainer** cmdlet은 Recovery Services 자격 증명 모음에서 Azure Site Recovery 보호 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c974b-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="c974b-110">보호 컨테이너는 보호 가능(검색) 및 보호된 개체(예: 가상 머신)에 대한 논리 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="c974b-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="c974b-111">복제 정책은 보호된 항목에 대한 복제 설정을 정의하며 보호 컨테이너와 연결하여 보호 가능한 항목에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c974b-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="c974b-112">예제</span><span class="sxs-lookup"><span data-stu-id="c974b-112">EXAMPLES</span></span>

### <span data-ttu-id="c974b-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="c974b-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="c974b-114">패브릭의 보호 컨테이너 목록 $fabric.</span><span class="sxs-lookup"><span data-stu-id="c974b-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="c974b-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="c974b-115">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="c974b-116">이름과 함께 패브릭 $fabric 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="c974b-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="c974b-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="c974b-117">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="c974b-118">친숙한 이름이 있는 $fabric 보호 컨테이너.</span><span class="sxs-lookup"><span data-stu-id="c974b-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="c974b-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c974b-119">PARAMETERS</span></span>

### <span data-ttu-id="c974b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c974b-120">-DefaultProfile</span></span>
<span data-ttu-id="c974b-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c974b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c974b-122">-Fabric</span><span class="sxs-lookup"><span data-stu-id="c974b-122">-Fabric</span></span>
<span data-ttu-id="c974b-123">지정된 ASR 패브릭에서 보호 컨테이너를 찾아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c974b-123">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="c974b-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c974b-124">-FriendlyName</span></span>
<span data-ttu-id="c974b-125">찾아야 하는 ASR 보호 컨테이너의 친숙한 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c974b-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="c974b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c974b-126">-Name</span></span>
<span data-ttu-id="c974b-127">찾아야 하는 ASR 보호 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c974b-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="c974b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c974b-128">CommonParameters</span></span>
<span data-ttu-id="c974b-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c974b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c974b-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c974b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c974b-131">입력</span><span class="sxs-lookup"><span data-stu-id="c974b-131">INPUTS</span></span>

### <span data-ttu-id="c974b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c974b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c974b-133">출력</span><span class="sxs-lookup"><span data-stu-id="c974b-133">OUTPUTS</span></span>

### <span data-ttu-id="c974b-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c974b-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="c974b-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c974b-135">NOTES</span></span>

## <span data-ttu-id="c974b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c974b-136">RELATED LINKS</span></span>
