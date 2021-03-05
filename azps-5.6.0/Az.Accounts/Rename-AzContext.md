---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 2ff8297ff04f18a903cca3a262d5232ace7c6ef1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965536"
---
# <span data-ttu-id="3c5d1-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="3c5d1-101">Rename-AzContext</span></span>

## <span data-ttu-id="3c5d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c5d1-102">SYNOPSIS</span></span>
<span data-ttu-id="3c5d1-103">Azure 컨텍스트의 이름을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-103">Rename an Azure context.</span></span>  <span data-ttu-id="3c5d1-104">기본 컨텍스트는 사용자 계정 및 구독에 의해 명명됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="3c5d1-105">구문</span><span class="sxs-lookup"><span data-stu-id="3c5d1-105">SYNTAX</span></span>

### <span data-ttu-id="3c5d1-106">이름 변경ByInputObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="3c5d1-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="3c5d1-107">이름명ByName</span><span class="sxs-lookup"><span data-stu-id="3c5d1-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="3c5d1-108">설명</span><span class="sxs-lookup"><span data-stu-id="3c5d1-108">DESCRIPTION</span></span>
<span data-ttu-id="3c5d1-109">Azure 컨텍스트의 이름을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-109">Rename an Azure context.</span></span>  <span data-ttu-id="3c5d1-110">기본 컨텍스트는 사용자 계정 및 구독에 의해 명명됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="3c5d1-111">예제</span><span class="sxs-lookup"><span data-stu-id="3c5d1-111">EXAMPLES</span></span>

### <span data-ttu-id="3c5d1-112">예제 1: 명명된 매개 변수를 사용하여 컨텍스트 이름 변경</span><span class="sxs-lookup"><span data-stu-id="3c5d1-112">Example 1: Rename a context using named parameters</span></span>
```powershell
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="3c5d1-113">'에 대한 컨텍스트의 이름을 user1@contoso.org '12345-6789-2345-3567890'로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="3c5d1-114">이 명령 후 'Select-AzContext Work'를 사용하여 컨텍스트를 대상으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="3c5d1-115">탭 완료를 사용하여 'SourceName'에 대한 값을 탭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="3c5d1-116">예제 2: 위치 매개 변수를 사용하여 컨텍스트 이름 변경</span><span class="sxs-lookup"><span data-stu-id="3c5d1-116">Example 2: Rename a context using positional parameters</span></span>
```powershell
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="3c5d1-117">"내 컨텍스트"라는 컨텍스트의 이름을 "Work"로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="3c5d1-118">이 명령 후 작업에서 컨텍스트를 대상으로 Select-AzContext 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="3c5d1-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3c5d1-119">PARAMETERS</span></span>

### <span data-ttu-id="3c5d1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c5d1-120">-DefaultProfile</span></span>
<span data-ttu-id="3c5d1-121">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3c5d1-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c5d1-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3c5d1-122">-Force</span></span>
<span data-ttu-id="3c5d1-123">대상 컨텍스트가 이미 있는 경우에도 컨텍스트 이름을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="3c5d1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c5d1-124">-InputObject</span></span>
<span data-ttu-id="3c5d1-125">일반적으로 파이프라인을 통해 전달되는 컨텍스트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c5d1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c5d1-126">-PassThru</span></span>
<span data-ttu-id="3c5d1-127">이름을 변경한 컨텍스트를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="3c5d1-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="3c5d1-128">-Scope</span></span>
<span data-ttu-id="3c5d1-129">컨텍스트 변경 범위(예: 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용)를 결정</span><span class="sxs-lookup"><span data-stu-id="3c5d1-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="3c5d1-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="3c5d1-130">-SourceName</span></span>
<span data-ttu-id="3c5d1-131">컨텍스트의 이름</span><span class="sxs-lookup"><span data-stu-id="3c5d1-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c5d1-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="3c5d1-132">-TargetName</span></span>
<span data-ttu-id="3c5d1-133">컨텍스트의 새 이름</span><span class="sxs-lookup"><span data-stu-id="3c5d1-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c5d1-134">-확인</span><span class="sxs-lookup"><span data-stu-id="3c5d1-134">-Confirm</span></span>
<span data-ttu-id="3c5d1-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c5d1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c5d1-136">-WhatIf</span></span>
<span data-ttu-id="3c5d1-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c5d1-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c5d1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c5d1-139">CommonParameters</span></span>
<span data-ttu-id="3c5d1-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3c5d1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c5d1-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c5d1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c5d1-142">입력</span><span class="sxs-lookup"><span data-stu-id="3c5d1-142">INPUTS</span></span>

### <span data-ttu-id="3c5d1-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="3c5d1-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="3c5d1-144">출력</span><span class="sxs-lookup"><span data-stu-id="3c5d1-144">OUTPUTS</span></span>

### <span data-ttu-id="3c5d1-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="3c5d1-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="3c5d1-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3c5d1-146">NOTES</span></span>

## <span data-ttu-id="3c5d1-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c5d1-147">RELATED LINKS</span></span>
