---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
ms.openlocfilehash: e0aec59bf78d9876f6b2ef061204bdb833624791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689243"
---
# <span data-ttu-id="ed1e3-101">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="ed1e3-101">Select-AzContext</span></span>

## <span data-ttu-id="ed1e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed1e3-102">SYNOPSIS</span></span>
<span data-ttu-id="ed1e3-103">Azure PowerShell cmdlet에서 대상 구독 및 계정 선택</span><span class="sxs-lookup"><span data-stu-id="ed1e3-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

## <span data-ttu-id="ed1e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed1e3-104">SYNTAX</span></span>

### <span data-ttu-id="ed1e3-105">SelectByInputObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="ed1e3-105">SelectByInputObject (Default)</span></span>
```
Select-AzContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed1e3-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="ed1e3-106">SelectByName</span></span>
```
Select-AzContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="ed1e3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ed1e3-107">DESCRIPTION</span></span>
<span data-ttu-id="ed1e3-108">Azure PowerShell cmdlet에서 대상 (또는 계정 또는 테 넌 트)에 대 한 구독을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1e3-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="ed1e3-109">이 cmdlet은 이후 cmdlet이 선택한 컨텍스트를 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1e3-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="ed1e3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ed1e3-110">EXAMPLES</span></span>

### <span data-ttu-id="ed1e3-111">예제 1: 명명 된 컨텍스트 대상 지정</span><span class="sxs-lookup"><span data-stu-id="ed1e3-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzContext "Work"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="ed1e3-112">후속 Azure PowerShell cmdlet을 ' Work ' 컨텍스트에서 계정, 테 넌 트 및 구독에서 대상으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1e3-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="ed1e3-113">변수</span><span class="sxs-lookup"><span data-stu-id="ed1e3-113">PARAMETERS</span></span>

### <span data-ttu-id="ed1e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed1e3-114">-DefaultProfile</span></span>
<span data-ttu-id="ed1e3-115">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ed1e3-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed1e3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed1e3-116">-InputObject</span></span>
<span data-ttu-id="ed1e3-117">일반적으로 파이프라인을 통해 전달 되는 컨텍스트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ed1e3-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: SelectByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed1e3-118">-이름</span><span class="sxs-lookup"><span data-stu-id="ed1e3-118">-Name</span></span>
<span data-ttu-id="ed1e3-119">컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="ed1e3-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: SelectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed1e3-120">-범위</span><span class="sxs-lookup"><span data-stu-id="ed1e3-120">-Scope</span></span>
<span data-ttu-id="ed1e3-121">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1e3-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="ed1e3-122">-확인</span><span class="sxs-lookup"><span data-stu-id="ed1e3-122">-Confirm</span></span>
<span data-ttu-id="ed1e3-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1e3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed1e3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed1e3-124">-WhatIf</span></span>
<span data-ttu-id="ed1e3-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed1e3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed1e3-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed1e3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed1e3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed1e3-127">CommonParameters</span></span>
<span data-ttu-id="ed1e3-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1e3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed1e3-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed1e3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed1e3-130">입력</span><span class="sxs-lookup"><span data-stu-id="ed1e3-130">INPUTS</span></span>

### <span data-ttu-id="ed1e3-131">Microsoft. Azure. a PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ed1e3-131">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="ed1e3-132">출력</span><span class="sxs-lookup"><span data-stu-id="ed1e3-132">OUTPUTS</span></span>

### <span data-ttu-id="ed1e3-133">Microsoft. Azure. a PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ed1e3-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="ed1e3-134">상속자</span><span class="sxs-lookup"><span data-stu-id="ed1e3-134">NOTES</span></span>

## <span data-ttu-id="ed1e3-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed1e3-135">RELATED LINKS</span></span>
