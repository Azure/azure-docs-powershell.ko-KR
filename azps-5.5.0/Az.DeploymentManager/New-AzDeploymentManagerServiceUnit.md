---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 9a03dd861ee380b0ab01348e01091844240bfc04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208629"
---
# <span data-ttu-id="df840-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="df840-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="df840-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df840-102">SYNOPSIS</span></span>
<span data-ttu-id="df840-103">지정된 서비스 및 서비스 토폴로지 아래에 서비스 단위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="df840-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="df840-104">구문</span><span class="sxs-lookup"><span data-stu-id="df840-104">SYNTAX</span></span>

### <span data-ttu-id="df840-105">ByTopologyAndServiceNames(기본값)</span><span class="sxs-lookup"><span data-stu-id="df840-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df840-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="df840-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df840-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="df840-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df840-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="df840-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df840-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="df840-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df840-110">설명</span><span class="sxs-lookup"><span data-stu-id="df840-110">DESCRIPTION</span></span>
<span data-ttu-id="df840-111">**New-AzDeploymentManagerServiceUnit** cmdlet은 서비스 토폴로지의 서비스 아래에 서비스를 만들고 해당 서비스 단위를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="df840-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="df840-112">이름, 서비스 이름, 서비스 토폴로지 및 리소스 그룹 이름으로 서비스 단위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df840-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="df840-113">cmdlet은 ServiceUnit 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="df840-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="df840-114">이 개체를 로컬로 수정한 다음, Set-AzDeploymentManagerService cmdlet을 사용하여 서비스에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df840-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="df840-115">예제</span><span class="sxs-lookup"><span data-stu-id="df840-115">EXAMPLES</span></span>

### <span data-ttu-id="df840-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="df840-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="df840-117">이 cmdlet은 미국 중부 위치에 있는 토폴로지 ContosoServiceTopology의 ContosoService2 서비스 아래에 ContosoResourceGroup에 ContosoService2Storage 이름이 있는 새 서비스 단위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="df840-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="df840-118">템플릿 및 매개 변수 파일은 서비스 토폴로지 ContosoServiceTopology에서 참조되는 아티팩트 원본 위치에 대한 상대 경로로 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="df840-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="df840-119">이 템플릿에 정의된 리소스는 배포 모드가 증분으로 설정된 대상 리소스 그룹 service2ResourceGroup에 배포됩니다.</span><span class="sxs-lookup"><span data-stu-id="df840-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="df840-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="df840-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="df840-121">이 cmdlet은 미국 중부 위치에 있는 토폴로지 ContosoServiceTopology의 ContosoService2 서비스 아래에 ContosoResourceGroup에 ContosoService2Storage 이름이 있는 새 서비스 단위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="df840-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="df840-122">템플릿 및 매개 변수 참조는 서비스 토폴로지 ContosoServiceTopology1에서 제공되지 않은 아티팩트 원본 ResourceId로 SAS Uri로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="df840-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="df840-123">이 템플릿에 정의된 리소스는 배포 모드가 완료로 설정된 대상 리소스 그룹 service2ResourceGroup에 배포됩니다.</span><span class="sxs-lookup"><span data-stu-id="df840-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="df840-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df840-124">PARAMETERS</span></span>

### <span data-ttu-id="df840-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df840-125">-AsJob</span></span>
<span data-ttu-id="df840-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="df840-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df840-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df840-127">-DefaultProfile</span></span>
<span data-ttu-id="df840-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df840-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="df840-129">-DeploymentMode</span></span>
<span data-ttu-id="df840-130">서비스 단위에서 리소스를 배포할 때 사용할 배포 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="df840-131">-Location</span><span class="sxs-lookup"><span data-stu-id="df840-131">-Location</span></span>
<span data-ttu-id="df840-132">서비스 단위 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="df840-133">-Name</span><span class="sxs-lookup"><span data-stu-id="df840-133">-Name</span></span>
<span data-ttu-id="df840-134">서비스 단위의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="df840-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="df840-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="df840-136">아티팩트 원본과 상대적인 매개 변수 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="df840-137">ServiceTopology에서 ArtifactSource를 참조해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="df840-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="df840-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="df840-138">-ParametersUri</span></span>
<span data-ttu-id="df840-139">매개 변수 파일에 대한 SAS Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="df840-140">ArtifactSourceId가 ServiceTopology에서 참조된 경우 ParametersArtifactSourceRelativePath를 사용하여 상대 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df840-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="df840-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df840-141">-ResourceGroupName</span></span>
<span data-ttu-id="df840-142">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-142">The resource group.</span></span>

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

### <span data-ttu-id="df840-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="df840-143">-ServiceName</span></span>
<span data-ttu-id="df840-144">이 서비스 단위의 일부인 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="df840-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="df840-145">-ServiceObject</span></span>
<span data-ttu-id="df840-146">서비스 단위를 만들어야 하는 서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-146">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="df840-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="df840-147">-ServiceResourceId</span></span>
<span data-ttu-id="df840-148">서비스 단위를 만들어야 하는 서비스 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-148">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="df840-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="df840-149">-ServiceTopologyName</span></span>
<span data-ttu-id="df840-150">이 서비스 단위는 서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-150">The name of the service topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="df840-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="df840-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="df840-152">서비스 단위를 만들어야 하는 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-152">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="df840-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="df840-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="df840-154">서비스 단위를 만들어야 하는 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-154">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="df840-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="df840-155">-Tag</span></span>
<span data-ttu-id="df840-156">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-156">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="df840-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="df840-157">-TargetResourceGroup</span></span>
<span data-ttu-id="df840-158">서비스 단위의 리소스가 배포되는 위치를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="df840-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="df840-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="df840-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="df840-160">아티팩트 원본을 상대로 하는 템플릿 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="df840-161">ServiceTopology에서 ArtifactSource를 참조해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="df840-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="df840-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="df840-162">-TemplateUri</span></span>
<span data-ttu-id="df840-163">템플릿 파일에 대한 SAS URI입니다.</span><span class="sxs-lookup"><span data-stu-id="df840-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="df840-164">ArtifactSourceId가 ServiceTopology에서 참조된 경우 TemplateArtifactSourceRelativePath를 사용하여 상대 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df840-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="df840-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df840-165">-Confirm</span></span>
<span data-ttu-id="df840-166">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="df840-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df840-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df840-167">-WhatIf</span></span>
<span data-ttu-id="df840-168">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="df840-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df840-169">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df840-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df840-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df840-170">CommonParameters</span></span>
<span data-ttu-id="df840-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df840-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df840-172">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="df840-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df840-173">입력</span><span class="sxs-lookup"><span data-stu-id="df840-173">INPUTS</span></span>

### <span data-ttu-id="df840-174">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="df840-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="df840-175">출력</span><span class="sxs-lookup"><span data-stu-id="df840-175">OUTPUTS</span></span>

### <span data-ttu-id="df840-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="df840-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="df840-177">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df840-177">NOTES</span></span>

## <span data-ttu-id="df840-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df840-178">RELATED LINKS</span></span>
