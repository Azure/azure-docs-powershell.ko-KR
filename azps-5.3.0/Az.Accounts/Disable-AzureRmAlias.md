---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 749507ba0bc0eec8aac7600c5262533ceb02a46b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494569"
---
# <span data-ttu-id="9c756-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="9c756-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="9c756-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c756-102">SYNOPSIS</span></span>
<span data-ttu-id="9c756-103">Az 모듈에 대한 AzureRm 연결부 별칭을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="9c756-104">구문</span><span class="sxs-lookup"><span data-stu-id="9c756-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c756-105">설명</span><span class="sxs-lookup"><span data-stu-id="9c756-105">DESCRIPTION</span></span>
<span data-ttu-id="9c756-106">Az 모듈에 대한 AzureRm 연결부 별칭을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="9c756-107">-Module을 지정하면 나열된 모듈만 별칭을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="9c756-108">그렇지 않으면 모든 AzureRm 별칭을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="9c756-109">예제</span><span class="sxs-lookup"><span data-stu-id="9c756-109">EXAMPLES</span></span>

### <span data-ttu-id="9c756-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9c756-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="9c756-111">현재 PowerShell 세션에 대한 모든 AzureRm 사전을 사용하지 않도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="9c756-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9c756-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="9c756-113">현재 프로세스와 현재 사용자 모두에 대해 Az.Accounts 모듈에 대한 AzureRm 별칭을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="9c756-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c756-114">PARAMETERS</span></span>

### <span data-ttu-id="9c756-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c756-115">-DefaultProfile</span></span>
<span data-ttu-id="9c756-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c756-117">-Module</span><span class="sxs-lookup"><span data-stu-id="9c756-117">-Module</span></span>
<span data-ttu-id="9c756-118">별칭을 사용하지 않도록 설정할 모듈을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="9c756-119">지정되지 않은 경우 기본값은 모두 사용하도록 설정된 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-119">If none are specified, default is all enabled modules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c756-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c756-120">-PassThru</span></span>
<span data-ttu-id="9c756-121">지정된 경우 cmdlet은 비활성화된 모든 별칭을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="9c756-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="9c756-122">-Scope</span></span>
<span data-ttu-id="9c756-123">사용할 수 있는 범위 별칭을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="9c756-124">기본값은 'Process'입니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-124">Default is 'Process'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c756-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c756-125">-Confirm</span></span>
<span data-ttu-id="9c756-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c756-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c756-127">-WhatIf</span></span>
<span data-ttu-id="9c756-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9c756-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c756-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c756-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c756-130">CommonParameters</span></span>
<span data-ttu-id="9c756-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9c756-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c756-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9c756-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c756-133">입력</span><span class="sxs-lookup"><span data-stu-id="9c756-133">INPUTS</span></span>

### <span data-ttu-id="9c756-134">없음</span><span class="sxs-lookup"><span data-stu-id="9c756-134">None</span></span>

## <span data-ttu-id="9c756-135">출력</span><span class="sxs-lookup"><span data-stu-id="9c756-135">OUTPUTS</span></span>

### <span data-ttu-id="9c756-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9c756-136">System.String</span></span>

## <span data-ttu-id="9c756-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9c756-137">NOTES</span></span>

## <span data-ttu-id="9c756-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c756-138">RELATED LINKS</span></span>
