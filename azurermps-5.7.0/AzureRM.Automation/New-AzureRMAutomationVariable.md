---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: 217a6553a21871e79998dcad0630f4c0e1b6aec4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535335"
---
# <span data-ttu-id="5532d-101">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5532d-101">New-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="5532d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5532d-102">SYNOPSIS</span></span>
<span data-ttu-id="5532d-103">자동화 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-103">Creates an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5532d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5532d-104">SYNTAX</span></span>

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5532d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5532d-105">DESCRIPTION</span></span>
<span data-ttu-id="5532d-106">**AzureRmAutomationVariable** Cmdlet은 Azure 자동화에서 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-106">The **New-AzureRmAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="5532d-107">변수를 암호화 하려면 *암호화* 된 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="5532d-108">생성 후 변수의 암호화 된 상태를 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="5532d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5532d-109">EXAMPLES</span></span>

### <span data-ttu-id="5532d-110">예제 1: 간단한 값을 사용 하 여 변수 만들기</span><span class="sxs-lookup"><span data-stu-id="5532d-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5532d-111">이 명령은 Contoso17 이라는 Automation 계정에 문자열 값이 있는 StringVariable22 라는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="5532d-112">예제 2: 복잡 한 값을 사용 하 여 변수 만들기</span><span class="sxs-lookup"><span data-stu-id="5532d-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5532d-113">첫 번째 명령은 Get-AzureVM cmdlet을 사용 하 여 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-113">The first command gets a virtual machine by using the Get-AzureVM cmdlet.</span></span>
<span data-ttu-id="5532d-114">명령이 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-114">The command stores it in the $VirtualMachine variable.</span></span>

<span data-ttu-id="5532d-115">두 번째 명령은 Contoso17 이라는 Automation 계정에 ComplexVariable01 이라는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="5532d-116">이 명령은 해당 값 (이 경우 $VirtualMachine의 가상 컴퓨터)에 대 한 복합 개체를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="5532d-117">변수</span><span class="sxs-lookup"><span data-stu-id="5532d-117">PARAMETERS</span></span>

### <span data-ttu-id="5532d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5532d-118">-AutomationAccountName</span></span>
<span data-ttu-id="5532d-119">변수를 저장할 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="5532d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5532d-120">-DefaultProfile</span></span>
<span data-ttu-id="5532d-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5532d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5532d-122">-설명</span><span class="sxs-lookup"><span data-stu-id="5532d-122">-Description</span></span>
<span data-ttu-id="5532d-123">변수에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-123">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5532d-124">암호화 된</span><span class="sxs-lookup"><span data-stu-id="5532d-124">-Encrypted</span></span>
<span data-ttu-id="5532d-125">이 cmdlet이 저장소의 변수 값을 암호화할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5532d-126">-이름</span><span class="sxs-lookup"><span data-stu-id="5532d-126">-Name</span></span>
<span data-ttu-id="5532d-127">변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-127">Specifies a name for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5532d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5532d-128">-ResourceGroupName</span></span>
<span data-ttu-id="5532d-129">이 cmdlet이 변수를 만드는 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="5532d-130">-값</span><span class="sxs-lookup"><span data-stu-id="5532d-130">-Value</span></span>
<span data-ttu-id="5532d-131">변수의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-131">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5532d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5532d-132">CommonParameters</span></span>
<span data-ttu-id="5532d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5532d-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5532d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5532d-135">입력</span><span class="sxs-lookup"><span data-stu-id="5532d-135">INPUTS</span></span>

### <span data-ttu-id="5532d-136">않아야</span><span class="sxs-lookup"><span data-stu-id="5532d-136">None</span></span>
<span data-ttu-id="5532d-137">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5532d-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5532d-138">출력</span><span class="sxs-lookup"><span data-stu-id="5532d-138">OUTPUTS</span></span>

### <span data-ttu-id="5532d-139">Microsoft. Azure. m a. 모델 변수</span><span class="sxs-lookup"><span data-stu-id="5532d-139">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="5532d-140">상속자</span><span class="sxs-lookup"><span data-stu-id="5532d-140">NOTES</span></span>

## <span data-ttu-id="5532d-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5532d-141">RELATED LINKS</span></span>

[<span data-ttu-id="5532d-142">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5532d-142">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="5532d-143">제거-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5532d-143">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="5532d-144">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5532d-144">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


