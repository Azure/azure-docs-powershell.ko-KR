---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385939"
---
# <span data-ttu-id="096d4-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="096d4-101">New-AzMlWebService</span></span>

## <span data-ttu-id="096d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="096d4-102">SYNOPSIS</span></span>
<span data-ttu-id="096d4-103">새 웹 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-103">Creates a new web service.</span></span>

## <span data-ttu-id="096d4-104">구문</span><span class="sxs-lookup"><span data-stu-id="096d4-104">SYNTAX</span></span>

### <span data-ttu-id="096d4-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="096d4-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="096d4-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="096d4-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="096d4-107">설명</span><span class="sxs-lookup"><span data-stu-id="096d4-107">DESCRIPTION</span></span>
<span data-ttu-id="096d4-108">기존 리소스 그룹에 Azure Machine Learning 웹 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="096d4-109">동일한 이름의 웹 서비스가 리소스 그룹에 있는 경우 호출은 업데이트 작업으로 작동하고 기존 웹 서비스를 덮어 덮어습니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="096d4-110">예제</span><span class="sxs-lookup"><span data-stu-id="096d4-110">EXAMPLES</span></span>

### <span data-ttu-id="096d4-111">예제 1: Json 파일 기반 정의에서 새 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="096d4-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="096d4-112">참조된 json 파일에 있는 정의에 따라 "myresourcegroup" 그룹 및 미국 중남부 지역에 "mywebservicename"이라는 새 Azure Machine Learning 웹 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="096d4-113">예제 2: 개체 인스턴스에서 새 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="096d4-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="096d4-114">Import-AzMlWebService cmdlet을 사용하여 리소스로 게시하기 전에 사용자 지정할 웹 서비스 개체 인스턴스를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="096d4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="096d4-115">PARAMETERS</span></span>

### <span data-ttu-id="096d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096d4-116">-DefaultProfile</span></span>
<span data-ttu-id="096d4-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="096d4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="096d4-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="096d4-118">-DefinitionFile</span></span>
<span data-ttu-id="096d4-119">웹 서비스의 JSON 형식 정의를 포함하는 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="096d4-120">웹 서비스 정의에 대한 최신 사양은 아래 swagger 사양에서 찾을 수 https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning 있습니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="096d4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="096d4-121">-Force</span></span>
<span data-ttu-id="096d4-122">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="096d4-123">-Location</span><span class="sxs-lookup"><span data-stu-id="096d4-123">-Location</span></span>
<span data-ttu-id="096d4-124">웹 서비스의 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-124">The region of the web service.</span></span>
<span data-ttu-id="096d4-125">Azure 데이터 센터 지역(예: "미국 서부" 또는 "동남 아시아")을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="096d4-126">해당 유형의 리소스를 지원하는 모든 지역에 웹 서비스를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="096d4-127">웹 서비스는 Azure 구독 또는 해당 리소스 그룹과 동일한 지역에 있을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="096d4-128">리소스 그룹은 다른 지역의 웹 서비스를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="096d4-129">각 리소스 종류를 지원하는 지역을 결정하기 위해 ProviderNamespace 매개 Get-AzResourceProvider cmdlet과 함께 다음을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="096d4-130">-Name</span><span class="sxs-lookup"><span data-stu-id="096d4-130">-Name</span></span>
<span data-ttu-id="096d4-131">웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-131">The name for the web service.</span></span>
<span data-ttu-id="096d4-132">이름은 리소스 그룹에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="096d4-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="096d4-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="096d4-134">서비스를 만드는 모든 속성을 포함하는 새 웹 서비스에 대한 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="096d4-135">이 매개 변수는 필수로, Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService 클래스의 인스턴스를 나타냈습니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="096d4-136">웹 서비스 정의에 대한 최신 사양은 아래 swagger 사양에서 찾을 수 https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json 있습니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="096d4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="096d4-137">-ResourceGroupName</span></span>
<span data-ttu-id="096d4-138">웹 서비스를 두는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="096d4-139">Azure 데이터 센터 지역(예: "미국 서부" 또는 "동남 아시아")을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="096d4-140">해당 유형의 리소스를 지원하는 모든 지역에 웹 서비스를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="096d4-141">웹 서비스는 Azure 구독 또는 해당 리소스 그룹과 동일한 지역에 있을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="096d4-142">리소스 그룹은 다른 지역의 웹 서비스를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="096d4-143">각 리소스 종류를 지원하는 지역을 결정하기 위해 ProviderNamespace 매개 Get-AzResourceProvider cmdlet과 함께 다음을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="096d4-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="096d4-144">-Confirm</span></span>
<span data-ttu-id="096d4-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="096d4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="096d4-146">-WhatIf</span></span>
<span data-ttu-id="096d4-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="096d4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="096d4-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="096d4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096d4-149">CommonParameters</span></span>
<span data-ttu-id="096d4-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="096d4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096d4-151">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="096d4-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096d4-152">입력</span><span class="sxs-lookup"><span data-stu-id="096d4-152">INPUTS</span></span>

### <span data-ttu-id="096d4-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="096d4-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="096d4-154">출력</span><span class="sxs-lookup"><span data-stu-id="096d4-154">OUTPUTS</span></span>

### <span data-ttu-id="096d4-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="096d4-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="096d4-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="096d4-156">NOTES</span></span>
<span data-ttu-id="096d4-157">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="096d4-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="096d4-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="096d4-158">RELATED LINKS</span></span>
