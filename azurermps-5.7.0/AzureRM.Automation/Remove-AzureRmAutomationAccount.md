---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: 854a5bd2fb9644d6060810edba44ac7082eb6903
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530565"
---
# <span data-ttu-id="f93fd-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f93fd-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="f93fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f93fd-102">SYNOPSIS</span></span>
<span data-ttu-id="f93fd-103">Automation 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f93fd-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f93fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f93fd-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f93fd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f93fd-105">DESCRIPTION</span></span>
<span data-ttu-id="f93fd-106">**AzureRmAutomationAccount** cmdlet은 리소스 그룹에서 Azure Automation 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f93fd-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>

<span data-ttu-id="f93fd-107">자동화 계정에 대 한 자세한 내용은 New-AzureRmAutomationAccount cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f93fd-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="f93fd-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f93fd-108">EXAMPLES</span></span>

### <span data-ttu-id="f93fd-109">예제 1: automation 계정 제거</span><span class="sxs-lookup"><span data-stu-id="f93fd-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f93fd-110">이 명령은 사용자 유효성 검사를 요청 하지 않고 ContosoAutomationAccount 이라는 이름의 automation 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f93fd-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="f93fd-111">변수</span><span class="sxs-lookup"><span data-stu-id="f93fd-111">PARAMETERS</span></span>

### <span data-ttu-id="f93fd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f93fd-112">-DefaultProfile</span></span>
<span data-ttu-id="f93fd-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f93fd-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93fd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f93fd-114">-Force</span></span>
<span data-ttu-id="f93fd-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="f93fd-115">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93fd-116">-이름</span><span class="sxs-lookup"><span data-stu-id="f93fd-116">-Name</span></span>
<span data-ttu-id="f93fd-117">이 cmdlet이 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f93fd-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93fd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f93fd-118">-ResourceGroupName</span></span>
<span data-ttu-id="f93fd-119">이 cmdlet이 Automation 계정을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f93fd-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93fd-120">-확인</span><span class="sxs-lookup"><span data-stu-id="f93fd-120">-Confirm</span></span>
<span data-ttu-id="f93fd-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f93fd-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93fd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f93fd-122">-WhatIf</span></span>
<span data-ttu-id="f93fd-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f93fd-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f93fd-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f93fd-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93fd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f93fd-125">CommonParameters</span></span>
<span data-ttu-id="f93fd-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f93fd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f93fd-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f93fd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f93fd-128">입력</span><span class="sxs-lookup"><span data-stu-id="f93fd-128">INPUTS</span></span>

### <span data-ttu-id="f93fd-129">않아야</span><span class="sxs-lookup"><span data-stu-id="f93fd-129">None</span></span>
<span data-ttu-id="f93fd-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f93fd-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f93fd-131">출력</span><span class="sxs-lookup"><span data-stu-id="f93fd-131">OUTPUTS</span></span>

### <span data-ttu-id="f93fd-132">Microsoft Azure. \*.</span><span class="sxs-lookup"><span data-stu-id="f93fd-132">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="f93fd-133">상속자</span><span class="sxs-lookup"><span data-stu-id="f93fd-133">NOTES</span></span>

## <span data-ttu-id="f93fd-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f93fd-134">RELATED LINKS</span></span>

[<span data-ttu-id="f93fd-135">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f93fd-135">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="f93fd-136">새로운 AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f93fd-136">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="f93fd-137">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f93fd-137">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


