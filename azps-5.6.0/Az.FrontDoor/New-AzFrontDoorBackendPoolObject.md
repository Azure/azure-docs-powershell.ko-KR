---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 5cfe83c48950fff7f300b07cf43ba32ff9739606
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965904"
---
# <span data-ttu-id="e955c-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="e955c-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="e955c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e955c-102">SYNOPSIS</span></span>
<span data-ttu-id="e955c-103">Front Door 만들기를 위한 PSBackendPool 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="e955c-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="e955c-104">구문</span><span class="sxs-lookup"><span data-stu-id="e955c-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e955c-105">설명</span><span class="sxs-lookup"><span data-stu-id="e955c-105">DESCRIPTION</span></span>
<span data-ttu-id="e955c-106">Front Door 만들기를 위한 PSBackendPool 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="e955c-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="e955c-107">예제</span><span class="sxs-lookup"><span data-stu-id="e955c-107">EXAMPLES</span></span>

### <span data-ttu-id="e955c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e955c-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
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

<span data-ttu-id="e955c-109">Front Door 만들기를 위한 PSBackendPool 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="e955c-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="e955c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e955c-110">PARAMETERS</span></span>

### <span data-ttu-id="e955c-111">-백end</span><span class="sxs-lookup"><span data-stu-id="e955c-111">-Backend</span></span>
<span data-ttu-id="e955c-112">이 풀에 대한 백END 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="e955c-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="e955c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e955c-113">-DefaultProfile</span></span>
<span data-ttu-id="e955c-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e955c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e955c-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="e955c-115">-FrontDoorName</span></span>
<span data-ttu-id="e955c-116">이 라우팅 규칙이 속한 Front Door의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e955c-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="e955c-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="e955c-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="e955c-118">이 백end 풀에 대한 상태 프로브 설정의 이름</span><span class="sxs-lookup"><span data-stu-id="e955c-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="e955c-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="e955c-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="e955c-120">이 백end 풀에 대한 부하 분산 설정의 이름</span><span class="sxs-lookup"><span data-stu-id="e955c-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="e955c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e955c-121">-Name</span></span>
<span data-ttu-id="e955c-122">BackendPool 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e955c-122">BackendPool name.</span></span>

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

### <span data-ttu-id="e955c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e955c-123">-ResourceGroupName</span></span>
<span data-ttu-id="e955c-124">RoutingRule이 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e955c-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="e955c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e955c-125">CommonParameters</span></span>
<span data-ttu-id="e955c-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e955c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e955c-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e955c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e955c-128">입력</span><span class="sxs-lookup"><span data-stu-id="e955c-128">INPUTS</span></span>

### <span data-ttu-id="e955c-129">없음</span><span class="sxs-lookup"><span data-stu-id="e955c-129">None</span></span>

## <span data-ttu-id="e955c-130">출력</span><span class="sxs-lookup"><span data-stu-id="e955c-130">OUTPUTS</span></span>

### <span data-ttu-id="e955c-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="e955c-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="e955c-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e955c-132">NOTES</span></span>

## <span data-ttu-id="e955c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e955c-133">RELATED LINKS</span></span>

<span data-ttu-id="e955c-134">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="e955c-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
