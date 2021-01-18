---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 6a530a0e20f3e69540320ad3eab8b8cc7f37b5af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494566"
---
# <span data-ttu-id="dcddc-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="dcddc-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="dcddc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcddc-102">SYNOPSIS</span></span>
<span data-ttu-id="dcddc-103">Az 모듈에 대한 AzureRm 연결부 별칭을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="dcddc-104">구문</span><span class="sxs-lookup"><span data-stu-id="dcddc-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcddc-105">설명</span><span class="sxs-lookup"><span data-stu-id="dcddc-105">DESCRIPTION</span></span>
<span data-ttu-id="dcddc-106">Az 모듈에 대한 AzureRm 연결부 별칭을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="dcddc-107">-Module을 지정하면 나열된 모듈만 별칭을 사용하도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="dcddc-108">그렇지 않으면 모든 AzureRm 별칭이 사용하도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="dcddc-109">예제</span><span class="sxs-lookup"><span data-stu-id="dcddc-109">EXAMPLES</span></span>

### <span data-ttu-id="dcddc-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="dcddc-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="dcddc-111">현재 PowerShell 세션에 대한 모든 AzureRm 연결부를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="dcddc-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="dcddc-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="dcddc-113">현재 프로세스와 현재 사용자 모두에 대해 Az.Accounts 모듈에 대한 AzureRm 별칭을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="dcddc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcddc-114">PARAMETERS</span></span>

### <span data-ttu-id="dcddc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcddc-115">-DefaultProfile</span></span>
<span data-ttu-id="dcddc-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcddc-117">-Module</span><span class="sxs-lookup"><span data-stu-id="dcddc-117">-Module</span></span>
<span data-ttu-id="dcddc-118">별칭을 사용할 모듈을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="dcddc-119">지정되지 않은 경우 기본값은 모든 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="dcddc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcddc-120">-PassThru</span></span>
<span data-ttu-id="dcddc-121">지정된 경우 cmdlet은 사용하도록 설정된 모든 별칭을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="dcddc-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="dcddc-122">-Scope</span></span>
<span data-ttu-id="dcddc-123">사용할 범위 별칭을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="dcddc-124">기본값은 'Local'입니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-124">Default is 'Local'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcddc-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcddc-125">-Confirm</span></span>
<span data-ttu-id="dcddc-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcddc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcddc-127">-WhatIf</span></span>
<span data-ttu-id="dcddc-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dcddc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcddc-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcddc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcddc-130">CommonParameters</span></span>
<span data-ttu-id="dcddc-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dcddc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcddc-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dcddc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcddc-133">입력</span><span class="sxs-lookup"><span data-stu-id="dcddc-133">INPUTS</span></span>

### <span data-ttu-id="dcddc-134">없음</span><span class="sxs-lookup"><span data-stu-id="dcddc-134">None</span></span>

## <span data-ttu-id="dcddc-135">출력</span><span class="sxs-lookup"><span data-stu-id="dcddc-135">OUTPUTS</span></span>

### <span data-ttu-id="dcddc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="dcddc-136">System.String</span></span>

## <span data-ttu-id="dcddc-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dcddc-137">NOTES</span></span>

## <span data-ttu-id="dcddc-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dcddc-138">RELATED LINKS</span></span>
