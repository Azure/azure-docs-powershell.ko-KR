---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 3fb795f614e6ccd7c4e97470d89c6c8923fa9165
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009947"
---
# <span data-ttu-id="b7bfc-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="b7bfc-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="b7bfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="b7bfc-103">Automation 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="b7bfc-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7bfc-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7bfc-105">설명</span><span class="sxs-lookup"><span data-stu-id="b7bfc-105">DESCRIPTION</span></span>
<span data-ttu-id="b7bfc-106">**Remove-AzAutomationCredential** cmdlet은 Azure Automation에서 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="b7bfc-107">예제</span><span class="sxs-lookup"><span data-stu-id="b7bfc-107">EXAMPLES</span></span>

### <span data-ttu-id="b7bfc-108">예제 1: 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="b7bfc-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b7bfc-109">이 명령은 Contoso17이라는 Azure Automation 계정에서 ContosoCredential이라는 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="b7bfc-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7bfc-110">PARAMETERS</span></span>

### <span data-ttu-id="b7bfc-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b7bfc-111">-AutomationAccountName</span></span>
<span data-ttu-id="b7bfc-112">이 cmdlet에서 자격 증명을 제거하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="b7bfc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7bfc-113">-DefaultProfile</span></span>
<span data-ttu-id="b7bfc-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b7bfc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7bfc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b7bfc-115">-Name</span></span>
<span data-ttu-id="b7bfc-116">이 cmdlet이 제거한 자격 증명의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b7bfc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7bfc-117">-ResourceGroupName</span></span>
<span data-ttu-id="b7bfc-118">이 cmdlet에서 자격 증명을 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="b7bfc-119">-확인</span><span class="sxs-lookup"><span data-stu-id="b7bfc-119">-Confirm</span></span>
<span data-ttu-id="b7bfc-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7bfc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7bfc-121">-WhatIf</span></span>
<span data-ttu-id="b7bfc-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7bfc-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7bfc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7bfc-124">CommonParameters</span></span>
<span data-ttu-id="b7bfc-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7bfc-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b7bfc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7bfc-127">입력</span><span class="sxs-lookup"><span data-stu-id="b7bfc-127">INPUTS</span></span>

### <span data-ttu-id="b7bfc-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b7bfc-128">System.String</span></span>

## <span data-ttu-id="b7bfc-129">출력</span><span class="sxs-lookup"><span data-stu-id="b7bfc-129">OUTPUTS</span></span>

### <span data-ttu-id="b7bfc-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="b7bfc-130">System.Void</span></span>

## <span data-ttu-id="b7bfc-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7bfc-131">NOTES</span></span>

## <span data-ttu-id="b7bfc-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7bfc-132">RELATED LINKS</span></span>

[<span data-ttu-id="b7bfc-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="b7bfc-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="b7bfc-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="b7bfc-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="b7bfc-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="b7bfc-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


