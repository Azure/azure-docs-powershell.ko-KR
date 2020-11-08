---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 49adcdefac7fe3f06cfd9678137dd58cff021f52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034357"
---
# <span data-ttu-id="47930-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="47930-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="47930-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47930-102">SYNOPSIS</span></span>
<span data-ttu-id="47930-103">ASR 패브릭에 지정 된 구성 서버에서 검색을 위해 등록 된 vCenter 서버의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47930-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="47930-104">구문과</span><span class="sxs-lookup"><span data-stu-id="47930-104">SYNTAX</span></span>

### <span data-ttu-id="47930-105">ByFabricObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="47930-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47930-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="47930-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47930-107">ByName</span><span class="sxs-lookup"><span data-stu-id="47930-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47930-108">설명은</span><span class="sxs-lookup"><span data-stu-id="47930-108">DESCRIPTION</span></span>
<span data-ttu-id="47930-109">**AzRecoveryServicesAsrvCenter** CMDLET은 ASR 패브릭에 지정 된 구성 서버에서 검색을 위해 등록 된 vCenter 서버의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47930-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="47930-110">예제의</span><span class="sxs-lookup"><span data-stu-id="47930-110">EXAMPLES</span></span>

### <span data-ttu-id="47930-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="47930-111">Example 1</span></span>
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

<span data-ttu-id="47930-112">패브릭 이름 및 vCenter 이름으로 azure site recovery vCenter를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47930-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="47930-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="47930-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="47930-114">패브릭 이름으로 azure site recovery vCenter 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47930-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="47930-115">변수</span><span class="sxs-lookup"><span data-stu-id="47930-115">PARAMETERS</span></span>

### <span data-ttu-id="47930-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47930-116">-DefaultProfile</span></span>
<span data-ttu-id="47930-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47930-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47930-118">-패브릭</span><span class="sxs-lookup"><span data-stu-id="47930-118">-Fabric</span></span>
<span data-ttu-id="47930-119">구성 서버를 나타내는 ASR fabric 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="47930-119">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="47930-120">-이름</span><span class="sxs-lookup"><span data-stu-id="47930-120">-Name</span></span>
<span data-ttu-id="47930-121">VCenter 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47930-121">Name of the vCenter server.</span></span>

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

### <span data-ttu-id="47930-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47930-122">-ResourceId</span></span>
<span data-ttu-id="47930-123">VCenter의 resourceId를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47930-123">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="47930-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47930-124">CommonParameters</span></span>
<span data-ttu-id="47930-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="47930-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47930-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="47930-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47930-127">입력</span><span class="sxs-lookup"><span data-stu-id="47930-127">INPUTS</span></span>

### <span data-ttu-id="47930-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="47930-128">System.String</span></span>

### <span data-ttu-id="47930-129">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="47930-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="47930-130">출력</span><span class="sxs-lookup"><span data-stu-id="47930-130">OUTPUTS</span></span>

### <span data-ttu-id="47930-131">SiteRecovery. r m/$ 명령</span><span class="sxs-lookup"><span data-stu-id="47930-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="47930-132">상속자</span><span class="sxs-lookup"><span data-stu-id="47930-132">NOTES</span></span>

## <span data-ttu-id="47930-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47930-133">RELATED LINKS</span></span>
