---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmDeployment.md
ms.openlocfilehash: fdfef01f9ba8013b25db227c0833a7add408c490
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529402"
---
# <span data-ttu-id="b78fe-101">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b78fe-101">Test-AzureRmDeployment</span></span>

## <span data-ttu-id="b78fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b78fe-102">SYNOPSIS</span></span>
<span data-ttu-id="b78fe-103">배포의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b78fe-103">Validates a deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b78fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b78fe-104">SYNTAX</span></span>

### <span data-ttu-id="b78fe-105">By서식 Filewithnoparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="b78fe-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b78fe-106">By서식 Fileandparameterobject</span><span class="sxs-lookup"><span data-stu-id="b78fe-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b78fe-107">By서식 Uriandparameterobject</span><span class="sxs-lookup"><span data-stu-id="b78fe-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b78fe-108">By서식 파일 Andparameterfile</span><span class="sxs-lookup"><span data-stu-id="b78fe-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b78fe-109">By서식 Uriandparameterfile</span><span class="sxs-lookup"><span data-stu-id="b78fe-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b78fe-110">By서식 Fileandparameteruri</span><span class="sxs-lookup"><span data-stu-id="b78fe-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b78fe-111">By서식 Uriandparameteruri</span><span class="sxs-lookup"><span data-stu-id="b78fe-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b78fe-112">By서식 Uriwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="b78fe-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b78fe-113">설명은</span><span class="sxs-lookup"><span data-stu-id="b78fe-113">DESCRIPTION</span></span>
<span data-ttu-id="b78fe-114">**AzureRmDeployment** cmdlet은 배포 템플릿과 해당 매개 변수 값이 유효한 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b78fe-114">The **Test-AzureRmDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="b78fe-115">예제의</span><span class="sxs-lookup"><span data-stu-id="b78fe-115">EXAMPLES</span></span>

### <span data-ttu-id="b78fe-116">예제 1: 사용자 지정 템플릿 및 매개 변수 파일을 사용 하 여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="b78fe-116">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\>Test-AzureRmDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="b78fe-117">이 명령은 지정 된 템플릿 파일 및 매개 변수 파일을 사용 하 여 현재 구독 범위에서 배포를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b78fe-117">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

## <span data-ttu-id="b78fe-118">변수</span><span class="sxs-lookup"><span data-stu-id="b78fe-118">PARAMETERS</span></span>

### <span data-ttu-id="b78fe-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b78fe-119">-ApiVersion</span></span>
<span data-ttu-id="b78fe-120">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b78fe-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b78fe-121">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b78fe-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b78fe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b78fe-122">-DefaultProfile</span></span>
<span data-ttu-id="b78fe-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b78fe-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b78fe-124">-위치</span><span class="sxs-lookup"><span data-stu-id="b78fe-124">-Location</span></span>
<span data-ttu-id="b78fe-125">배포 데이터를 저장할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b78fe-125">The location to store deployment data.</span></span>

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

### <span data-ttu-id="b78fe-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="b78fe-126">-Pre</span></span>
<span data-ttu-id="b78fe-127">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b78fe-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b78fe-128">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="b78fe-128">-TemplateFile</span></span>
<span data-ttu-id="b78fe-129">서식 파일에 대 한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b78fe-129">Local path to the template file.</span></span>

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

### <span data-ttu-id="b78fe-130">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="b78fe-130">-TemplateParameterFile</span></span>
<span data-ttu-id="b78fe-131">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="b78fe-131">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="b78fe-132">------# Parameterobject</span><span class="sxs-lookup"><span data-stu-id="b78fe-132">-TemplateParameterObject</span></span>
<span data-ttu-id="b78fe-133">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="b78fe-133">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="b78fe-134">--# Parameteruri</span><span class="sxs-lookup"><span data-stu-id="b78fe-134">-TemplateParameterUri</span></span>
<span data-ttu-id="b78fe-135">Template 매개 변수 파일에 대 한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="b78fe-135">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="b78fe-136">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="b78fe-136">-TemplateUri</span></span>
<span data-ttu-id="b78fe-137">템플릿 파일에 대 한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="b78fe-137">Uri to the template file.</span></span>

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

### <span data-ttu-id="b78fe-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b78fe-138">CommonParameters</span></span>
<span data-ttu-id="b78fe-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b78fe-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b78fe-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b78fe-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b78fe-141">입력</span><span class="sxs-lookup"><span data-stu-id="b78fe-141">INPUTS</span></span>

### <span data-ttu-id="b78fe-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b78fe-142">System.String</span></span>
<span data-ttu-id="b78fe-143">DeploymentMode. 컬렉션. m a m.</span><span class="sxs-lookup"><span data-stu-id="b78fe-143">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode System.Collections.Hashtable</span></span>

## <span data-ttu-id="b78fe-144">출력</span><span class="sxs-lookup"><span data-stu-id="b78fe-144">OUTPUTS</span></span>

### <span data-ttu-id="b78fe-145">SdkModels. PSResourceManagerError에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="b78fe-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="b78fe-146">상속자</span><span class="sxs-lookup"><span data-stu-id="b78fe-146">NOTES</span></span>

## <span data-ttu-id="b78fe-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b78fe-147">RELATED LINKS</span></span>
