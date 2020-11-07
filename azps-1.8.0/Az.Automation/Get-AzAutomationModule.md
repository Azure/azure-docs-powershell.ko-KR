---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: 54bbda0226cf2aa374e149bc4b5885b86b31ef12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701610"
---
# <span data-ttu-id="f15ba-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f15ba-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="f15ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f15ba-102">SYNOPSIS</span></span>
<span data-ttu-id="f15ba-103">자동화에서 모듈에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f15ba-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="f15ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f15ba-104">SYNTAX</span></span>

### <span data-ttu-id="f15ba-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="f15ba-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f15ba-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f15ba-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f15ba-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f15ba-107">DESCRIPTION</span></span>
<span data-ttu-id="f15ba-108">**AzAutomationModule** Cmdlet은 Azure 자동화에서 모듈에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f15ba-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="f15ba-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f15ba-109">EXAMPLES</span></span>

### <span data-ttu-id="f15ba-110">예제 1: 모든 모듈 가져오기</span><span class="sxs-lookup"><span data-stu-id="f15ba-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f15ba-111">이 명령은 Contoso17 이라는 자동화 계정에 있는 모든 모듈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f15ba-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f15ba-112">예제 2: 모듈 가져오기</span><span class="sxs-lookup"><span data-stu-id="f15ba-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f15ba-113">이 명령은 Contoso17 이라는 Automation 계정의 ContosoModule 라는 모듈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f15ba-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f15ba-114">변수</span><span class="sxs-lookup"><span data-stu-id="f15ba-114">PARAMETERS</span></span>

### <span data-ttu-id="f15ba-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f15ba-115">-AutomationAccountName</span></span>
<span data-ttu-id="f15ba-116">이 cmdlet이 모듈 메타 데이터를 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f15ba-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="f15ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f15ba-117">-DefaultProfile</span></span>
<span data-ttu-id="f15ba-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f15ba-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f15ba-119">-이름</span><span class="sxs-lookup"><span data-stu-id="f15ba-119">-Name</span></span>
<span data-ttu-id="f15ba-120">이 cmdlet이 메타 데이터를 가져오는 모듈의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f15ba-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f15ba-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f15ba-121">-ResourceGroupName</span></span>
<span data-ttu-id="f15ba-122">이 cmdlet이 모듈 메타 데이터를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f15ba-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="f15ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f15ba-123">CommonParameters</span></span>
<span data-ttu-id="f15ba-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f15ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f15ba-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f15ba-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f15ba-126">입력</span><span class="sxs-lookup"><span data-stu-id="f15ba-126">INPUTS</span></span>

### <span data-ttu-id="f15ba-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f15ba-127">System.String</span></span>

## <span data-ttu-id="f15ba-128">출력</span><span class="sxs-lookup"><span data-stu-id="f15ba-128">OUTPUTS</span></span>

### <span data-ttu-id="f15ba-129">Microsoft Azure. 모듈별. 모듈</span><span class="sxs-lookup"><span data-stu-id="f15ba-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="f15ba-130">상속자</span><span class="sxs-lookup"><span data-stu-id="f15ba-130">NOTES</span></span>

## <span data-ttu-id="f15ba-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f15ba-131">RELATED LINKS</span></span>

[<span data-ttu-id="f15ba-132">새로운 AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f15ba-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="f15ba-133">제거-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f15ba-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="f15ba-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f15ba-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


