---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: a8238cf9de2b0b20cb347d16bb74623f6469c03c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044987"
---
# <span data-ttu-id="90971-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="90971-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="90971-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90971-102">SYNOPSIS</span></span>
<span data-ttu-id="90971-103">자동화 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90971-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="90971-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90971-104">SYNTAX</span></span>

### <span data-ttu-id="90971-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="90971-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90971-106">ByName</span><span class="sxs-lookup"><span data-stu-id="90971-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90971-107">설명은</span><span class="sxs-lookup"><span data-stu-id="90971-107">DESCRIPTION</span></span>
<span data-ttu-id="90971-108">**Get-AzAutomationVariable** cmdlet은 하나 이상의 Azure 자동화 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90971-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="90971-109">특정 변수를 가져오려면 해당 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90971-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="90971-110">예제의</span><span class="sxs-lookup"><span data-stu-id="90971-110">EXAMPLES</span></span>

### <span data-ttu-id="90971-111">예제 1: 변수 가져오기</span><span class="sxs-lookup"><span data-stu-id="90971-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="90971-112">첫 번째 명령은 Contoso17 라는 계정에서 Variable06 이라는 자동화 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90971-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="90971-113">명령이 $Variable 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="90971-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="90971-114">두 번째 명령은 표준 점 표기법을 사용 하 여 $Variable의 **value** 속성을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="90971-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="90971-115">명령이 $value 변수에 값을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="90971-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="90971-116">변수</span><span class="sxs-lookup"><span data-stu-id="90971-116">PARAMETERS</span></span>

### <span data-ttu-id="90971-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="90971-117">-AutomationAccountName</span></span>
<span data-ttu-id="90971-118">이 cmdlet이 가져오는 변수를 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90971-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="90971-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90971-119">-DefaultProfile</span></span>
<span data-ttu-id="90971-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="90971-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90971-121">-이름</span><span class="sxs-lookup"><span data-stu-id="90971-121">-Name</span></span>
<span data-ttu-id="90971-122">이 cmdlet이 가져오는 변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90971-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="90971-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90971-123">-ResourceGroupName</span></span>
<span data-ttu-id="90971-124">이 cmdlet이 변수를 가져오는 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90971-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="90971-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90971-125">CommonParameters</span></span>
<span data-ttu-id="90971-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90971-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90971-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90971-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90971-128">입력</span><span class="sxs-lookup"><span data-stu-id="90971-128">INPUTS</span></span>

### <span data-ttu-id="90971-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="90971-129">System.String</span></span>

## <span data-ttu-id="90971-130">출력</span><span class="sxs-lookup"><span data-stu-id="90971-130">OUTPUTS</span></span>

### <span data-ttu-id="90971-131">Microsoft. Azure. m a. 모델 변수</span><span class="sxs-lookup"><span data-stu-id="90971-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="90971-132">상속자</span><span class="sxs-lookup"><span data-stu-id="90971-132">NOTES</span></span>

## <span data-ttu-id="90971-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90971-133">RELATED LINKS</span></span>

[<span data-ttu-id="90971-134">새로운 AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="90971-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="90971-135">제거-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="90971-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="90971-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="90971-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


