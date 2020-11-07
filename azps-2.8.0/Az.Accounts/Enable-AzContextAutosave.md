---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: eedd28fe1df7992658dfe9b36ebab58e77eb87c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698266"
---
# <span data-ttu-id="aca4e-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="aca4e-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="aca4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aca4e-102">SYNOPSIS</span></span>
<span data-ttu-id="aca4e-103">Azure 자격 증명, 계정, 구독 정보를 저장 하 고 PowerShell 창을 열 때 자동으로 로드 하도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca4e-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="aca4e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aca4e-104">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aca4e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aca4e-105">DESCRIPTION</span></span>
<span data-ttu-id="aca4e-106">Azure 자격 증명, 계정, 구독 정보를 저장 하 고 PowerShell 창을 열 때 자동으로 로드 하도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca4e-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="aca4e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aca4e-107">EXAMPLES</span></span>

### <span data-ttu-id="aca4e-108">현재 사용자에 대해 autosaving 자격 증명 사용</span><span class="sxs-lookup"><span data-stu-id="aca4e-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzContextAutosave
```

<span data-ttu-id="aca4e-109">현재 사용자에 대 한 자격 증명 자동 저장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca4e-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="aca4e-110">Powershell 창을 열 때마다 로그인 하지 않고 현재 컨텍스트가 기억 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca4e-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="aca4e-111">변수</span><span class="sxs-lookup"><span data-stu-id="aca4e-111">PARAMETERS</span></span>

### <span data-ttu-id="aca4e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aca4e-112">-DefaultProfile</span></span>
<span data-ttu-id="aca4e-113">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="aca4e-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aca4e-114">-범위</span><span class="sxs-lookup"><span data-stu-id="aca4e-114">-Scope</span></span>
<span data-ttu-id="aca4e-115">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca4e-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="aca4e-116">-확인</span><span class="sxs-lookup"><span data-stu-id="aca4e-116">-Confirm</span></span>
<span data-ttu-id="aca4e-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca4e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aca4e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aca4e-118">-WhatIf</span></span>
<span data-ttu-id="aca4e-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aca4e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aca4e-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca4e-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aca4e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca4e-121">CommonParameters</span></span>
<span data-ttu-id="aca4e-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca4e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca4e-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aca4e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca4e-124">입력</span><span class="sxs-lookup"><span data-stu-id="aca4e-124">INPUTS</span></span>

### <span data-ttu-id="aca4e-125">않아야</span><span class="sxs-lookup"><span data-stu-id="aca4e-125">None</span></span>

## <span data-ttu-id="aca4e-126">출력</span><span class="sxs-lookup"><span data-stu-id="aca4e-126">OUTPUTS</span></span>

### <span data-ttu-id="aca4e-127">Microsoft. Azure. Common. 인증. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="aca4e-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="aca4e-128">상속자</span><span class="sxs-lookup"><span data-stu-id="aca4e-128">NOTES</span></span>

## <span data-ttu-id="aca4e-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aca4e-129">RELATED LINKS</span></span>
