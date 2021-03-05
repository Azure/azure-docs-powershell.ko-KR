---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 8cd5adee5e8b992cf709b76996a70760f3fd90a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986510"
---
# <span data-ttu-id="d3df1-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="d3df1-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="d3df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3df1-102">SYNOPSIS</span></span>
<span data-ttu-id="d3df1-103">구독에 대한 보안 연락처를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="d3df1-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3df1-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3df1-105">설명</span><span class="sxs-lookup"><span data-stu-id="d3df1-105">DESCRIPTION</span></span>
<span data-ttu-id="d3df1-106">구독에 대한 보안 연락처를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="d3df1-107">예제</span><span class="sxs-lookup"><span data-stu-id="d3df1-107">EXAMPLES</span></span>

### <span data-ttu-id="d3df1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d3df1-108">Example 1</span></span>
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

<span data-ttu-id="d3df1-109">구독에 대한 보안 연락처를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="d3df1-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d3df1-110">PARAMETERS</span></span>

### <span data-ttu-id="d3df1-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="d3df1-111">-AlertAdmin</span></span>
<span data-ttu-id="d3df1-112">관리자에 대한 경고입니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="d3df1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3df1-113">-DefaultProfile</span></span>
<span data-ttu-id="d3df1-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3df1-115">-email</span><span class="sxs-lookup"><span data-stu-id="d3df1-115">-Email</span></span>
<span data-ttu-id="d3df1-116">전자 메일.</span><span class="sxs-lookup"><span data-stu-id="d3df1-116">E-Mail.</span></span>

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

### <span data-ttu-id="d3df1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d3df1-117">-Name</span></span>
<span data-ttu-id="d3df1-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-118">Resource name.</span></span>

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

### <span data-ttu-id="d3df1-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="d3df1-119">-NotifyOnAlert</span></span>
<span data-ttu-id="d3df1-120">경고 알림.</span><span class="sxs-lookup"><span data-stu-id="d3df1-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="d3df1-121">-Phone</span><span class="sxs-lookup"><span data-stu-id="d3df1-121">-Phone</span></span>
<span data-ttu-id="d3df1-122">전화.</span><span class="sxs-lookup"><span data-stu-id="d3df1-122">Phone.</span></span>

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

### <span data-ttu-id="d3df1-123">-확인</span><span class="sxs-lookup"><span data-stu-id="d3df1-123">-Confirm</span></span>
<span data-ttu-id="d3df1-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3df1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3df1-125">-WhatIf</span></span>
<span data-ttu-id="d3df1-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3df1-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3df1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3df1-128">CommonParameters</span></span>
<span data-ttu-id="d3df1-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3df1-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3df1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3df1-131">입력</span><span class="sxs-lookup"><span data-stu-id="d3df1-131">INPUTS</span></span>

### <span data-ttu-id="d3df1-132">없음</span><span class="sxs-lookup"><span data-stu-id="d3df1-132">None</span></span>

## <span data-ttu-id="d3df1-133">출력</span><span class="sxs-lookup"><span data-stu-id="d3df1-133">OUTPUTS</span></span>

### <span data-ttu-id="d3df1-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="d3df1-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="d3df1-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d3df1-135">NOTES</span></span>

## <span data-ttu-id="d3df1-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3df1-136">RELATED LINKS</span></span>
