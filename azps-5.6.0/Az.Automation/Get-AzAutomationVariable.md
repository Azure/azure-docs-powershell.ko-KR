---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: c30e78b21c8f0dbc59e12c0fbecad14cfc93781a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014128"
---
# <span data-ttu-id="efdff-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="efdff-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="efdff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efdff-102">SYNOPSIS</span></span>
<span data-ttu-id="efdff-103">Automation 변수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efdff-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="efdff-104">구문</span><span class="sxs-lookup"><span data-stu-id="efdff-104">SYNTAX</span></span>

### <span data-ttu-id="efdff-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="efdff-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efdff-106">ByName</span><span class="sxs-lookup"><span data-stu-id="efdff-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efdff-107">설명</span><span class="sxs-lookup"><span data-stu-id="efdff-107">DESCRIPTION</span></span>
<span data-ttu-id="efdff-108">**Get-AzAutomationVariable** cmdlet은 하나 이상의 Azure Automation 변수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efdff-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="efdff-109">특정 변수를 얻지 못하도록 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efdff-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="efdff-110">예제</span><span class="sxs-lookup"><span data-stu-id="efdff-110">EXAMPLES</span></span>

### <span data-ttu-id="efdff-111">예제 1: 변수를 얻다</span><span class="sxs-lookup"><span data-stu-id="efdff-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="efdff-112">첫 번째 명령은 Contoso17이라는 계정에서 Variable06이라는 Automation 변수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efdff-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="efdff-113">명령은 해당 개체를 $Variable 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="efdff-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="efdff-114">두 번째 명령은 표준 점표를  사용하여 $Variable.</span><span class="sxs-lookup"><span data-stu-id="efdff-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="efdff-115">명령은 변수 변수에 $value 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="efdff-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="efdff-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="efdff-116">PARAMETERS</span></span>

### <span data-ttu-id="efdff-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="efdff-117">-AutomationAccountName</span></span>
<span data-ttu-id="efdff-118">이 cmdlet이 얻을 변수를 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efdff-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="efdff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efdff-119">-DefaultProfile</span></span>
<span data-ttu-id="efdff-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="efdff-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efdff-121">-Name</span><span class="sxs-lookup"><span data-stu-id="efdff-121">-Name</span></span>
<span data-ttu-id="efdff-122">이 cmdlet이 얻을 변수의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efdff-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="efdff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efdff-123">-ResourceGroupName</span></span>
<span data-ttu-id="efdff-124">이 cmdlet에서 변수를 얻을 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efdff-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="efdff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efdff-125">CommonParameters</span></span>
<span data-ttu-id="efdff-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="efdff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efdff-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="efdff-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efdff-128">입력</span><span class="sxs-lookup"><span data-stu-id="efdff-128">INPUTS</span></span>

### <span data-ttu-id="efdff-129">System.String</span><span class="sxs-lookup"><span data-stu-id="efdff-129">System.String</span></span>

## <span data-ttu-id="efdff-130">출력</span><span class="sxs-lookup"><span data-stu-id="efdff-130">OUTPUTS</span></span>

### <span data-ttu-id="efdff-131">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="efdff-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="efdff-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="efdff-132">NOTES</span></span>

## <span data-ttu-id="efdff-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efdff-133">RELATED LINKS</span></span>

[<span data-ttu-id="efdff-134">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="efdff-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="efdff-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="efdff-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="efdff-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="efdff-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


