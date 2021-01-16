---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: 0ca1e99b68f7cca8d39647357ee81770ea41cefc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494209"
---
# <span data-ttu-id="f4f35-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f4f35-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="f4f35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4f35-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f35-103">Automation 변수를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f35-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="f4f35-104">구문</span><span class="sxs-lookup"><span data-stu-id="f4f35-104">SYNTAX</span></span>

### <span data-ttu-id="f4f35-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="f4f35-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4f35-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="f4f35-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4f35-107">설명</span><span class="sxs-lookup"><span data-stu-id="f4f35-107">DESCRIPTION</span></span>
<span data-ttu-id="f4f35-108">**Set-AzAutomationVariable** cmdlet은 Azure Automation에서 변수의 값 또는 설명을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f35-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="f4f35-109">변수를 암호화하기 위해 Encrypted 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="f4f35-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="f4f35-110">변수를 생성한 후 암호화된 상태를 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f35-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="f4f35-111">암호화되지  않은 기존 변수에 대해 암호화를 지정하는 데 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f35-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="f4f35-112">예제</span><span class="sxs-lookup"><span data-stu-id="f4f35-112">EXAMPLES</span></span>

### <span data-ttu-id="f4f35-113">예제 1: 변수 값 설정</span><span class="sxs-lookup"><span data-stu-id="f4f35-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="f4f35-114">이 명령은 Contoso17이라는 Azure Automation 계정에서 StringVariable22라는 변수에 대한 새 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f35-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f4f35-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4f35-115">PARAMETERS</span></span>

### <span data-ttu-id="f4f35-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f4f35-116">-AutomationAccountName</span></span>
<span data-ttu-id="f4f35-117">변수가 저장되는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f35-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="f4f35-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f35-118">-DefaultProfile</span></span>
<span data-ttu-id="f4f35-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f4f35-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4f35-120">-Description</span><span class="sxs-lookup"><span data-stu-id="f4f35-120">-Description</span></span>
<span data-ttu-id="f4f35-121">변수에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f35-121">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVariableDescription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4f35-122">-Encrypted</span><span class="sxs-lookup"><span data-stu-id="f4f35-122">-Encrypted</span></span>
<span data-ttu-id="f4f35-123">cmdlet이 저장소에 대한 변수 값을 암호화할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f35-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4f35-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f4f35-124">-Name</span></span>
<span data-ttu-id="f4f35-125">이 cmdlet이 수정하는 변수의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f35-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f4f35-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4f35-126">-ResourceGroupName</span></span>
<span data-ttu-id="f4f35-127">이 cmdlet이 변수를 수정하는 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f35-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="f4f35-128">-Value</span><span class="sxs-lookup"><span data-stu-id="f4f35-128">-Value</span></span>
<span data-ttu-id="f4f35-129">변수에 대한 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f35-129">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4f35-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f35-130">CommonParameters</span></span>
<span data-ttu-id="f4f35-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f35-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f35-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f4f35-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f35-133">입력</span><span class="sxs-lookup"><span data-stu-id="f4f35-133">INPUTS</span></span>

### <span data-ttu-id="f4f35-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f4f35-134">System.String</span></span>

### <span data-ttu-id="f4f35-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f4f35-135">System.Boolean</span></span>

### <span data-ttu-id="f4f35-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="f4f35-136">System.Object</span></span>

## <span data-ttu-id="f4f35-137">출력</span><span class="sxs-lookup"><span data-stu-id="f4f35-137">OUTPUTS</span></span>

### <span data-ttu-id="f4f35-138">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="f4f35-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="f4f35-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f4f35-139">NOTES</span></span>

## <span data-ttu-id="f4f35-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4f35-140">RELATED LINKS</span></span>

[<span data-ttu-id="f4f35-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f4f35-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="f4f35-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f4f35-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="f4f35-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f4f35-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


