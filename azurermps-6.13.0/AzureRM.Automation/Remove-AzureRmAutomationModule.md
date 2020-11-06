---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 2d3a8d2b247da8f1a2149fd15372858a3b2b3775
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528656"
---
# <span data-ttu-id="68ed3-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="68ed3-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="68ed3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68ed3-102">SYNOPSIS</span></span>
<span data-ttu-id="68ed3-103">자동화에서 모듈을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed3-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68ed3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68ed3-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68ed3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="68ed3-105">DESCRIPTION</span></span>
<span data-ttu-id="68ed3-106">**AzureRmAutomationModule** Cmdlet은 Azure Automation의 자동화 계정에서 모듈을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed3-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="68ed3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="68ed3-107">EXAMPLES</span></span>

### <span data-ttu-id="68ed3-108">예제 1: 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="68ed3-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="68ed3-109">이 명령은 Contoso17 이라는 자동화 계정에서 ContosoModule 이라는 모듈을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed3-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="68ed3-110">변수</span><span class="sxs-lookup"><span data-stu-id="68ed3-110">PARAMETERS</span></span>

### <span data-ttu-id="68ed3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="68ed3-111">-AutomationAccountName</span></span>
<span data-ttu-id="68ed3-112">이 cmdlet에서 모듈을 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed3-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="68ed3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ed3-113">-DefaultProfile</span></span>
<span data-ttu-id="68ed3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="68ed3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ed3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="68ed3-115">-Force</span></span>
<span data-ttu-id="68ed3-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="68ed3-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ed3-117">-이름</span><span class="sxs-lookup"><span data-stu-id="68ed3-117">-Name</span></span>
<span data-ttu-id="68ed3-118">이 cmdlet이 제거 하는 모듈의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed3-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="68ed3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ed3-119">-ResourceGroupName</span></span>
<span data-ttu-id="68ed3-120">이 cmdlet이 모듈을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed3-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="68ed3-121">-확인</span><span class="sxs-lookup"><span data-stu-id="68ed3-121">-Confirm</span></span>
<span data-ttu-id="68ed3-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ed3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68ed3-123">-WhatIf</span></span>
<span data-ttu-id="68ed3-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68ed3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68ed3-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68ed3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68ed3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ed3-126">CommonParameters</span></span>
<span data-ttu-id="68ed3-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ed3-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68ed3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ed3-129">입력</span><span class="sxs-lookup"><span data-stu-id="68ed3-129">INPUTS</span></span>

### <span data-ttu-id="68ed3-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="68ed3-130">System.String</span></span>

## <span data-ttu-id="68ed3-131">출력</span><span class="sxs-lookup"><span data-stu-id="68ed3-131">OUTPUTS</span></span>

### <span data-ttu-id="68ed3-132">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="68ed3-132">System.Void</span></span>

## <span data-ttu-id="68ed3-133">상속자</span><span class="sxs-lookup"><span data-stu-id="68ed3-133">NOTES</span></span>

## <span data-ttu-id="68ed3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68ed3-134">RELATED LINKS</span></span>

[<span data-ttu-id="68ed3-135">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="68ed3-135">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="68ed3-136">새로운 AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="68ed3-136">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="68ed3-137">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="68ed3-137">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


