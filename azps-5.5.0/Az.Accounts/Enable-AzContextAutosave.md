---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195444"
---
# <span data-ttu-id="a2b4d-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="a2b4d-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="a2b4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b4d-103">Azure 컨텍스트는 명령을 실행할 활성 구독을 나타내는 PowerShell 개체 및 Azure 클라우드에 연결하는 데 필요한 인증 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="a2b4d-104">Azure 컨텍스트를 사용하면 구독을 전환할 때마다 Azure PowerShell에서 계정을 다시 등록할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="a2b4d-105">자세한 내용은 [Azure PowerShell 컨텍스트 개체를 참조하세요.](https://docs.microsoft.com/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="a2b4d-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="a2b4d-106">이 cmdlet을 사용하면 PowerShell 프로세스를 시작할 때 Azure 컨텍스트 정보를 저장하고 자동으로 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="a2b4d-107">예를 들어 새 창을 열 때입니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="a2b4d-108">구문</span><span class="sxs-lookup"><span data-stu-id="a2b4d-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2b4d-109">설명</span><span class="sxs-lookup"><span data-stu-id="a2b4d-109">DESCRIPTION</span></span>

<span data-ttu-id="a2b4d-110">PowerShell 프로세스가 시작될 때 Azure 컨텍스트 정보를 저장하고 자동으로 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="a2b4d-111">컨텍스트는 컨텍스트에 영향을 주는 모든 cmdlet의 실행 끝에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="a2b4d-112">예를 들어 모든 프로필 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="a2b4d-113">사용자 인증을 사용하는 경우 cmdlet을 실행하는 동안 토큰을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="a2b4d-114">예제</span><span class="sxs-lookup"><span data-stu-id="a2b4d-114">EXAMPLES</span></span>

### <span data-ttu-id="a2b4d-115">예제 1: 현재 사용자에 대한 자격 증명 자동 저장 사용</span><span class="sxs-lookup"><span data-stu-id="a2b4d-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="a2b4d-116">현재 사용자에 대한 자격 증명 자동 저장을 켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="a2b4d-117">PowerShell 창이 열리면 현재 컨텍스트가 로그인하지 않고 기억됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="a2b4d-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="a2b4d-118">Example 2</span></span>

<span data-ttu-id="a2b4d-119">이 PowerShell 세션에서 PowerShell 창을 열 때 Azure 자격 증명, 계정 및 구독 정보를 저장하고 자동으로 로드하도록 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="a2b4d-120">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="a2b4d-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="a2b4d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2b4d-121">PARAMETERS</span></span>

### <span data-ttu-id="a2b4d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b4d-122">-DefaultProfile</span></span>

<span data-ttu-id="a2b4d-123">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a2b4d-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="a2b4d-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="a2b4d-124">-Scope</span></span>

<span data-ttu-id="a2b4d-125">컨텍스트 변경의 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-125">Determines the scope of context changes.</span></span> <span data-ttu-id="a2b4d-126">예를 들어 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용될지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="a2b4d-127">범위를 변경하면 사용자가 시작한 모든 `CurrentUser` PowerShell 세션에 영향을 미치게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="a2b4d-128">특정 세션에 다른 설정이 필요한 경우 범위를 `Process` 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

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

### <span data-ttu-id="a2b4d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2b4d-129">-Confirm</span></span>

<span data-ttu-id="a2b4d-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2b4d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2b4d-131">-WhatIf</span></span>

<span data-ttu-id="a2b4d-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a2b4d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2b4d-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="a2b4d-134">일반 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a2b4d-134">Common Parameters</span></span>

<span data-ttu-id="a2b4d-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b4d-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a2b4d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b4d-137">입력</span><span class="sxs-lookup"><span data-stu-id="a2b4d-137">INPUTS</span></span>

### <span data-ttu-id="a2b4d-138">없음</span><span class="sxs-lookup"><span data-stu-id="a2b4d-138">None</span></span>

## <span data-ttu-id="a2b4d-139">출력</span><span class="sxs-lookup"><span data-stu-id="a2b4d-139">OUTPUTS</span></span>

### <span data-ttu-id="a2b4d-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="a2b4d-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="a2b4d-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a2b4d-141">NOTES</span></span>

## <span data-ttu-id="a2b4d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2b4d-142">RELATED LINKS</span></span>
