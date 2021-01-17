---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
ms.openlocfilehash: 53fa3d21089b150a7436311597a88e827f391562
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368362"
---
# <span data-ttu-id="c75e1-101">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c75e1-101">Set-AzLogicApp</span></span>

## <span data-ttu-id="c75e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c75e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c75e1-103">리소스 그룹의 논리 앱을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-103">Modifies a logic app in a resource group.</span></span>

## <span data-ttu-id="c75e1-104">구문</span><span class="sxs-lookup"><span data-stu-id="c75e1-104">SYNTAX</span></span>

### <span data-ttu-id="c75e1-105">소비(기본값)</span><span class="sxs-lookup"><span data-stu-id="c75e1-105">Consumption (Default)</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c75e1-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="c75e1-106">HostingPlan</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c75e1-107">설명</span><span class="sxs-lookup"><span data-stu-id="c75e1-107">DESCRIPTION</span></span>
<span data-ttu-id="c75e1-108">**Set-AzLogicApp** cmdlet은 Logic Apps 기능을 사용하여 논리 앱을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-108">The **Set-AzLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="c75e1-109">논리 앱은 논리 앱 정의에 정의된 작업 또는 트리거의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="c75e1-110">이 cmdlet은 **워크플로** 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="c75e1-111">이름, 위치, 논리 앱 정의, 리소스 그룹 및 계획을 지정하여 논리 앱을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="c75e1-112">논리 앱 정의 및 매개 변수는 JSON(JavaScript Object Notation)으로 형식이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="c75e1-113">논리 앱을 정의 및 매개 변수에 대한 템플릿으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="c75e1-114">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c75e1-115">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c75e1-116">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c75e1-117">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="c75e1-118">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="c75e1-119">예제</span><span class="sxs-lookup"><span data-stu-id="c75e1-119">EXAMPLES</span></span>

### <span data-ttu-id="c75e1-120">예제 1: 논리 앱 수정</span><span class="sxs-lookup"><span data-stu-id="c75e1-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp1
Name                         : LogicApp17
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp17
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
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan17
Version                      : 08587489107859952120
```

<span data-ttu-id="c75e1-121">이 명령은 논리 앱을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="c75e1-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c75e1-122">PARAMETERS</span></span>

### <span data-ttu-id="c75e1-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c75e1-123">-AppServicePlan</span></span>
<span data-ttu-id="c75e1-124">계획의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-124">Specifies the name of a plan.</span></span>

```yaml
Type: System.String
Parameter Sets: HostingPlan
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c75e1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c75e1-125">-DefaultProfile</span></span>
<span data-ttu-id="c75e1-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c75e1-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c75e1-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="c75e1-127">-Definition</span></span>
<span data-ttu-id="c75e1-128">JSON(JavaScript Object Notation) 형식의 개체 또는 문자열로 논리 앱의 정의를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="c75e1-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="c75e1-129">-DefinitionFilePath</span></span>
<span data-ttu-id="c75e1-130">논리 앱의 정의를 JSON 형식의 정의 파일의 경로로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="c75e1-131">-Force</span><span class="sxs-lookup"><span data-stu-id="c75e1-131">-Force</span></span>
<span data-ttu-id="c75e1-132">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-132">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c75e1-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="c75e1-133">-IntegrationAccountId</span></span>
<span data-ttu-id="c75e1-134">논리 앱에 대한 통합 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-134">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="c75e1-135">-Name</span><span class="sxs-lookup"><span data-stu-id="c75e1-135">-Name</span></span>
<span data-ttu-id="c75e1-136">논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-136">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="c75e1-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="c75e1-137">-ParameterFilePath</span></span>
<span data-ttu-id="c75e1-138">JSON 형식 매개 변수 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-138">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="c75e1-139">-Parameters</span><span class="sxs-lookup"><span data-stu-id="c75e1-139">-Parameters</span></span>
<span data-ttu-id="c75e1-140">논리 앱에 대한 매개 변수 컬렉션 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="c75e1-141">해시 테이블, 사전 \<string\> 또는 사전을 \<string, WorkflowParameter\> 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="c75e1-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c75e1-142">-ResourceGroupName</span></span>
<span data-ttu-id="c75e1-143">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-143">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c75e1-144">-State</span><span class="sxs-lookup"><span data-stu-id="c75e1-144">-State</span></span>
<span data-ttu-id="c75e1-145">논리 앱의 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="c75e1-146">이 매개 변수에 허용되는 값은 Enabled 및 Disabled입니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="c75e1-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="c75e1-147">-UseConsumptionModel</span></span>
<span data-ttu-id="c75e1-148">논리 앱 청구에서 사용량 기반 모델을 사용 중입니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-148">Indicates that the logic app billing use the consumption based model.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c75e1-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c75e1-149">-Confirm</span></span>
<span data-ttu-id="c75e1-150">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c75e1-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c75e1-151">-WhatIf</span></span>
<span data-ttu-id="c75e1-152">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c75e1-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c75e1-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c75e1-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c75e1-154">CommonParameters</span></span>
<span data-ttu-id="c75e1-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c75e1-156">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c75e1-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c75e1-157">입력</span><span class="sxs-lookup"><span data-stu-id="c75e1-157">INPUTS</span></span>

### <span data-ttu-id="c75e1-158">System.String</span><span class="sxs-lookup"><span data-stu-id="c75e1-158">System.String</span></span>

## <span data-ttu-id="c75e1-159">출력</span><span class="sxs-lookup"><span data-stu-id="c75e1-159">OUTPUTS</span></span>

### <span data-ttu-id="c75e1-160">System.Object</span><span class="sxs-lookup"><span data-stu-id="c75e1-160">System.Object</span></span>

## <span data-ttu-id="c75e1-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c75e1-161">NOTES</span></span>

## <span data-ttu-id="c75e1-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c75e1-162">RELATED LINKS</span></span>

[<span data-ttu-id="c75e1-163">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c75e1-163">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="c75e1-164">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c75e1-164">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="c75e1-165">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c75e1-165">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="c75e1-166">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c75e1-166">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


