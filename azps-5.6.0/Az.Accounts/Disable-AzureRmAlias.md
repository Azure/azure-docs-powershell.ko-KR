---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 1f9f17e03a9b3cf79b2764c7711da9eee6ca104d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999077"
---
# <span data-ttu-id="21173-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="21173-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="21173-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21173-102">SYNOPSIS</span></span>
<span data-ttu-id="21173-103">Az 모듈에 대해 AzureRm의 별칭을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="21173-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="21173-104">구문</span><span class="sxs-lookup"><span data-stu-id="21173-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21173-105">설명</span><span class="sxs-lookup"><span data-stu-id="21173-105">DESCRIPTION</span></span>
<span data-ttu-id="21173-106">Az 모듈에 대해 AzureRm의 별칭을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="21173-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="21173-107">-Module을 지정하면 나열된 모듈만 별칭을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="21173-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="21173-108">그렇지 않으면 모든 AzureRm 별칭을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="21173-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="21173-109">예제</span><span class="sxs-lookup"><span data-stu-id="21173-109">EXAMPLES</span></span>

### <span data-ttu-id="21173-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="21173-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="21173-111">현재 PowerShell 세션에 대한 모든 AzureRm 사전을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="21173-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="21173-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="21173-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="21173-113">현재 프로세스와 현재 사용자 모두에 대해 Az.Accounts 모듈에 대해 AzureRm 별칭을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="21173-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="21173-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="21173-114">PARAMETERS</span></span>

### <span data-ttu-id="21173-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21173-115">-DefaultProfile</span></span>
<span data-ttu-id="21173-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21173-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21173-117">-Module</span><span class="sxs-lookup"><span data-stu-id="21173-117">-Module</span></span>
<span data-ttu-id="21173-118">별칭을 사용하지 않도록 설정할 모듈을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="21173-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="21173-119">지정되지 않은 경우 기본값은 모두 사용 가능한 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="21173-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="21173-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21173-120">-PassThru</span></span>
<span data-ttu-id="21173-121">지정된 경우 cmdlet은 사용하지 않도록 설정된 모든 별칭을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="21173-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="21173-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="21173-122">-Scope</span></span>
<span data-ttu-id="21173-123">어떤 범위 별칭을 사용하지 않도록 설정해야 하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="21173-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="21173-124">기본값은 '프로세스'입니다.</span><span class="sxs-lookup"><span data-stu-id="21173-124">Default is 'Process'</span></span>

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

### <span data-ttu-id="21173-125">-확인</span><span class="sxs-lookup"><span data-stu-id="21173-125">-Confirm</span></span>
<span data-ttu-id="21173-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="21173-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21173-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21173-127">-WhatIf</span></span>
<span data-ttu-id="21173-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="21173-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21173-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21173-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21173-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21173-130">CommonParameters</span></span>
<span data-ttu-id="21173-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21173-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21173-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21173-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21173-133">입력</span><span class="sxs-lookup"><span data-stu-id="21173-133">INPUTS</span></span>

### <span data-ttu-id="21173-134">없음</span><span class="sxs-lookup"><span data-stu-id="21173-134">None</span></span>

## <span data-ttu-id="21173-135">출력</span><span class="sxs-lookup"><span data-stu-id="21173-135">OUTPUTS</span></span>

### <span data-ttu-id="21173-136">System.String</span><span class="sxs-lookup"><span data-stu-id="21173-136">System.String</span></span>

## <span data-ttu-id="21173-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="21173-137">NOTES</span></span>

## <span data-ttu-id="21173-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21173-138">RELATED LINKS</span></span>
