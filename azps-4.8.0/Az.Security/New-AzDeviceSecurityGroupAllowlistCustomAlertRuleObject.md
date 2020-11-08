---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047630"
---
# <span data-ttu-id="f2e07-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="f2e07-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="f2e07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2e07-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e07-103">장치 보안 그룹에 대 한 새 허용 목록 사용자 지정 알림 규칙 만들기 (IoT 보안)</span><span class="sxs-lookup"><span data-stu-id="f2e07-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="f2e07-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2e07-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2e07-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f2e07-105">DESCRIPTION</span></span>
<span data-ttu-id="f2e07-106">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet은 IoT security 솔루션에서 장치 보안 그룹에 대해 허용 되는 사용자 지정 알림 규칙의 새 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f2e07-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="f2e07-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f2e07-107">EXAMPLES</span></span>

### <span data-ttu-id="f2e07-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f2e07-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="f2e07-109">새 허용 목록 만들기 "LocalUserNotAllowed" 유형에 서 사용 안 함으로 설정 된 사용자 지정 경고 rull</span><span class="sxs-lookup"><span data-stu-id="f2e07-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="f2e07-110">변수</span><span class="sxs-lookup"><span data-stu-id="f2e07-110">PARAMETERS</span></span>

### <span data-ttu-id="f2e07-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="f2e07-111">-AllowlistValue</span></span>
<span data-ttu-id="f2e07-112">허용 목록 값.</span><span class="sxs-lookup"><span data-stu-id="f2e07-112">Allow list values.</span></span>

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

### <span data-ttu-id="f2e07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e07-113">-DefaultProfile</span></span>
<span data-ttu-id="f2e07-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e07-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2e07-115">-사용</span><span class="sxs-lookup"><span data-stu-id="f2e07-115">-Enabled</span></span>
<span data-ttu-id="f2e07-116">규칙을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e07-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="f2e07-117">-Type</span><span class="sxs-lookup"><span data-stu-id="f2e07-117">-Type</span></span>
<span data-ttu-id="f2e07-118">규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e07-118">Rule type.</span></span>

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

### <span data-ttu-id="f2e07-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e07-119">CommonParameters</span></span>
<span data-ttu-id="f2e07-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e07-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e07-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f2e07-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e07-122">입력</span><span class="sxs-lookup"><span data-stu-id="f2e07-122">INPUTS</span></span>

### <span data-ttu-id="f2e07-123">않아야</span><span class="sxs-lookup"><span data-stu-id="f2e07-123">None</span></span>

## <span data-ttu-id="f2e07-124">출력</span><span class="sxs-lookup"><span data-stu-id="f2e07-124">OUTPUTS</span></span>

### <span data-ttu-id="f2e07-125">DeviceSecurityGroups. PSAllowlistCustomAlertRule에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="f2e07-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="f2e07-126">상속자</span><span class="sxs-lookup"><span data-stu-id="f2e07-126">NOTES</span></span>

## <span data-ttu-id="f2e07-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2e07-127">RELATED LINKS</span></span>
