---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877726"
---
# <span data-ttu-id="e56f7-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="e56f7-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="e56f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e56f7-102">SYNOPSIS</span></span>
<span data-ttu-id="e56f7-103">전방 도어 만들기에 대 한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="e56f7-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="e56f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e56f7-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e56f7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e56f7-105">DESCRIPTION</span></span>
<span data-ttu-id="e56f7-106">전방 도어 만들기에 대 한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="e56f7-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="e56f7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e56f7-107">EXAMPLES</span></span>

### <span data-ttu-id="e56f7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e56f7-108">Example 1</span></span>
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

<span data-ttu-id="e56f7-109">참고: HealthProbeMethod 설정은 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e56f7-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="e56f7-110">전방 도어 만들기에 대 한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="e56f7-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="e56f7-111">변수</span><span class="sxs-lookup"><span data-stu-id="e56f7-111">PARAMETERS</span></span>

### <span data-ttu-id="e56f7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e56f7-112">-DefaultProfile</span></span>
<span data-ttu-id="e56f7-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e56f7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e56f7-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e56f7-114">-EnabledState</span></span>
<span data-ttu-id="e56f7-115">BackendPools에 정의 된 backends에 대해 상태 프로브를 사용할지 여부</span><span class="sxs-lookup"><span data-stu-id="e56f7-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="e56f7-116">상태 프로브는 단일 지원 백 엔드 풀에 활성화 된 백 엔드가 있는 경우에만 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e56f7-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="e56f7-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="e56f7-117">-HealthProbeMethod</span></span>
<span data-ttu-id="e56f7-118">BackendPools 아래에 정의 된 백 엔드를 검색 하는 데 사용할 HTTP 메서드를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e56f7-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="e56f7-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e56f7-119">-IntervalInSeconds</span></span>
<span data-ttu-id="e56f7-120">상태 프로브 사이의 초 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e56f7-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="e56f7-121">기본값은 30입니다.</span><span class="sxs-lookup"><span data-stu-id="e56f7-121">Default value is 30</span></span>

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

### <span data-ttu-id="e56f7-122">-이름</span><span class="sxs-lookup"><span data-stu-id="e56f7-122">-Name</span></span>
<span data-ttu-id="e56f7-123">상태 검색 설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e56f7-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="e56f7-124">-Path</span><span class="sxs-lookup"><span data-stu-id="e56f7-124">-Path</span></span>
<span data-ttu-id="e56f7-125">상태 프로브에 사용할 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e56f7-125">The path to use for the health probe.</span></span>
<span data-ttu-id="e56f7-126">기본값은/</span><span class="sxs-lookup"><span data-stu-id="e56f7-126">Default is /</span></span>

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

### <span data-ttu-id="e56f7-127">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="e56f7-127">-Protocol</span></span>
<span data-ttu-id="e56f7-128">이 프로브 기본값에 사용할 프로토콜 스키마는 HTTP입니다.</span><span class="sxs-lookup"><span data-stu-id="e56f7-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="e56f7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e56f7-129">CommonParameters</span></span>
<span data-ttu-id="e56f7-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e56f7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e56f7-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e56f7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e56f7-132">입력</span><span class="sxs-lookup"><span data-stu-id="e56f7-132">INPUTS</span></span>

### <span data-ttu-id="e56f7-133">않아야</span><span class="sxs-lookup"><span data-stu-id="e56f7-133">None</span></span>
## <span data-ttu-id="e56f7-134">출력</span><span class="sxs-lookup"><span data-stu-id="e56f7-134">OUTPUTS</span></span>

### <span data-ttu-id="e56f7-135">FrontDoor. PSHealthProbeSetting/.</span><span class="sxs-lookup"><span data-stu-id="e56f7-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="e56f7-136">상속자</span><span class="sxs-lookup"><span data-stu-id="e56f7-136">NOTES</span></span>

## <span data-ttu-id="e56f7-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e56f7-137">RELATED LINKS</span></span>

<span data-ttu-id="e56f7-138">[새로운 AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="e56f7-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
