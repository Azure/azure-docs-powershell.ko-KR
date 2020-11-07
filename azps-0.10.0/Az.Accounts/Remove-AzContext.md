---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: accea2f11e00cecf3771e87e14a42a446a75367d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875283"
---
# <span data-ttu-id="20b9d-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="20b9d-101">Remove-AzContext</span></span>

## <span data-ttu-id="20b9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="20b9d-103">사용 가능한 컨텍스트 집합에서 컨텍스트 제거</span><span class="sxs-lookup"><span data-stu-id="20b9d-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="20b9d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20b9d-104">SYNTAX</span></span>

### <span data-ttu-id="20b9d-105">RemoveByInputObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="20b9d-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20b9d-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="20b9d-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="20b9d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="20b9d-107">DESCRIPTION</span></span>
<span data-ttu-id="20b9d-108">컨텍스트 집합에서 azure 컨텍스트 제거</span><span class="sxs-lookup"><span data-stu-id="20b9d-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="20b9d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="20b9d-109">EXAMPLES</span></span>

### <span data-ttu-id="20b9d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="20b9d-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="20b9d-111">Default 라는 컨텍스트 제거</span><span class="sxs-lookup"><span data-stu-id="20b9d-111">Remove the context named default</span></span>

## <span data-ttu-id="20b9d-112">변수</span><span class="sxs-lookup"><span data-stu-id="20b9d-112">PARAMETERS</span></span>

### <span data-ttu-id="20b9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b9d-113">-DefaultProfile</span></span>
<span data-ttu-id="20b9d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20b9d-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20b9d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="20b9d-115">-Force</span></span>
<span data-ttu-id="20b9d-116">Default 인 경우에도 컨텍스트 제거</span><span class="sxs-lookup"><span data-stu-id="20b9d-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="20b9d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20b9d-117">-InputObject</span></span>
<span data-ttu-id="20b9d-118">일반적으로 파이프라인을 통해 전달 되는 컨텍스트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="20b9d-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="20b9d-119">-이름</span><span class="sxs-lookup"><span data-stu-id="20b9d-119">-Name</span></span>
<span data-ttu-id="20b9d-120">컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="20b9d-120">The name of the context</span></span>

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

### <span data-ttu-id="20b9d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20b9d-121">-PassThru</span></span>
<span data-ttu-id="20b9d-122">제거 된 컨텍스트 반환</span><span class="sxs-lookup"><span data-stu-id="20b9d-122">Return the removed context</span></span>

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

### <span data-ttu-id="20b9d-123">-범위</span><span class="sxs-lookup"><span data-stu-id="20b9d-123">-Scope</span></span>
<span data-ttu-id="20b9d-124">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20b9d-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="20b9d-125">-확인</span><span class="sxs-lookup"><span data-stu-id="20b9d-125">-Confirm</span></span>
<span data-ttu-id="20b9d-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="20b9d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20b9d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b9d-127">-WhatIf</span></span>
<span data-ttu-id="20b9d-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="20b9d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20b9d-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20b9d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20b9d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b9d-130">CommonParameters</span></span>
<span data-ttu-id="20b9d-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20b9d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b9d-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="20b9d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b9d-133">입력</span><span class="sxs-lookup"><span data-stu-id="20b9d-133">INPUTS</span></span>

### <span data-ttu-id="20b9d-134">Microsoft. Azure. a PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="20b9d-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="20b9d-135">출력</span><span class="sxs-lookup"><span data-stu-id="20b9d-135">OUTPUTS</span></span>

### <span data-ttu-id="20b9d-136">Microsoft. Azure. a PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="20b9d-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="20b9d-137">상속자</span><span class="sxs-lookup"><span data-stu-id="20b9d-137">NOTES</span></span>

## <span data-ttu-id="20b9d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20b9d-138">RELATED LINKS</span></span>
