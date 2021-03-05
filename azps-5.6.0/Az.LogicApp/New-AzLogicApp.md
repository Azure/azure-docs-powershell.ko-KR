---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 98fb733f661d4d1c5a6c50ce472005763584a72c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968955"
---
# <span data-ttu-id="4b7ed-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4b7ed-101">New-AzLogicApp</span></span>

## <span data-ttu-id="4b7ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b7ed-102">SYNOPSIS</span></span>
<span data-ttu-id="4b7ed-103">리소스 그룹에 논리 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="4b7ed-104">구문</span><span class="sxs-lookup"><span data-stu-id="4b7ed-104">SYNTAX</span></span>

### <span data-ttu-id="4b7ed-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b7ed-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7ed-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b7ed-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b7ed-107">설명</span><span class="sxs-lookup"><span data-stu-id="4b7ed-107">DESCRIPTION</span></span>
<span data-ttu-id="4b7ed-108">**New-AzLogicApp** cmdlet은 Logic Apps 기능을 사용하여 논리 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="4b7ed-109">논리 앱은 Logic App 정의에 정의된 작업 또는 트리거의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="4b7ed-110">이 cmdlet은 **워크플로** 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="4b7ed-111">이름, 위치, 논리 앱 정의, 리소스 그룹 및 계획을 지정하여 논리 앱을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="4b7ed-112">논리 앱 정의 및 매개 변수는 JSON(JavaScript 개체 표시)에 서식이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="4b7ed-113">논리 앱을 정의 및 매개 변수에 대한 템플릿으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="4b7ed-114">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4b7ed-115">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4b7ed-116">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4b7ed-117">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="4b7ed-118">명령줄에서 지정한 템플릿 매개 변수 파일 값은 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="4b7ed-119">예제</span><span class="sxs-lookup"><span data-stu-id="4b7ed-119">EXAMPLES</span></span>

### <span data-ttu-id="4b7ed-120">예제 1: 정의 및 매개 변수 파일 경로를 사용하여 논리 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="4b7ed-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
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

<span data-ttu-id="4b7ed-121">이 명령은 지정된 리소스 그룹에 논리 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="4b7ed-122">논리 앱에는 파일 경로에 의해 지정된 정의 및 매개 변수가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="4b7ed-123">예제 2: 정의 및 매개 변수 개체를 사용하여 논리 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="4b7ed-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
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

<span data-ttu-id="4b7ed-124">이 명령은 지정된 리소스 그룹 리소스 그룹에 논리 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="4b7ed-125">예제 3: 파이프라인을 사용하여 리소스 그룹을 지정하여 논리 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="4b7ed-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
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

<span data-ttu-id="4b7ed-126">이 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="4b7ed-127">명령은 파이프라인 연산자를 사용하여 현재 cmdlet에 리소스 그룹을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4b7ed-128">현재 cmdlet은 리소스 그룹에 논리 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="4b7ed-129">논리 앱에는 파일 경로에 의해 지정된 정의 및 매개 변수가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="4b7ed-130">예제 4: 기존 논리 앱을 기반으로 논리 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="4b7ed-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
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

<span data-ttu-id="4b7ed-131">첫 번째 명령은 Get-AzLogicApp cmdlet을 사용하여 LogicApp03이라는 논리 앱을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="4b7ed-132">명령은 논리 앱을 $Workflow 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="4b7ed-133">두 번째 명령은 에 저장된 논리 앱의 정의 및 매개 변수를 사용하는 새 논리 앱을 $Workflow.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="4b7ed-134">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4b7ed-134">PARAMETERS</span></span>

### <span data-ttu-id="4b7ed-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b7ed-135">-DefaultProfile</span></span>
<span data-ttu-id="4b7ed-136">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4b7ed-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b7ed-137">-Definition</span><span class="sxs-lookup"><span data-stu-id="4b7ed-137">-Definition</span></span>
<span data-ttu-id="4b7ed-138">논리 앱에 대한 정의를 개체 또는 JSON(JavaScript 개체 표기)형식으로 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7ed-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="4b7ed-139">-DefinitionFilePath</span></span>
<span data-ttu-id="4b7ed-140">논리 앱의 정의를 JSON 형식의 정의 파일의 경로로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7ed-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="4b7ed-141">-IntegrationAccountId</span></span>
<span data-ttu-id="4b7ed-142">논리 앱에 대한 통합 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-142">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="4b7ed-143">-Location</span><span class="sxs-lookup"><span data-stu-id="4b7ed-143">-Location</span></span>
<span data-ttu-id="4b7ed-144">논리 앱의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="4b7ed-145">미국 서부 또는 동남 아시아와 같은 Azure 데이터 센터 위치를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="4b7ed-146">논리 앱을 모든 위치에 위치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-146">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="4b7ed-147">-Name</span><span class="sxs-lookup"><span data-stu-id="4b7ed-147">-Name</span></span>
<span data-ttu-id="4b7ed-148">논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-148">Specifies the name for the logic app.</span></span>

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

### <span data-ttu-id="4b7ed-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="4b7ed-149">-ParameterFilePath</span></span>
<span data-ttu-id="4b7ed-150">JSON 형식 매개 변수 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-150">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="4b7ed-151">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="4b7ed-151">-Parameters</span></span>
<span data-ttu-id="4b7ed-152">Logic App에 대한 매개 변수 컬렉션 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="4b7ed-153">해시 테이블, 사전 \<string\> 또는 \<string, WorkflowParameter\> 사전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="4b7ed-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b7ed-154">-ResourceGroupName</span></span>
<span data-ttu-id="4b7ed-155">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-155">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4b7ed-156">-State</span><span class="sxs-lookup"><span data-stu-id="4b7ed-156">-State</span></span>
<span data-ttu-id="4b7ed-157">논리 앱의 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="4b7ed-158">이 매개 변수에 대해 허용되는 값은 사용 및 사용 안 하다입니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="4b7ed-159">-확인</span><span class="sxs-lookup"><span data-stu-id="4b7ed-159">-Confirm</span></span>
<span data-ttu-id="4b7ed-160">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b7ed-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b7ed-161">-WhatIf</span></span>
<span data-ttu-id="4b7ed-162">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b7ed-163">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b7ed-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b7ed-164">CommonParameters</span></span>
<span data-ttu-id="4b7ed-165">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b7ed-166">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4b7ed-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b7ed-167">입력</span><span class="sxs-lookup"><span data-stu-id="4b7ed-167">INPUTS</span></span>

### <span data-ttu-id="4b7ed-168">System.String</span><span class="sxs-lookup"><span data-stu-id="4b7ed-168">System.String</span></span>

## <span data-ttu-id="4b7ed-169">출력</span><span class="sxs-lookup"><span data-stu-id="4b7ed-169">OUTPUTS</span></span>

### <span data-ttu-id="4b7ed-170">System.Object</span><span class="sxs-lookup"><span data-stu-id="4b7ed-170">System.Object</span></span>

## <span data-ttu-id="4b7ed-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b7ed-171">NOTES</span></span>

## <span data-ttu-id="4b7ed-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b7ed-172">RELATED LINKS</span></span>

[<span data-ttu-id="4b7ed-173">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4b7ed-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="4b7ed-174">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4b7ed-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="4b7ed-175">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4b7ed-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="4b7ed-176">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4b7ed-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


