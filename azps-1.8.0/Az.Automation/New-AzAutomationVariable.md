---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: ea07e0d0b0c60b35186224d7ea0284df17d1e27b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701554"
---
# <span data-ttu-id="b8ccb-101">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b8ccb-101">New-AzAutomationVariable</span></span>

## <span data-ttu-id="b8ccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ccb-103">자동화 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="b8ccb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8ccb-104">SYNTAX</span></span>

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8ccb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b8ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="b8ccb-106">**AzAutomationVariable** Cmdlet은 Azure 자동화에서 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-106">The **New-AzAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="b8ccb-107">변수를 암호화 하려면 *암호화* 된 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="b8ccb-108">생성 후 변수의 암호화 된 상태를 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="b8ccb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b8ccb-109">EXAMPLES</span></span>

### <span data-ttu-id="b8ccb-110">예제 1: 간단한 값을 사용 하 여 변수 만들기</span><span class="sxs-lookup"><span data-stu-id="b8ccb-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b8ccb-111">이 명령은 Contoso17 이라는 Automation 계정에 문자열 값이 있는 StringVariable22 라는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b8ccb-112">예제 2: 복잡 한 값을 사용 하 여 변수 만들기</span><span class="sxs-lookup"><span data-stu-id="b8ccb-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b8ccb-113">첫 번째 명령은 Get-AzVM cmdlet을 사용 하 여 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-113">The first command gets a virtual machine by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="b8ccb-114">명령이 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b8ccb-115">두 번째 명령은 Contoso17 이라는 Automation 계정에 ComplexVariable01 이라는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="b8ccb-116">이 명령은 해당 값 (이 경우 $VirtualMachine의 가상 컴퓨터)에 대 한 복합 개체를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="b8ccb-117">변수</span><span class="sxs-lookup"><span data-stu-id="b8ccb-117">PARAMETERS</span></span>

### <span data-ttu-id="b8ccb-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b8ccb-118">-AutomationAccountName</span></span>
<span data-ttu-id="b8ccb-119">변수를 저장할 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="b8ccb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ccb-120">-DefaultProfile</span></span>
<span data-ttu-id="b8ccb-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b8ccb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8ccb-122">-설명</span><span class="sxs-lookup"><span data-stu-id="b8ccb-122">-Description</span></span>
<span data-ttu-id="b8ccb-123">변수에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-123">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="b8ccb-124">암호화 된</span><span class="sxs-lookup"><span data-stu-id="b8ccb-124">-Encrypted</span></span>
<span data-ttu-id="b8ccb-125">이 cmdlet이 저장소의 변수 값을 암호화할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="b8ccb-126">-이름</span><span class="sxs-lookup"><span data-stu-id="b8ccb-126">-Name</span></span>
<span data-ttu-id="b8ccb-127">변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="b8ccb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8ccb-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8ccb-129">이 cmdlet이 변수를 만드는 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="b8ccb-130">-값</span><span class="sxs-lookup"><span data-stu-id="b8ccb-130">-Value</span></span>
<span data-ttu-id="b8ccb-131">변수의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-131">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="b8ccb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ccb-132">CommonParameters</span></span>
<span data-ttu-id="b8ccb-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ccb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ccb-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8ccb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ccb-135">입력</span><span class="sxs-lookup"><span data-stu-id="b8ccb-135">INPUTS</span></span>

### <span data-ttu-id="b8ccb-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b8ccb-136">System.String</span></span>

### <span data-ttu-id="b8ccb-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b8ccb-137">System.Boolean</span></span>

### <span data-ttu-id="b8ccb-138">System. 개체</span><span class="sxs-lookup"><span data-stu-id="b8ccb-138">System.Object</span></span>

## <span data-ttu-id="b8ccb-139">출력</span><span class="sxs-lookup"><span data-stu-id="b8ccb-139">OUTPUTS</span></span>

### <span data-ttu-id="b8ccb-140">Microsoft. Azure. m a. 모델 변수</span><span class="sxs-lookup"><span data-stu-id="b8ccb-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="b8ccb-141">상속자</span><span class="sxs-lookup"><span data-stu-id="b8ccb-141">NOTES</span></span>

## <span data-ttu-id="b8ccb-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8ccb-142">RELATED LINKS</span></span>

[<span data-ttu-id="b8ccb-143">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b8ccb-143">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="b8ccb-144">제거-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b8ccb-144">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="b8ccb-145">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b8ccb-145">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


