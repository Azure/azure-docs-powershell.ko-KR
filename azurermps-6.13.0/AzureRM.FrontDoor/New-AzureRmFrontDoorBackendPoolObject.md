---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendPoolObject.md
ms.openlocfilehash: 13b28d236e1c6e758c4f7883285c55017ce5a727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702932"
---
# <span data-ttu-id="cfec5-101">New-AzureRmFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="cfec5-101">New-AzureRmFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="cfec5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfec5-102">SYNOPSIS</span></span>
<span data-ttu-id="cfec5-103">전방 도어 만들기에 대 한 PSBackendPool 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="cfec5-103">Create a PSBackendPool object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfec5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cfec5-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfec5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cfec5-105">DESCRIPTION</span></span>
<span data-ttu-id="cfec5-106">전방 도어 만들기에 대 한 PSBackendPool 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="cfec5-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="cfec5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cfec5-107">EXAMPLES</span></span>

### <span data-ttu-id="cfec5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cfec5-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
althProbeSettingsName "healthProbeSetting1" -LoadBalancingSettingsName "loadBalancingSetting1"


Backends                : {Microsoft.Azure.Commands.FrontDoor.Models.PSBackend}
LoadBalancingSettingRef : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/LoadBalancingSettings/loadBalancingSetting1
HealthProbeSettingRef   : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/HealthProbeSettings/healthProbeSetting1
EnabledState            : Enabled
ResourceState           :
Id                      :
Name                    : backendpool1
Type                    :
```

<span data-ttu-id="cfec5-109">전방 도어 만들기에 대 한 PSBackendPool 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="cfec5-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="cfec5-110">변수</span><span class="sxs-lookup"><span data-stu-id="cfec5-110">PARAMETERS</span></span>

### <span data-ttu-id="cfec5-111">-백 엔드</span><span class="sxs-lookup"><span data-stu-id="cfec5-111">-Backend</span></span>
<span data-ttu-id="cfec5-112">이 풀의 백 엔드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="cfec5-112">The set of backends for this pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackend[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfec5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfec5-113">-DefaultProfile</span></span>
<span data-ttu-id="cfec5-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cfec5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfec5-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="cfec5-115">-FrontDoorName</span></span>
<span data-ttu-id="cfec5-116">이 라우팅 규칙이 속한 앞면 도어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cfec5-116">The name of the Front Door to which this routing rule belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfec5-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="cfec5-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="cfec5-118">이 백 엔드 풀에 대 한 상태 프로브 설정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cfec5-118">The name of the health probe settings for this backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfec5-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="cfec5-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="cfec5-120">이 백 엔드 풀에 대 한 부하 분산 설정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cfec5-120">The name of the load balancing settings for this backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfec5-121">-이름</span><span class="sxs-lookup"><span data-stu-id="cfec5-121">-Name</span></span>
<span data-ttu-id="cfec5-122">BackendPool 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cfec5-122">BackendPool name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfec5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfec5-123">-ResourceGroupName</span></span>
<span data-ttu-id="cfec5-124">RoutingRule를 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cfec5-124">The resource group name that the RoutingRule will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfec5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfec5-125">CommonParameters</span></span>
<span data-ttu-id="cfec5-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfec5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfec5-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfec5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfec5-128">입력</span><span class="sxs-lookup"><span data-stu-id="cfec5-128">INPUTS</span></span>

### <span data-ttu-id="cfec5-129">않아야</span><span class="sxs-lookup"><span data-stu-id="cfec5-129">None</span></span>

## <span data-ttu-id="cfec5-130">출력</span><span class="sxs-lookup"><span data-stu-id="cfec5-130">OUTPUTS</span></span>

### <span data-ttu-id="cfec5-131">FrontDoor. PSBackendPool/.</span><span class="sxs-lookup"><span data-stu-id="cfec5-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="cfec5-132">상속자</span><span class="sxs-lookup"><span data-stu-id="cfec5-132">NOTES</span></span>

## <span data-ttu-id="cfec5-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cfec5-133">RELATED LINKS</span></span>

<span data-ttu-id="cfec5-134">[새로운 AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [새로운 AzureRmFrontDoorBackendObject](./New-AzureRmFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="cfec5-134">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorBackendObject](./New-AzureRmFrontDoorBackendObject.md)</span></span>
