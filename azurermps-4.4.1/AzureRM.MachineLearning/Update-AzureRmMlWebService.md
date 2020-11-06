---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 75f94e5c93f81fa88dd33c3c0b94cb2b36ca291f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532237"
---
# <span data-ttu-id="f9f64-101">Update-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="f9f64-101">Update-AzureRmMlWebService</span></span>

## <span data-ttu-id="f9f64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9f64-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f64-103">기존 웹 서비스 리소스의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-103">Updates properties of an existing web service resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9f64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9f64-104">SYNTAX</span></span>

### <span data-ttu-id="f9f64-105">의 특정 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-105">Update specific properties of the .</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9f64-106">WebService 인스턴스 정의에서 새 Azure ML webservice를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-106">Create a new Azure ML webservice from a WebService instance definition.</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9f64-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f9f64-107">DESCRIPTION</span></span>
<span data-ttu-id="f9f64-108">Update-AzureRmMlWebService cmdlet에서는 웹 서비스의 비정적 속성을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-108">The Update-AzureRmMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="f9f64-109">Cmdlet은 패치 작업으로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="f9f64-110">수정 하려는 속성만 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="f9f64-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f9f64-111">EXAMPLES</span></span>

### <span data-ttu-id="f9f64-112">--------------------------예제 1: 선택적 업데이트 인수--------------------------</span><span class="sxs-lookup"><span data-stu-id="f9f64-112">--------------------------  Example 1: Selective update arguments  --------------------------</span></span>
<span data-ttu-id="f9f64-113">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="f9f64-113">@{paragraph=PS C:\\\>}</span></span>





```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="f9f64-114">여기서는 설명, 기본 선택 키를 변경 하 고 런타임 중에 웹 서비스의 모든 추적에 대 한 진단 컬렉션을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-114">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="f9f64-115">--------------------------예제 2: 웹 서비스 인스턴스를 기반으로 하는 업데이트--------------------------</span><span class="sxs-lookup"><span data-stu-id="f9f64-115">--------------------------  Example 2: Update based on a web service instance  --------------------------</span></span>
<span data-ttu-id="f9f64-116">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="f9f64-116">@{paragraph=PS C:\\\>}</span></span>





```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="f9f64-117">이 예제에서는 먼저 업데이트 될 필드만 포함 하는 웹 서비스 정의를 만든 다음 ServiceUpdates 매개 변수를 사용 하 여이를 적용 하기 위해 Update-AzureRmMlWebService 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-117">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzureRmMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="f9f64-118">변수</span><span class="sxs-lookup"><span data-stu-id="f9f64-118">PARAMETERS</span></span>

