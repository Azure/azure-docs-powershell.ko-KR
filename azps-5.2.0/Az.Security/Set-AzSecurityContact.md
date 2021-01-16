---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 504f07092a0a8e246e778421748f1cd807b04a77
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356366"
---
# <span data-ttu-id="aa663-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="aa663-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="aa663-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa663-102">SYNOPSIS</span></span>
<span data-ttu-id="aa663-103">구독에 대한 보안 연락처를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aa663-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="aa663-104">구문</span><span class="sxs-lookup"><span data-stu-id="aa663-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa663-105">설명</span><span class="sxs-lookup"><span data-stu-id="aa663-105">DESCRIPTION</span></span>
<span data-ttu-id="aa663-106">구독에 대한 보안 연락처를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aa663-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="aa663-107">예제</span><span class="sxs-lookup"><span data-stu-id="aa663-107">EXAMPLES</span></span>

### <span data-ttu-id="aa663-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="aa663-108">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="aa663-109">구독에 대한 보안 연락처를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aa663-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="aa663-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa663-110">PARAMETERS</span></span>

### <span data-ttu-id="aa663-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="aa663-111">-AlertAdmin</span></span>
<span data-ttu-id="aa663-112">관리자에게 경고합니다.</span><span class="sxs-lookup"><span data-stu-id="aa663-112">Alerts To Administrators.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa663-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa663-113">-DefaultProfile</span></span>
<span data-ttu-id="aa663-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa663-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa663-115">-Email</span><span class="sxs-lookup"><span data-stu-id="aa663-115">-Email</span></span>
<span data-ttu-id="aa663-116">전자 메일.</span><span class="sxs-lookup"><span data-stu-id="aa663-116">E-Mail.</span></span>

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

### <span data-ttu-id="aa663-117">-Name</span><span class="sxs-lookup"><span data-stu-id="aa663-117">-Name</span></span>
<span data-ttu-id="aa663-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa663-118">Resource name.</span></span>

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

### <span data-ttu-id="aa663-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="aa663-119">-NotifyOnAlert</span></span>
<span data-ttu-id="aa663-120">경고 알림.</span><span class="sxs-lookup"><span data-stu-id="aa663-120">Alert Notifications.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa663-121">-Phone</span><span class="sxs-lookup"><span data-stu-id="aa663-121">-Phone</span></span>
<span data-ttu-id="aa663-122">전화.</span><span class="sxs-lookup"><span data-stu-id="aa663-122">Phone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa663-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa663-123">-Confirm</span></span>
<span data-ttu-id="aa663-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa663-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa663-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa663-125">-WhatIf</span></span>
<span data-ttu-id="aa663-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="aa663-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa663-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa663-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa663-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa663-128">CommonParameters</span></span>
<span data-ttu-id="aa663-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa663-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa663-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aa663-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa663-131">입력</span><span class="sxs-lookup"><span data-stu-id="aa663-131">INPUTS</span></span>

### <span data-ttu-id="aa663-132">없음</span><span class="sxs-lookup"><span data-stu-id="aa663-132">None</span></span>

## <span data-ttu-id="aa663-133">출력</span><span class="sxs-lookup"><span data-stu-id="aa663-133">OUTPUTS</span></span>

### <span data-ttu-id="aa663-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="aa663-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="aa663-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa663-135">NOTES</span></span>

## <span data-ttu-id="aa663-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa663-136">RELATED LINKS</span></span>
