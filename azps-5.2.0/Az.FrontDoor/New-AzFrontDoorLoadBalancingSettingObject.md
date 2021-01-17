---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326374"
---
# <span data-ttu-id="2f001-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="2f001-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="2f001-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f001-102">SYNOPSIS</span></span>
<span data-ttu-id="2f001-103">Front Door 만들기를 위한 PSLoadBalancingSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="2f001-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="2f001-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f001-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f001-105">설명</span><span class="sxs-lookup"><span data-stu-id="2f001-105">DESCRIPTION</span></span>
<span data-ttu-id="2f001-106">Front Door 만들기를 위한 PSLoadBalancingSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="2f001-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="2f001-107">예제</span><span class="sxs-lookup"><span data-stu-id="2f001-107">EXAMPLES</span></span>

### <span data-ttu-id="2f001-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2f001-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="2f001-109">Front Door 만들기를 위한 PSLoadBalancingSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="2f001-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="2f001-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f001-110">PARAMETERS</span></span>

### <span data-ttu-id="2f001-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="2f001-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="2f001-112">프로브가 가장 낮은 대기 시간 버킷에 떨어질 추가 대기 시간(밀리초)입니다.</span><span class="sxs-lookup"><span data-stu-id="2f001-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="2f001-113">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="2f001-113">Default value is 0</span></span>

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

### <span data-ttu-id="2f001-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f001-114">-DefaultProfile</span></span>
<span data-ttu-id="2f001-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f001-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f001-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2f001-116">-Name</span></span>
<span data-ttu-id="2f001-117">상태 프로브 설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f001-117">health probe setting name.</span></span>

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

### <span data-ttu-id="2f001-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="2f001-118">-SampleSize</span></span>
<span data-ttu-id="2f001-119">부하 분산 결정을 위해 고려할 샘플 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2f001-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="2f001-120">기본값은 4입니다.</span><span class="sxs-lookup"><span data-stu-id="2f001-120">Default value is 4</span></span>

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

### <span data-ttu-id="2f001-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="2f001-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="2f001-122">성공해야 하는 샘플 기간 내의 샘플 수는 기본값이 2입니다.</span><span class="sxs-lookup"><span data-stu-id="2f001-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="2f001-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f001-123">CommonParameters</span></span>
<span data-ttu-id="2f001-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f001-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f001-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2f001-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f001-126">입력</span><span class="sxs-lookup"><span data-stu-id="2f001-126">INPUTS</span></span>

### <span data-ttu-id="2f001-127">없음</span><span class="sxs-lookup"><span data-stu-id="2f001-127">None</span></span>

## <span data-ttu-id="2f001-128">출력</span><span class="sxs-lookup"><span data-stu-id="2f001-128">OUTPUTS</span></span>

### <span data-ttu-id="2f001-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="2f001-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="2f001-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f001-130">NOTES</span></span>

## <span data-ttu-id="2f001-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f001-131">RELATED LINKS</span></span>

<span data-ttu-id="2f001-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="2f001-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
