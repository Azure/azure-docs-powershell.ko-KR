---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
ms.openlocfilehash: 5fccd3f6aa193a3c2cacf39e6b72bccdf440b393
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538079"
---
# <span data-ttu-id="fd770-101">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="fd770-101">Get-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="fd770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd770-102">SYNOPSIS</span></span>
<span data-ttu-id="fd770-103">자동화 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd770-103">Gets an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd770-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd770-104">SYNTAX</span></span>

### <span data-ttu-id="fd770-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="fd770-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd770-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fd770-106">ByName</span></span>
```
Get-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd770-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fd770-107">DESCRIPTION</span></span>
<span data-ttu-id="fd770-108">**Get-AzureRmAutomationVariable** cmdlet은 하나 이상의 Azure 자동화 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd770-108">The **Get-AzureRmAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="fd770-109">특정 변수를 가져오려면 해당 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd770-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="fd770-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fd770-110">EXAMPLES</span></span>

### <span data-ttu-id="fd770-111">예제 1: 변수 가져오기</span><span class="sxs-lookup"><span data-stu-id="fd770-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="fd770-112">첫 번째 명령은 Contoso17 라는 계정에서 Variable06 이라는 자동화 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd770-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="fd770-113">명령이 $Variable 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd770-113">The command stores that object in the $Variable variable.</span></span>

<span data-ttu-id="fd770-114">두 번째 명령은 표준 점 표기법을 사용 하 여 $Variable의 **value** 속성을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd770-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="fd770-115">명령이 $value 변수에 값을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd770-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="fd770-116">변수</span><span class="sxs-lookup"><span data-stu-id="fd770-116">PARAMETERS</span></span>

### <span data-ttu-id="fd770-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fd770-117">-AutomationAccountName</span></span>
<span data-ttu-id="fd770-118">이 cmdlet이 가져오는 변수를 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd770-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fd770-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd770-119">-DefaultProfile</span></span>
<span data-ttu-id="fd770-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fd770-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd770-121">-이름</span><span class="sxs-lookup"><span data-stu-id="fd770-121">-Name</span></span>
<span data-ttu-id="fd770-122">이 cmdlet이 가져오는 변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd770-122">Specifies the name of a variable that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd770-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd770-123">-ResourceGroupName</span></span>
<span data-ttu-id="fd770-124">이 cmdlet이 변수를 가져오는 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd770-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="fd770-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd770-125">CommonParameters</span></span>
<span data-ttu-id="fd770-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd770-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd770-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd770-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd770-128">입력</span><span class="sxs-lookup"><span data-stu-id="fd770-128">INPUTS</span></span>

### <span data-ttu-id="fd770-129">않아야</span><span class="sxs-lookup"><span data-stu-id="fd770-129">None</span></span>
<span data-ttu-id="fd770-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd770-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd770-131">출력</span><span class="sxs-lookup"><span data-stu-id="fd770-131">OUTPUTS</span></span>

### <span data-ttu-id="fd770-132">Microsoft. Azure. m a. 모델 변수</span><span class="sxs-lookup"><span data-stu-id="fd770-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="fd770-133">상속자</span><span class="sxs-lookup"><span data-stu-id="fd770-133">NOTES</span></span>

## <span data-ttu-id="fd770-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd770-134">RELATED LINKS</span></span>

[<span data-ttu-id="fd770-135">새로운 AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="fd770-135">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="fd770-136">제거-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="fd770-136">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="fd770-137">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="fd770-137">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


