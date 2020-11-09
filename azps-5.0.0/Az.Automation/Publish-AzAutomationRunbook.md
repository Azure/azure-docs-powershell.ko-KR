---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: feca8adfbfe24ce006c2fc5f52618f43591fa0b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307514"
---
# <span data-ttu-id="31798-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="31798-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="31798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31798-102">SYNOPSIS</span></span>
<span data-ttu-id="31798-103">Runbook을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31798-103">Publishes a runbook.</span></span>

## <span data-ttu-id="31798-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31798-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31798-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31798-105">DESCRIPTION</span></span>
<span data-ttu-id="31798-106">**AzAutomationRunbook** Cmdlet은 Azure Automation의 프로덕션 환경에서 사용할 runbook을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31798-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="31798-107">예제의</span><span class="sxs-lookup"><span data-stu-id="31798-107">EXAMPLES</span></span>

### <span data-ttu-id="31798-108">예제 1: runbook 게시</span><span class="sxs-lookup"><span data-stu-id="31798-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="31798-109">이 명령은 Contoso17 이라는 Azure Automation 계정에 Runbk01 라는 runbook을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31798-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="31798-110">변수</span><span class="sxs-lookup"><span data-stu-id="31798-110">PARAMETERS</span></span>

### <span data-ttu-id="31798-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="31798-111">-AutomationAccountName</span></span>
<span data-ttu-id="31798-112">이 cmdlet이 runbook을 게시 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31798-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="31798-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31798-113">-DefaultProfile</span></span>
<span data-ttu-id="31798-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="31798-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31798-115">-이름</span><span class="sxs-lookup"><span data-stu-id="31798-115">-Name</span></span>
<span data-ttu-id="31798-116">이 cmdlet이 게시 하는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31798-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31798-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31798-117">-ResourceGroupName</span></span>
<span data-ttu-id="31798-118">이 cmdlet이 runbook을 게시할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31798-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="31798-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31798-119">CommonParameters</span></span>
<span data-ttu-id="31798-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31798-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31798-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31798-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31798-122">입력</span><span class="sxs-lookup"><span data-stu-id="31798-122">INPUTS</span></span>

### <span data-ttu-id="31798-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="31798-123">System.String</span></span>

## <span data-ttu-id="31798-124">출력</span><span class="sxs-lookup"><span data-stu-id="31798-124">OUTPUTS</span></span>

### <span data-ttu-id="31798-125">Microsoft. Azure. i a m. Runbook</span><span class="sxs-lookup"><span data-stu-id="31798-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="31798-126">상속자</span><span class="sxs-lookup"><span data-stu-id="31798-126">NOTES</span></span>

## <span data-ttu-id="31798-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31798-127">RELATED LINKS</span></span>

[<span data-ttu-id="31798-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="31798-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="31798-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="31798-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="31798-130">가져오기-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="31798-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="31798-131">새로운 AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="31798-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="31798-132">새로운 AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="31798-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="31798-133">제거-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="31798-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="31798-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="31798-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="31798-135">시작-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="31798-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


