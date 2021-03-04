---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: f5307df3a91503f072c8292fe37957ce9af0df49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954928"
---
# <span data-ttu-id="0621e-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="0621e-101">Remove-AzContext</span></span>

## <span data-ttu-id="0621e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0621e-102">SYNOPSIS</span></span>
<span data-ttu-id="0621e-103">사용 가능한 컨텍스트 집합에서 컨텍스트 제거</span><span class="sxs-lookup"><span data-stu-id="0621e-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="0621e-104">구문</span><span class="sxs-lookup"><span data-stu-id="0621e-104">SYNTAX</span></span>

### <span data-ttu-id="0621e-105">RemoveByInputObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="0621e-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0621e-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="0621e-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="0621e-107">설명</span><span class="sxs-lookup"><span data-stu-id="0621e-107">DESCRIPTION</span></span>
<span data-ttu-id="0621e-108">컨텍스트 집합에서 Azure 컨텍스트 제거</span><span class="sxs-lookup"><span data-stu-id="0621e-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="0621e-109">예제</span><span class="sxs-lookup"><span data-stu-id="0621e-109">EXAMPLES</span></span>

### <span data-ttu-id="0621e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0621e-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="0621e-111">기본값이라는 컨텍스트 제거</span><span class="sxs-lookup"><span data-stu-id="0621e-111">Remove the context named default</span></span>

## <span data-ttu-id="0621e-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0621e-112">PARAMETERS</span></span>

### <span data-ttu-id="0621e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0621e-113">-DefaultProfile</span></span>
<span data-ttu-id="0621e-114">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0621e-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0621e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0621e-115">-Force</span></span>
<span data-ttu-id="0621e-116">기본값인 경우에도 컨텍스트 제거</span><span class="sxs-lookup"><span data-stu-id="0621e-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="0621e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0621e-117">-InputObject</span></span>
<span data-ttu-id="0621e-118">일반적으로 파이프라인을 통해 전달되는 컨텍스트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0621e-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0621e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0621e-119">-Name</span></span>
<span data-ttu-id="0621e-120">컨텍스트의 이름</span><span class="sxs-lookup"><span data-stu-id="0621e-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0621e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0621e-121">-PassThru</span></span>
<span data-ttu-id="0621e-122">제거된 컨텍스트 반환</span><span class="sxs-lookup"><span data-stu-id="0621e-122">Return the removed context</span></span>

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

### <span data-ttu-id="0621e-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="0621e-123">-Scope</span></span>
<span data-ttu-id="0621e-124">컨텍스트 변경 범위(예: 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용)를 결정</span><span class="sxs-lookup"><span data-stu-id="0621e-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="0621e-125">-확인</span><span class="sxs-lookup"><span data-stu-id="0621e-125">-Confirm</span></span>
<span data-ttu-id="0621e-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0621e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0621e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0621e-127">-WhatIf</span></span>
<span data-ttu-id="0621e-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0621e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0621e-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0621e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0621e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0621e-130">CommonParameters</span></span>
<span data-ttu-id="0621e-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0621e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0621e-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0621e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0621e-133">입력</span><span class="sxs-lookup"><span data-stu-id="0621e-133">INPUTS</span></span>

### <span data-ttu-id="0621e-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="0621e-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="0621e-135">출력</span><span class="sxs-lookup"><span data-stu-id="0621e-135">OUTPUTS</span></span>

### <span data-ttu-id="0621e-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="0621e-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="0621e-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0621e-137">NOTES</span></span>

## <span data-ttu-id="0621e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0621e-138">RELATED LINKS</span></span>
