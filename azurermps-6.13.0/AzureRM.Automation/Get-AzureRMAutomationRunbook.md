---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: 5a47676a7c01052f44acba6362bd24eb65e4c05f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534495"
---
# <span data-ttu-id="78f55-101">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="78f55-101">Get-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="78f55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78f55-102">SYNOPSIS</span></span>
<span data-ttu-id="78f55-103">Runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78f55-103">Gets a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78f55-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78f55-104">SYNTAX</span></span>

### <span data-ttu-id="78f55-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="78f55-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78f55-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="78f55-106">ByRunbookName</span></span>
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78f55-107">설명은</span><span class="sxs-lookup"><span data-stu-id="78f55-107">DESCRIPTION</span></span>
<span data-ttu-id="78f55-108">**AzureRmAutomationRunbook** Cmdlet은 Azure Automation runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78f55-108">The **Get-AzureRmAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="78f55-109">특정 runbook을 가져오려면 해당 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78f55-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="78f55-110">예제의</span><span class="sxs-lookup"><span data-stu-id="78f55-110">EXAMPLES</span></span>

### <span data-ttu-id="78f55-111">예제 1: 모든 runbook 가져오기</span><span class="sxs-lookup"><span data-stu-id="78f55-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="78f55-112">이 명령은 Contoso17 이라는 Azure Automation 계정의 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78f55-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="78f55-113">변수</span><span class="sxs-lookup"><span data-stu-id="78f55-113">PARAMETERS</span></span>

### <span data-ttu-id="78f55-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="78f55-114">-AutomationAccountName</span></span>
<span data-ttu-id="78f55-115">이 cmdlet이 runbook을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78f55-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="78f55-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f55-116">-DefaultProfile</span></span>
<span data-ttu-id="78f55-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="78f55-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78f55-118">-이름</span><span class="sxs-lookup"><span data-stu-id="78f55-118">-Name</span></span>
<span data-ttu-id="78f55-119">이 cmdlet이 가져오는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78f55-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f55-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f55-120">-ResourceGroupName</span></span>
<span data-ttu-id="78f55-121">이 cmdlet이 runbook을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78f55-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="78f55-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f55-122">CommonParameters</span></span>
<span data-ttu-id="78f55-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78f55-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f55-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78f55-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f55-125">입력</span><span class="sxs-lookup"><span data-stu-id="78f55-125">INPUTS</span></span>

### <span data-ttu-id="78f55-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="78f55-126">System.String</span></span>

## <span data-ttu-id="78f55-127">출력</span><span class="sxs-lookup"><span data-stu-id="78f55-127">OUTPUTS</span></span>

### <span data-ttu-id="78f55-128">Microsoft. Azure. i a m. Runbook</span><span class="sxs-lookup"><span data-stu-id="78f55-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="78f55-129">상속자</span><span class="sxs-lookup"><span data-stu-id="78f55-129">NOTES</span></span>

## <span data-ttu-id="78f55-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78f55-130">RELATED LINKS</span></span>

[<span data-ttu-id="78f55-131">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="78f55-131">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="78f55-132">가져오기-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="78f55-132">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="78f55-133">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="78f55-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="78f55-134">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="78f55-134">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="78f55-135">게시-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="78f55-135">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="78f55-136">제거-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="78f55-136">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="78f55-137">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="78f55-137">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="78f55-138">시작-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="78f55-138">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


