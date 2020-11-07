---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 809ec5bb5388447e5f20fe267598660ac0e49ec8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689244"
---
# <span data-ttu-id="37b90-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="37b90-101">Rename-AzContext</span></span>

## <span data-ttu-id="37b90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37b90-102">SYNOPSIS</span></span>
<span data-ttu-id="37b90-103">Azure 컨텍스트의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-103">Rename an Azure context.</span></span>  <span data-ttu-id="37b90-104">기본적으로 컨텍스트는 사용자 계정과 구독으로 명명 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="37b90-105">구문과</span><span class="sxs-lookup"><span data-stu-id="37b90-105">SYNTAX</span></span>

### <span data-ttu-id="37b90-106">RenameByInputObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="37b90-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="37b90-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="37b90-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="37b90-108">설명은</span><span class="sxs-lookup"><span data-stu-id="37b90-108">DESCRIPTION</span></span>
<span data-ttu-id="37b90-109">Azure 컨텍스트의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-109">Rename an Azure context.</span></span>  <span data-ttu-id="37b90-110">기본적으로 컨텍스트는 사용자 계정과 구독으로 명명 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="37b90-111">예제의</span><span class="sxs-lookup"><span data-stu-id="37b90-111">EXAMPLES</span></span>

### <span data-ttu-id="37b90-112">명명 된 매개 변수를 사용 하 여 컨텍스트 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="37b90-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="37b90-113">' user1@contoso.org 12345-6789-2345-3567890 ' 구독을 사용 하 여 ' ' 작업 '에 대 한 컨텍스트의 이름을 ' Work '로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="37b90-114">이 명령 다음에는 ' AzContext 작업 '을 사용 하 여 컨텍스트를 대상으로 지정할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="37b90-115">탭 완료를 사용 하 여 ' SourceName '에 대 한 값을 tab으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="37b90-116">위치 매개 변수를 사용 하 여 컨텍스트 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="37b90-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="37b90-117">"내 컨텍스트" 라는 컨텍스트의 이름을 "Work"로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="37b90-118">이 명령 다음에 Select-AzContext 작업을 사용 하 여 컨텍스트를 대상으로 지정할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="37b90-119">변수</span><span class="sxs-lookup"><span data-stu-id="37b90-119">PARAMETERS</span></span>

### <span data-ttu-id="37b90-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b90-120">-DefaultProfile</span></span>
<span data-ttu-id="37b90-121">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="37b90-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37b90-122">-Force</span><span class="sxs-lookup"><span data-stu-id="37b90-122">-Force</span></span>
<span data-ttu-id="37b90-123">대상 컨텍스트가 이미 있는 경우에도 컨텍스트 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="37b90-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="37b90-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37b90-124">-InputObject</span></span>
<span data-ttu-id="37b90-125">일반적으로 파이프라인을 통해 전달 되는 컨텍스트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-125">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="37b90-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37b90-126">-PassThru</span></span>
<span data-ttu-id="37b90-127">이름을 바꾼 컨텍스트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="37b90-128">-범위</span><span class="sxs-lookup"><span data-stu-id="37b90-128">-Scope</span></span>
<span data-ttu-id="37b90-129">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="37b90-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="37b90-130">-SourceName</span></span>
<span data-ttu-id="37b90-131">컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="37b90-131">The name of the context</span></span>

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

### <span data-ttu-id="37b90-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="37b90-132">-TargetName</span></span>
<span data-ttu-id="37b90-133">컨텍스트의 새 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-133">The new name of the context</span></span>

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

### <span data-ttu-id="37b90-134">-확인</span><span class="sxs-lookup"><span data-stu-id="37b90-134">-Confirm</span></span>
<span data-ttu-id="37b90-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37b90-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37b90-136">-WhatIf</span></span>
<span data-ttu-id="37b90-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37b90-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37b90-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b90-139">CommonParameters</span></span>
<span data-ttu-id="37b90-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b90-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b90-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37b90-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b90-142">입력</span><span class="sxs-lookup"><span data-stu-id="37b90-142">INPUTS</span></span>

### <span data-ttu-id="37b90-143">Microsoft. Azure. a PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="37b90-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="37b90-144">출력</span><span class="sxs-lookup"><span data-stu-id="37b90-144">OUTPUTS</span></span>

### <span data-ttu-id="37b90-145">Microsoft. Azure. a PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="37b90-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="37b90-146">상속자</span><span class="sxs-lookup"><span data-stu-id="37b90-146">NOTES</span></span>

## <span data-ttu-id="37b90-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37b90-147">RELATED LINKS</span></span>