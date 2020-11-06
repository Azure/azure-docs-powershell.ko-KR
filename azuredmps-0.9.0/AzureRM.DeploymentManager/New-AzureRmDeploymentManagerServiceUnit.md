---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e732463984088bbcb507eb55594f7de2114d25d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523087"
---
# <span data-ttu-id="83fe7-101">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="83fe7-101">New-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="83fe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="83fe7-103">서비스 토폴로지의 서비스에서 새 서비스 단위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-103">Creates a new service unit under a service in a service topology.</span></span>

## <span data-ttu-id="83fe7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83fe7-104">SYNTAX</span></span>

### <span data-ttu-id="83fe7-105">ByTopologyAndServiceNames (기본값)</span><span class="sxs-lookup"><span data-stu-id="83fe7-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83fe7-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="83fe7-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopology] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83fe7-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="83fe7-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83fe7-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="83fe7-108">ByServiceObject</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-Service] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83fe7-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="83fe7-109">ByServiceResourceId</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83fe7-110">설명은</span><span class="sxs-lookup"><span data-stu-id="83fe7-110">DESCRIPTION</span></span>
<span data-ttu-id="83fe7-111">**AzureRmDeploymentManagerServiceUnit** cmdlet은 서비스 토폴로지의 서비스 아래에 서비스를 만들고 해당 서비스 단위를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-111">The **New-AzureRmDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="83fe7-112">서비스 단위를 이름, 서비스 이름, 서비스 토폴로지, 그리고 리소스 그룹 이름으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="83fe7-113">Cmdlet은 ServiceUnit 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="83fe7-114">이 개체를 로컬로 수정한 다음 Set-AzureRmDeploymentManagerService cmdlet을 사용 하 여 서비스에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="83fe7-115">예제의</span><span class="sxs-lookup"><span data-stu-id="83fe7-115">EXAMPLES</span></span>

### <span data-ttu-id="83fe7-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="83fe7-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="83fe7-117">이 cmdlet은 ContosoResourceGroup의 서비스 ContosoService2에서 ContosoServiceTopology에 있는 ContosoService2Storage 이름으로 새 서비스 단위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="83fe7-118">템플릿 및 매개 변수 파일은 서비스 토폴로지 ContosoServiceTopology에서 참조 하는 아티팩트 원본 위치에 대 한 상대 경로로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="83fe7-119">이 템플릿에 정의 된 리소스는 배포 모드가 점진적으로 설정 된 대상 리소스 그룹 service2ResourceGroup에 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="83fe7-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="83fe7-120">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="83fe7-121">이 cmdlet은 ContosoResourceGroup의 서비스 ContosoService2에서 ContosoServiceTopology에 있는 ContosoService2Storage 이름으로 새 서비스 단위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="83fe7-122">템플릿 및 매개 변수 참조는 아티팩트 원본 ResourceId로 제공 되며, 서비스 토폴로지 ContosoServiceTopology1에는 Uri가 제공 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="83fe7-123">이 템플릿에 정의 된 리소스는 배포 모드가 완료로 설정 된 대상 리소스 그룹 service2ResourceGroup에 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="83fe7-124">변수</span><span class="sxs-lookup"><span data-stu-id="83fe7-124">PARAMETERS</span></span>

### <span data-ttu-id="83fe7-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83fe7-125">-AsJob</span></span>
<span data-ttu-id="83fe7-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="83fe7-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83fe7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83fe7-127">-DefaultProfile</span></span>
<span data-ttu-id="83fe7-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83fe7-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="83fe7-129">-DeploymentMode</span></span>
<span data-ttu-id="83fe7-130">서비스 단위에 리소스를 배포할 때 사용 하는 배포 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe7-131">-위치</span><span class="sxs-lookup"><span data-stu-id="83fe7-131">-Location</span></span>
<span data-ttu-id="83fe7-132">서비스 단위 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="83fe7-133">-이름</span><span class="sxs-lookup"><span data-stu-id="83fe7-133">-Name</span></span>
<span data-ttu-id="83fe7-134">서비스 단위의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-134">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe7-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="83fe7-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="83fe7-136">서비스 단위에 리소스를 배포할 때 사용 하는 배포 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-136">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="83fe7-137">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="83fe7-137">-ParametersUri</span></span>
<span data-ttu-id="83fe7-138">서비스 단위에 리소스를 배포할 때 사용 하는 배포 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-138">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="83fe7-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83fe7-139">-ResourceGroupName</span></span>
<span data-ttu-id="83fe7-140">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="83fe7-140">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe7-141">-서비스</span><span class="sxs-lookup"><span data-stu-id="83fe7-141">-Service</span></span>
<span data-ttu-id="83fe7-142">서비스 단위를 만들 서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-142">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe7-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="83fe7-143">-ServiceName</span></span>
<span data-ttu-id="83fe7-144">이 서비스 단위를 포함 하는 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-144">The name of the service this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe7-145">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="83fe7-145">-ServiceResourceId</span></span>
<span data-ttu-id="83fe7-146">서비스 단위를 만들 서비스 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-146">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe7-147">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="83fe7-147">-ServiceTopology</span></span>
<span data-ttu-id="83fe7-148">서비스 단위를 만들 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-148">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe7-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="83fe7-149">-ServiceTopologyName</span></span>
<span data-ttu-id="83fe7-150">이 서비스 단위를 포함 하는 서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-150">The name of the serivce topology this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe7-151">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="83fe7-151">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="83fe7-152">서비스 단위를 만들 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-152">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe7-153">태그</span><span class="sxs-lookup"><span data-stu-id="83fe7-153">-Tag</span></span>
<span data-ttu-id="83fe7-154">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-154">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83fe7-155">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="83fe7-155">-TargetResourceGroup</span></span>
<span data-ttu-id="83fe7-156">서비스 단위 아래의 리소스가 배포 되는 위치를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-156">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="83fe7-157">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="83fe7-157">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="83fe7-158">서비스 단위에 리소스를 배포할 때 사용 하는 배포 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-158">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="83fe7-159">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="83fe7-159">-TemplateUri</span></span>
<span data-ttu-id="83fe7-160">서비스 단위에 리소스를 배포할 때 사용 하는 배포 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-160">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="83fe7-161">-확인</span><span class="sxs-lookup"><span data-stu-id="83fe7-161">-Confirm</span></span>
<span data-ttu-id="83fe7-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83fe7-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83fe7-163">-WhatIf</span></span>
<span data-ttu-id="83fe7-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83fe7-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83fe7-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83fe7-166">CommonParameters</span></span>
<span data-ttu-id="83fe7-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83fe7-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83fe7-168">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83fe7-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83fe7-169">입력</span><span class="sxs-lookup"><span data-stu-id="83fe7-169">INPUTS</span></span>

### <span data-ttu-id="83fe7-170">않아야</span><span class="sxs-lookup"><span data-stu-id="83fe7-170">None</span></span>

## <span data-ttu-id="83fe7-171">출력</span><span class="sxs-lookup"><span data-stu-id="83fe7-171">OUTPUTS</span></span>

### <span data-ttu-id="83fe7-172">Microsoft. Azure. Psservicemanager 리소스</span><span class="sxs-lookup"><span data-stu-id="83fe7-172">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="83fe7-173">상속자</span><span class="sxs-lookup"><span data-stu-id="83fe7-173">NOTES</span></span>

## <span data-ttu-id="83fe7-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83fe7-174">RELATED LINKS</span></span>

[<span data-ttu-id="83fe7-175">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="83fe7-175">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="83fe7-176">제거-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="83fe7-176">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="83fe7-177">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="83fe7-177">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)