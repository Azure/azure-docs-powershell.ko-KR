---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: e37a2c0acf1cf1fa750e62f26431272fcc70b767
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699731"
---
# <span data-ttu-id="7700e-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7700e-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="7700e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7700e-102">SYNOPSIS</span></span>
<span data-ttu-id="7700e-103">복구 서비스 자격 증명 모음에서 ASR 보호 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7700e-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="7700e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7700e-104">SYNTAX</span></span>

### <span data-ttu-id="7700e-105">ByFabricObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="7700e-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7700e-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="7700e-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7700e-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7700e-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7700e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7700e-108">DESCRIPTION</span></span>
<span data-ttu-id="7700e-109">**AzRecoveryServicesAsrProtectionContainer** Cmdlet은 Recovery Services 자격 증명 모음에서 Azure Site Recovery 보호 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7700e-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="7700e-110">보호 컨테이너는 가상 컴퓨터와 같은 보호 되는 (검색 된) 개체를 위한 논리적 컨테이너 이며,</span><span class="sxs-lookup"><span data-stu-id="7700e-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="7700e-111">복제 정책은 보호 된 항목에 대 한 복제 설정을 정의 하 고 보호 컨테이너에 연결 하 고 보호 가능한 항목에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7700e-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="7700e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="7700e-112">EXAMPLES</span></span>

### <span data-ttu-id="7700e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="7700e-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="7700e-114">패브릭 $fabric의 보호 컨테이너 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7700e-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="7700e-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="7700e-115">Example 2</span></span>
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

<span data-ttu-id="7700e-116">이름의 패브릭 $fabric 보호 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="7700e-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="7700e-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="7700e-117">Example 3</span></span>
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

<span data-ttu-id="7700e-118">이름에 이름이 있는 패브릭 $fabric의 보호 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="7700e-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="7700e-119">변수</span><span class="sxs-lookup"><span data-stu-id="7700e-119">PARAMETERS</span></span>

### <span data-ttu-id="7700e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7700e-120">-DefaultProfile</span></span>
<span data-ttu-id="7700e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7700e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7700e-122">-패브릭</span><span class="sxs-lookup"><span data-stu-id="7700e-122">-Fabric</span></span>
<span data-ttu-id="7700e-123">지정 된 ASR 패브릭에서 보호 컨테이너를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7700e-123">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="7700e-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7700e-124">-FriendlyName</span></span>
<span data-ttu-id="7700e-125">찾을 ASR 보호 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7700e-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="7700e-126">-이름</span><span class="sxs-lookup"><span data-stu-id="7700e-126">-Name</span></span>
<span data-ttu-id="7700e-127">찾을 ASR 보호 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7700e-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="7700e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7700e-128">CommonParameters</span></span>
<span data-ttu-id="7700e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7700e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7700e-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7700e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7700e-131">입력</span><span class="sxs-lookup"><span data-stu-id="7700e-131">INPUTS</span></span>

### <span data-ttu-id="7700e-132">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="7700e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="7700e-133">출력</span><span class="sxs-lookup"><span data-stu-id="7700e-133">OUTPUTS</span></span>

### <span data-ttu-id="7700e-134">SiteRecovery. ASRProtectionContainer에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="7700e-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="7700e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="7700e-135">NOTES</span></span>

## <span data-ttu-id="7700e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7700e-136">RELATED LINKS</span></span>
