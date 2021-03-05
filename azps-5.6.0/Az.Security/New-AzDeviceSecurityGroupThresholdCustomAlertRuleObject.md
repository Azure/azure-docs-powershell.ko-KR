---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 869512fb91e86d90381bbcba9e492198b9a51005
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984176"
---
# <span data-ttu-id="21aea-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="21aea-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="21aea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21aea-102">SYNOPSIS</span></span>
<span data-ttu-id="21aea-103">디바이스 보안 그룹에 대한 새 임계값 사용자 지정 경고 규칙 만들기(IoT Security)</span><span class="sxs-lookup"><span data-stu-id="21aea-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="21aea-104">구문</span><span class="sxs-lookup"><span data-stu-id="21aea-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21aea-105">설명</span><span class="sxs-lookup"><span data-stu-id="21aea-105">DESCRIPTION</span></span>
<span data-ttu-id="21aea-106">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet은 IoT 보안 솔루션의 디바이스 보안 그룹에 대한 임계값 사용자 지정 경고 규칙의 새 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="21aea-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="21aea-107">예제</span><span class="sxs-lookup"><span data-stu-id="21aea-107">EXAMPLES</span></span>

### <span data-ttu-id="21aea-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="21aea-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="21aea-109">최소 및 최대 임계값에 대한 상태 사용 개미 값을 사용하여 "SomeRuleType" 형식에서 새 임계값 사용자 지정 경고 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="21aea-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="21aea-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="21aea-110">PARAMETERS</span></span>

### <span data-ttu-id="21aea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21aea-111">-DefaultProfile</span></span>
<span data-ttu-id="21aea-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21aea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21aea-113">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="21aea-113">-Enabled</span></span>
<span data-ttu-id="21aea-114">규칙이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21aea-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="21aea-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="21aea-115">-MaxThreshold</span></span>
<span data-ttu-id="21aea-116">최대 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="21aea-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="21aea-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="21aea-117">-MinThreshold</span></span>
<span data-ttu-id="21aea-118">최소 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="21aea-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="21aea-119">-Type</span><span class="sxs-lookup"><span data-stu-id="21aea-119">-Type</span></span>
<span data-ttu-id="21aea-120">규칙 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="21aea-120">Rule type.</span></span>

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

### <span data-ttu-id="21aea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21aea-121">CommonParameters</span></span>
<span data-ttu-id="21aea-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21aea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21aea-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21aea-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21aea-124">입력</span><span class="sxs-lookup"><span data-stu-id="21aea-124">INPUTS</span></span>

### <span data-ttu-id="21aea-125">없음</span><span class="sxs-lookup"><span data-stu-id="21aea-125">None</span></span>

## <span data-ttu-id="21aea-126">출력</span><span class="sxs-lookup"><span data-stu-id="21aea-126">OUTPUTS</span></span>

### <span data-ttu-id="21aea-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="21aea-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="21aea-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="21aea-128">NOTES</span></span>

## <span data-ttu-id="21aea-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21aea-129">RELATED LINKS</span></span>
