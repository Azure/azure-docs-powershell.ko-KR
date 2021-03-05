---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: 5b74f378bc867c1d39f27ebdd9972dfdda5457c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007328"
---
# <span data-ttu-id="1ed9f-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1ed9f-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="1ed9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ed9f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed9f-103">Batch 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed9f-103">Removes a Batch account.</span></span>

## <span data-ttu-id="1ed9f-104">구문</span><span class="sxs-lookup"><span data-stu-id="1ed9f-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ed9f-105">설명</span><span class="sxs-lookup"><span data-stu-id="1ed9f-105">DESCRIPTION</span></span>
<span data-ttu-id="1ed9f-106">**Remove-AzBatchAccount** cmdlet은 Azure Batch 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed9f-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="1ed9f-107">이 cmdlet은 Force 매개 변수를 지정하지 않는 한 계정을 제거하기 전에 메시지를 *표시합니다.*</span><span class="sxs-lookup"><span data-stu-id="1ed9f-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="1ed9f-108">예제</span><span class="sxs-lookup"><span data-stu-id="1ed9f-108">EXAMPLES</span></span>

### <span data-ttu-id="1ed9f-109">예제 1: Batch 계정 제거</span><span class="sxs-lookup"><span data-stu-id="1ed9f-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="1ed9f-110">이 명령은 pfuller라는 Batch 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed9f-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="1ed9f-111">이 명령은 계정을 삭제하기 전에 확인을 묻는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed9f-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="1ed9f-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1ed9f-112">PARAMETERS</span></span>

### <span data-ttu-id="1ed9f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1ed9f-113">-AccountName</span></span>
<span data-ttu-id="1ed9f-114">이 cmdlet이 제거한 Batch 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed9f-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1ed9f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ed9f-115">-DefaultProfile</span></span>
<span data-ttu-id="1ed9f-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ed9f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ed9f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1ed9f-117">-Force</span></span>
<span data-ttu-id="1ed9f-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed9f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ed9f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ed9f-119">-ResourceGroupName</span></span>
<span data-ttu-id="1ed9f-120">이 cmdlet이 제거한 계정의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed9f-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1ed9f-121">-확인</span><span class="sxs-lookup"><span data-stu-id="1ed9f-121">-Confirm</span></span>
<span data-ttu-id="1ed9f-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ed9f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ed9f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ed9f-123">-WhatIf</span></span>
<span data-ttu-id="1ed9f-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1ed9f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ed9f-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ed9f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ed9f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed9f-126">CommonParameters</span></span>
<span data-ttu-id="1ed9f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed9f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed9f-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ed9f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed9f-129">입력</span><span class="sxs-lookup"><span data-stu-id="1ed9f-129">INPUTS</span></span>

### <span data-ttu-id="1ed9f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1ed9f-130">System.String</span></span>

## <span data-ttu-id="1ed9f-131">출력</span><span class="sxs-lookup"><span data-stu-id="1ed9f-131">OUTPUTS</span></span>

### <span data-ttu-id="1ed9f-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="1ed9f-132">System.Void</span></span>

## <span data-ttu-id="1ed9f-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1ed9f-133">NOTES</span></span>

## <span data-ttu-id="1ed9f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ed9f-134">RELATED LINKS</span></span>

[<span data-ttu-id="1ed9f-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1ed9f-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="1ed9f-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1ed9f-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="1ed9f-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1ed9f-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="1ed9f-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1ed9f-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
