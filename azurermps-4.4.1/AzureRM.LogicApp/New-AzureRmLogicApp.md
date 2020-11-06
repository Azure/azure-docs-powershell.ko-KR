---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmLogicApp.md
ms.openlocfilehash: 990423db13f13f18f10fb768ac55d2e59b4f2baf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538151"
---
# <span data-ttu-id="ee330-101">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ee330-101">New-AzureRmLogicApp</span></span>

## <span data-ttu-id="ee330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee330-102">SYNOPSIS</span></span>
<span data-ttu-id="ee330-103">리소스 그룹에 논리 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-103">Creates a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee330-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee330-104">SYNTAX</span></span>

### <span data-ttu-id="ee330-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee330-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee330-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee330-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee330-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ee330-107">DESCRIPTION</span></span>
<span data-ttu-id="ee330-108">**새 AzureRmLogicApp** Cmdlet은 논리 앱 기능을 사용 하 여 논리 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-108">The **New-AzureRmLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="ee330-109">논리 앱은 논리 앱 정의에 정의 된 작업 또는 트리거의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="ee330-110">이 cmdlet은 **워크플로** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="ee330-111">이름, 위치, 논리 앱 정의, 리소스 그룹 및 계획을 지정 하 여 논리 앱을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="ee330-112">논리 앱 정의 및 매개 변수는 JSON (JavaScript 개체 표기법)으로 서식이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="ee330-113">논리 앱을 정의 및 매개 변수에 대 한 템플릿으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="ee330-114">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ee330-115">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ee330-116">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ee330-117">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="ee330-118">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="ee330-119">예제의</span><span class="sxs-lookup"><span data-stu-id="ee330-119">EXAMPLES</span></span>

### <span data-ttu-id="ee330-120">예제 1: 정의 및 매개 변수 파일 경로를 사용 하 여 논리 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="ee330-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup1/providers/Microsoft.Logic/workflows/LogicApp1
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="ee330-121">이 명령은 지정 된 리소스 그룹에 논리 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="ee330-122">논리 앱에는 파일 경로로 지정 된 정의 및 매개 변수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="ee330-123">예제 2: 정의 및 매개 변수 개체를 사용 하 여 논리 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="ee330-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp05
Name                         : LogicApp05
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp05
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan1
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="ee330-124">이 명령은 지정 된 리소스 그룹 리소스 그룹에 논리 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="ee330-125">예제 3: 파이프라인을 사용 하 여 리소스 그룹을 지정 하 여 논리 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="ee330-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzureRmLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp11
Name                         : LogicApp11
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp11
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="ee330-126">이 명령은 Get-AzureRmResourceGroup cmdlet을 사용 하 여 ResourceGroup11 라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-126">This command gets the resource group named ResourceGroup11 by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="ee330-127">이 명령은 파이프라인 연산자를 사용 하 여 해당 리소스 그룹을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ee330-128">현재 cmdlet은 해당 리소스 그룹에 논리 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="ee330-129">논리 앱에는 파일 경로로 지정 된 정의 및 매개 변수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="ee330-130">예제 4: 기존 논리 앱을 기반으로 논리 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="ee330-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp13
Name                         : LogicApp13
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp13
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="ee330-131">첫 번째 명령은 Get-AzureRmLogicApp cmdlet을 사용 하 여 LogicApp03 이라는 논리 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-131">The first command gets the logic app named LogicApp03 by using the Get-AzureRmLogicApp cmdlet.</span></span>
<span data-ttu-id="ee330-132">이 명령은 논리 앱을 $Workflow 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-132">The command stores the logic app in the $Workflow variable.</span></span>

<span data-ttu-id="ee330-133">두 번째 명령은 $Workflow에 저장 된 논리 앱의 정의 및 매개 변수를 사용 하는 새 논리 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="ee330-134">변수</span><span class="sxs-lookup"><span data-stu-id="ee330-134">PARAMETERS</span></span>

