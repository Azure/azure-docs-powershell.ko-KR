---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
ms.openlocfilehash: 1f98fb17f6dc5604dfd19faeb9b9d6ec54e859c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711712"
---
# <span data-ttu-id="fab86-101">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="fab86-101">Set-AzureRmLogicApp</span></span>

## <span data-ttu-id="fab86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fab86-102">SYNOPSIS</span></span>
<span data-ttu-id="fab86-103">리소스 그룹의 논리 앱을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-103">Modifies a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fab86-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fab86-104">SYNTAX</span></span>

### <span data-ttu-id="fab86-105">소비량 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fab86-105">Consumption (Default)</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fab86-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="fab86-106">HostingPlan</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fab86-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fab86-107">DESCRIPTION</span></span>
<span data-ttu-id="fab86-108">**AzureRmLogicApp** Cmdlet은 로직 앱 기능을 사용 하 여 논리 앱을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-108">The **Set-AzureRmLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="fab86-109">논리 앱은 논리 앱 정의에 정의 된 작업 또는 트리거의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="fab86-110">이 cmdlet은 **워크플로** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="fab86-111">이름, 위치, 논리 앱 정의, 리소스 그룹 및 계획을 지정 하 여 논리 앱을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="fab86-112">논리 앱 정의 및 매개 변수는 JSON (JavaScript 개체 표기법)으로 서식이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="fab86-113">논리 앱을 정의 및 매개 변수에 대 한 템플릿으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="fab86-114">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fab86-115">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fab86-116">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fab86-117">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="fab86-118">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="fab86-119">예제의</span><span class="sxs-lookup"><span data-stu-id="fab86-119">EXAMPLES</span></span>

### <span data-ttu-id="fab86-120">예제 1: 논리 앱 수정</span><span class="sxs-lookup"><span data-stu-id="fab86-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
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

<span data-ttu-id="fab86-121">이 명령은 논리 앱을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="fab86-122">변수</span><span class="sxs-lookup"><span data-stu-id="fab86-122">PARAMETERS</span></span>

### <span data-ttu-id="fab86-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fab86-123">-AppServicePlan</span></span>
<span data-ttu-id="fab86-124">계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-124">Specifies the name of a plan.</span></span>

```yaml
Type: String
Parameter Sets: HostingPlan
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fab86-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab86-125">-DefaultProfile</span></span>
<span data-ttu-id="fab86-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fab86-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fab86-127">-정의</span><span class="sxs-lookup"><span data-stu-id="fab86-127">-Definition</span></span>
<span data-ttu-id="fab86-128">논리 앱의 정의를 개체 또는 JSON (JavaScript 개체 표시법) 형식의 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab86-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="fab86-129">-DefinitionFilePath</span></span>
<span data-ttu-id="fab86-130">논리 앱의 정의를 JSON 형식의 정의 파일 경로로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab86-131">-Force</span><span class="sxs-lookup"><span data-stu-id="fab86-131">-Force</span></span>
<span data-ttu-id="fab86-132">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-132">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab86-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="fab86-133">-IntegrationAccountId</span></span>
<span data-ttu-id="fab86-134">논리 앱의 통합 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-134">Specifies an integration account ID for the logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab86-135">-이름</span><span class="sxs-lookup"><span data-stu-id="fab86-135">-Name</span></span>
<span data-ttu-id="fab86-136">논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-136">Specifies the name of a logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab86-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="fab86-137">-ParameterFilePath</span></span>
<span data-ttu-id="fab86-138">JSON 형식의 매개 변수 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-138">Specifies the path of a JSON formatted parameter file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab86-139">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="fab86-139">-Parameters</span></span>
<span data-ttu-id="fab86-140">논리 앱에 대 한 parameters 컬렉션 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="fab86-141">해시 테이블, 사전 \<string\> 또는 사전을 지정 \<string, WorkflowParameter\> 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab86-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab86-142">-ResourceGroupName</span></span>
<span data-ttu-id="fab86-143">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-143">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fab86-144">-상태</span><span class="sxs-lookup"><span data-stu-id="fab86-144">-State</span></span>
<span data-ttu-id="fab86-145">논리 앱의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="fab86-146">이 매개 변수에 허용 되는 값은 사용 및 사용 안 함입니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab86-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="fab86-147">-UseConsumptionModel</span></span>
<span data-ttu-id="fab86-148">논리 앱 청구에서 소비 기반 모델을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-148">Indicates that the logic app billing use the consumption based model.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Consumption
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab86-149">-확인</span><span class="sxs-lookup"><span data-stu-id="fab86-149">-Confirm</span></span>
<span data-ttu-id="fab86-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab86-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab86-151">-WhatIf</span></span>
<span data-ttu-id="fab86-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fab86-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab86-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab86-154">CommonParameters</span></span>
<span data-ttu-id="fab86-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab86-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fab86-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab86-157">입력</span><span class="sxs-lookup"><span data-stu-id="fab86-157">INPUTS</span></span>

### <span data-ttu-id="fab86-158">않아야</span><span class="sxs-lookup"><span data-stu-id="fab86-158">None</span></span>
<span data-ttu-id="fab86-159">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fab86-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fab86-160">출력</span><span class="sxs-lookup"><span data-stu-id="fab86-160">OUTPUTS</span></span>

### <span data-ttu-id="fab86-161">Microsoft. Azure. 관리 워크플로</span><span class="sxs-lookup"><span data-stu-id="fab86-161">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="fab86-162">상속자</span><span class="sxs-lookup"><span data-stu-id="fab86-162">NOTES</span></span>

## <span data-ttu-id="fab86-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fab86-163">RELATED LINKS</span></span>

[<span data-ttu-id="fab86-164">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="fab86-164">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="fab86-165">새로운 AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="fab86-165">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="fab86-166">제거-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="fab86-166">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="fab86-167">시작-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="fab86-167">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


