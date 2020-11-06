---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 689f432f117e67a3770518a3b2e86f1678f3662b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531689"
---
# <span data-ttu-id="2a273-101">Get-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="2a273-101">Get-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="2a273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a273-102">SYNOPSIS</span></span>
<span data-ttu-id="2a273-103">ASR 패브릭에 지정 된 구성 서버에서 검색을 위해 등록 된 vCenter 서버의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a273-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a273-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a273-104">SYNTAX</span></span>

### <span data-ttu-id="2a273-105">ByFabricObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="2a273-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a273-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a273-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a273-107">ByName</span><span class="sxs-lookup"><span data-stu-id="2a273-107">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a273-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2a273-108">DESCRIPTION</span></span>
<span data-ttu-id="2a273-109">**AzureRmRecoveryServicesAsrvCenter** CMDLET은 ASR 패브릭에 지정 된 구성 서버에서 검색을 위해 등록 된 vCenter 서버의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a273-109">The **Get-AzureRmRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="2a273-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2a273-110">EXAMPLES</span></span>

### <span data-ttu-id="2a273-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2a273-111">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

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

<span data-ttu-id="2a273-112">패브릭 이름 및 vCenter 이름으로 azure site recovery vCenter를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a273-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="2a273-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="2a273-113">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="2a273-114">패브릭 이름으로 azure site recovery vCenter 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a273-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="2a273-115">변수</span><span class="sxs-lookup"><span data-stu-id="2a273-115">PARAMETERS</span></span>

### <span data-ttu-id="2a273-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a273-116">-DefaultProfile</span></span>
<span data-ttu-id="2a273-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a273-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a273-118">-패브릭</span><span class="sxs-lookup"><span data-stu-id="2a273-118">-Fabric</span></span>
<span data-ttu-id="2a273-119">구성 서버를 나타내는 ASR fabric 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2a273-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a273-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2a273-120">-Name</span></span>
<span data-ttu-id="2a273-121">VCenter 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a273-121">Name of the vCenter server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a273-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a273-122">-ResourceId</span></span>
<span data-ttu-id="2a273-123">VCenter의 resourceId를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a273-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a273-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a273-124">CommonParameters</span></span>
<span data-ttu-id="2a273-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a273-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a273-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a273-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a273-127">입력</span><span class="sxs-lookup"><span data-stu-id="2a273-127">INPUTS</span></span>

### <span data-ttu-id="2a273-128">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="2a273-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2a273-129">출력</span><span class="sxs-lookup"><span data-stu-id="2a273-129">OUTPUTS</span></span>

### <span data-ttu-id="2a273-130">System.webserver. t e r ' 1 [[SiteRecovery] Recoveryrvcenter, Microsoft Azure. SiteRecovery, Version = 0.1.1.0, Culture = 중립, PublicKeyToken = null]])]</span><span class="sxs-lookup"><span data-stu-id="2a273-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2a273-131">상속자</span><span class="sxs-lookup"><span data-stu-id="2a273-131">NOTES</span></span>

## <span data-ttu-id="2a273-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a273-132">RELATED LINKS</span></span>
