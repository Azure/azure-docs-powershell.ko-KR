---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: d9ffd6ae2f7695a02f8c29fbe745202642039af6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536839"
---
# <span data-ttu-id="dabd2-101">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dabd2-101">Get-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="dabd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dabd2-102">SYNOPSIS</span></span>
<span data-ttu-id="dabd2-103">Runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dabd2-103">Gets a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dabd2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dabd2-104">SYNTAX</span></span>

### <span data-ttu-id="dabd2-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="dabd2-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dabd2-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="dabd2-106">ByRunbookName</span></span>
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dabd2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dabd2-107">DESCRIPTION</span></span>
<span data-ttu-id="dabd2-108">**AzureRmAutomationRunbook** Cmdlet은 Azure Automation runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dabd2-108">The **Get-AzureRmAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="dabd2-109">특정 runbook을 가져오려면 해당 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dabd2-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="dabd2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dabd2-110">EXAMPLES</span></span>

### <span data-ttu-id="dabd2-111">예제 1: 모든 runbook 가져오기</span><span class="sxs-lookup"><span data-stu-id="dabd2-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dabd2-112">이 명령은 Contoso17 이라는 Azure Automation 계정의 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dabd2-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="dabd2-113">변수</span><span class="sxs-lookup"><span data-stu-id="dabd2-113">PARAMETERS</span></span>

### <span data-ttu-id="dabd2-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dabd2-114">-AutomationAccountName</span></span>
<span data-ttu-id="dabd2-115">이 cmdlet이 runbook을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dabd2-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="dabd2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabd2-116">-DefaultProfile</span></span>
<span data-ttu-id="dabd2-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dabd2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dabd2-118">-이름</span><span class="sxs-lookup"><span data-stu-id="dabd2-118">-Name</span></span>
<span data-ttu-id="dabd2-119">이 cmdlet이 가져오는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dabd2-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabd2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dabd2-120">-ResourceGroupName</span></span>
<span data-ttu-id="dabd2-121">이 cmdlet이 runbook을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dabd2-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="dabd2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabd2-122">CommonParameters</span></span>
<span data-ttu-id="dabd2-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dabd2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabd2-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dabd2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabd2-125">입력</span><span class="sxs-lookup"><span data-stu-id="dabd2-125">INPUTS</span></span>

### <span data-ttu-id="dabd2-126">않아야</span><span class="sxs-lookup"><span data-stu-id="dabd2-126">None</span></span>
<span data-ttu-id="dabd2-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dabd2-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dabd2-128">출력</span><span class="sxs-lookup"><span data-stu-id="dabd2-128">OUTPUTS</span></span>

### <span data-ttu-id="dabd2-129">Microsoft. Azure. i a m. Runbook</span><span class="sxs-lookup"><span data-stu-id="dabd2-129">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="dabd2-130">상속자</span><span class="sxs-lookup"><span data-stu-id="dabd2-130">NOTES</span></span>

## <span data-ttu-id="dabd2-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dabd2-131">RELATED LINKS</span></span>

[<span data-ttu-id="dabd2-132">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dabd2-132">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dabd2-133">가져오기-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dabd2-133">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dabd2-134">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dabd2-134">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dabd2-135">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dabd2-135">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dabd2-136">게시-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dabd2-136">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dabd2-137">제거-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dabd2-137">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dabd2-138">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dabd2-138">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dabd2-139">시작-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dabd2-139">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


