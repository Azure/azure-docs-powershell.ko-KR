---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: a170d21a2301541f1346905ed701d477ecba4204
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362503"
---
# <span data-ttu-id="17f8b-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="17f8b-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="17f8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="17f8b-103">기존 웹 서비스 리소스의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="17f8b-104">구문</span><span class="sxs-lookup"><span data-stu-id="17f8b-104">SYNTAX</span></span>

### <span data-ttu-id="17f8b-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="17f8b-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f8b-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="17f8b-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17f8b-107">설명</span><span class="sxs-lookup"><span data-stu-id="17f8b-107">DESCRIPTION</span></span>
<span data-ttu-id="17f8b-108">Update-AzMlWebService cmdlet을 사용하면 웹 서비스의 비정적 속성을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="17f8b-109">cmdlet은 패치 작업으로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="17f8b-110">수정하려는 속성만 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="17f8b-111">예제</span><span class="sxs-lookup"><span data-stu-id="17f8b-111">EXAMPLES</span></span>

### <span data-ttu-id="17f8b-112">예제 1: 선택적 업데이트 인수</span><span class="sxs-lookup"><span data-stu-id="17f8b-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="17f8b-113">여기서는 설명, 기본 액세스 키를 변경하고 웹 서비스에 대한 런타임 동안 모든 추적에 대해 진단 컬렉션을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="17f8b-114">예제 2: 웹 서비스 인스턴스를 기반으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="17f8b-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="17f8b-115">이 예제에서는 먼저 업데이트할 필드만 포함하는 웹 서비스 정의를 만든 다음 serviceUpdates 매개 변수를 사용하여 Update-AzMlWebService 웹 서비스 정의를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="17f8b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17f8b-116">PARAMETERS</span></span>

### <span data-ttu-id="17f8b-117">-Assets</span><span class="sxs-lookup"><span data-stu-id="17f8b-117">-Assets</span></span>
<span data-ttu-id="17f8b-118">웹 서비스를 구성하는 자산 집합(예: 모듈, 데이터 세트)입니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f8b-119">-DefaultProfile</span></span>
<span data-ttu-id="17f8b-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="17f8b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17f8b-121">-Description</span><span class="sxs-lookup"><span data-stu-id="17f8b-121">-Description</span></span>
<span data-ttu-id="17f8b-122">웹 서비스의 설명에 대한 새 값입니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-122">The new value for the web service's description.</span></span>
<span data-ttu-id="17f8b-123">서비스의 Swagger API Schema에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-124">-Diagnostics</span><span class="sxs-lookup"><span data-stu-id="17f8b-124">-Diagnostics</span></span>
<span data-ttu-id="17f8b-125">웹 서비스에 대한 진단 추적 컬렉션을 제어하는 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="17f8b-126">-Force</span></span>
<span data-ttu-id="17f8b-127">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="17f8b-128">-Input</span><span class="sxs-lookup"><span data-stu-id="17f8b-128">-Input</span></span>
<span data-ttu-id="17f8b-129">Swagger Schema 구문으로 제공되는 웹 서비스의 입력에 대한 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="17f8b-130">-IsReadOnly</span></span>
<span data-ttu-id="17f8b-131">이 웹 서비스가 읽기 전용으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="17f8b-132">설정되면 이 속성의 값을 변경하는 등 웹 서비스를 더 이상 업데이트할 수 있으며 삭제할 수만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-133">-Keys</span><span class="sxs-lookup"><span data-stu-id="17f8b-133">-Keys</span></span>
<span data-ttu-id="17f8b-134">서비스의 런타임 API에 대한 호출을 인증하는 데 사용되는 액세스 키 중 하나 또는 둘 다를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-135">-Name</span><span class="sxs-lookup"><span data-stu-id="17f8b-135">-Name</span></span>
<span data-ttu-id="17f8b-136">업데이트할 웹 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-136">The name of the web service resource to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-137">-Output</span><span class="sxs-lookup"><span data-stu-id="17f8b-137">-Output</span></span>
<span data-ttu-id="17f8b-138">Swagger schema 구문으로 제공되는 웹 서비스의 출력에 대한 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-139">-Package</span><span class="sxs-lookup"><span data-stu-id="17f8b-139">-Package</span></span>
<span data-ttu-id="17f8b-140">이 웹 서비스를 정의하는 그래프 패키지의 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="17f8b-141">-Parameters</span></span>
<span data-ttu-id="17f8b-142">전역 매개 변수 이름(기본값 컬렉션)으로 제공된 웹 서비스에 대해 정의된 전역 매개 \> 변수 값 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="17f8b-143">기본값을 지정하지 않으면 매개 변수가 필요한 것으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="17f8b-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="17f8b-145">서비스의 실시간 엔드포인트 구성에 대한 업데이트입니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17f8b-146">-ResourceGroupName</span></span>
<span data-ttu-id="17f8b-147">업데이트할 웹 서비스를 포함하는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-147">The resource group that contains the web service to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="17f8b-148">-ServiceUpdates</span></span>
<span data-ttu-id="17f8b-149">웹 서비스 정의 인스턴스로 제공되는 웹 서비스에 적용할 업데이트 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="17f8b-150">비정적 필드만 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: UpdateFromObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="17f8b-151">-StorageAccountKey</span></span>
<span data-ttu-id="17f8b-152">웹 서비스에 연결된 저장소 계정에 대한 액세스 키를 회전합니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-153">-Title</span><span class="sxs-lookup"><span data-stu-id="17f8b-153">-Title</span></span>
<span data-ttu-id="17f8b-154">웹 서비스의 타이틀에 대한 새 값입니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-154">The new value for the web service's title.</span></span>
<span data-ttu-id="17f8b-155">서비스의 Swagger API Schema에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17f8b-156">-Confirm</span></span>
<span data-ttu-id="17f8b-157">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17f8b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17f8b-158">-WhatIf</span></span>
<span data-ttu-id="17f8b-159">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="17f8b-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17f8b-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17f8b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f8b-161">CommonParameters</span></span>
<span data-ttu-id="17f8b-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17f8b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f8b-163">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="17f8b-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f8b-164">입력</span><span class="sxs-lookup"><span data-stu-id="17f8b-164">INPUTS</span></span>

### <span data-ttu-id="17f8b-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="17f8b-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="17f8b-166">출력</span><span class="sxs-lookup"><span data-stu-id="17f8b-166">OUTPUTS</span></span>

### <span data-ttu-id="17f8b-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="17f8b-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="17f8b-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17f8b-168">NOTES</span></span>
<span data-ttu-id="17f8b-169">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="17f8b-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="17f8b-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17f8b-170">RELATED LINKS</span></span>