### <span data-ttu-id="f9f64-119">-자산</span><span class="sxs-lookup"><span data-stu-id="f9f64-119">-Assets</span></span>
<span data-ttu-id="f9f64-120">웹 서비스를 구성 하는 자산 집합 (예: 모듈, 데이터 집합)입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-120">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f64-121">-설명</span><span class="sxs-lookup"><span data-stu-id="f9f64-121">-Description</span></span>
<span data-ttu-id="f9f64-122">웹 서비스 설명에 대 한 새 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-122">The new value for the web service's description.</span></span>
<span data-ttu-id="f9f64-123">이는 서비스의 Swagger API 스키마에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f64-124">-진단</span><span class="sxs-lookup"><span data-stu-id="f9f64-124">-Diagnostics</span></span>
<span data-ttu-id="f9f64-125">웹 서비스에 대 한 진단 추적 컬렉션을 제어 하는 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f64-126">-Force</span><span class="sxs-lookup"><span data-stu-id="f9f64-126">-Force</span></span>
<span data-ttu-id="f9f64-127">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f9f64-128">-입력</span><span class="sxs-lookup"><span data-stu-id="f9f64-128">-Input</span></span>
<span data-ttu-id="f9f64-129">Swagger 스키마 구문으로 제공 되는 웹 서비스의 입력에 대 한 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f64-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="f9f64-130">-IsReadOnly</span></span>
<span data-ttu-id="f9f64-131">이 웹 serviceis 읽기 전용 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-131">Specifies that this web serviceis readonly.</span></span>
<span data-ttu-id="f9f64-132">설정한 후에는이 속성 값을 변경 하는 등 웹 서비스를 더 오랫동안 업데이트할 수 있으며, 삭제할 수만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f64-133">-키</span><span class="sxs-lookup"><span data-stu-id="f9f64-133">-Keys</span></span>
<span data-ttu-id="f9f64-134">서비스의 런타임 Api에 대 한 호출을 인증 하는 데 사용 되는 선택 키 중 하나 또는 모두를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f64-135">-이름</span><span class="sxs-lookup"><span data-stu-id="f9f64-135">-Name</span></span>
<span data-ttu-id="f9f64-136">업데이트 될 웹 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="f9f64-137">-출력</span><span class="sxs-lookup"><span data-stu-id="f9f64-137">-Output</span></span>
<span data-ttu-id="f9f64-138">Swagger 스키마 구문으로 제공 되는 웹 서비스의 출력에 대 한 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f64-139">-패키지</span><span class="sxs-lookup"><span data-stu-id="f9f64-139">-Package</span></span>
<span data-ttu-id="f9f64-140">이 웹 서비스를 정의 하는 그래프 패키지의 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f64-141">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="f9f64-141">-Parameters</span></span>
<span data-ttu-id="f9f64-142">전역 매개 변수 이름-기본 값 컬렉션으로 지정 된 웹 서비스에 대해 정의 된 전역 매개 변수 값 집합 \> 입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="f9f64-143">Default 값이 지정 되지 않은 경우 매개 변수는 필수로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f64-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9f64-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="f9f64-145">서비스의 실시간 끝점 구성에 대 한 업데이트입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f64-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9f64-146">-ResourceGroupName</span></span>
<span data-ttu-id="f9f64-147">업데이트 될 웹 서비스를 포함 하는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="f9f64-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="f9f64-148">-ServiceUpdates</span></span>
<span data-ttu-id="f9f64-149">웹 서비스 정의 인스턴스로 제공 되는 웹 서비스에 적용할 업데이트 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="f9f64-150">비정적 필드만 수정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9f64-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f9f64-151">-StorageAccountKey</span></span>
<span data-ttu-id="f9f64-152">웹 서비스와 연결 된 저장소 계정에 대 한 선택 키를 회전 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f64-153">-Title</span><span class="sxs-lookup"><span data-stu-id="f9f64-153">-Title</span></span>
<span data-ttu-id="f9f64-154">웹 서비스 제목의 새 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-154">The new value for the web service's title.</span></span>
<span data-ttu-id="f9f64-155">이는 서비스의 Swagger API 스키마에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f64-156">-확인</span><span class="sxs-lookup"><span data-stu-id="f9f64-156">-Confirm</span></span>
<span data-ttu-id="f9f64-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9f64-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9f64-158">-WhatIf</span></span>
<span data-ttu-id="f9f64-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9f64-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9f64-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f64-161">-DefaultProfile</span></span>
<span data-ttu-id="f9f64-162">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9f64-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f64-163">CommonParameters</span></span>
<span data-ttu-id="f9f64-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f64-165">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9f64-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f64-166">입력</span><span class="sxs-lookup"><span data-stu-id="f9f64-166">INPUTS</span></span>

### <span data-ttu-id="f9f64-167">용</span><span class="sxs-lookup"><span data-stu-id="f9f64-167">WebService</span></span>
<span data-ttu-id="f9f64-168">' ServiceUpdates ' 매개 변수는 파이프라인에서 ' WebService ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-168">Parameter 'ServiceUpdates' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="f9f64-169">출력</span><span class="sxs-lookup"><span data-stu-id="f9f64-169">OUTPUTS</span></span>

### <span data-ttu-id="f9f64-170">MachineLearning. WebServices의 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="f9f64-170">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="f9f64-171">Azure 기계 학습 웹 서비스에 대 한 요약 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-171">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="f9f64-172">기존 웹 서비스에서 Get-AzureRmMlWebService cmdlet을 호출 하 여 반환 되는 설명과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-172">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="f9f64-173">이 설명에는 저장소 계정의 자격 증명 및 서비스의 선택 키와 같은 중요 한 속성이 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f64-173">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="f9f64-174">상속자</span><span class="sxs-lookup"><span data-stu-id="f9f64-174">NOTES</span></span>
<span data-ttu-id="f9f64-175">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="f9f64-175">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f9f64-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9f64-176">RELATED LINKS</span></span>

