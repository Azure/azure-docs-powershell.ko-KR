---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218013"
---
# <span data-ttu-id="95fbc-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="95fbc-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="95fbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="95fbc-103">장치 보안 그룹에 대 한 새 임계값 사용자 지정 알림 규칙 만들기 (IoT 보안)</span><span class="sxs-lookup"><span data-stu-id="95fbc-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="95fbc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95fbc-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95fbc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95fbc-105">DESCRIPTION</span></span>
<span data-ttu-id="95fbc-106">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet은 IoT security 솔루션에서 디바이스 보안 그룹에 대 한 임계값 사용자 지정 알림 규칙의 새 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95fbc-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="95fbc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="95fbc-107">EXAMPLES</span></span>

### <span data-ttu-id="95fbc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="95fbc-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="95fbc-109">상태를 사용 하 여 "SomeRuleType" 형식에서 새 임계값 사용자 지정 알림 규칙 만들기 최소 및 최대 임계값에 대 한 ant 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95fbc-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="95fbc-110">변수</span><span class="sxs-lookup"><span data-stu-id="95fbc-110">PARAMETERS</span></span>

### <span data-ttu-id="95fbc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95fbc-111">-DefaultProfile</span></span>
<span data-ttu-id="95fbc-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95fbc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95fbc-113">-사용</span><span class="sxs-lookup"><span data-stu-id="95fbc-113">-Enabled</span></span>
<span data-ttu-id="95fbc-114">규칙을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95fbc-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="95fbc-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="95fbc-115">-MaxThreshold</span></span>
<span data-ttu-id="95fbc-116">최대 임계값.</span><span class="sxs-lookup"><span data-stu-id="95fbc-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="95fbc-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="95fbc-117">-MinThreshold</span></span>
<span data-ttu-id="95fbc-118">최소 임계값.</span><span class="sxs-lookup"><span data-stu-id="95fbc-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="95fbc-119">-Type</span><span class="sxs-lookup"><span data-stu-id="95fbc-119">-Type</span></span>
<span data-ttu-id="95fbc-120">규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="95fbc-120">Rule type.</span></span>

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

### <span data-ttu-id="95fbc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95fbc-121">CommonParameters</span></span>
<span data-ttu-id="95fbc-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95fbc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95fbc-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95fbc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95fbc-124">입력</span><span class="sxs-lookup"><span data-stu-id="95fbc-124">INPUTS</span></span>

### <span data-ttu-id="95fbc-125">않아야</span><span class="sxs-lookup"><span data-stu-id="95fbc-125">None</span></span>

## <span data-ttu-id="95fbc-126">출력</span><span class="sxs-lookup"><span data-stu-id="95fbc-126">OUTPUTS</span></span>

### <span data-ttu-id="95fbc-127">DeviceSecurityGroups. PSThresholdCustomAlertRule에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="95fbc-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="95fbc-128">상속자</span><span class="sxs-lookup"><span data-stu-id="95fbc-128">NOTES</span></span>

## <span data-ttu-id="95fbc-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95fbc-129">RELATED LINKS</span></span>
