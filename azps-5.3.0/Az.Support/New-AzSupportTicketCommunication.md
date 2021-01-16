---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384189"
---
# <span data-ttu-id="fb6d7-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="fb6d7-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="fb6d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6d7-103">새 지원 티켓 통신을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d7-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="fb6d7-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb6d7-104">SYNTAX</span></span>

### <span data-ttu-id="fb6d7-105">CreateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fb6d7-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb6d7-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb6d7-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb6d7-107">설명</span><span class="sxs-lookup"><span data-stu-id="fb6d7-107">DESCRIPTION</span></span>
<span data-ttu-id="fb6d7-108">Azure 지원 티켓에 새 고객 통신을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d7-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="fb6d7-109">예제</span><span class="sxs-lookup"><span data-stu-id="fb6d7-109">EXAMPLES</span></span>

### <span data-ttu-id="fb6d7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb6d7-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="fb6d7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb6d7-111">PARAMETERS</span></span>

### <span data-ttu-id="fb6d7-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb6d7-112">-AsJob</span></span>
<span data-ttu-id="fb6d7-113">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d7-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="fb6d7-114">-Body</span><span class="sxs-lookup"><span data-stu-id="fb6d7-114">-Body</span></span>
<span data-ttu-id="fb6d7-115">통신 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d7-115">Body of the communication.</span></span>

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

### <span data-ttu-id="fb6d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6d7-116">-DefaultProfile</span></span>
<span data-ttu-id="fb6d7-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb6d7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fb6d7-118">-Name</span></span>
<span data-ttu-id="fb6d7-119">통신 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d7-119">Name of the communication resource.</span></span>

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

### <span data-ttu-id="fb6d7-120">-Sender</span><span class="sxs-lookup"><span data-stu-id="fb6d7-120">-Sender</span></span>
<span data-ttu-id="fb6d7-121">보낸 사람 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d7-121">Email address of the sender.</span></span>

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

### <span data-ttu-id="fb6d7-122">-Subject</span><span class="sxs-lookup"><span data-stu-id="fb6d7-122">-Subject</span></span>
<span data-ttu-id="fb6d7-123">통신의 주체입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d7-123">Subject of the communication.</span></span>

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

### <span data-ttu-id="fb6d7-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="fb6d7-124">-SupportTicketName</span></span>
<span data-ttu-id="fb6d7-125">지원 티켓 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d7-125">Support ticket name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6d7-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="fb6d7-126">-SupportTicketObject</span></span>
<span data-ttu-id="fb6d7-127">지원 티켓 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d7-127">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb6d7-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb6d7-128">-Confirm</span></span>
<span data-ttu-id="fb6d7-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb6d7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb6d7-130">-WhatIf</span></span>
<span data-ttu-id="fb6d7-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fb6d7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb6d7-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb6d7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6d7-133">CommonParameters</span></span>
<span data-ttu-id="fb6d7-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6d7-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fb6d7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6d7-136">입력</span><span class="sxs-lookup"><span data-stu-id="fb6d7-136">INPUTS</span></span>

### <span data-ttu-id="fb6d7-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="fb6d7-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="fb6d7-138">출력</span><span class="sxs-lookup"><span data-stu-id="fb6d7-138">OUTPUTS</span></span>

### <span data-ttu-id="fb6d7-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="fb6d7-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="fb6d7-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb6d7-140">NOTES</span></span>

## <span data-ttu-id="fb6d7-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb6d7-141">RELATED LINKS</span></span>
