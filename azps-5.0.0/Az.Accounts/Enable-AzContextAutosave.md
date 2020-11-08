---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218266"
---
# <span data-ttu-id="51b42-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="51b42-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="51b42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51b42-102">SYNOPSIS</span></span>
<span data-ttu-id="51b42-103">Azure 컨텍스트는 명령을 실행할 활성 구독을 나타내는 PowerShell 개체와 Azure 클라우드에 연결 하는 데 필요한 인증 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="51b42-104">Azure 컨텍스트를 사용 하는 경우 Azure PowerShell에서는 구독을 전환할 때마다 계정을 다시 인증 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="51b42-105">자세한 내용은 [Azure PowerShell 컨텍스트 개체](https://docs.microsoft.com/powershell/azure/context-persistence)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="51b42-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="51b42-106">이 cmdlet을 사용 하면 PowerShell 프로세스를 시작할 때 Azure 컨텍스트 정보가 저장 되 고 자동으로 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="51b42-107">예를 들어 새 창을 열 때</span><span class="sxs-lookup"><span data-stu-id="51b42-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="51b42-108">구문과</span><span class="sxs-lookup"><span data-stu-id="51b42-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51b42-109">설명은</span><span class="sxs-lookup"><span data-stu-id="51b42-109">DESCRIPTION</span></span>

<span data-ttu-id="51b42-110">Azure 컨텍스트 정보를 저장 하 고 PowerShell 프로세스가 시작 될 때 자동으로 로드 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="51b42-111">컨텍스트는 컨텍스트에 영향을 주는 cmdlet 실행의 끝에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="51b42-112">예를 들어 모든 프로필 cmdlet을 사용할 경우</span><span class="sxs-lookup"><span data-stu-id="51b42-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="51b42-113">사용자 인증을 사용 하는 경우 cmdlet을 실행 하는 동안 토큰을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="51b42-114">예제의</span><span class="sxs-lookup"><span data-stu-id="51b42-114">EXAMPLES</span></span>

### <span data-ttu-id="51b42-115">예제 1: 현재 사용자에 대해 autosaving 자격 증명 사용</span><span class="sxs-lookup"><span data-stu-id="51b42-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="51b42-116">현재 사용자에 대 한 자격 증명 자동 저장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="51b42-117">PowerShell 창을 열 때마다 로그인 하지 않고 현재 컨텍스트가 기억 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="51b42-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="51b42-118">Example 2</span></span>

<span data-ttu-id="51b42-119">이 PowerShell 세션에서 PowerShell 창을 열 때 Azure 자격 증명, 계정 및 구독 정보를 저장 하 고 자동으로 로드 하도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="51b42-120">생성</span><span class="sxs-lookup"><span data-stu-id="51b42-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="51b42-121">변수</span><span class="sxs-lookup"><span data-stu-id="51b42-121">PARAMETERS</span></span>

### <span data-ttu-id="51b42-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b42-122">-DefaultProfile</span></span>

<span data-ttu-id="51b42-123">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="51b42-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="51b42-124">-범위</span><span class="sxs-lookup"><span data-stu-id="51b42-124">-Scope</span></span>

<span data-ttu-id="51b42-125">컨텍스트 변경의 범위를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-125">Determines the scope of context changes.</span></span> <span data-ttu-id="51b42-126">예를 들어 변경 내용이 현재 프로세스 또는이 사용자가 시작한 모든 세션에만 적용 되는지 여부</span><span class="sxs-lookup"><span data-stu-id="51b42-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="51b42-127">범위를 변경 하면 `CurrentUser` 사용자가 시작한 모든 PowerShell 세션에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="51b42-128">특정 세션에 다른 설정이 필요한 경우 범위를 사용 `Process` 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

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

### <span data-ttu-id="51b42-129">-확인</span><span class="sxs-lookup"><span data-stu-id="51b42-129">-Confirm</span></span>

<span data-ttu-id="51b42-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51b42-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51b42-131">-WhatIf</span></span>

<span data-ttu-id="51b42-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51b42-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="51b42-134">공통 매개 변수</span><span class="sxs-lookup"><span data-stu-id="51b42-134">Common Parameters</span></span>

<span data-ttu-id="51b42-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b42-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b42-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="51b42-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b42-137">입력</span><span class="sxs-lookup"><span data-stu-id="51b42-137">INPUTS</span></span>

### <span data-ttu-id="51b42-138">않아야</span><span class="sxs-lookup"><span data-stu-id="51b42-138">None</span></span>

## <span data-ttu-id="51b42-139">출력</span><span class="sxs-lookup"><span data-stu-id="51b42-139">OUTPUTS</span></span>

### <span data-ttu-id="51b42-140">Microsoft. Azure. Common. 인증. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="51b42-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="51b42-141">상속자</span><span class="sxs-lookup"><span data-stu-id="51b42-141">NOTES</span></span>

## <span data-ttu-id="51b42-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51b42-142">RELATED LINKS</span></span>
