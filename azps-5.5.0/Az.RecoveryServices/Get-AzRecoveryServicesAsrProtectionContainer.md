---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 6db09c69d112e2638026fde97d586f7945f0508e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202049"
---
# <span data-ttu-id="4b881-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4b881-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="4b881-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b881-102">SYNOPSIS</span></span>
<span data-ttu-id="4b881-103">Recovery Services 자격 증명 모음에서 ASR 보호 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b881-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="4b881-104">구문</span><span class="sxs-lookup"><span data-stu-id="4b881-104">SYNTAX</span></span>

### <span data-ttu-id="4b881-105">ByFabricObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="4b881-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b881-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4b881-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b881-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4b881-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b881-108">설명</span><span class="sxs-lookup"><span data-stu-id="4b881-108">DESCRIPTION</span></span>
<span data-ttu-id="4b881-109">**Get-AzRecoveryServicesAsrProtectionContainer** cmdlet은 Recovery Services 자격 증명 모음에서 Azure Site Recovery 보호 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b881-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="4b881-110">보호 컨테이너는 가상 머신과 같은 보호 가능한(검색) 및 보호된 개체를 위한 논리적 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="4b881-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="4b881-111">복제 정책은 보호된 항목에 대한 복제 설정을 정의하고 보호 컨테이너와 연결하여 보호 가능한 항목에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b881-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="4b881-112">예제</span><span class="sxs-lookup"><span data-stu-id="4b881-112">EXAMPLES</span></span>

### <span data-ttu-id="4b881-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="4b881-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="4b881-114">패브릭 컨테이너의 보호 컨테이너 $fabric.</span><span class="sxs-lookup"><span data-stu-id="4b881-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="4b881-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="4b881-115">Example 2</span></span>
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

<span data-ttu-id="4b881-116">이름과 함께 패브릭 $fabric 보호 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="4b881-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="4b881-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="4b881-117">Example 3</span></span>
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

<span data-ttu-id="4b881-118">이름과 함께 패브릭 $fabric 보호 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="4b881-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="4b881-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b881-119">PARAMETERS</span></span>

### <span data-ttu-id="4b881-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b881-120">-DefaultProfile</span></span>
<span data-ttu-id="4b881-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b881-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4b881-122">-Fabric</span><span class="sxs-lookup"><span data-stu-id="4b881-122">-Fabric</span></span>
<span data-ttu-id="4b881-123">지정된 ASR 패브릭에서 보호 컨테이너를 찾아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b881-123">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="4b881-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4b881-124">-FriendlyName</span></span>
<span data-ttu-id="4b881-125">찾아보는 ASR 보호 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b881-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="4b881-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4b881-126">-Name</span></span>
<span data-ttu-id="4b881-127">찾아보는 ASR 보호 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b881-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="4b881-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b881-128">CommonParameters</span></span>
<span data-ttu-id="4b881-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b881-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b881-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4b881-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b881-131">입력</span><span class="sxs-lookup"><span data-stu-id="4b881-131">INPUTS</span></span>

### <span data-ttu-id="4b881-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4b881-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="4b881-133">출력</span><span class="sxs-lookup"><span data-stu-id="4b881-133">OUTPUTS</span></span>

### <span data-ttu-id="4b881-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4b881-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="4b881-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b881-135">NOTES</span></span>

## <span data-ttu-id="4b881-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b881-136">RELATED LINKS</span></span>
