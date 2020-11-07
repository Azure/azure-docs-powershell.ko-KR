---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: 41d43bcb1164907bc7a06a7de4477f8a719604eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689282"
---
# <span data-ttu-id="0070c-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="0070c-101">Clear-AzDefault</span></span>

## <span data-ttu-id="0070c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0070c-102">SYNOPSIS</span></span>
<span data-ttu-id="0070c-103">현재 컨텍스트에서 사용자가 설정한 기본값을 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="0070c-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="0070c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0070c-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0070c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0070c-105">DESCRIPTION</span></span>
<span data-ttu-id="0070c-106">Clear-AzDefault cmdlet은 사용자가 지정한 스위치 매개 변수에 따라 사용자가 설정한 기본값을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0070c-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="0070c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0070c-107">EXAMPLES</span></span>

### <span data-ttu-id="0070c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0070c-108">Example 1</span></span>
```
PS C:\> Clear-AzDefault
```

<span data-ttu-id="0070c-109">이 명령은 현재 컨텍스트에서 사용자가 설정한 모든 기본값을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0070c-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="0070c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0070c-110">Example 1</span></span>
```
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="0070c-111">이 명령은 현재 컨텍스트에서 사용자가 설정한 기본 리소스 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0070c-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="0070c-112">변수</span><span class="sxs-lookup"><span data-stu-id="0070c-112">PARAMETERS</span></span>

### <span data-ttu-id="0070c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0070c-113">-DefaultProfile</span></span>
<span data-ttu-id="0070c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0070c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0070c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0070c-115">-Force</span></span>
<span data-ttu-id="0070c-116">기본값을 지정 하지 않으면 모든 기본값을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0070c-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="0070c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0070c-117">-PassThru</span></span>
<span data-ttu-id="0070c-118">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="0070c-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0070c-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0070c-119">-ResourceGroup</span></span>
<span data-ttu-id="0070c-120">기본 리소스 그룹 지우기</span><span class="sxs-lookup"><span data-stu-id="0070c-120">Clear Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0070c-121">-범위</span><span class="sxs-lookup"><span data-stu-id="0070c-121">-Scope</span></span>
<span data-ttu-id="0070c-122">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0070c-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0070c-123">-확인</span><span class="sxs-lookup"><span data-stu-id="0070c-123">-Confirm</span></span>
<span data-ttu-id="0070c-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0070c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0070c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0070c-125">-WhatIf</span></span>
<span data-ttu-id="0070c-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0070c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0070c-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0070c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0070c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0070c-128">CommonParameters</span></span>
<span data-ttu-id="0070c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0070c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0070c-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0070c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0070c-131">입력</span><span class="sxs-lookup"><span data-stu-id="0070c-131">INPUTS</span></span>

### <span data-ttu-id="0070c-132">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0070c-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0070c-133">출력</span><span class="sxs-lookup"><span data-stu-id="0070c-133">OUTPUTS</span></span>

### <span data-ttu-id="0070c-134">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0070c-134">System.Boolean</span></span>

## <span data-ttu-id="0070c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="0070c-135">NOTES</span></span>

## <span data-ttu-id="0070c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0070c-136">RELATED LINKS</span></span>
