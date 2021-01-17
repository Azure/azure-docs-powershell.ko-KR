---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b808f9272c000ed0ef17079dd31800860a31449b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327830"
---
# <span data-ttu-id="99615-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="99615-101">Clear-AzContext</span></span>

## <span data-ttu-id="99615-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99615-102">SYNOPSIS</span></span>
<span data-ttu-id="99615-103">모든 Azure 자격 증명, 계정 및 구독 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="99615-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="99615-104">구문</span><span class="sxs-lookup"><span data-stu-id="99615-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99615-105">설명</span><span class="sxs-lookup"><span data-stu-id="99615-105">DESCRIPTION</span></span>
<span data-ttu-id="99615-106">모든 Azure 자격 증명, 계정 및 구독 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="99615-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="99615-107">예제</span><span class="sxs-lookup"><span data-stu-id="99615-107">EXAMPLES</span></span>

### <span data-ttu-id="99615-108">예제 1: 전역 컨텍스트 지우기</span><span class="sxs-lookup"><span data-stu-id="99615-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="99615-109">PowerShell 세션에 대한 모든 계정, 구독 및 자격 증명 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="99615-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="99615-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99615-110">PARAMETERS</span></span>

### <span data-ttu-id="99615-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99615-111">-DefaultProfile</span></span>
<span data-ttu-id="99615-112">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="99615-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99615-113">-Force</span><span class="sxs-lookup"><span data-stu-id="99615-113">-Force</span></span>
<span data-ttu-id="99615-114">메시지가 표시되지 않고 전역 범위에서 모든 사용자 및 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="99615-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="99615-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99615-115">-PassThru</span></span>
<span data-ttu-id="99615-116">성공 또는 실패를 나타내는 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="99615-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="99615-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="99615-117">-Scope</span></span>
<span data-ttu-id="99615-118">현재 PowerShell 세션 또는 모든 세션에 대한 컨텍스트만 지우기</span><span class="sxs-lookup"><span data-stu-id="99615-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="99615-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99615-119">-Confirm</span></span>
<span data-ttu-id="99615-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="99615-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99615-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99615-121">-WhatIf</span></span>
<span data-ttu-id="99615-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="99615-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99615-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99615-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99615-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99615-124">CommonParameters</span></span>
<span data-ttu-id="99615-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="99615-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99615-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="99615-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99615-127">입력</span><span class="sxs-lookup"><span data-stu-id="99615-127">INPUTS</span></span>

### <span data-ttu-id="99615-128">없음</span><span class="sxs-lookup"><span data-stu-id="99615-128">None</span></span>

## <span data-ttu-id="99615-129">출력</span><span class="sxs-lookup"><span data-stu-id="99615-129">OUTPUTS</span></span>

### <span data-ttu-id="99615-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="99615-130">System.Boolean</span></span>

## <span data-ttu-id="99615-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="99615-131">NOTES</span></span>

## <span data-ttu-id="99615-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99615-132">RELATED LINKS</span></span>