### <span data-ttu-id="ee330-135">-정의</span><span class="sxs-lookup"><span data-stu-id="ee330-135">-Definition</span></span>
<span data-ttu-id="ee330-136">응용 프로그램에 대 한 정의를 개체 또는 JSON (JavaScript Object Notataion) 형식의 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-136">Specifies the definition for your logic app as an object or a string in JavaScript Object Notataion (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee330-137">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="ee330-137">-DefinitionFilePath</span></span>
<span data-ttu-id="ee330-138">논리 앱의 정의를 JSON 형식의 정의 파일 경로로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-138">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee330-139">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="ee330-139">-IntegrationAccountId</span></span>
<span data-ttu-id="ee330-140">논리 앱의 통합 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-140">Specifies an integration account ID for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee330-141">-위치</span><span class="sxs-lookup"><span data-stu-id="ee330-141">-Location</span></span>
<span data-ttu-id="ee330-142">논리 앱의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-142">Specifies the location of the logic app.</span></span>
<span data-ttu-id="ee330-143">Azure 데이터 센터 위치 (예: 서쪽 미국 또는 동남 아시아)를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-143">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="ee330-144">임의의 위치에 논리 앱을 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-144">You can place a logic app in any location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee330-145">-이름</span><span class="sxs-lookup"><span data-stu-id="ee330-145">-Name</span></span>
<span data-ttu-id="ee330-146">논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-146">Specifies the name for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee330-147">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="ee330-147">-ParameterFilePath</span></span>
<span data-ttu-id="ee330-148">JSON 형식의 매개 변수 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-148">Specifies the path of a JSON formatted parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee330-149">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="ee330-149">-Parameters</span></span>
<span data-ttu-id="ee330-150">논리 앱에 대 한 parameters 컬렉션 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-150">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="ee330-151">해시 테이블, 사전 \<string\> 또는 사전을 지정 \<string, WorkflowParameter\> 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-151">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee330-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee330-152">-ResourceGroupName</span></span>
<span data-ttu-id="ee330-153">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-153">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee330-154">-상태</span><span class="sxs-lookup"><span data-stu-id="ee330-154">-State</span></span>
<span data-ttu-id="ee330-155">논리 앱의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-155">Specifies the state of the logic app.</span></span>
<span data-ttu-id="ee330-156">이 매개 변수에 허용 되는 값은 사용 및 사용 안 함입니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-156">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee330-157">-확인</span><span class="sxs-lookup"><span data-stu-id="ee330-157">-Confirm</span></span>
<span data-ttu-id="ee330-158">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee330-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee330-159">-WhatIf</span></span>
<span data-ttu-id="ee330-160">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee330-161">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-161">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee330-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee330-162">-DefaultProfile</span></span>
<span data-ttu-id="ee330-163">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-163">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee330-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee330-164">CommonParameters</span></span>
<span data-ttu-id="ee330-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee330-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee330-166">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee330-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee330-167">입력</span><span class="sxs-lookup"><span data-stu-id="ee330-167">INPUTS</span></span>

### <span data-ttu-id="ee330-168">않아야</span><span class="sxs-lookup"><span data-stu-id="ee330-168">None</span></span>

## <span data-ttu-id="ee330-169">출력</span><span class="sxs-lookup"><span data-stu-id="ee330-169">OUTPUTS</span></span>

### <span data-ttu-id="ee330-170">Microsoft. Azure. 관리 워크플로</span><span class="sxs-lookup"><span data-stu-id="ee330-170">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="ee330-171">상속자</span><span class="sxs-lookup"><span data-stu-id="ee330-171">NOTES</span></span>

## <span data-ttu-id="ee330-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee330-172">RELATED LINKS</span></span>

[<span data-ttu-id="ee330-173">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ee330-173">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="ee330-174">제거-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ee330-174">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="ee330-175">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ee330-175">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="ee330-176">시작-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ee330-176">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


