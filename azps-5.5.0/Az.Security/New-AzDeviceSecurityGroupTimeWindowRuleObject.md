---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197905"
---
# <span data-ttu-id="41f61-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="41f61-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="41f61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41f61-102">SYNOPSIS</span></span>
<span data-ttu-id="41f61-103">디바이스 보안 그룹에 대한 새 기간 규칙 만들기(IoT 보안)</span><span class="sxs-lookup"><span data-stu-id="41f61-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="41f61-104">구문</span><span class="sxs-lookup"><span data-stu-id="41f61-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41f61-105">설명</span><span class="sxs-lookup"><span data-stu-id="41f61-105">DESCRIPTION</span></span>
<span data-ttu-id="41f61-106">이 New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet은 IoT 보안 솔루션의 디바이스 보안 그룹에 대한 새로운 시간 창 경고 규칙 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41f61-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="41f61-107">예제</span><span class="sxs-lookup"><span data-stu-id="41f61-107">EXAMPLES</span></span>

### <span data-ttu-id="41f61-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="41f61-108">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize $TimeWindowSize -MinThreshold 0 -MaxThreshold 30 -Enabled $true -Type "ActiveConnectionsNotInAllowedRange"

RuleType: "ActiveConnectionsNotInAllowedRange"
DisplayName: "Number of active connections is not in allowed range"
Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 30
TimeWindowSize: "PT5M"
```

<span data-ttu-id="41f61-109">"ActiveConnectionsNotInAllowedRange" 형식에서 새 기간 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="41f61-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="41f61-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41f61-110">PARAMETERS</span></span>

### <span data-ttu-id="41f61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f61-111">-DefaultProfile</span></span>
<span data-ttu-id="41f61-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41f61-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41f61-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="41f61-113">-Enabled</span></span>
<span data-ttu-id="41f61-114">규칙이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41f61-114">Is rule enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f61-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="41f61-115">-MaxThreshold</span></span>
<span data-ttu-id="41f61-116">최대 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="41f61-116">Maximum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f61-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="41f61-117">-MinThreshold</span></span>
<span data-ttu-id="41f61-118">최소 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="41f61-118">Minimum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f61-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="41f61-119">-TimeWindowSize</span></span>
<span data-ttu-id="41f61-120">기간 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="41f61-120">Time window size.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f61-121">-Type</span><span class="sxs-lookup"><span data-stu-id="41f61-121">-Type</span></span>
<span data-ttu-id="41f61-122">규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="41f61-122">Rule type.</span></span>

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

### <span data-ttu-id="41f61-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f61-123">CommonParameters</span></span>
<span data-ttu-id="41f61-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="41f61-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f61-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41f61-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f61-126">입력</span><span class="sxs-lookup"><span data-stu-id="41f61-126">INPUTS</span></span>

### <span data-ttu-id="41f61-127">없음</span><span class="sxs-lookup"><span data-stu-id="41f61-127">None</span></span>

## <span data-ttu-id="41f61-128">출력</span><span class="sxs-lookup"><span data-stu-id="41f61-128">OUTPUTS</span></span>

### <span data-ttu-id="41f61-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="41f61-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="41f61-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="41f61-130">NOTES</span></span>

## <span data-ttu-id="41f61-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41f61-131">RELATED LINKS</span></span>
