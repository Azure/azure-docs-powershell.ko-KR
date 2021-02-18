---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: f60e254e9addf2e7052b010033d9c81ccc6a0a98
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201001"
---
# <span data-ttu-id="b635e-101">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b635e-101">New-AzAutomationVariable</span></span>

## <span data-ttu-id="b635e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b635e-102">SYNOPSIS</span></span>
<span data-ttu-id="b635e-103">Automation 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b635e-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="b635e-104">구문</span><span class="sxs-lookup"><span data-stu-id="b635e-104">SYNTAX</span></span>

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b635e-105">설명</span><span class="sxs-lookup"><span data-stu-id="b635e-105">DESCRIPTION</span></span>
<span data-ttu-id="b635e-106">**New-AzAutomationVariable** cmdlet은 Azure Automation에서 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b635e-106">The **New-AzAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="b635e-107">변수를 암호화하기 위해 Encrypted 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="b635e-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="b635e-108">변수를 생성한 후 암호화된 상태를 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b635e-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="b635e-109">예제</span><span class="sxs-lookup"><span data-stu-id="b635e-109">EXAMPLES</span></span>

### <span data-ttu-id="b635e-110">예제 1: 간단한 값을 사용하여 변수 만들기</span><span class="sxs-lookup"><span data-stu-id="b635e-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b635e-111">이 명령은 Contoso17이라는 Automation 계정에 문자열 값을 사용하여 StringVariable22라는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b635e-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b635e-112">예제 2: 복잡한 값을 사용하여 변수 만들기</span><span class="sxs-lookup"><span data-stu-id="b635e-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b635e-113">첫 번째 명령은 Get-AzVM cmdlet을 사용하여 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b635e-113">The first command gets a virtual machine by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="b635e-114">명령은 이 변수를 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b635e-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b635e-115">두 번째 명령은 Contoso17이라는 Automation 계정에 ComplexVariable01이라는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b635e-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="b635e-116">이 명령은 값에 복합 개체를 사용합니다. 이 경우 가상 머신은 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b635e-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="b635e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b635e-117">PARAMETERS</span></span>

### <span data-ttu-id="b635e-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b635e-118">-AutomationAccountName</span></span>
<span data-ttu-id="b635e-119">변수를 저장할 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b635e-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="b635e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b635e-120">-DefaultProfile</span></span>
<span data-ttu-id="b635e-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b635e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b635e-122">-Description</span><span class="sxs-lookup"><span data-stu-id="b635e-122">-Description</span></span>
<span data-ttu-id="b635e-123">변수에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b635e-123">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b635e-124">-Encrypted</span><span class="sxs-lookup"><span data-stu-id="b635e-124">-Encrypted</span></span>
<span data-ttu-id="b635e-125">이 cmdlet이 저장소에 대한 변수 값을 암호화할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b635e-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b635e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b635e-126">-Name</span></span>
<span data-ttu-id="b635e-127">변수의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b635e-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="b635e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b635e-128">-ResourceGroupName</span></span>
<span data-ttu-id="b635e-129">이 cmdlet이 변수를 만드는 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b635e-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="b635e-130">-Value</span><span class="sxs-lookup"><span data-stu-id="b635e-130">-Value</span></span>
<span data-ttu-id="b635e-131">변수에 대한 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b635e-131">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b635e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b635e-132">CommonParameters</span></span>
<span data-ttu-id="b635e-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b635e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b635e-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b635e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b635e-135">입력</span><span class="sxs-lookup"><span data-stu-id="b635e-135">INPUTS</span></span>

### <span data-ttu-id="b635e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b635e-136">System.String</span></span>

### <span data-ttu-id="b635e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b635e-137">System.Boolean</span></span>

### <span data-ttu-id="b635e-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="b635e-138">System.Object</span></span>

## <span data-ttu-id="b635e-139">출력</span><span class="sxs-lookup"><span data-stu-id="b635e-139">OUTPUTS</span></span>

### <span data-ttu-id="b635e-140">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="b635e-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="b635e-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b635e-141">NOTES</span></span>

## <span data-ttu-id="b635e-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b635e-142">RELATED LINKS</span></span>

[<span data-ttu-id="b635e-143">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b635e-143">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="b635e-144">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b635e-144">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="b635e-145">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b635e-145">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


