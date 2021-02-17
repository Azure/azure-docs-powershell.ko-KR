---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197916"
---
# <span data-ttu-id="97219-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="97219-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="97219-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97219-102">SYNOPSIS</span></span>
<span data-ttu-id="97219-103">디바이스 보안 그룹에 대한 새 허용 목록 사용자 지정 경고 규칙 만들기(IoT 보안)</span><span class="sxs-lookup"><span data-stu-id="97219-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="97219-104">구문</span><span class="sxs-lookup"><span data-stu-id="97219-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97219-105">설명</span><span class="sxs-lookup"><span data-stu-id="97219-105">DESCRIPTION</span></span>
<span data-ttu-id="97219-106">이 New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet은 IoT 보안 솔루션에서 디바이스 보안 그룹에 대해 허용되는 사용자 지정 경고 규칙의 새 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97219-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="97219-107">예제</span><span class="sxs-lookup"><span data-stu-id="97219-107">EXAMPLES</span></span>

### <span data-ttu-id="97219-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="97219-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="97219-109">상태가 사용 안 하도록 설정된 "LocalUserNotAllowed" 형식에서 새 허용 목록 사용자 지정 경고 ull 만들기</span><span class="sxs-lookup"><span data-stu-id="97219-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="97219-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97219-110">PARAMETERS</span></span>

### <span data-ttu-id="97219-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="97219-111">-AllowlistValue</span></span>
<span data-ttu-id="97219-112">목록 값을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="97219-112">Allow list values.</span></span>

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

### <span data-ttu-id="97219-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97219-113">-DefaultProfile</span></span>
<span data-ttu-id="97219-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97219-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97219-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="97219-115">-Enabled</span></span>
<span data-ttu-id="97219-116">규칙이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97219-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="97219-117">-Type</span><span class="sxs-lookup"><span data-stu-id="97219-117">-Type</span></span>
<span data-ttu-id="97219-118">규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="97219-118">Rule type.</span></span>

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

### <span data-ttu-id="97219-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97219-119">CommonParameters</span></span>
<span data-ttu-id="97219-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="97219-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97219-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="97219-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97219-122">입력</span><span class="sxs-lookup"><span data-stu-id="97219-122">INPUTS</span></span>

### <span data-ttu-id="97219-123">없음</span><span class="sxs-lookup"><span data-stu-id="97219-123">None</span></span>

## <span data-ttu-id="97219-124">출력</span><span class="sxs-lookup"><span data-stu-id="97219-124">OUTPUTS</span></span>

### <span data-ttu-id="97219-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="97219-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="97219-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="97219-126">NOTES</span></span>

## <span data-ttu-id="97219-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97219-127">RELATED LINKS</span></span>
