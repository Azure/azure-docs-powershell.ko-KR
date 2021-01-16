---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 34f09ca41326b2f6686a41cdeba0910317bc7a2c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344306"
---
# <span data-ttu-id="f6be0-101">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f6be0-101">Start-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="f6be0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6be0-102">SYNOPSIS</span></span>
<span data-ttu-id="f6be0-103">Automation에서 DSC 구성을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-103">Compiles a DSC configuration in Automation.</span></span>

## <span data-ttu-id="f6be0-104">구문</span><span class="sxs-lookup"><span data-stu-id="f6be0-104">SYNTAX</span></span>

```
Start-AzAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6be0-105">설명</span><span class="sxs-lookup"><span data-stu-id="f6be0-105">DESCRIPTION</span></span>
<span data-ttu-id="f6be0-106">**Start-AzAutomationDscCompilationJob** cmdlet은 Azure Automation에서 APS DSC(Desired State Configuration) 구성을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-106">The **Start-AzAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="f6be0-107">예제</span><span class="sxs-lookup"><span data-stu-id="f6be0-107">EXAMPLES</span></span>

### <span data-ttu-id="f6be0-108">예제 1: Automation에서 Azure DSC 구성 컴파일</span><span class="sxs-lookup"><span data-stu-id="f6be0-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f6be0-109">첫 번째 명령은 매개 변수의 사전을 만들고 매개 변수에 $Params 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="f6be0-110">두 번째 명령은 Config01이라는 DSC 구성을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="f6be0-111">이 명령은 DSC 구성 매개 변수에 대한 $Params 값을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="f6be0-112">예제 2: 새 노드 구성 빌드 버전을 사용하여 Automation에서 Azure DSC 구성을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="f6be0-113">첫 번째 예제와 마찬가지로 첫 번째 명령은 매개 변수 사전을 만들고 매개 변수의 $Params 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="f6be0-114">두 번째 명령은 Config01이라는 DSC 구성을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="f6be0-115">이 명령은 DSC 구성 매개 변수에 대한 $Params 값을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-115">The command includes the values in $Params for DSC configuration parameters.</span></span>
<span data-ttu-id="f6be0-116">Config01[<2 /> 이름으로 새 노드 구성을 만들어서 이전의 기존 노드 구성을>. <NodeName></span><span class="sxs-lookup"><span data-stu-id="f6be0-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="f6be0-117">버전 번호는 이미 있는 기존 버전 번호에 따라 증분됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="f6be0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6be0-118">PARAMETERS</span></span>

### <span data-ttu-id="f6be0-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f6be0-119">-AutomationAccountName</span></span>
<span data-ttu-id="f6be0-120">이 cmdlet이 컴파일하는 DSC 구성을 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="f6be0-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="f6be0-121">-ConfigurationData</span></span>
<span data-ttu-id="f6be0-122">DSC 구성에 대한 구성 데이터의 사전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6be0-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f6be0-123">-ConfigurationName</span></span>
<span data-ttu-id="f6be0-124">이 cmdlet이 컴파일하는 DSC 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6be0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6be0-125">-DefaultProfile</span></span>
<span data-ttu-id="f6be0-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f6be0-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6be0-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="f6be0-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="f6be0-128">새 노드 구성 빌드 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-128">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6be0-129">-Parameters</span><span class="sxs-lookup"><span data-stu-id="f6be0-129">-Parameters</span></span>
<span data-ttu-id="f6be0-130">이 cmdlet이 DSC 구성을 컴파일하는 데 사용하는 매개 변수 사전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6be0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6be0-131">-ResourceGroupName</span></span>
<span data-ttu-id="f6be0-132">이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="f6be0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6be0-133">-Confirm</span></span>
<span data-ttu-id="f6be0-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6be0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6be0-135">-WhatIf</span></span>
<span data-ttu-id="f6be0-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f6be0-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6be0-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6be0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6be0-138">CommonParameters</span></span>
<span data-ttu-id="f6be0-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6be0-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f6be0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6be0-141">입력</span><span class="sxs-lookup"><span data-stu-id="f6be0-141">INPUTS</span></span>

### <span data-ttu-id="f6be0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f6be0-142">System.String</span></span>

## <span data-ttu-id="f6be0-143">출력</span><span class="sxs-lookup"><span data-stu-id="f6be0-143">OUTPUTS</span></span>

### <span data-ttu-id="f6be0-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="f6be0-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="f6be0-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f6be0-145">NOTES</span></span>

## <span data-ttu-id="f6be0-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6be0-146">RELATED LINKS</span></span>

[<span data-ttu-id="f6be0-147">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f6be0-147">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="f6be0-148">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="f6be0-148">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)


