---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216734"
---
# <span data-ttu-id="da305-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="da305-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="da305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da305-102">SYNOPSIS</span></span>
<span data-ttu-id="da305-103">새 거부 목록 만들기 장치 보안 그룹에 대 한 사용자 지정 알림 규칙 (IoT 보안)</span><span class="sxs-lookup"><span data-stu-id="da305-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="da305-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da305-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da305-105">설명은</span><span class="sxs-lookup"><span data-stu-id="da305-105">DESCRIPTION</span></span>
<span data-ttu-id="da305-106">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet은 IoT security 솔루션에서 장치 보안 그룹에 대 한 denyed 사용자 지정 알림 규칙의 새 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da305-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="da305-107">예제의</span><span class="sxs-lookup"><span data-stu-id="da305-107">EXAMPLES</span></span>

### <span data-ttu-id="da305-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="da305-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="da305-109">새 거부 목록 만들기 rull 유형이 "SomeRuleType"이 고 상태가 desable로 설정 된 사용자 지정 알림 규칙</span><span class="sxs-lookup"><span data-stu-id="da305-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="da305-110">변수</span><span class="sxs-lookup"><span data-stu-id="da305-110">PARAMETERS</span></span>

### <span data-ttu-id="da305-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da305-111">-DefaultProfile</span></span>
<span data-ttu-id="da305-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da305-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da305-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="da305-113">-DenylistValue</span></span>
<span data-ttu-id="da305-114">목록 값을 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="da305-114">Deny list values.</span></span>

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

### <span data-ttu-id="da305-115">-사용</span><span class="sxs-lookup"><span data-stu-id="da305-115">-Enabled</span></span>
<span data-ttu-id="da305-116">규칙을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da305-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="da305-117">-Type</span><span class="sxs-lookup"><span data-stu-id="da305-117">-Type</span></span>
<span data-ttu-id="da305-118">규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="da305-118">Rule type.</span></span>

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

### <span data-ttu-id="da305-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da305-119">CommonParameters</span></span>
<span data-ttu-id="da305-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da305-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da305-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da305-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da305-122">입력</span><span class="sxs-lookup"><span data-stu-id="da305-122">INPUTS</span></span>

### <span data-ttu-id="da305-123">않아야</span><span class="sxs-lookup"><span data-stu-id="da305-123">None</span></span>

## <span data-ttu-id="da305-124">출력</span><span class="sxs-lookup"><span data-stu-id="da305-124">OUTPUTS</span></span>

### <span data-ttu-id="da305-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="da305-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="da305-126">상속자</span><span class="sxs-lookup"><span data-stu-id="da305-126">NOTES</span></span>

## <span data-ttu-id="da305-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da305-127">RELATED LINKS</span></span>
