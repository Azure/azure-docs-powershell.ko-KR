---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: ac017af710531ff3294f858a8f95ad7529cd1c11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990612"
---
# <span data-ttu-id="b2d2a-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="b2d2a-101">Clear-AzDefault</span></span>

## <span data-ttu-id="b2d2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d2a-103">현재 컨텍스트에서 사용자가 설정한 기본값을 지운다.</span><span class="sxs-lookup"><span data-stu-id="b2d2a-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="b2d2a-104">구문</span><span class="sxs-lookup"><span data-stu-id="b2d2a-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2d2a-105">설명</span><span class="sxs-lookup"><span data-stu-id="b2d2a-105">DESCRIPTION</span></span>
<span data-ttu-id="b2d2a-106">Clear-AzDefault cmdlet은 사용자가 지정한 스위치 매개 변수에 따라 사용자가 설정한 기본값을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b2d2a-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="b2d2a-107">예제</span><span class="sxs-lookup"><span data-stu-id="b2d2a-107">EXAMPLES</span></span>

### <span data-ttu-id="b2d2a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b2d2a-108">Example 1</span></span>
```powershell
PS C:\> Clear-AzDefault
```

<span data-ttu-id="b2d2a-109">이 명령은 현재 컨텍스트에서 사용자가 설정한 모든 기본값을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b2d2a-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="b2d2a-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="b2d2a-110">Example 2</span></span>
```powershell
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="b2d2a-111">이 명령은 현재 컨텍스트에서 사용자가 설정한 기본 리소스 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b2d2a-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="b2d2a-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b2d2a-112">PARAMETERS</span></span>

### <span data-ttu-id="b2d2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d2a-113">-DefaultProfile</span></span>
<span data-ttu-id="b2d2a-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2d2a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2d2a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b2d2a-115">-Force</span></span>
<span data-ttu-id="b2d2a-116">기본값이 지정되지 않은 경우 모든 기본값 제거</span><span class="sxs-lookup"><span data-stu-id="b2d2a-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="b2d2a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2d2a-117">-PassThru</span></span>
<span data-ttu-id="b2d2a-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b2d2a-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b2d2a-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b2d2a-119">-ResourceGroup</span></span>
<span data-ttu-id="b2d2a-120">기본 리소스 그룹 지우기</span><span class="sxs-lookup"><span data-stu-id="b2d2a-120">Clear Default Resource Group</span></span>

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

### <span data-ttu-id="b2d2a-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="b2d2a-121">-Scope</span></span>
<span data-ttu-id="b2d2a-122">컨텍스트 변경 범위(예: 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용되는지 여부)를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2d2a-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="b2d2a-123">-확인</span><span class="sxs-lookup"><span data-stu-id="b2d2a-123">-Confirm</span></span>
<span data-ttu-id="b2d2a-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2d2a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2d2a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2d2a-125">-WhatIf</span></span>
<span data-ttu-id="b2d2a-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b2d2a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2d2a-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2d2a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2d2a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d2a-128">CommonParameters</span></span>
<span data-ttu-id="b2d2a-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b2d2a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d2a-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2d2a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d2a-131">입력</span><span class="sxs-lookup"><span data-stu-id="b2d2a-131">INPUTS</span></span>

### <span data-ttu-id="b2d2a-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b2d2a-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b2d2a-133">출력</span><span class="sxs-lookup"><span data-stu-id="b2d2a-133">OUTPUTS</span></span>

### <span data-ttu-id="b2d2a-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b2d2a-134">System.Boolean</span></span>

## <span data-ttu-id="b2d2a-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b2d2a-135">NOTES</span></span>

## <span data-ttu-id="b2d2a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2d2a-136">RELATED LINKS</span></span>
