---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: ae67aac391f2cce2a37be8a5a15a0fd0ea37cdd9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494101"
---
# <span data-ttu-id="724e6-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="724e6-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="724e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="724e6-102">SYNOPSIS</span></span>
<span data-ttu-id="724e6-103">Batch 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="724e6-103">Removes a Batch account.</span></span>

## <span data-ttu-id="724e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="724e6-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="724e6-105">설명</span><span class="sxs-lookup"><span data-stu-id="724e6-105">DESCRIPTION</span></span>
<span data-ttu-id="724e6-106">**Remove-AzBatchAccount** cmdlet은 Azure Batch 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="724e6-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="724e6-107">이 cmdlet은 *Force* 매개 변수를 지정하지 않는 한 계정을 제거하기 전에 프롬프트를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="724e6-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="724e6-108">예제</span><span class="sxs-lookup"><span data-stu-id="724e6-108">EXAMPLES</span></span>

### <span data-ttu-id="724e6-109">예제 1: Batch 계정 제거</span><span class="sxs-lookup"><span data-stu-id="724e6-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="724e6-110">이 명령은 pfuller라는 Batch 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="724e6-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="724e6-111">이 명령은 계정을 삭제하기 전에 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="724e6-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="724e6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="724e6-112">PARAMETERS</span></span>

### <span data-ttu-id="724e6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="724e6-113">-AccountName</span></span>
<span data-ttu-id="724e6-114">이 cmdlet이 제거하는 Batch 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="724e6-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="724e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="724e6-115">-DefaultProfile</span></span>
<span data-ttu-id="724e6-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="724e6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="724e6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="724e6-117">-Force</span></span>
<span data-ttu-id="724e6-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="724e6-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="724e6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="724e6-119">-ResourceGroupName</span></span>
<span data-ttu-id="724e6-120">이 cmdlet이 제거하는 계정의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="724e6-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="724e6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="724e6-121">-Confirm</span></span>
<span data-ttu-id="724e6-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="724e6-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724e6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="724e6-123">-WhatIf</span></span>
<span data-ttu-id="724e6-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="724e6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="724e6-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="724e6-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724e6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="724e6-126">CommonParameters</span></span>
<span data-ttu-id="724e6-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="724e6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="724e6-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="724e6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="724e6-129">입력</span><span class="sxs-lookup"><span data-stu-id="724e6-129">INPUTS</span></span>

### <span data-ttu-id="724e6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="724e6-130">System.String</span></span>

## <span data-ttu-id="724e6-131">출력</span><span class="sxs-lookup"><span data-stu-id="724e6-131">OUTPUTS</span></span>

### <span data-ttu-id="724e6-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="724e6-132">System.Void</span></span>

## <span data-ttu-id="724e6-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="724e6-133">NOTES</span></span>

## <span data-ttu-id="724e6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="724e6-134">RELATED LINKS</span></span>

[<span data-ttu-id="724e6-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="724e6-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="724e6-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="724e6-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="724e6-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="724e6-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="724e6-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="724e6-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
