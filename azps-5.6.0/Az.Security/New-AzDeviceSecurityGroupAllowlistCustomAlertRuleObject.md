---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: 0f46a0f009085aa7ef7b66ac91d621338a7358b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979280"
---
# <span data-ttu-id="90c72-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="90c72-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="90c72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90c72-102">SYNOPSIS</span></span>
<span data-ttu-id="90c72-103">디바이스 보안 그룹에 대한 새 허용 목록 사용자 지정 경고 규칙 만들기(IoT Security)</span><span class="sxs-lookup"><span data-stu-id="90c72-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="90c72-104">구문</span><span class="sxs-lookup"><span data-stu-id="90c72-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90c72-105">설명</span><span class="sxs-lookup"><span data-stu-id="90c72-105">DESCRIPTION</span></span>
<span data-ttu-id="90c72-106">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet은 IoT 보안 솔루션에서 디바이스 보안 그룹에 대해 허용되는 사용자 지정 경고 규칙의 새 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90c72-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="90c72-107">예제</span><span class="sxs-lookup"><span data-stu-id="90c72-107">EXAMPLES</span></span>

### <span data-ttu-id="90c72-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="90c72-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="90c72-109">사용 안 하도록 설정되어 있는 "LocalUserNotAllowed" 형식의 새 허용 목록 사용자 지정 경고 헐 만들기</span><span class="sxs-lookup"><span data-stu-id="90c72-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="90c72-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="90c72-110">PARAMETERS</span></span>

### <span data-ttu-id="90c72-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="90c72-111">-AllowlistValue</span></span>
<span data-ttu-id="90c72-112">목록 값을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="90c72-112">Allow list values.</span></span>

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

### <span data-ttu-id="90c72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c72-113">-DefaultProfile</span></span>
<span data-ttu-id="90c72-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90c72-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90c72-115">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="90c72-115">-Enabled</span></span>
<span data-ttu-id="90c72-116">규칙이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90c72-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="90c72-117">-Type</span><span class="sxs-lookup"><span data-stu-id="90c72-117">-Type</span></span>
<span data-ttu-id="90c72-118">규칙 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="90c72-118">Rule type.</span></span>

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

### <span data-ttu-id="90c72-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c72-119">CommonParameters</span></span>
<span data-ttu-id="90c72-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90c72-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c72-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90c72-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c72-122">입력</span><span class="sxs-lookup"><span data-stu-id="90c72-122">INPUTS</span></span>

### <span data-ttu-id="90c72-123">없음</span><span class="sxs-lookup"><span data-stu-id="90c72-123">None</span></span>

## <span data-ttu-id="90c72-124">출력</span><span class="sxs-lookup"><span data-stu-id="90c72-124">OUTPUTS</span></span>

### <span data-ttu-id="90c72-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="90c72-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="90c72-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90c72-126">NOTES</span></span>

## <span data-ttu-id="90c72-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90c72-127">RELATED LINKS</span></span>
