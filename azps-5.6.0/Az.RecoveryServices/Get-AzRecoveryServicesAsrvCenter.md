---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: eb358a0caf2b1ea5ccba8d92c39562d2c39706c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995297"
---
# <span data-ttu-id="64bd7-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="64bd7-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="64bd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64bd7-102">SYNOPSIS</span></span>
<span data-ttu-id="64bd7-103">ASR 패브릭에서 지정한 구성 서버에서 검색에 등록된 vCenter 서버의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64bd7-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="64bd7-104">구문</span><span class="sxs-lookup"><span data-stu-id="64bd7-104">SYNTAX</span></span>

### <span data-ttu-id="64bd7-105">ByFabricObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="64bd7-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64bd7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="64bd7-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64bd7-107">ByName</span><span class="sxs-lookup"><span data-stu-id="64bd7-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64bd7-108">설명</span><span class="sxs-lookup"><span data-stu-id="64bd7-108">DESCRIPTION</span></span>
<span data-ttu-id="64bd7-109">**Get-AzRecoveryServicesAsrvCenter** cmdlet은 ASR 패브릭에서 지정한 구성 서버에서 검색을 위해 등록된 vCenter 서버의 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="64bd7-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="64bd7-110">예제</span><span class="sxs-lookup"><span data-stu-id="64bd7-110">EXAMPLES</span></span>

### <span data-ttu-id="64bd7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="64bd7-111">Example 1</span></span>
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

<span data-ttu-id="64bd7-112">vCenter의 패브릭 이름 및 이름을 사용하여 Azure Site Recovery vCenter를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64bd7-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="64bd7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="64bd7-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="64bd7-114">패브릭 이름으로 azure site recovery vCenter 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64bd7-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="64bd7-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="64bd7-115">PARAMETERS</span></span>

### <span data-ttu-id="64bd7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64bd7-116">-DefaultProfile</span></span>
<span data-ttu-id="64bd7-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64bd7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64bd7-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="64bd7-118">-Fabric</span></span>
<span data-ttu-id="64bd7-119">구성 서버를 나타내는 ASR 패브릭 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="64bd7-119">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="64bd7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="64bd7-120">-Name</span></span>
<span data-ttu-id="64bd7-121">vCenter 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64bd7-121">Name of the vCenter server.</span></span>

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

### <span data-ttu-id="64bd7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64bd7-122">-ResourceId</span></span>
<span data-ttu-id="64bd7-123">vCenter의 resourceId를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64bd7-123">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="64bd7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64bd7-124">CommonParameters</span></span>
<span data-ttu-id="64bd7-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="64bd7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64bd7-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64bd7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64bd7-127">입력</span><span class="sxs-lookup"><span data-stu-id="64bd7-127">INPUTS</span></span>

### <span data-ttu-id="64bd7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="64bd7-128">System.String</span></span>

### <span data-ttu-id="64bd7-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="64bd7-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="64bd7-130">출력</span><span class="sxs-lookup"><span data-stu-id="64bd7-130">OUTPUTS</span></span>

### <span data-ttu-id="64bd7-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="64bd7-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="64bd7-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="64bd7-132">NOTES</span></span>

## <span data-ttu-id="64bd7-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64bd7-133">RELATED LINKS</span></span>
