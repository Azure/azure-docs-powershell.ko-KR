---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216195"
---
# <span data-ttu-id="54ccb-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="54ccb-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="54ccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="54ccb-103">장치 보안 그룹에 대 한 새 시간 창 규칙 만들기 (IoT 보안)</span><span class="sxs-lookup"><span data-stu-id="54ccb-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="54ccb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54ccb-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54ccb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="54ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="54ccb-106">New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet은 IoT security 솔루션에서 장치 보안 그룹에 대 한 새 시간 창 알림 규칙 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54ccb-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="54ccb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="54ccb-107">EXAMPLES</span></span>

### <span data-ttu-id="54ccb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="54ccb-108">Example 1</span></span>
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

<span data-ttu-id="54ccb-109">"ActiveConnectionsNotInAllowedRange" 형식으로 새 시간 창 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="54ccb-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="54ccb-110">변수</span><span class="sxs-lookup"><span data-stu-id="54ccb-110">PARAMETERS</span></span>

### <span data-ttu-id="54ccb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54ccb-111">-DefaultProfile</span></span>
<span data-ttu-id="54ccb-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54ccb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54ccb-113">-사용</span><span class="sxs-lookup"><span data-stu-id="54ccb-113">-Enabled</span></span>
<span data-ttu-id="54ccb-114">규칙을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54ccb-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="54ccb-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="54ccb-115">-MaxThreshold</span></span>
<span data-ttu-id="54ccb-116">최대 임계값.</span><span class="sxs-lookup"><span data-stu-id="54ccb-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="54ccb-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="54ccb-117">-MinThreshold</span></span>
<span data-ttu-id="54ccb-118">최소 임계값.</span><span class="sxs-lookup"><span data-stu-id="54ccb-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="54ccb-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="54ccb-119">-TimeWindowSize</span></span>
<span data-ttu-id="54ccb-120">시간 창 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="54ccb-120">Time window size.</span></span>

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

### <span data-ttu-id="54ccb-121">-Type</span><span class="sxs-lookup"><span data-stu-id="54ccb-121">-Type</span></span>
<span data-ttu-id="54ccb-122">규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="54ccb-122">Rule type.</span></span>

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

### <span data-ttu-id="54ccb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ccb-123">CommonParameters</span></span>
<span data-ttu-id="54ccb-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54ccb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ccb-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="54ccb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ccb-126">입력</span><span class="sxs-lookup"><span data-stu-id="54ccb-126">INPUTS</span></span>

### <span data-ttu-id="54ccb-127">않아야</span><span class="sxs-lookup"><span data-stu-id="54ccb-127">None</span></span>

## <span data-ttu-id="54ccb-128">출력</span><span class="sxs-lookup"><span data-stu-id="54ccb-128">OUTPUTS</span></span>

### <span data-ttu-id="54ccb-129">DeviceSecurityGroups. PSTimeWindowCustomAlertRule에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="54ccb-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="54ccb-130">상속자</span><span class="sxs-lookup"><span data-stu-id="54ccb-130">NOTES</span></span>

## <span data-ttu-id="54ccb-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54ccb-131">RELATED LINKS</span></span>
