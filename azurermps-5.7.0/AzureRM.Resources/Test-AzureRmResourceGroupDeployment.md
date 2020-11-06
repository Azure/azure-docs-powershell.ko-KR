---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 0caf541aeadcbf2617ae5d31d0dfaf69e432e888
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534683"
---
# <span data-ttu-id="6554c-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6554c-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="6554c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6554c-102">SYNOPSIS</span></span>
<span data-ttu-id="6554c-103">리소스 그룹 배포의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6554c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6554c-104">SYNTAX</span></span>

### <span data-ttu-id="6554c-105">By서식 Filewithnoparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="6554c-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6554c-106">By서식 Fileandparameterobject</span><span class="sxs-lookup"><span data-stu-id="6554c-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6554c-107">By서식 Uriandparameterobject</span><span class="sxs-lookup"><span data-stu-id="6554c-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6554c-108">By서식 파일 Andparameterfile</span><span class="sxs-lookup"><span data-stu-id="6554c-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6554c-109">By서식 Uriandparameterfile</span><span class="sxs-lookup"><span data-stu-id="6554c-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6554c-110">By서식 Fileandparameteruri</span><span class="sxs-lookup"><span data-stu-id="6554c-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6554c-111">By서식 Uriandparameteruri</span><span class="sxs-lookup"><span data-stu-id="6554c-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6554c-112">By서식 Uriwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="6554c-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6554c-113">설명은</span><span class="sxs-lookup"><span data-stu-id="6554c-113">DESCRIPTION</span></span>
<span data-ttu-id="6554c-114">**AzureRmResourceGroupDeployment** Cmdlet은 Azure 리소스 그룹 배포 템플릿과 해당 매개 변수 값이 유효한 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="6554c-115">예제의</span><span class="sxs-lookup"><span data-stu-id="6554c-115">EXAMPLES</span></span>

## <span data-ttu-id="6554c-116">변수</span><span class="sxs-lookup"><span data-stu-id="6554c-116">PARAMETERS</span></span>

### <span data-ttu-id="6554c-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6554c-117">-ApiVersion</span></span>
<span data-ttu-id="6554c-118">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="6554c-119">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="6554c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6554c-120">-DefaultProfile</span></span>
<span data-ttu-id="6554c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6554c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6554c-122">-모드</span><span class="sxs-lookup"><span data-stu-id="6554c-122">-Mode</span></span>
<span data-ttu-id="6554c-123">배포 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="6554c-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6554c-125">진행</span><span class="sxs-lookup"><span data-stu-id="6554c-125">Incremental</span></span>
- <span data-ttu-id="6554c-126">마칠</span><span class="sxs-lookup"><span data-stu-id="6554c-126">Complete</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6554c-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="6554c-127">-Pre</span></span>
<span data-ttu-id="6554c-128">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6554c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6554c-129">-ResourceGroupName</span></span>
<span data-ttu-id="6554c-130">테스트할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="6554c-131">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="6554c-131">-TemplateFile</span></span>
<span data-ttu-id="6554c-132">JSON 템플릿 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-132">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6554c-133">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="6554c-133">-TemplateParameterFile</span></span>
<span data-ttu-id="6554c-134">템플릿 매개 변수의 이름 및 값이 포함 된 JSON 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-134">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6554c-135">------# Parameterobject</span><span class="sxs-lookup"><span data-stu-id="6554c-135">-TemplateParameterObject</span></span>
<span data-ttu-id="6554c-136">템플릿 매개 변수 이름 및 값의 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-136">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6554c-137">--# Parameteruri</span><span class="sxs-lookup"><span data-stu-id="6554c-137">-TemplateParameterUri</span></span>
<span data-ttu-id="6554c-138">템플릿 매개 변수 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-138">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6554c-139">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="6554c-139">-TemplateUri</span></span>
<span data-ttu-id="6554c-140">JSON 템플릿 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-140">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6554c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6554c-141">CommonParameters</span></span>
<span data-ttu-id="6554c-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6554c-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6554c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6554c-144">입력</span><span class="sxs-lookup"><span data-stu-id="6554c-144">INPUTS</span></span>

### <span data-ttu-id="6554c-145">않아야</span><span class="sxs-lookup"><span data-stu-id="6554c-145">None</span></span>
<span data-ttu-id="6554c-146">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6554c-147">출력</span><span class="sxs-lookup"><span data-stu-id="6554c-147">OUTPUTS</span></span>

### <span data-ttu-id="6554c-148">System.webserver. List ' 1 [SdkModels. t e PSResourceManagerError]를 목록으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6554c-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="6554c-149">상속자</span><span class="sxs-lookup"><span data-stu-id="6554c-149">NOTES</span></span>

## <span data-ttu-id="6554c-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6554c-150">RELATED LINKS</span></span>

[<span data-ttu-id="6554c-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6554c-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="6554c-152">새로운 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6554c-152">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="6554c-153">제거-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6554c-153">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="6554c-154">중지-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6554c-154">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


