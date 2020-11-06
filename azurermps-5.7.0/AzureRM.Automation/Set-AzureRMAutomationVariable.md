---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
ms.openlocfilehash: 7426f49d94e82865163320fecd85704aeeff14b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531782"
---
# <span data-ttu-id="c9c45-101">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c9c45-101">Set-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="c9c45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9c45-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c45-103">자동화 변수를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c45-103">Modifies an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9c45-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9c45-104">SYNTAX</span></span>

### <span data-ttu-id="c9c45-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="c9c45-105">UpdateVariableValue</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9c45-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="c9c45-106">UpdateVariableDescription</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9c45-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c9c45-107">DESCRIPTION</span></span>
<span data-ttu-id="c9c45-108">**AzureRmAutomationVariable** Cmdlet은 Azure Automation에서 변수의 값 또는 설명을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c45-108">The **Set-AzureRmAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="c9c45-109">변수를 암호화 하려면 *암호화* 된 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c45-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="c9c45-110">생성 후 변수의 암호화 된 상태를 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c9c45-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="c9c45-111">암호화 되지 않은 기존 변수에 대해 *암호화* 를 지정 하면 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c45-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="c9c45-112">예제의</span><span class="sxs-lookup"><span data-stu-id="c9c45-112">EXAMPLES</span></span>

### <span data-ttu-id="c9c45-113">예제 1: 변수 값 설정</span><span class="sxs-lookup"><span data-stu-id="c9c45-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="c9c45-114">이 명령은 Contoso17 이라는 Azure Automation 계정의 StringVariable22 라는 변수에 대해 새 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c45-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="c9c45-115">변수</span><span class="sxs-lookup"><span data-stu-id="c9c45-115">PARAMETERS</span></span>

### <span data-ttu-id="c9c45-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c9c45-116">-AutomationAccountName</span></span>
<span data-ttu-id="c9c45-117">변수가 저장 된 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c45-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="c9c45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c45-118">-DefaultProfile</span></span>
<span data-ttu-id="c9c45-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c9c45-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9c45-120">-설명</span><span class="sxs-lookup"><span data-stu-id="c9c45-120">-Description</span></span>
<span data-ttu-id="c9c45-121">변수에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c45-121">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: UpdateVariableDescription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c45-122">암호화 된</span><span class="sxs-lookup"><span data-stu-id="c9c45-122">-Encrypted</span></span>
<span data-ttu-id="c9c45-123">Cmdlet이 저장소의 변수 값을 암호화할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c45-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c45-124">-이름</span><span class="sxs-lookup"><span data-stu-id="c9c45-124">-Name</span></span>
<span data-ttu-id="c9c45-125">이 cmdlet이 수정 하는 변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c45-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c9c45-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9c45-126">-ResourceGroupName</span></span>
<span data-ttu-id="c9c45-127">이 cmdlet이 변수를 수정할 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c45-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="c9c45-128">-값</span><span class="sxs-lookup"><span data-stu-id="c9c45-128">-Value</span></span>
<span data-ttu-id="c9c45-129">변수의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c45-129">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c45-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c45-130">CommonParameters</span></span>
<span data-ttu-id="c9c45-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c45-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c45-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9c45-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c45-133">입력</span><span class="sxs-lookup"><span data-stu-id="c9c45-133">INPUTS</span></span>

### <span data-ttu-id="c9c45-134">않아야</span><span class="sxs-lookup"><span data-stu-id="c9c45-134">None</span></span>
<span data-ttu-id="c9c45-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9c45-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9c45-136">출력</span><span class="sxs-lookup"><span data-stu-id="c9c45-136">OUTPUTS</span></span>

### <span data-ttu-id="c9c45-137">Microsoft. Azure. m a. 모델 변수</span><span class="sxs-lookup"><span data-stu-id="c9c45-137">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="c9c45-138">상속자</span><span class="sxs-lookup"><span data-stu-id="c9c45-138">NOTES</span></span>

## <span data-ttu-id="c9c45-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9c45-139">RELATED LINKS</span></span>

[<span data-ttu-id="c9c45-140">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c9c45-140">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="c9c45-141">새로운 AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c9c45-141">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="c9c45-142">제거-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c9c45-142">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)


