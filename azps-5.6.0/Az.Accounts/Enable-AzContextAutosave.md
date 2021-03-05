---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 8bca1314433f8fcbcc0c9f395783bbb3d9835ffb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999054"
---
# <span data-ttu-id="b3cdf-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="b3cdf-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="b3cdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="b3cdf-103">Azure 컨텍스트는 Azure 클라우드에 연결하는 데 필요한 인증 정보를 실행하기 위해 활성 구독을 나타내는 PowerShell 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="b3cdf-104">Azure 컨텍스트를 사용하면 구독을 전환할 때마다 Azure PowerShell에서 계정을 다시 등록할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="b3cdf-105">자세한 내용은 [Azure PowerShell 컨텍스트 개체 를 참조하세요.](https://docs.microsoft.com/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="b3cdf-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="b3cdf-106">이 cmdlet을 사용하면 PowerShell 프로세스를 시작할 때 Azure 컨텍스트 정보를 저장하고 자동으로 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="b3cdf-107">예를 들어 새 창을 여는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="b3cdf-108">구문</span><span class="sxs-lookup"><span data-stu-id="b3cdf-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3cdf-109">설명</span><span class="sxs-lookup"><span data-stu-id="b3cdf-109">DESCRIPTION</span></span>

<span data-ttu-id="b3cdf-110">PowerShell 프로세스가 시작될 때 Azure 컨텍스트 정보를 저장하고 자동으로 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="b3cdf-111">컨텍스트는 컨텍스트에 영향을 주는 모든 cmdlet의 실행 끝에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="b3cdf-112">예를 들어 모든 프로필 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="b3cdf-113">사용자 인증을 사용하는 경우 cmdlet을 실행하는 동안 토큰을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="b3cdf-114">예제</span><span class="sxs-lookup"><span data-stu-id="b3cdf-114">EXAMPLES</span></span>

### <span data-ttu-id="b3cdf-115">예제 1: 현재 사용자에 대한 자동 저장 자격 증명 사용</span><span class="sxs-lookup"><span data-stu-id="b3cdf-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="b3cdf-116">현재 사용자의 자격 증명 자동 저장을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="b3cdf-117">PowerShell 창이 열리면 로그인하지 않고 현재 컨텍스트가 기억됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="b3cdf-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="b3cdf-118">Example 2</span></span>

<span data-ttu-id="b3cdf-119">이 PowerShell 세션에서 PowerShell 창을 열 때 Azure 자격 증명, 계정 및 구독 정보를 저장하고 자동으로 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="b3cdf-120">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="b3cdf-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="b3cdf-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b3cdf-121">PARAMETERS</span></span>

### <span data-ttu-id="b3cdf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3cdf-122">-DefaultProfile</span></span>

<span data-ttu-id="b3cdf-123">Azure와 통신하는 데 사용되는 자격 증명, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b3cdf-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="b3cdf-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="b3cdf-124">-Scope</span></span>

<span data-ttu-id="b3cdf-125">컨텍스트 변경의 범위를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-125">Determines the scope of context changes.</span></span> <span data-ttu-id="b3cdf-126">예를 들어 변경 내용이 현재 프로세스에만 적용되는지 아니면 이 사용자가 시작한 모든 세션에 적용하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="b3cdf-127">범위가 변경된 경우 사용자가 시작한 `CurrentUser` 모든 PowerShell 세션에 영향을 미치게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="b3cdf-128">특정 세션에 다른 설정이 필요한 경우 범위 `Process` 를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3cdf-129">-확인</span><span class="sxs-lookup"><span data-stu-id="b3cdf-129">-Confirm</span></span>

<span data-ttu-id="b3cdf-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3cdf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3cdf-131">-WhatIf</span></span>

<span data-ttu-id="b3cdf-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3cdf-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="b3cdf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3cdf-134">CommonParameters</span></span>
<span data-ttu-id="b3cdf-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b3cdf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3cdf-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3cdf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3cdf-137">입력</span><span class="sxs-lookup"><span data-stu-id="b3cdf-137">INPUTS</span></span>

### <span data-ttu-id="b3cdf-138">없음</span><span class="sxs-lookup"><span data-stu-id="b3cdf-138">None</span></span>

## <span data-ttu-id="b3cdf-139">출력</span><span class="sxs-lookup"><span data-stu-id="b3cdf-139">OUTPUTS</span></span>

### <span data-ttu-id="b3cdf-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="b3cdf-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="b3cdf-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b3cdf-141">NOTES</span></span>

## <span data-ttu-id="b3cdf-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3cdf-142">RELATED LINKS</span></span>
