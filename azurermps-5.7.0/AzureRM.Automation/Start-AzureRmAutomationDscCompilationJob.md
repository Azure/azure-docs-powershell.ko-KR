---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 790a0f0383796728b4754c4d64d98ef2ca7ed3c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529037"
---
# <span data-ttu-id="e6cfe-101">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="e6cfe-101">Start-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="e6cfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6cfe-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cfe-103">자동화에서 DSC 구성을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-103">Compiles a DSC configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6cfe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6cfe-104">SYNTAX</span></span>

```
Start-AzureRmAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6cfe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e6cfe-105">DESCRIPTION</span></span>
<span data-ttu-id="e6cfe-106">**AzureRmAutomationDscCompilationJob** Cmdlet은 Azure AUTOMATION에서 Ap (원하는 상태 구성) 구성을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-106">The **Start-AzureRmAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="e6cfe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e6cfe-107">EXAMPLES</span></span>

### <span data-ttu-id="e6cfe-108">예제 1: 자동화에서 Azure DSC 구성 컴파일</span><span class="sxs-lookup"><span data-stu-id="e6cfe-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e6cfe-109">첫 번째 명령은 매개 변수 사전을 만들어 $Params 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="e6cfe-110">두 번째 명령은 Config01 이라는 DSC 구성을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="e6cfe-111">명령에는 DSC 구성 매개 변수에 대 한 $Params 값이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="e6cfe-112">예제 2: 새 노드 구성 빌드 버전을 사용 하 여 자동화에서 Azure DSC 구성을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="e6cfe-113">첫 번째 예제와 마찬가지로 첫 번째 명령은 매개 변수 사전을 만들어 $Params 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="e6cfe-114">두 번째 명령은 Config01 이라는 DSC 구성을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="e6cfe-115">명령에는 DSC 구성 매개 변수에 대 한 $Params 값이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-115">The command includes the values in $Params for DSC configuration parameters.</span></span>

<span data-ttu-id="e6cfe-116">이름이 Config01 [<2>] 인 새 노드 구성을 만들어 이전의 기존 노드 구성을 재정의 하지 <NodeName> 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="e6cfe-117">버전 번호는 이미 존재 하는 기존 버전 번호에 따라 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="e6cfe-118">변수</span><span class="sxs-lookup"><span data-stu-id="e6cfe-118">PARAMETERS</span></span>

### <span data-ttu-id="e6cfe-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e6cfe-119">-AutomationAccountName</span></span>
<span data-ttu-id="e6cfe-120">이 cmdlet이 컴파일하는 DSC 구성을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="e6cfe-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="e6cfe-121">-ConfigurationData</span></span>
<span data-ttu-id="e6cfe-122">DSC 구성에 대 한 구성 데이터 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cfe-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e6cfe-123">-ConfigurationName</span></span>
<span data-ttu-id="e6cfe-124">이 cmdlet이 컴파일하는 DSC 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6cfe-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6cfe-125">-DefaultProfile</span></span>
<span data-ttu-id="e6cfe-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e6cfe-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6cfe-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="e6cfe-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="e6cfe-128">새 노드 구성 빌드 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-128">Creates a new Node Configuration build version.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cfe-129">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="e6cfe-129">-Parameters</span></span>
<span data-ttu-id="e6cfe-130">이 cmdlet이 DSC 구성을 컴파일하는 데 사용 하는 매개 변수 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cfe-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6cfe-131">-ResourceGroupName</span></span>
<span data-ttu-id="e6cfe-132">이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="e6cfe-133">-확인</span><span class="sxs-lookup"><span data-stu-id="e6cfe-133">-Confirm</span></span>
<span data-ttu-id="e6cfe-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cfe-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6cfe-135">-WhatIf</span></span>
<span data-ttu-id="e6cfe-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6cfe-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cfe-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cfe-138">CommonParameters</span></span>
<span data-ttu-id="e6cfe-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cfe-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6cfe-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cfe-141">입력</span><span class="sxs-lookup"><span data-stu-id="e6cfe-141">INPUTS</span></span>

### <span data-ttu-id="e6cfe-142">않아야</span><span class="sxs-lookup"><span data-stu-id="e6cfe-142">None</span></span>
<span data-ttu-id="e6cfe-143">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e6cfe-144">출력</span><span class="sxs-lookup"><span data-stu-id="e6cfe-144">OUTPUTS</span></span>

### <span data-ttu-id="e6cfe-145">CompilationJob를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-145">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="e6cfe-146">상속자</span><span class="sxs-lookup"><span data-stu-id="e6cfe-146">NOTES</span></span>

## <span data-ttu-id="e6cfe-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6cfe-147">RELATED LINKS</span></span>

[<span data-ttu-id="e6cfe-148">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="e6cfe-148">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="e6cfe-149">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="e6cfe-149">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)


