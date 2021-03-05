---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: fb068adcf7a7775106714dce9d91d23ae5e2c240
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984160"
---
# <span data-ttu-id="0504c-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="0504c-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="0504c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0504c-102">SYNOPSIS</span></span>
<span data-ttu-id="0504c-103">디바이스 보안 그룹에 대한 새 시간 창 규칙 만들기(IoT Security)</span><span class="sxs-lookup"><span data-stu-id="0504c-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="0504c-104">구문</span><span class="sxs-lookup"><span data-stu-id="0504c-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0504c-105">설명</span><span class="sxs-lookup"><span data-stu-id="0504c-105">DESCRIPTION</span></span>
<span data-ttu-id="0504c-106">New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet은 IoT 보안 솔루션의 디바이스 보안 그룹에 대한 새 시간 창 경고 규칙 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0504c-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="0504c-107">예제</span><span class="sxs-lookup"><span data-stu-id="0504c-107">EXAMPLES</span></span>

### <span data-ttu-id="0504c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0504c-108">Example 1</span></span>
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

<span data-ttu-id="0504c-109">"ActiveConnectionsNotInAllowedRange" 형식에서 새 시간 창 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="0504c-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="0504c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0504c-110">PARAMETERS</span></span>

### <span data-ttu-id="0504c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0504c-111">-DefaultProfile</span></span>
<span data-ttu-id="0504c-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0504c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0504c-113">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="0504c-113">-Enabled</span></span>
<span data-ttu-id="0504c-114">규칙이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0504c-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="0504c-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="0504c-115">-MaxThreshold</span></span>
<span data-ttu-id="0504c-116">최대 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="0504c-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="0504c-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="0504c-117">-MinThreshold</span></span>
<span data-ttu-id="0504c-118">최소 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="0504c-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="0504c-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="0504c-119">-TimeWindowSize</span></span>
<span data-ttu-id="0504c-120">시간 창 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="0504c-120">Time window size.</span></span>

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

### <span data-ttu-id="0504c-121">-Type</span><span class="sxs-lookup"><span data-stu-id="0504c-121">-Type</span></span>
<span data-ttu-id="0504c-122">규칙 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="0504c-122">Rule type.</span></span>

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

### <span data-ttu-id="0504c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0504c-123">CommonParameters</span></span>
<span data-ttu-id="0504c-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0504c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0504c-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0504c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0504c-126">입력</span><span class="sxs-lookup"><span data-stu-id="0504c-126">INPUTS</span></span>

### <span data-ttu-id="0504c-127">없음</span><span class="sxs-lookup"><span data-stu-id="0504c-127">None</span></span>

## <span data-ttu-id="0504c-128">출력</span><span class="sxs-lookup"><span data-stu-id="0504c-128">OUTPUTS</span></span>

### <span data-ttu-id="0504c-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="0504c-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="0504c-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0504c-130">NOTES</span></span>

## <span data-ttu-id="0504c-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0504c-131">RELATED LINKS</span></span>
