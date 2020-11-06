---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 5862d76c574b469d3bc0e559892b505e1b90beab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528874"
---
# <span data-ttu-id="068f8-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="068f8-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="068f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="068f8-102">SYNOPSIS</span></span>
<span data-ttu-id="068f8-103">복구 서비스 자격 증명 모음에서 ASR 보호 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="068f8-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="068f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="068f8-104">SYNTAX</span></span>

### <span data-ttu-id="068f8-105">ByFabricObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="068f8-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="068f8-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="068f8-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="068f8-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="068f8-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="068f8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="068f8-108">DESCRIPTION</span></span>
<span data-ttu-id="068f8-109">**AzureRmRecoveryServicesAsrProtectionContainer** Cmdlet은 Recovery Services 자격 증명 모음에서 Azure Site Recovery 보호 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="068f8-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="068f8-110">보호 컨테이너는 가상 컴퓨터와 같은 보호 되는 (검색 된) 개체를 위한 논리적 컨테이너 이며,</span><span class="sxs-lookup"><span data-stu-id="068f8-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="068f8-111">복제 정책은 보호 된 항목에 대 한 복제 설정을 정의 하 고 보호 컨테이너에 연결 하 고 보호 가능한 항목에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="068f8-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="068f8-112">예제의</span><span class="sxs-lookup"><span data-stu-id="068f8-112">EXAMPLES</span></span>

### <span data-ttu-id="068f8-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="068f8-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="068f8-114">패브릭 $fabric의 보호 컨테이너 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="068f8-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="068f8-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="068f8-115">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
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

<span data-ttu-id="068f8-116">이름의 패브릭 $fabric 보호 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="068f8-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="068f8-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="068f8-117">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
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

<span data-ttu-id="068f8-118">이름에 이름이 있는 패브릭 $fabric의 보호 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="068f8-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="068f8-119">변수</span><span class="sxs-lookup"><span data-stu-id="068f8-119">PARAMETERS</span></span>

### <span data-ttu-id="068f8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="068f8-120">-DefaultProfile</span></span>
<span data-ttu-id="068f8-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="068f8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068f8-122">-패브릭</span><span class="sxs-lookup"><span data-stu-id="068f8-122">-Fabric</span></span>
<span data-ttu-id="068f8-123">지정 된 ASR 패브릭에서 보호 컨테이너를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="068f8-123">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="068f8-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="068f8-124">-FriendlyName</span></span>
<span data-ttu-id="068f8-125">찾을 ASR 보호 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="068f8-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="068f8-126">-이름</span><span class="sxs-lookup"><span data-stu-id="068f8-126">-Name</span></span>
<span data-ttu-id="068f8-127">찾을 ASR 보호 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="068f8-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="068f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="068f8-128">CommonParameters</span></span>
<span data-ttu-id="068f8-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="068f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="068f8-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="068f8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="068f8-131">입력</span><span class="sxs-lookup"><span data-stu-id="068f8-131">INPUTS</span></span>

### <span data-ttu-id="068f8-132">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="068f8-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="068f8-133">출력</span><span class="sxs-lookup"><span data-stu-id="068f8-133">OUTPUTS</span></span>

### <span data-ttu-id="068f8-134">System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRProtectionContainer, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="068f8-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="068f8-135">상속자</span><span class="sxs-lookup"><span data-stu-id="068f8-135">NOTES</span></span>

## <span data-ttu-id="068f8-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="068f8-136">RELATED LINKS</span></span>
