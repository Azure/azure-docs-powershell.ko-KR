---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
ms.openlocfilehash: d60897564843c403f5502da22e2f7a7122b1f841
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538147"
---
# <span data-ttu-id="93f6c-101">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="93f6c-101">Set-AzureRmLogicApp</span></span>

## <span data-ttu-id="93f6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="93f6c-103">리소스 그룹의 논리 앱을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-103">Modifies a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93f6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93f6c-104">SYNTAX</span></span>

### <span data-ttu-id="93f6c-105">소비량 (기본값)</span><span class="sxs-lookup"><span data-stu-id="93f6c-105">Consumption (Default)</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93f6c-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="93f6c-106">HostingPlan</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93f6c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="93f6c-107">DESCRIPTION</span></span>
<span data-ttu-id="93f6c-108">**AzureRmLogicApp** Cmdlet은 로직 앱 기능을 사용 하 여 논리 앱을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-108">The **Set-AzureRmLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="93f6c-109">논리 앱은 논리 앱 정의에 정의 된 작업 또는 트리거의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="93f6c-110">이 cmdlet은 **워크플로** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="93f6c-111">이름, 위치, 논리 앱 정의, 리소스 그룹 및 계획을 지정 하 여 논리 앱을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="93f6c-112">논리 앱 정의 및 매개 변수는 JSON (JavaScript 개체 표기법)으로 서식이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="93f6c-113">논리 앱을 정의 및 매개 변수에 대 한 템플릿으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="93f6c-114">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="93f6c-115">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="93f6c-116">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="93f6c-117">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="93f6c-118">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="93f6c-119">예제의</span><span class="sxs-lookup"><span data-stu-id="93f6c-119">EXAMPLES</span></span>

### <span data-ttu-id="93f6c-120">예제 1: 논리 앱 수정</span><span class="sxs-lookup"><span data-stu-id="93f6c-120">Example 1: Modify a logic app</span></span>
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

<span data-ttu-id="93f6c-121">이 명령은 논리 앱을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="93f6c-122">변수</span><span class="sxs-lookup"><span data-stu-id="93f6c-122">PARAMETERS</span></span>

### <span data-ttu-id="93f6c-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93f6c-123">-AppServicePlan</span></span>
<span data-ttu-id="93f6c-124">계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-124">Specifies the name of a plan.</span></span>

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

### <span data-ttu-id="93f6c-125">-정의</span><span class="sxs-lookup"><span data-stu-id="93f6c-125">-Definition</span></span>
<span data-ttu-id="93f6c-126">논리 앱의 정의를 개체 또는 JSON (JavaScript 개체 표시법) 형식의 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-126">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="93f6c-127">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="93f6c-127">-DefinitionFilePath</span></span>
<span data-ttu-id="93f6c-128">논리 앱의 정의를 JSON 형식의 정의 파일 경로로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-128">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="93f6c-129">-Force</span><span class="sxs-lookup"><span data-stu-id="93f6c-129">-Force</span></span>
<span data-ttu-id="93f6c-130">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93f6c-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="93f6c-131">-IntegrationAccountId</span></span>
<span data-ttu-id="93f6c-132">논리 앱의 통합 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="93f6c-133">-이름</span><span class="sxs-lookup"><span data-stu-id="93f6c-133">-Name</span></span>
<span data-ttu-id="93f6c-134">논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-134">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="93f6c-135">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="93f6c-135">-ParameterFilePath</span></span>
<span data-ttu-id="93f6c-136">JSON 형식의 매개 변수 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-136">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="93f6c-137">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="93f6c-137">-Parameters</span></span>
<span data-ttu-id="93f6c-138">논리 앱에 대 한 parameters 컬렉션 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-138">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="93f6c-139">해시 테이블, 사전 \<string\> 또는 사전을 지정 \<string, WorkflowParameter\> 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-139">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="93f6c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93f6c-140">-ResourceGroupName</span></span>
<span data-ttu-id="93f6c-141">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-141">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="93f6c-142">-상태</span><span class="sxs-lookup"><span data-stu-id="93f6c-142">-State</span></span>
<span data-ttu-id="93f6c-143">논리 앱의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-143">Specifies the state of the logic app.</span></span>
<span data-ttu-id="93f6c-144">이 매개 변수에 허용 되는 값은 사용 및 사용 안 함입니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-144">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="93f6c-145">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="93f6c-145">-UseConsumptionModel</span></span>
<span data-ttu-id="93f6c-146">논리 앱 청구에서 소비 기반 모델을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-146">Indicates that the logic app billing use the consumption based model.</span></span>

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

### <span data-ttu-id="93f6c-147">-확인</span><span class="sxs-lookup"><span data-stu-id="93f6c-147">-Confirm</span></span>
<span data-ttu-id="93f6c-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93f6c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93f6c-149">-WhatIf</span></span>
<span data-ttu-id="93f6c-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93f6c-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93f6c-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f6c-152">-DefaultProfile</span></span>
<span data-ttu-id="93f6c-153">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93f6c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f6c-154">CommonParameters</span></span>
<span data-ttu-id="93f6c-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f6c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f6c-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93f6c-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f6c-157">입력</span><span class="sxs-lookup"><span data-stu-id="93f6c-157">INPUTS</span></span>

## <span data-ttu-id="93f6c-158">출력</span><span class="sxs-lookup"><span data-stu-id="93f6c-158">OUTPUTS</span></span>

### <span data-ttu-id="93f6c-159">Microsoft. Azure. 관리 워크플로</span><span class="sxs-lookup"><span data-stu-id="93f6c-159">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="93f6c-160">상속자</span><span class="sxs-lookup"><span data-stu-id="93f6c-160">NOTES</span></span>

## <span data-ttu-id="93f6c-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93f6c-161">RELATED LINKS</span></span>

[<span data-ttu-id="93f6c-162">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="93f6c-162">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="93f6c-163">새로운 AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="93f6c-163">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="93f6c-164">제거-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="93f6c-164">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="93f6c-165">시작-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="93f6c-165">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


