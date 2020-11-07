---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: a4c8e2687fd525b32ef3a9da3684a3da9f3c5717
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689412"
---
# <span data-ttu-id="23e14-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="23e14-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="23e14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23e14-102">SYNOPSIS</span></span>
<span data-ttu-id="23e14-103">기존 웹 서비스 리소스의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="23e14-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23e14-104">SYNTAX</span></span>

### <span data-ttu-id="23e14-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="23e14-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23e14-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="23e14-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23e14-107">설명은</span><span class="sxs-lookup"><span data-stu-id="23e14-107">DESCRIPTION</span></span>
<span data-ttu-id="23e14-108">Update-AzMlWebService cmdlet에서는 웹 서비스의 비정적 속성을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="23e14-109">Cmdlet은 패치 작업으로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="23e14-110">수정 하려는 속성만 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="23e14-111">예제의</span><span class="sxs-lookup"><span data-stu-id="23e14-111">EXAMPLES</span></span>

### <span data-ttu-id="23e14-112">예제 1: 선택적 업데이트 인수</span><span class="sxs-lookup"><span data-stu-id="23e14-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="23e14-113">여기서는 설명, 기본 선택 키를 변경 하 고 런타임 중에 웹 서비스의 모든 추적에 대 한 진단 컬렉션을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="23e14-114">예제 2: 웹 서비스 인스턴스를 기반으로 하는 업데이트</span><span class="sxs-lookup"><span data-stu-id="23e14-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="23e14-115">이 예제에서는 먼저 업데이트 될 필드만 포함 하는 웹 서비스 정의를 만든 다음 ServiceUpdates 매개 변수를 사용 하 여이를 적용 하기 위해 Update-AzMlWebService 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="23e14-116">변수</span><span class="sxs-lookup"><span data-stu-id="23e14-116">PARAMETERS</span></span>

### <span data-ttu-id="23e14-117">-자산</span><span class="sxs-lookup"><span data-stu-id="23e14-117">-Assets</span></span>
<span data-ttu-id="23e14-118">웹 서비스를 구성 하는 자산 집합 (예: 모듈, 데이터 집합)입니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

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

### <span data-ttu-id="23e14-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e14-119">-DefaultProfile</span></span>
<span data-ttu-id="23e14-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="23e14-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23e14-121">-설명</span><span class="sxs-lookup"><span data-stu-id="23e14-121">-Description</span></span>
<span data-ttu-id="23e14-122">웹 서비스 설명에 대 한 새 값입니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-122">The new value for the web service's description.</span></span>
<span data-ttu-id="23e14-123">이는 서비스의 Swagger API 스키마에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-123">This is visible in the service's Swagger API schema.</span></span>

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

### <span data-ttu-id="23e14-124">-진단</span><span class="sxs-lookup"><span data-stu-id="23e14-124">-Diagnostics</span></span>
<span data-ttu-id="23e14-125">웹 서비스에 대 한 진단 추적 컬렉션을 제어 하는 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-125">The settings that control the diagnostics traces collection for the web service.</span></span>

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

### <span data-ttu-id="23e14-126">-Force</span><span class="sxs-lookup"><span data-stu-id="23e14-126">-Force</span></span>
<span data-ttu-id="23e14-127">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="23e14-128">-입력</span><span class="sxs-lookup"><span data-stu-id="23e14-128">-Input</span></span>
<span data-ttu-id="23e14-129">Swagger 스키마 구문으로 제공 되는 웹 서비스의 입력에 대 한 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

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

### <span data-ttu-id="23e14-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="23e14-130">-IsReadOnly</span></span>
<span data-ttu-id="23e14-131">이 웹 서비스를 읽기 전용으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="23e14-132">설정한 후에는이 속성 값을 변경 하는 등 웹 서비스를 더 오랫동안 업데이트할 수 있으며, 삭제할 수만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

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

