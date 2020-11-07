---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 703be26244e61b797f3359ef508d92e38847bf8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701536"
---
# <span data-ttu-id="7bc90-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7bc90-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="7bc90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bc90-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc90-103">자동화 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc90-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="7bc90-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7bc90-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bc90-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7bc90-105">DESCRIPTION</span></span>
<span data-ttu-id="7bc90-106">**AzAutomationCredential** Cmdlet은 Azure Automation에서 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc90-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="7bc90-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7bc90-107">EXAMPLES</span></span>

### <span data-ttu-id="7bc90-108">예제 1: 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="7bc90-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7bc90-109">이 명령은 Contoso17 이라는 Azure Automation 계정에서 ContosoCredential 이라는 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc90-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="7bc90-110">변수</span><span class="sxs-lookup"><span data-stu-id="7bc90-110">PARAMETERS</span></span>

### <span data-ttu-id="7bc90-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7bc90-111">-AutomationAccountName</span></span>
<span data-ttu-id="7bc90-112">이 cmdlet에서 자격 증명을 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc90-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc90-113">-DefaultProfile</span></span>
<span data-ttu-id="7bc90-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7bc90-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bc90-115">-이름</span><span class="sxs-lookup"><span data-stu-id="7bc90-115">-Name</span></span>
<span data-ttu-id="7bc90-116">이 cmdlet이 제거 하는 자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc90-116">Specifies the name of the credential that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc90-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bc90-117">-ResourceGroupName</span></span>
<span data-ttu-id="7bc90-118">이 cmdlet에서 자격 증명을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc90-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc90-119">-확인</span><span class="sxs-lookup"><span data-stu-id="7bc90-119">-Confirm</span></span>
<span data-ttu-id="7bc90-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc90-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bc90-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bc90-121">-WhatIf</span></span>
<span data-ttu-id="7bc90-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7bc90-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bc90-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bc90-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bc90-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc90-124">CommonParameters</span></span>
<span data-ttu-id="7bc90-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc90-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc90-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc90-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc90-127">입력</span><span class="sxs-lookup"><span data-stu-id="7bc90-127">INPUTS</span></span>

### <span data-ttu-id="7bc90-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7bc90-128">System.String</span></span>

## <span data-ttu-id="7bc90-129">출력</span><span class="sxs-lookup"><span data-stu-id="7bc90-129">OUTPUTS</span></span>

### <span data-ttu-id="7bc90-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="7bc90-130">System.Void</span></span>

## <span data-ttu-id="7bc90-131">상속자</span><span class="sxs-lookup"><span data-stu-id="7bc90-131">NOTES</span></span>

## <span data-ttu-id="7bc90-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7bc90-132">RELATED LINKS</span></span>

[<span data-ttu-id="7bc90-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7bc90-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="7bc90-134">새로운 AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7bc90-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="7bc90-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7bc90-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


