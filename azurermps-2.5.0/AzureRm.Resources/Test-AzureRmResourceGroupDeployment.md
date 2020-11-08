---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 97fbda90b27cbfabca8cbfd21c5bf375b86f7adb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881685"
---
# <span data-ttu-id="2918b-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2918b-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="2918b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2918b-102">SYNOPSIS</span></span>
<span data-ttu-id="2918b-103">리소스 그룹 배포의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2918b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2918b-104">SYNTAX</span></span>

### <span data-ttu-id="2918b-105">By서식 Filewithnoparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="2918b-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateFile <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2918b-106">By서식 Fileandparameterobject</span><span class="sxs-lookup"><span data-stu-id="2918b-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2918b-107">By서식 Uriandparameterobject</span><span class="sxs-lookup"><span data-stu-id="2918b-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2918b-108">By서식 파일 Andparameterfile</span><span class="sxs-lookup"><span data-stu-id="2918b-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2918b-109">By서식 Uriandparameterfile</span><span class="sxs-lookup"><span data-stu-id="2918b-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2918b-110">By서식 Fileandparameteruri</span><span class="sxs-lookup"><span data-stu-id="2918b-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2918b-111">By서식 Uriandparameteruri</span><span class="sxs-lookup"><span data-stu-id="2918b-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2918b-112">By서식 Uriwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="2918b-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateUri <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2918b-113">설명은</span><span class="sxs-lookup"><span data-stu-id="2918b-113">DESCRIPTION</span></span>
<span data-ttu-id="2918b-114">**AzureRmResourceGroupDeployment** Cmdlet은 Azure 리소스 그룹 배포 템플릿과 해당 매개 변수 값이 유효한 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="2918b-115">예제의</span><span class="sxs-lookup"><span data-stu-id="2918b-115">EXAMPLES</span></span>

## <span data-ttu-id="2918b-116">변수</span><span class="sxs-lookup"><span data-stu-id="2918b-116">PARAMETERS</span></span>

### <span data-ttu-id="2918b-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2918b-117">-ApiVersion</span></span>
<span data-ttu-id="2918b-118">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2918b-119">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="2918b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2918b-120">-DefaultProfile</span></span>
<span data-ttu-id="2918b-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2918b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2918b-122">-모드</span><span class="sxs-lookup"><span data-stu-id="2918b-122">-Mode</span></span>
<span data-ttu-id="2918b-123">배포 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="2918b-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2918b-125">진행</span><span class="sxs-lookup"><span data-stu-id="2918b-125">Incremental</span></span>
- <span data-ttu-id="2918b-126">마칠</span><span class="sxs-lookup"><span data-stu-id="2918b-126">Complete</span></span>

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

### <span data-ttu-id="2918b-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="2918b-127">-Pre</span></span>
<span data-ttu-id="2918b-128">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2918b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2918b-129">-ResourceGroupName</span></span>
<span data-ttu-id="2918b-130">테스트할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="2918b-131">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="2918b-131">-RollBackDeploymentName</span></span>
<span data-ttu-id="2918b-132">-RollbackToLastDeployment가 사용 되는 경우 리소스 그룹에서 지정 된 이름을 사용 하 여 성공한 배포로 롤백할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-132">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2918b-133">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="2918b-133">-RollbackToLastDeployment</span></span>
<span data-ttu-id="2918b-134">-RollBackDeploymentName가 사용 되는 경우 리소스 그룹에서 마지막으로 성공한 배포에 롤백하는 것으로 표시 되지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-134">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="2918b-135">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="2918b-135">-TemplateFile</span></span>
<span data-ttu-id="2918b-136">JSON 템플릿 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-136">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2918b-137">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="2918b-137">-TemplateParameterFile</span></span>
<span data-ttu-id="2918b-138">템플릿 매개 변수의 이름 및 값이 포함 된 JSON 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-138">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2918b-139">------# Parameterobject</span><span class="sxs-lookup"><span data-stu-id="2918b-139">-TemplateParameterObject</span></span>
<span data-ttu-id="2918b-140">템플릿 매개 변수 이름 및 값의 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-140">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2918b-141">--# Parameteruri</span><span class="sxs-lookup"><span data-stu-id="2918b-141">-TemplateParameterUri</span></span>
<span data-ttu-id="2918b-142">템플릿 매개 변수 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-142">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2918b-143">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="2918b-143">-TemplateUri</span></span>
<span data-ttu-id="2918b-144">JSON 템플릿 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-144">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2918b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2918b-145">CommonParameters</span></span>
<span data-ttu-id="2918b-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2918b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2918b-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2918b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2918b-148">입력</span><span class="sxs-lookup"><span data-stu-id="2918b-148">INPUTS</span></span>

### <span data-ttu-id="2918b-149">않아야</span><span class="sxs-lookup"><span data-stu-id="2918b-149">None</span></span>

## <span data-ttu-id="2918b-150">출력</span><span class="sxs-lookup"><span data-stu-id="2918b-150">OUTPUTS</span></span>

### <span data-ttu-id="2918b-151">PSResourceManagerError/. m m.</span><span class="sxs-lookup"><span data-stu-id="2918b-151">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceManagerError</span></span>

## <span data-ttu-id="2918b-152">상속자</span><span class="sxs-lookup"><span data-stu-id="2918b-152">NOTES</span></span>

## <span data-ttu-id="2918b-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2918b-153">RELATED LINKS</span></span>

[<span data-ttu-id="2918b-154">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2918b-154">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2918b-155">새로운 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2918b-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2918b-156">제거-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2918b-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2918b-157">중지-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2918b-157">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