### <span data-ttu-id="23e14-133">-키</span><span class="sxs-lookup"><span data-stu-id="23e14-133">-Keys</span></span>
<span data-ttu-id="23e14-134">서비스의 런타임 Api에 대 한 호출을 인증 하는 데 사용 되는 선택 키 중 하나 또는 모두를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

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

### <span data-ttu-id="23e14-135">-이름</span><span class="sxs-lookup"><span data-stu-id="23e14-135">-Name</span></span>
<span data-ttu-id="23e14-136">업데이트 될 웹 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="23e14-137">-출력</span><span class="sxs-lookup"><span data-stu-id="23e14-137">-Output</span></span>
<span data-ttu-id="23e14-138">Swagger 스키마 구문으로 제공 되는 웹 서비스의 출력에 대 한 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

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

### <span data-ttu-id="23e14-139">-패키지</span><span class="sxs-lookup"><span data-stu-id="23e14-139">-Package</span></span>
<span data-ttu-id="23e14-140">이 웹 서비스를 정의 하는 그래프 패키지의 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-140">The definition of the graph package that defines this web service.</span></span>

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

### <span data-ttu-id="23e14-141">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="23e14-141">-Parameters</span></span>
<span data-ttu-id="23e14-142">전역 매개 변수 이름-기본 값 컬렉션으로 지정 된 웹 서비스에 대해 정의 된 전역 매개 변수 값 집합 \> 입니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="23e14-143">Default 값이 지정 되지 않은 경우 매개 변수는 필수로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-143">If no default value is specified, the parameter is considered to be required.</span></span>

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

### <span data-ttu-id="23e14-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="23e14-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="23e14-145">서비스의 실시간 끝점 구성에 대 한 업데이트입니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-145">Updates for the configuration of the service's realtime endpoint.</span></span>

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

### <span data-ttu-id="23e14-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23e14-146">-ResourceGroupName</span></span>
<span data-ttu-id="23e14-147">업데이트 될 웹 서비스를 포함 하는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="23e14-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="23e14-148">-ServiceUpdates</span></span>
<span data-ttu-id="23e14-149">웹 서비스 정의 인스턴스로 제공 되는 웹 서비스에 적용할 업데이트 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="23e14-150">비정적 필드만 수정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-150">Only non-static fields are modified.</span></span>

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

### <span data-ttu-id="23e14-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="23e14-151">-StorageAccountKey</span></span>
<span data-ttu-id="23e14-152">웹 서비스와 연결 된 저장소 계정에 대 한 선택 키를 회전 합니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-152">Rotates the access key for the storage account associated with the web service.</span></span>

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

### <span data-ttu-id="23e14-153">-Title</span><span class="sxs-lookup"><span data-stu-id="23e14-153">-Title</span></span>
<span data-ttu-id="23e14-154">웹 서비스 제목의 새 값입니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-154">The new value for the web service's title.</span></span>
<span data-ttu-id="23e14-155">이는 서비스의 Swagger API 스키마에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-155">This is visible in the service's Swagger API schema.</span></span>

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

### <span data-ttu-id="23e14-156">-확인</span><span class="sxs-lookup"><span data-stu-id="23e14-156">-Confirm</span></span>
<span data-ttu-id="23e14-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23e14-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23e14-158">-WhatIf</span></span>
<span data-ttu-id="23e14-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23e14-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23e14-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e14-161">CommonParameters</span></span>
<span data-ttu-id="23e14-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23e14-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e14-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23e14-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e14-164">입력</span><span class="sxs-lookup"><span data-stu-id="23e14-164">INPUTS</span></span>

### <span data-ttu-id="23e14-165">MachineLearning. WebServices의 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="23e14-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="23e14-166">출력</span><span class="sxs-lookup"><span data-stu-id="23e14-166">OUTPUTS</span></span>

### <span data-ttu-id="23e14-167">MachineLearning. WebServices의 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="23e14-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="23e14-168">상속자</span><span class="sxs-lookup"><span data-stu-id="23e14-168">NOTES</span></span>
<span data-ttu-id="23e14-169">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="23e14-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="23e14-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23e14-170">RELATED LINKS</span></span>
