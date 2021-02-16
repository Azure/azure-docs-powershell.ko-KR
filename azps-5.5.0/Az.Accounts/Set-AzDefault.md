---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 25fd0e1cd651f70fa0900c528f9e5297a8eaf2df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176521"
---
# <span data-ttu-id="16bc1-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="16bc1-101">Set-AzDefault</span></span>

## <span data-ttu-id="16bc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="16bc1-103">현재 컨텍스트에서 기본값 설정</span><span class="sxs-lookup"><span data-stu-id="16bc1-103">Sets a default in the current context</span></span>

## <span data-ttu-id="16bc1-104">구문</span><span class="sxs-lookup"><span data-stu-id="16bc1-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16bc1-105">설명</span><span class="sxs-lookup"><span data-stu-id="16bc1-105">DESCRIPTION</span></span>
<span data-ttu-id="16bc1-106">Set-AzDefault cmdlet은 현재 컨텍스트의 기본값을 추가하거나 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc1-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="16bc1-107">예제</span><span class="sxs-lookup"><span data-stu-id="16bc1-107">EXAMPLES</span></span>

### <span data-ttu-id="16bc1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="16bc1-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="16bc1-109">이 명령은 사용자가 지정한 리소스 그룹으로 기본 리소스 그룹을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc1-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="16bc1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16bc1-110">PARAMETERS</span></span>

### <span data-ttu-id="16bc1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16bc1-111">-DefaultProfile</span></span>
<span data-ttu-id="16bc1-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16bc1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16bc1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="16bc1-113">-Force</span></span>
<span data-ttu-id="16bc1-114">지정된 기본값이 없는 경우 새 리소스 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="16bc1-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="16bc1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16bc1-115">-ResourceGroupName</span></span>
<span data-ttu-id="16bc1-116">기본값으로 설정되는 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="16bc1-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16bc1-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="16bc1-117">-Scope</span></span>
<span data-ttu-id="16bc1-118">컨텍스트 변경 범위(예: 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용되는지 여부)를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc1-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="16bc1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16bc1-119">-Confirm</span></span>
<span data-ttu-id="16bc1-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bc1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16bc1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16bc1-121">-WhatIf</span></span>
<span data-ttu-id="16bc1-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="16bc1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16bc1-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16bc1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16bc1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16bc1-124">CommonParameters</span></span>
<span data-ttu-id="16bc1-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16bc1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16bc1-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="16bc1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16bc1-127">입력</span><span class="sxs-lookup"><span data-stu-id="16bc1-127">INPUTS</span></span>

### <span data-ttu-id="16bc1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="16bc1-128">System.String</span></span>

## <span data-ttu-id="16bc1-129">출력</span><span class="sxs-lookup"><span data-stu-id="16bc1-129">OUTPUTS</span></span>

### <span data-ttu-id="16bc1-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="16bc1-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="16bc1-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16bc1-131">NOTES</span></span>

## <span data-ttu-id="16bc1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16bc1-132">RELATED LINKS</span></span>
