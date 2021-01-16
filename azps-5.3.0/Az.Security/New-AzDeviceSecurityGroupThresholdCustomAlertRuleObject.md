---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377756"
---
# <span data-ttu-id="5bb81-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="5bb81-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="5bb81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bb81-102">SYNOPSIS</span></span>
<span data-ttu-id="5bb81-103">디바이스 보안 그룹에 대한 새 임계값 사용자 지정 경고 규칙 만들기(IoT 보안)</span><span class="sxs-lookup"><span data-stu-id="5bb81-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="5bb81-104">구문</span><span class="sxs-lookup"><span data-stu-id="5bb81-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bb81-105">설명</span><span class="sxs-lookup"><span data-stu-id="5bb81-105">DESCRIPTION</span></span>
<span data-ttu-id="5bb81-106">이 New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet은 IoT 보안 솔루션의 디바이스 보안 그룹에 대한 임계값 사용자 지정 경고 규칙의 새 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5bb81-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="5bb81-107">예제</span><span class="sxs-lookup"><span data-stu-id="5bb81-107">EXAMPLES</span></span>

### <span data-ttu-id="5bb81-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5bb81-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="5bb81-109">최소 및 최대 임계값에 대해 상태가 설정된 ant 값을 사용하여 "SomeRuleType" 형식의 새 임계값 사용자 지정 경고 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="5bb81-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="5bb81-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bb81-110">PARAMETERS</span></span>

### <span data-ttu-id="5bb81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bb81-111">-DefaultProfile</span></span>
<span data-ttu-id="5bb81-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5bb81-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bb81-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="5bb81-113">-Enabled</span></span>
<span data-ttu-id="5bb81-114">규칙이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bb81-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="5bb81-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="5bb81-115">-MaxThreshold</span></span>
<span data-ttu-id="5bb81-116">최대 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="5bb81-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="5bb81-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="5bb81-117">-MinThreshold</span></span>
<span data-ttu-id="5bb81-118">최소 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="5bb81-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="5bb81-119">-Type</span><span class="sxs-lookup"><span data-stu-id="5bb81-119">-Type</span></span>
<span data-ttu-id="5bb81-120">규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5bb81-120">Rule type.</span></span>

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

### <span data-ttu-id="5bb81-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bb81-121">CommonParameters</span></span>
<span data-ttu-id="5bb81-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5bb81-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bb81-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5bb81-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bb81-124">입력</span><span class="sxs-lookup"><span data-stu-id="5bb81-124">INPUTS</span></span>

### <span data-ttu-id="5bb81-125">없음</span><span class="sxs-lookup"><span data-stu-id="5bb81-125">None</span></span>

## <span data-ttu-id="5bb81-126">출력</span><span class="sxs-lookup"><span data-stu-id="5bb81-126">OUTPUTS</span></span>

### <span data-ttu-id="5bb81-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="5bb81-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="5bb81-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5bb81-128">NOTES</span></span>

## <span data-ttu-id="5bb81-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5bb81-129">RELATED LINKS</span></span>
