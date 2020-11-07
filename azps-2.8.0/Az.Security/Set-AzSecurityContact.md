---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 1bf9e6b51899054899e819784872cf688a182e16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873177"
---
# <span data-ttu-id="73e3e-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="73e3e-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="73e3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="73e3e-103">구독에 대 한 보안 연락처를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73e3e-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="73e3e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73e3e-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73e3e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="73e3e-105">DESCRIPTION</span></span>
<span data-ttu-id="73e3e-106">구독에 대 한 보안 연락처를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73e3e-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="73e3e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="73e3e-107">EXAMPLES</span></span>

### <span data-ttu-id="73e3e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="73e3e-108">Example 1</span></span>
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

<span data-ttu-id="73e3e-109">구독에 대 한 보안 연락처를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73e3e-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="73e3e-110">변수</span><span class="sxs-lookup"><span data-stu-id="73e3e-110">PARAMETERS</span></span>

### <span data-ttu-id="73e3e-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="73e3e-111">-AlertAdmin</span></span>
<span data-ttu-id="73e3e-112">관리자에 게 알림이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73e3e-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="73e3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73e3e-113">-DefaultProfile</span></span>
<span data-ttu-id="73e3e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73e3e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73e3e-115">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="73e3e-115">-Email</span></span>
<span data-ttu-id="73e3e-116">이메일.</span><span class="sxs-lookup"><span data-stu-id="73e3e-116">E-Mail.</span></span>

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

### <span data-ttu-id="73e3e-117">-이름</span><span class="sxs-lookup"><span data-stu-id="73e3e-117">-Name</span></span>
<span data-ttu-id="73e3e-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73e3e-118">Resource name.</span></span>

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

### <span data-ttu-id="73e3e-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="73e3e-119">-NotifyOnAlert</span></span>
<span data-ttu-id="73e3e-120">알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="73e3e-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="73e3e-121">-전화</span><span class="sxs-lookup"><span data-stu-id="73e3e-121">-Phone</span></span>
<span data-ttu-id="73e3e-122">전화.</span><span class="sxs-lookup"><span data-stu-id="73e3e-122">Phone.</span></span>

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

### <span data-ttu-id="73e3e-123">-확인</span><span class="sxs-lookup"><span data-stu-id="73e3e-123">-Confirm</span></span>
<span data-ttu-id="73e3e-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73e3e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73e3e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73e3e-125">-WhatIf</span></span>
<span data-ttu-id="73e3e-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73e3e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73e3e-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73e3e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73e3e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e3e-128">CommonParameters</span></span>
<span data-ttu-id="73e3e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73e3e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e3e-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73e3e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e3e-131">입력</span><span class="sxs-lookup"><span data-stu-id="73e3e-131">INPUTS</span></span>

### <span data-ttu-id="73e3e-132">않아야</span><span class="sxs-lookup"><span data-stu-id="73e3e-132">None</span></span>

## <span data-ttu-id="73e3e-133">출력</span><span class="sxs-lookup"><span data-stu-id="73e3e-133">OUTPUTS</span></span>

### <span data-ttu-id="73e3e-134">Microsoft. Azure. m a m a 연락처. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="73e3e-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="73e3e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="73e3e-135">NOTES</span></span>

## <span data-ttu-id="73e3e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73e3e-136">RELATED LINKS</span></span>
