---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337401"
---
# <span data-ttu-id="13204-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="13204-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="13204-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13204-102">SYNOPSIS</span></span>
<span data-ttu-id="13204-103">디바이스 보안 그룹에 대한 새 거부 목록 사용자 지정 경고 규칙 만들기(IoT 보안)</span><span class="sxs-lookup"><span data-stu-id="13204-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="13204-104">구문</span><span class="sxs-lookup"><span data-stu-id="13204-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13204-105">설명</span><span class="sxs-lookup"><span data-stu-id="13204-105">DESCRIPTION</span></span>
<span data-ttu-id="13204-106">이 New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet은 IoT 보안 솔루션의 디바이스 보안 그룹에 대해 거부된 사용자 지정 경고 규칙의 새 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13204-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="13204-107">예제</span><span class="sxs-lookup"><span data-stu-id="13204-107">EXAMPLES</span></span>

### <span data-ttu-id="13204-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="13204-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="13204-109">"SomeRuleType" 및 상태를 desable으로 설정하여 새 거부 목록 사용자 지정 경고 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="13204-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="13204-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13204-110">PARAMETERS</span></span>

### <span data-ttu-id="13204-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13204-111">-DefaultProfile</span></span>
<span data-ttu-id="13204-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13204-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13204-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="13204-113">-DenylistValue</span></span>
<span data-ttu-id="13204-114">목록 값을 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="13204-114">Deny list values.</span></span>

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

### <span data-ttu-id="13204-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="13204-115">-Enabled</span></span>
<span data-ttu-id="13204-116">규칙이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13204-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="13204-117">-Type</span><span class="sxs-lookup"><span data-stu-id="13204-117">-Type</span></span>
<span data-ttu-id="13204-118">규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="13204-118">Rule type.</span></span>

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

### <span data-ttu-id="13204-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13204-119">CommonParameters</span></span>
<span data-ttu-id="13204-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13204-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13204-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13204-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13204-122">입력</span><span class="sxs-lookup"><span data-stu-id="13204-122">INPUTS</span></span>

### <span data-ttu-id="13204-123">없음</span><span class="sxs-lookup"><span data-stu-id="13204-123">None</span></span>

## <span data-ttu-id="13204-124">출력</span><span class="sxs-lookup"><span data-stu-id="13204-124">OUTPUTS</span></span>

### <span data-ttu-id="13204-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="13204-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="13204-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13204-126">NOTES</span></span>

## <span data-ttu-id="13204-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13204-127">RELATED LINKS</span></span>
