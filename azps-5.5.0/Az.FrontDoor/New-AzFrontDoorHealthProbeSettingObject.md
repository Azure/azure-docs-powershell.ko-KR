---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180665"
---
# <span data-ttu-id="90253-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="90253-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="90253-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90253-102">SYNOPSIS</span></span>
<span data-ttu-id="90253-103">Front Door 만들기를 위한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="90253-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="90253-104">구문</span><span class="sxs-lookup"><span data-stu-id="90253-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90253-105">설명</span><span class="sxs-lookup"><span data-stu-id="90253-105">DESCRIPTION</span></span>
<span data-ttu-id="90253-106">Front Door 만들기를 위한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="90253-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="90253-107">예제</span><span class="sxs-lookup"><span data-stu-id="90253-107">EXAMPLES</span></span>

### <span data-ttu-id="90253-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="90253-108">Example 1</span></span>
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

<span data-ttu-id="90253-109">참고: HealthProbeMethod 설정은 대/소문자 구분이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="90253-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="90253-110">Front Door 만들기를 위한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="90253-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="90253-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90253-111">PARAMETERS</span></span>

### <span data-ttu-id="90253-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90253-112">-DefaultProfile</span></span>
<span data-ttu-id="90253-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90253-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90253-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="90253-114">-EnabledState</span></span>
<span data-ttu-id="90253-115">backendPools 아래에 정의된 백드에 대해 상태 프로브를 만들지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="90253-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="90253-116">상태 프로브는 활성화된 단일 백end 풀에 단일 활성화된 백드가 있는 경우 비활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90253-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="90253-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="90253-117">-HealthProbeMethod</span></span>
<span data-ttu-id="90253-118">backendPools에서 정의된 백안을 프로브하는 데 사용할 HTTP 메서드를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="90253-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="90253-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="90253-119">-IntervalInSeconds</span></span>
<span data-ttu-id="90253-120">상태 프로브 사이의 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="90253-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="90253-121">기본값은 30입니다.</span><span class="sxs-lookup"><span data-stu-id="90253-121">Default value is 30</span></span>

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

### <span data-ttu-id="90253-122">-Name</span><span class="sxs-lookup"><span data-stu-id="90253-122">-Name</span></span>
<span data-ttu-id="90253-123">상태 프로브 설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90253-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="90253-124">-Path</span><span class="sxs-lookup"><span data-stu-id="90253-124">-Path</span></span>
<span data-ttu-id="90253-125">상태 프로브에 사용할 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="90253-125">The path to use for the health probe.</span></span>
<span data-ttu-id="90253-126">기본값은 /입니다.</span><span class="sxs-lookup"><span data-stu-id="90253-126">Default is /</span></span>

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

### <span data-ttu-id="90253-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="90253-127">-Protocol</span></span>
<span data-ttu-id="90253-128">이 프로브에 사용할 프로토콜 스키마 기본값은 HTTP입니다.</span><span class="sxs-lookup"><span data-stu-id="90253-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="90253-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90253-129">CommonParameters</span></span>
<span data-ttu-id="90253-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90253-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90253-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="90253-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90253-132">입력</span><span class="sxs-lookup"><span data-stu-id="90253-132">INPUTS</span></span>

### <span data-ttu-id="90253-133">없음</span><span class="sxs-lookup"><span data-stu-id="90253-133">None</span></span>
## <span data-ttu-id="90253-134">출력</span><span class="sxs-lookup"><span data-stu-id="90253-134">OUTPUTS</span></span>

### <span data-ttu-id="90253-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="90253-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="90253-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90253-136">NOTES</span></span>

## <span data-ttu-id="90253-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90253-137">RELATED LINKS</span></span>

<span data-ttu-id="90253-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="90253-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
