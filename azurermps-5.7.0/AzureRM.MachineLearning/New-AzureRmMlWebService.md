---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: df6392e339063ccb2cc60411b77f73936071ab3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537720"
---
# <span data-ttu-id="57d98-101">New-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="57d98-101">New-AzureRmMlWebService</span></span>

## <span data-ttu-id="57d98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57d98-102">SYNOPSIS</span></span>
<span data-ttu-id="57d98-103">새 웹 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-103">Creates a new web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57d98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57d98-104">SYNTAX</span></span>

### <span data-ttu-id="57d98-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="57d98-105">CreateFromFile</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57d98-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="57d98-106">CreateFromInstance</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57d98-107">설명은</span><span class="sxs-lookup"><span data-stu-id="57d98-107">DESCRIPTION</span></span>
<span data-ttu-id="57d98-108">기존 리소스 그룹에 Azure 기계 학습 웹 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="57d98-109">리소스 그룹에 같은 이름의 웹 서비스가 있으면 해당 호출이 업데이트 작업으로 작동 하 고 기존 웹 서비스를 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="57d98-110">예제의</span><span class="sxs-lookup"><span data-stu-id="57d98-110">EXAMPLES</span></span>

### <span data-ttu-id="57d98-111">--------------------------예제 1: Json 파일 기반 정의에서 새 서비스 만들기--------------------------</span><span class="sxs-lookup"><span data-stu-id="57d98-111">--------------------------  Example 1: Create a new service from a Json file based definition  --------------------------</span></span>
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="57d98-112">참조 된 json 파일에 있는 정의에 따라 "myresourcegroup" 그룹 및 미국 중앙 US 지역에 "mywebservicename" 이라는 새 Azure 기계 학습 웹 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="57d98-113">--------------------------예제 2: 개체 인스턴스에서 새 서비스 만들기--------------------------</span><span class="sxs-lookup"><span data-stu-id="57d98-113">--------------------------  Example 2: Create a new service from an object instance  --------------------------</span></span>
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="57d98-114">Import-AzureRmMlWebService cmdlet을 사용 하 여 리소스로 게시 하기 전에 웹 서비스 개체 인스턴스를 가져와 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="57d98-115">변수</span><span class="sxs-lookup"><span data-stu-id="57d98-115">PARAMETERS</span></span>

### <span data-ttu-id="57d98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d98-116">-DefaultProfile</span></span>
<span data-ttu-id="57d98-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="57d98-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57d98-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="57d98-118">-DefinitionFile</span></span>
<span data-ttu-id="57d98-119">웹 서비스의 JSON 형식 정의를 포함 하는 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="57d98-120">의 swagger 사양에는 웹 서비스 정의에 대 한 최신 사양이 나와 있습니다 https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="57d98-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: String
Parameter Sets: CreateFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d98-121">-Force</span><span class="sxs-lookup"><span data-stu-id="57d98-121">-Force</span></span>
<span data-ttu-id="57d98-122">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="57d98-123">-위치</span><span class="sxs-lookup"><span data-stu-id="57d98-123">-Location</span></span>
<span data-ttu-id="57d98-124">웹 서비스의 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-124">The region of the web service.</span></span>
<span data-ttu-id="57d98-125">Azure 데이터 센터 지역 (예: "경기도 US" 또는 "동남 아시아")을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="57d98-126">해당 형식의 리소스를 지 원하는 모든 지역에 웹 서비스를 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="57d98-127">웹 서비스는 Azure 구독 또는 리소스 그룹과 동일한 지역에 있을 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="57d98-128">리소스 그룹에는 다른 지역의 웹 서비스가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="57d98-129">각 리소스 형식을 지 원하는 영역을 확인 하려면 ProviderNamespace 매개 변수 cmdlet이 포함 된 Get-AzureRmResourceProvider를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-129">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d98-130">-이름</span><span class="sxs-lookup"><span data-stu-id="57d98-130">-Name</span></span>
<span data-ttu-id="57d98-131">웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-131">The name for the web service.</span></span>
<span data-ttu-id="57d98-132">이름은 리소스 그룹에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-132">The name must be unique in the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d98-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="57d98-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="57d98-134">서비스를 만드는 모든 속성이 포함 된 새 웹 서비스에 대 한 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="57d98-135">이 매개 변수는 필수 이며 WebServices 클래스의 인스턴스를 나타냅니다. MachineLearning.</span><span class="sxs-lookup"><span data-stu-id="57d98-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="57d98-136">의 swagger 사양에는 웹 서비스 정의에 대 한 최신 사양이 나와 있습니다 https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="57d98-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: WebService
Parameter Sets: CreateFromInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57d98-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57d98-137">-ResourceGroupName</span></span>
<span data-ttu-id="57d98-138">웹 서비스를 배치할 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="57d98-139">Azure 데이터 센터 지역 (예: "경기도 US" 또는 "동남 아시아")을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="57d98-140">해당 형식의 리소스를 지 원하는 모든 지역에 웹 서비스를 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="57d98-141">웹 서비스는 Azure 구독 또는 리소스 그룹과 동일한 지역에 있을 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="57d98-142">리소스 그룹에는 다른 지역의 웹 서비스가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="57d98-143">각 리소스 형식을 지 원하는 영역을 확인 하려면 ProviderNamespace 매개 변수 cmdlet이 포함 된 Get-AzureRmResourceProvider를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-143">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d98-144">-확인</span><span class="sxs-lookup"><span data-stu-id="57d98-144">-Confirm</span></span>
<span data-ttu-id="57d98-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d98-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57d98-146">-WhatIf</span></span>
<span data-ttu-id="57d98-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57d98-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d98-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d98-149">CommonParameters</span></span>
<span data-ttu-id="57d98-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d98-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57d98-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d98-152">입력</span><span class="sxs-lookup"><span data-stu-id="57d98-152">INPUTS</span></span>

### <span data-ttu-id="57d98-153">용</span><span class="sxs-lookup"><span data-stu-id="57d98-153">WebService</span></span>
<span data-ttu-id="57d98-154">' NewWebServiceDefinition ' 매개 변수는 파이프라인에서 ' WebService ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-154">Parameter 'NewWebServiceDefinition' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="57d98-155">출력</span><span class="sxs-lookup"><span data-stu-id="57d98-155">OUTPUTS</span></span>

### <span data-ttu-id="57d98-156">MachineLearning. WebServices의 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="57d98-156">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="57d98-157">Azure 기계 학습 웹 서비스에 대 한 요약 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-157">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="57d98-158">기존 웹 서비스에서 Get-AzureRmMlWebService cmdlet을 호출 하 여 반환 되는 설명과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-158">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="57d98-159">이 설명에는 저장소 계정의 자격 증명 및 서비스의 선택 키와 같은 중요 한 속성이 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57d98-159">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="57d98-160">상속자</span><span class="sxs-lookup"><span data-stu-id="57d98-160">NOTES</span></span>
<span data-ttu-id="57d98-161">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="57d98-161">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="57d98-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57d98-162">RELATED LINKS</span></span>

