---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: b357215bf2c4ba032ca44e37cc445e12606aeffe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530702"
---
# <span data-ttu-id="d218a-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d218a-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="d218a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d218a-102">SYNOPSIS</span></span>
<span data-ttu-id="d218a-103">리소스 그룹 배포의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d218a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d218a-104">SYNTAX</span></span>

### <span data-ttu-id="d218a-105">매개 변수 없이 서식 파일을 통한 배포 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d218a-105">Deployment via template file without parameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d218a-106">서식 파일 및 템플릿 매개 변수 개체를 통한 배포</span><span class="sxs-lookup"><span data-stu-id="d218a-106">Deployment via template file and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d218a-107">템플릿 uri 및 템플릿 매개 변수 개체를 통한 배포</span><span class="sxs-lookup"><span data-stu-id="d218a-107">Deployment via template uri and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d218a-108">서식 파일 및 템플릿 매개 변수 파일을 통한 배포</span><span class="sxs-lookup"><span data-stu-id="d218a-108">Deployment via template file and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d218a-109">템플릿 uri 및 템플릿 매개 변수 파일을 통한 배포</span><span class="sxs-lookup"><span data-stu-id="d218a-109">Deployment via template uri and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d218a-110">템플릿 파일 템플릿 매개 변수 uri를 통한 배포</span><span class="sxs-lookup"><span data-stu-id="d218a-110">Deployment via template file template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d218a-111">템플릿 uri 및 템플릿 매개 변수 uri를 통한 배포</span><span class="sxs-lookup"><span data-stu-id="d218a-111">Deployment via template uri and template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d218a-112">매개 변수 없이 템플릿 uri를 통한 배포</span><span class="sxs-lookup"><span data-stu-id="d218a-112">Deployment via template uri without parameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d218a-113">설명은</span><span class="sxs-lookup"><span data-stu-id="d218a-113">DESCRIPTION</span></span>
<span data-ttu-id="d218a-114">**AzureRmResourceGroupDeployment** Cmdlet은 Azure 리소스 그룹 배포 템플릿과 해당 매개 변수 값이 유효한 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="d218a-115">예제의</span><span class="sxs-lookup"><span data-stu-id="d218a-115">EXAMPLES</span></span>

## <span data-ttu-id="d218a-116">변수</span><span class="sxs-lookup"><span data-stu-id="d218a-116">PARAMETERS</span></span>

### <span data-ttu-id="d218a-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d218a-117">-ApiVersion</span></span>
<span data-ttu-id="d218a-118">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d218a-119">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="d218a-120">-모드</span><span class="sxs-lookup"><span data-stu-id="d218a-120">-Mode</span></span>
<span data-ttu-id="d218a-121">배포 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-121">Specifies the deployment mode.</span></span>
<span data-ttu-id="d218a-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d218a-123">진행</span><span class="sxs-lookup"><span data-stu-id="d218a-123">Incremental</span></span>
- <span data-ttu-id="d218a-124">마칠</span><span class="sxs-lookup"><span data-stu-id="d218a-124">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d218a-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="d218a-125">-Pre</span></span>
<span data-ttu-id="d218a-126">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d218a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d218a-127">-ResourceGroupName</span></span>
<span data-ttu-id="d218a-128">테스트할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-128">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="d218a-129">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="d218a-129">-TemplateFile</span></span>
<span data-ttu-id="d218a-130">JSON 템플릿 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-130">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d218a-131">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="d218a-131">-TemplateParameterFile</span></span>
<span data-ttu-id="d218a-132">템플릿 매개 변수의 이름 및 값이 포함 된 JSON 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-132">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d218a-133">------# Parameterobject</span><span class="sxs-lookup"><span data-stu-id="d218a-133">-TemplateParameterObject</span></span>
<span data-ttu-id="d218a-134">템플릿 매개 변수 이름 및 값의 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-134">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d218a-135">--# Parameteruri</span><span class="sxs-lookup"><span data-stu-id="d218a-135">-TemplateParameterUri</span></span>
<span data-ttu-id="d218a-136">템플릿 매개 변수 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-136">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d218a-137">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="d218a-137">-TemplateUri</span></span>
<span data-ttu-id="d218a-138">JSON 템플릿 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-138">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d218a-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d218a-139">-DefaultProfile</span></span>
<span data-ttu-id="d218a-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d218a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d218a-141">CommonParameters</span></span>
<span data-ttu-id="d218a-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d218a-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d218a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d218a-144">입력</span><span class="sxs-lookup"><span data-stu-id="d218a-144">INPUTS</span></span>

## <span data-ttu-id="d218a-145">출력</span><span class="sxs-lookup"><span data-stu-id="d218a-145">OUTPUTS</span></span>

### <span data-ttu-id="d218a-146">System.webserver. List ' 1 [SdkModels. t e PSResourceManagerError]를 목록으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d218a-146">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="d218a-147">상속자</span><span class="sxs-lookup"><span data-stu-id="d218a-147">NOTES</span></span>

## <span data-ttu-id="d218a-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d218a-148">RELATED LINKS</span></span>

[<span data-ttu-id="d218a-149">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d218a-149">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d218a-150">새로운 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d218a-150">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d218a-151">제거-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d218a-151">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d218a-152">중지-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d218a-152">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


