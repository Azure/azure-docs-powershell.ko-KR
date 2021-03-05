---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 4d65985d724033244f761748634adb3b2002a199
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971019"
---
# <span data-ttu-id="9f309-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="9f309-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="9f309-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f309-102">SYNOPSIS</span></span>
<span data-ttu-id="9f309-103">Front Door 만들기를 위한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="9f309-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="9f309-104">구문</span><span class="sxs-lookup"><span data-stu-id="9f309-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f309-105">설명</span><span class="sxs-lookup"><span data-stu-id="9f309-105">DESCRIPTION</span></span>
<span data-ttu-id="9f309-106">Front Door 만들기를 위한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="9f309-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="9f309-107">예제</span><span class="sxs-lookup"><span data-stu-id="9f309-107">EXAMPLES</span></span>

### <span data-ttu-id="9f309-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9f309-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
HealthProbeMethod : Head
EnabledState      : Enabled
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="9f309-109">참고: HealthProbeMethod 설정은 대/대/미 구분이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9f309-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="9f309-110">Front Door 만들기를 위한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="9f309-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="9f309-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9f309-111">PARAMETERS</span></span>

### <span data-ttu-id="9f309-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f309-112">-DefaultProfile</span></span>
<span data-ttu-id="9f309-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f309-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f309-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="9f309-114">-EnabledState</span></span>
<span data-ttu-id="9f309-115">백endPools에서 정의된 백end에 대해 상태 프로브를 만들지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="9f309-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="9f309-116">상태 프로브는 사용 가능한 단일 백드 풀에 단일 사용 백END가 있는 경우만 비활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f309-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f309-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="9f309-117">-HealthProbeMethod</span></span>
<span data-ttu-id="9f309-118">백endPools에서 정의된 백END를 프로브하는 데 사용할 HTTP 메서드를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="9f309-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f309-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9f309-119">-IntervalInSeconds</span></span>
<span data-ttu-id="9f309-120">상태 프로브 사이의 초 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9f309-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="9f309-121">기본값은 30입니다.</span><span class="sxs-lookup"><span data-stu-id="9f309-121">Default value is 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f309-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9f309-122">-Name</span></span>
<span data-ttu-id="9f309-123">상태 프로브 설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f309-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="9f309-124">-Path</span><span class="sxs-lookup"><span data-stu-id="9f309-124">-Path</span></span>
<span data-ttu-id="9f309-125">상태 프로브에 사용할 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9f309-125">The path to use for the health probe.</span></span>
<span data-ttu-id="9f309-126">기본값은 /입니다.</span><span class="sxs-lookup"><span data-stu-id="9f309-126">Default is /</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f309-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9f309-127">-Protocol</span></span>
<span data-ttu-id="9f309-128">이 프로브에 사용할 프로토콜 구성표 기본값은 HTTP입니다.</span><span class="sxs-lookup"><span data-stu-id="9f309-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f309-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f309-129">CommonParameters</span></span>
<span data-ttu-id="9f309-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9f309-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f309-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f309-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f309-132">입력</span><span class="sxs-lookup"><span data-stu-id="9f309-132">INPUTS</span></span>

### <span data-ttu-id="9f309-133">없음</span><span class="sxs-lookup"><span data-stu-id="9f309-133">None</span></span>
## <span data-ttu-id="9f309-134">출력</span><span class="sxs-lookup"><span data-stu-id="9f309-134">OUTPUTS</span></span>

### <span data-ttu-id="9f309-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="9f309-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="9f309-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9f309-136">NOTES</span></span>

## <span data-ttu-id="9f309-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f309-137">RELATED LINKS</span></span>

<span data-ttu-id="9f309-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="9f309-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
