---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
ms.openlocfilehash: a4f65e20253ef979cba5d3907faeba3fb58e7fe6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536824"
---
# <span data-ttu-id="7eefc-101">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7eefc-101">Remove-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="7eefc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eefc-102">SYNOPSIS</span></span>
<span data-ttu-id="7eefc-103">Runbook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eefc-103">Removes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eefc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7eefc-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7eefc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7eefc-105">DESCRIPTION</span></span>
<span data-ttu-id="7eefc-106">**AzureRmAutomationRunbook** Cmdlet은 Azure 자동화에서 runbook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eefc-106">The **Remove-AzureRmAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="7eefc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7eefc-107">EXAMPLES</span></span>

### <span data-ttu-id="7eefc-108">예제 1: runbook 제거</span><span class="sxs-lookup"><span data-stu-id="7eefc-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7eefc-109">이 명령은 Contoso17 이라는 Azure Automation 계정에서 Runbook03 라는 runbook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eefc-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="7eefc-110">변수</span><span class="sxs-lookup"><span data-stu-id="7eefc-110">PARAMETERS</span></span>

### <span data-ttu-id="7eefc-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7eefc-111">-AutomationAccountName</span></span>
<span data-ttu-id="7eefc-112">이 cmdlet이 runbook을 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eefc-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eefc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eefc-113">-DefaultProfile</span></span>
<span data-ttu-id="7eefc-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7eefc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7eefc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7eefc-115">-Force</span></span>
<span data-ttu-id="7eefc-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="7eefc-116">ps_force</span></span>

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

### <span data-ttu-id="7eefc-117">-이름</span><span class="sxs-lookup"><span data-stu-id="7eefc-117">-Name</span></span>
<span data-ttu-id="7eefc-118">이 cmdlet이 제거 하는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eefc-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eefc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eefc-119">-ResourceGroupName</span></span>
<span data-ttu-id="7eefc-120">이 cmdlet이 runbook을 게시할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eefc-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="7eefc-121">-확인</span><span class="sxs-lookup"><span data-stu-id="7eefc-121">-Confirm</span></span>
<span data-ttu-id="7eefc-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eefc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eefc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eefc-123">-WhatIf</span></span>
<span data-ttu-id="7eefc-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7eefc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eefc-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7eefc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eefc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eefc-126">CommonParameters</span></span>
<span data-ttu-id="7eefc-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eefc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eefc-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eefc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eefc-129">입력</span><span class="sxs-lookup"><span data-stu-id="7eefc-129">INPUTS</span></span>

### <span data-ttu-id="7eefc-130">않아야</span><span class="sxs-lookup"><span data-stu-id="7eefc-130">None</span></span>
<span data-ttu-id="7eefc-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7eefc-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7eefc-132">출력</span><span class="sxs-lookup"><span data-stu-id="7eefc-132">OUTPUTS</span></span>

## <span data-ttu-id="7eefc-133">상속자</span><span class="sxs-lookup"><span data-stu-id="7eefc-133">NOTES</span></span>

## <span data-ttu-id="7eefc-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7eefc-134">RELATED LINKS</span></span>

[<span data-ttu-id="7eefc-135">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7eefc-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7eefc-136">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7eefc-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7eefc-137">가져오기-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7eefc-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7eefc-138">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7eefc-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7eefc-139">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7eefc-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7eefc-140">게시-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7eefc-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7eefc-141">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7eefc-141">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7eefc-142">시작-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7eefc-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


