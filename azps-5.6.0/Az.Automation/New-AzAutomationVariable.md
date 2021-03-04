---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: d5058a3741bfaf598793f81ae030541d26aa4aa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956480"
---
# <span data-ttu-id="928b5-101">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="928b5-101">New-AzAutomationVariable</span></span>

## <span data-ttu-id="928b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="928b5-102">SYNOPSIS</span></span>
<span data-ttu-id="928b5-103">Automation 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="928b5-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="928b5-104">구문</span><span class="sxs-lookup"><span data-stu-id="928b5-104">SYNTAX</span></span>

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="928b5-105">설명</span><span class="sxs-lookup"><span data-stu-id="928b5-105">DESCRIPTION</span></span>
<span data-ttu-id="928b5-106">**New-AzAutomationVariable** cmdlet은 Azure Automation에서 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="928b5-106">The **New-AzAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="928b5-107">변수를 암호화하기 위해 암호화된 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="928b5-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="928b5-108">생성 후 변수의 암호화된 상태를 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="928b5-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="928b5-109">예제</span><span class="sxs-lookup"><span data-stu-id="928b5-109">EXAMPLES</span></span>

### <span data-ttu-id="928b5-110">예제 1: 간단한 값으로 변수 만들기</span><span class="sxs-lookup"><span data-stu-id="928b5-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="928b5-111">이 명령은 Contoso17이라는 Automation 계정에 문자열 값이 있는 StringVariable22라는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="928b5-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="928b5-112">예제 2: 복잡한 값을 사용하여 변수 만들기</span><span class="sxs-lookup"><span data-stu-id="928b5-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="928b5-113">첫 번째 명령은 Get-AzVM cmdlet을 사용하여 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="928b5-113">The first command gets a virtual machine by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="928b5-114">명령은 이 변수를 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="928b5-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="928b5-115">두 번째 명령은 Contoso17이라는 Automation 계정에 ComplexVariable01이라는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="928b5-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="928b5-116">이 명령은 해당 값에 대해 복잡한 개체를 사용합니다. 이 경우 가상 머신은 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="928b5-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="928b5-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="928b5-117">PARAMETERS</span></span>

### <span data-ttu-id="928b5-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="928b5-118">-AutomationAccountName</span></span>
<span data-ttu-id="928b5-119">변수를 저장할 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="928b5-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="928b5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="928b5-120">-DefaultProfile</span></span>
<span data-ttu-id="928b5-121">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="928b5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="928b5-122">-Description</span><span class="sxs-lookup"><span data-stu-id="928b5-122">-Description</span></span>
<span data-ttu-id="928b5-123">변수에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="928b5-123">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="928b5-124">-암호화</span><span class="sxs-lookup"><span data-stu-id="928b5-124">-Encrypted</span></span>
<span data-ttu-id="928b5-125">이 cmdlet이 저장소에 대한 변수 값을 암호화하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="928b5-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="928b5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="928b5-126">-Name</span></span>
<span data-ttu-id="928b5-127">변수의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="928b5-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="928b5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="928b5-128">-ResourceGroupName</span></span>
<span data-ttu-id="928b5-129">이 cmdlet에서 변수를 만드는 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="928b5-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="928b5-130">-Value</span><span class="sxs-lookup"><span data-stu-id="928b5-130">-Value</span></span>
<span data-ttu-id="928b5-131">변수에 대한 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="928b5-131">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="928b5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928b5-132">CommonParameters</span></span>
<span data-ttu-id="928b5-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="928b5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928b5-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="928b5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928b5-135">입력</span><span class="sxs-lookup"><span data-stu-id="928b5-135">INPUTS</span></span>

### <span data-ttu-id="928b5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="928b5-136">System.String</span></span>

### <span data-ttu-id="928b5-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="928b5-137">System.Boolean</span></span>

### <span data-ttu-id="928b5-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="928b5-138">System.Object</span></span>

## <span data-ttu-id="928b5-139">출력</span><span class="sxs-lookup"><span data-stu-id="928b5-139">OUTPUTS</span></span>

### <span data-ttu-id="928b5-140">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="928b5-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="928b5-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="928b5-141">NOTES</span></span>

## <span data-ttu-id="928b5-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="928b5-142">RELATED LINKS</span></span>

[<span data-ttu-id="928b5-143">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="928b5-143">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="928b5-144">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="928b5-144">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="928b5-145">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="928b5-145">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


