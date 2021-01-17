---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 49adcdefac7fe3f06cfd9678137dd58cff021f52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352545"
---
# <span data-ttu-id="d335c-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="d335c-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="d335c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d335c-102">SYNOPSIS</span></span>
<span data-ttu-id="d335c-103">ASR 패브릭에서 지정한 구성 서버에서 검색을 위해 등록된 vCenter 서버의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d335c-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="d335c-104">구문</span><span class="sxs-lookup"><span data-stu-id="d335c-104">SYNTAX</span></span>

### <span data-ttu-id="d335c-105">ByFabricObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="d335c-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d335c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d335c-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d335c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="d335c-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d335c-108">설명</span><span class="sxs-lookup"><span data-stu-id="d335c-108">DESCRIPTION</span></span>
<span data-ttu-id="d335c-109">**Get-AzRecoveryServicesAsrvCenter** cmdlet은 ASR 패브릭에서 지정한 구성 서버에서 검색을 위해 등록된 vCenter 서버의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d335c-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="d335c-110">예제</span><span class="sxs-lookup"><span data-stu-id="d335c-110">EXAMPLES</span></span>

### <span data-ttu-id="d335c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d335c-111">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

FriendlyName          : inmtest81
Server                : 10.150.209.27
Port                  : 443
Name                  : inmtest81
ID                    : /Subscriptions/xxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxx/replicationvCenters/inmtest81
FabricArmResourceName : d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9
ProcessServerId       : 526C9B6C-4039-D841-97A92FB0BD153B53
AccountId             : 2
DiscoveryStatus       : Pending
LastHeartbeat         :
```

<span data-ttu-id="d335c-112">패브릭 이름 및 vCenter의 이름으로 Azure Site Recovery vCenter를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d335c-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="d335c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d335c-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="d335c-114">패브릭 이름으로 Azure Site Recovery vCenter 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d335c-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="d335c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d335c-115">PARAMETERS</span></span>

### <span data-ttu-id="d335c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d335c-116">-DefaultProfile</span></span>
<span data-ttu-id="d335c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d335c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d335c-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="d335c-118">-Fabric</span></span>
<span data-ttu-id="d335c-119">구성 서버를 나타내는 ASR 패브릭 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d335c-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d335c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d335c-120">-Name</span></span>
<span data-ttu-id="d335c-121">vCenter 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d335c-121">Name of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d335c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d335c-122">-ResourceId</span></span>
<span data-ttu-id="d335c-123">vCenter의 resourceId를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d335c-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d335c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d335c-124">CommonParameters</span></span>
<span data-ttu-id="d335c-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d335c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d335c-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d335c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d335c-127">입력</span><span class="sxs-lookup"><span data-stu-id="d335c-127">INPUTS</span></span>

### <span data-ttu-id="d335c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d335c-128">System.String</span></span>

### <span data-ttu-id="d335c-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d335c-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d335c-130">출력</span><span class="sxs-lookup"><span data-stu-id="d335c-130">OUTPUTS</span></span>

### <span data-ttu-id="d335c-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="d335c-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="d335c-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d335c-132">NOTES</span></span>

## <span data-ttu-id="d335c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d335c-133">RELATED LINKS</span></span>
