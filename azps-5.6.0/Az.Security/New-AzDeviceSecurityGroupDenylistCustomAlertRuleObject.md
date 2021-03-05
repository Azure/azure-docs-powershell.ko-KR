---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0b915176858c0641ca3076ea10022ae193718807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979275"
---
# <span data-ttu-id="0ae5a-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="0ae5a-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="0ae5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ae5a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae5a-103">디바이스 보안 그룹에 대한 새 거부 목록 사용자 지정 경고 규칙 만들기(IoT Security)</span><span class="sxs-lookup"><span data-stu-id="0ae5a-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="0ae5a-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ae5a-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ae5a-105">설명</span><span class="sxs-lookup"><span data-stu-id="0ae5a-105">DESCRIPTION</span></span>
<span data-ttu-id="0ae5a-106">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet은 IoT 보안 솔루션의 디바이스 보안 그룹에 대한 거부된 사용자 지정 경고 규칙의 새 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ae5a-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="0ae5a-107">예제</span><span class="sxs-lookup"><span data-stu-id="0ae5a-107">EXAMPLES</span></span>

### <span data-ttu-id="0ae5a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0ae5a-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="0ae5a-109">rull 형식 "SomeRuleType" 및 상태를 desable로 설정하여 새 거부 목록 사용자 지정 경고 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="0ae5a-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="0ae5a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ae5a-110">PARAMETERS</span></span>

### <span data-ttu-id="0ae5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ae5a-111">-DefaultProfile</span></span>
<span data-ttu-id="0ae5a-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae5a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ae5a-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="0ae5a-113">-DenylistValue</span></span>
<span data-ttu-id="0ae5a-114">목록 값을 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae5a-114">Deny list values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ae5a-115">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="0ae5a-115">-Enabled</span></span>
<span data-ttu-id="0ae5a-116">규칙이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ae5a-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="0ae5a-117">-Type</span><span class="sxs-lookup"><span data-stu-id="0ae5a-117">-Type</span></span>
<span data-ttu-id="0ae5a-118">규칙 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae5a-118">Rule type.</span></span>

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

### <span data-ttu-id="0ae5a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae5a-119">CommonParameters</span></span>
<span data-ttu-id="0ae5a-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae5a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae5a-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ae5a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae5a-122">입력</span><span class="sxs-lookup"><span data-stu-id="0ae5a-122">INPUTS</span></span>

### <span data-ttu-id="0ae5a-123">없음</span><span class="sxs-lookup"><span data-stu-id="0ae5a-123">None</span></span>

## <span data-ttu-id="0ae5a-124">출력</span><span class="sxs-lookup"><span data-stu-id="0ae5a-124">OUTPUTS</span></span>

### <span data-ttu-id="0ae5a-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="0ae5a-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="0ae5a-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ae5a-126">NOTES</span></span>

## <span data-ttu-id="0ae5a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ae5a-127">RELATED LINKS</span></span>
