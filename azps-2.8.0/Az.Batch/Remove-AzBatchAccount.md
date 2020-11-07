---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: 47d10b02cbe019571a94ffcc1384340daff15c31
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880033"
---
# <span data-ttu-id="eb857-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="eb857-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="eb857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb857-102">SYNOPSIS</span></span>
<span data-ttu-id="eb857-103">일괄 처리 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb857-103">Removes a Batch account.</span></span>

## <span data-ttu-id="eb857-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb857-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb857-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eb857-105">DESCRIPTION</span></span>
<span data-ttu-id="eb857-106">**AzBatchAccount** Cmdlet은 Azure Batch 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb857-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="eb857-107">이 cmdlet은 *Force* 매개 변수를 지정 하지 않는 한 계정을 제거 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb857-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="eb857-108">예제의</span><span class="sxs-lookup"><span data-stu-id="eb857-108">EXAMPLES</span></span>

### <span data-ttu-id="eb857-109">예제 1: 일괄 처리 계정 제거</span><span class="sxs-lookup"><span data-stu-id="eb857-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="eb857-110">이 명령은 pfuller 이름의 일괄 처리 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb857-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="eb857-111">이 명령은 계정을 삭제 하기 전에 확인을 요청 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb857-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="eb857-112">변수</span><span class="sxs-lookup"><span data-stu-id="eb857-112">PARAMETERS</span></span>

### <span data-ttu-id="eb857-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eb857-113">-AccountName</span></span>
<span data-ttu-id="eb857-114">이 cmdlet이 제거 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb857-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eb857-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb857-115">-DefaultProfile</span></span>
<span data-ttu-id="eb857-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb857-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb857-117">-Force</span><span class="sxs-lookup"><span data-stu-id="eb857-117">-Force</span></span>
<span data-ttu-id="eb857-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb857-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eb857-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb857-119">-ResourceGroupName</span></span>
<span data-ttu-id="eb857-120">이 cmdlet이 제거 하는 계정의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb857-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eb857-121">-확인</span><span class="sxs-lookup"><span data-stu-id="eb857-121">-Confirm</span></span>
<span data-ttu-id="eb857-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb857-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb857-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb857-123">-WhatIf</span></span>
<span data-ttu-id="eb857-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eb857-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb857-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb857-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb857-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb857-126">CommonParameters</span></span>
<span data-ttu-id="eb857-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb857-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb857-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb857-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb857-129">입력</span><span class="sxs-lookup"><span data-stu-id="eb857-129">INPUTS</span></span>

### <span data-ttu-id="eb857-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eb857-130">System.String</span></span>

## <span data-ttu-id="eb857-131">출력</span><span class="sxs-lookup"><span data-stu-id="eb857-131">OUTPUTS</span></span>

### <span data-ttu-id="eb857-132">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="eb857-132">System.Void</span></span>

## <span data-ttu-id="eb857-133">상속자</span><span class="sxs-lookup"><span data-stu-id="eb857-133">NOTES</span></span>

## <span data-ttu-id="eb857-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb857-134">RELATED LINKS</span></span>

[<span data-ttu-id="eb857-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="eb857-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="eb857-136">새로운 AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="eb857-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="eb857-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="eb857-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="eb857-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eb857-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


