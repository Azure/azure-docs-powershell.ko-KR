---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: 8db930fe362d25a7b1069af6c3855ef71644e874
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990626"
---
# <span data-ttu-id="49d4c-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="49d4c-101">Clear-AzContext</span></span>

## <span data-ttu-id="49d4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="49d4c-103">모든 Azure 자격 증명, 계정 및 구독 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="49d4c-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="49d4c-104">구문</span><span class="sxs-lookup"><span data-stu-id="49d4c-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49d4c-105">설명</span><span class="sxs-lookup"><span data-stu-id="49d4c-105">DESCRIPTION</span></span>
<span data-ttu-id="49d4c-106">모든 Azure 자격 증명, 계정 및 구독 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="49d4c-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="49d4c-107">예제</span><span class="sxs-lookup"><span data-stu-id="49d4c-107">EXAMPLES</span></span>

### <span data-ttu-id="49d4c-108">예제 1: 전역 컨텍스트 지우기</span><span class="sxs-lookup"><span data-stu-id="49d4c-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="49d4c-109">Powershell 세션에 대한 모든 계정, 구독 및 자격 증명 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="49d4c-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="49d4c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="49d4c-110">PARAMETERS</span></span>

### <span data-ttu-id="49d4c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49d4c-111">-DefaultProfile</span></span>
<span data-ttu-id="49d4c-112">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="49d4c-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49d4c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="49d4c-113">-Force</span></span>
<span data-ttu-id="49d4c-114">메시지가 표시되지 않고 전역 범위에서 모든 사용자 및 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="49d4c-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="49d4c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49d4c-115">-PassThru</span></span>
<span data-ttu-id="49d4c-116">성공 또는 실패를 나타내는 값 반환</span><span class="sxs-lookup"><span data-stu-id="49d4c-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="49d4c-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="49d4c-117">-Scope</span></span>
<span data-ttu-id="49d4c-118">현재 PowerShell 세션 또는 모든 세션에 대한 컨텍스트를 지워야 합니다.</span><span class="sxs-lookup"><span data-stu-id="49d4c-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="49d4c-119">-확인</span><span class="sxs-lookup"><span data-stu-id="49d4c-119">-Confirm</span></span>
<span data-ttu-id="49d4c-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="49d4c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49d4c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49d4c-121">-WhatIf</span></span>
<span data-ttu-id="49d4c-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="49d4c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49d4c-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49d4c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49d4c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d4c-124">CommonParameters</span></span>
<span data-ttu-id="49d4c-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49d4c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49d4c-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49d4c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d4c-127">입력</span><span class="sxs-lookup"><span data-stu-id="49d4c-127">INPUTS</span></span>

### <span data-ttu-id="49d4c-128">없음</span><span class="sxs-lookup"><span data-stu-id="49d4c-128">None</span></span>

## <span data-ttu-id="49d4c-129">출력</span><span class="sxs-lookup"><span data-stu-id="49d4c-129">OUTPUTS</span></span>

### <span data-ttu-id="49d4c-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49d4c-130">System.Boolean</span></span>

## <span data-ttu-id="49d4c-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49d4c-131">NOTES</span></span>

## <span data-ttu-id="49d4c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49d4c-132">RELATED LINKS</span></span>
