---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 5c4b418812c6cbe3ee1b5e1f8ee82baa05723f86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962160"
---
# <span data-ttu-id="b2f2f-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b2f2f-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="b2f2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f2f-103">지정된 서비스 및 서비스 토폴로지 아래에 서비스 단위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="b2f2f-104">구문</span><span class="sxs-lookup"><span data-stu-id="b2f2f-104">SYNTAX</span></span>

### <span data-ttu-id="b2f2f-105">ByTopologyAndServiceNames(기본값)</span><span class="sxs-lookup"><span data-stu-id="b2f2f-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2f2f-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="b2f2f-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2f2f-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="b2f2f-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2f2f-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="b2f2f-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2f2f-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="b2f2f-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2f2f-110">설명</span><span class="sxs-lookup"><span data-stu-id="b2f2f-110">DESCRIPTION</span></span>
<span data-ttu-id="b2f2f-111">**New-AzDeploymentManagerServiceUnit** cmdlet은 서비스 토폴로지에서 서비스 아래에 서비스를 만들고 해당 서비스 단위를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="b2f2f-112">서비스 단위를 이름, 서비스 이름, 있는 서비스 토폴로지 및 리소스 그룹 이름으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="b2f2f-113">cmdlet은 ServiceUnit 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="b2f2f-114">이 개체를 로컬로 수정한 다음, cmdlet을 사용하여 서비스에 Set-AzDeploymentManagerService 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="b2f2f-115">예제</span><span class="sxs-lookup"><span data-stu-id="b2f2f-115">EXAMPLES</span></span>

### <span data-ttu-id="b2f2f-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="b2f2f-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="b2f2f-117">이 cmdlet은 미국 중부의 토폴로지 ContosoServiceTopology의 ContosoServiceTopology의 ContosoService2 서비스 아래에 ContosoResourceGroup에 ContosoService2Storage 이름이 있는 새 서비스 단위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="b2f2f-118">템플릿 및 매개 변수 파일은 서비스 토폴로지 ContosoServiceTopology에서 참조하는 아티팩트 원본 위치에 대한 상대 경로로 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="b2f2f-119">이 템플릿에 정의된 리소스는 대상 리소스 그룹 service2ResourceGroup에 배포 모드가 증분으로 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="b2f2f-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="b2f2f-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="b2f2f-121">이 cmdlet은 미국 중부의 토폴로지 ContosoServiceTopology의 ContosoServiceTopology의 ContosoService2 서비스 아래에 ContosoResourceGroup에 ContosoService2Storage 이름이 있는 새 서비스 단위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="b2f2f-122">템플릿 및 매개 변수 참조는 SAS Uri의 아티팩트 원본 ResourceId가 Service 토폴로지 ContosoServiceTopology1에 제공되지 않은 것으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="b2f2f-123">이 템플릿에 정의된 리소스는 배포 모드가 완료로 설정된 대상 리소스 그룹 service2ResourceGroup에 배포해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="b2f2f-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b2f2f-124">PARAMETERS</span></span>

### <span data-ttu-id="b2f2f-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2f2f-125">-AsJob</span></span>
<span data-ttu-id="b2f2f-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b2f2f-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2f2f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f2f-127">-DefaultProfile</span></span>
<span data-ttu-id="b2f2f-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2f2f-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="b2f2f-129">-DeploymentMode</span></span>
<span data-ttu-id="b2f2f-130">서비스 단위에서 리소스를 배포할 때 사용할 배포 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="b2f2f-131">-Location</span><span class="sxs-lookup"><span data-stu-id="b2f2f-131">-Location</span></span>
<span data-ttu-id="b2f2f-132">서비스 단위 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="b2f2f-133">-Name</span><span class="sxs-lookup"><span data-stu-id="b2f2f-133">-Name</span></span>
<span data-ttu-id="b2f2f-134">서비스 단위의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="b2f2f-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="b2f2f-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="b2f2f-136">아티팩트 원본을 상대로 하는 매개 변수 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="b2f2f-137">ServiceTopology에서 아티팩트Source를 참조해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="b2f2f-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="b2f2f-138">-ParametersUri</span></span>
<span data-ttu-id="b2f2f-139">매개 변수 파일에 대한 SAS Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="b2f2f-140">아티팩트SourceId가 ServiceTopology에서 참조된 경우 ParametersArtifactSourceRelativePath를 사용하여 상대 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="b2f2f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2f2f-141">-ResourceGroupName</span></span>
<span data-ttu-id="b2f2f-142">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-142">The resource group.</span></span>

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

### <span data-ttu-id="b2f2f-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b2f2f-143">-ServiceName</span></span>
<span data-ttu-id="b2f2f-144">이 서비스 단위의 일부인 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="b2f2f-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="b2f2f-145">-ServiceObject</span></span>
<span data-ttu-id="b2f2f-146">서비스 단위를 만들어야 하는 서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-146">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="b2f2f-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="b2f2f-147">-ServiceResourceId</span></span>
<span data-ttu-id="b2f2f-148">서비스 단위를 만들어야 하는 서비스 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-148">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="b2f2f-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="b2f2f-149">-ServiceTopologyName</span></span>
<span data-ttu-id="b2f2f-150">이 서비스 단위의 서비스 토폴로지 이름은 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-150">The name of the service topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="b2f2f-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="b2f2f-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="b2f2f-152">서비스 단위를 만들어야 하는 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-152">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="b2f2f-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="b2f2f-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="b2f2f-154">서비스 단위를 만들어야 하는 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-154">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="b2f2f-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2f2f-155">-Tag</span></span>
<span data-ttu-id="b2f2f-156">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-156">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="b2f2f-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b2f2f-157">-TargetResourceGroup</span></span>
<span data-ttu-id="b2f2f-158">서비스 단위의 리소스가 배포될 위치를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="b2f2f-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="b2f2f-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="b2f2f-160">아티팩트 원본을 상대로 하는 템플릿 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="b2f2f-161">ServiceTopology에서 아티팩트Source를 참조해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="b2f2f-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b2f2f-162">-TemplateUri</span></span>
<span data-ttu-id="b2f2f-163">템플릿 파일에 대한 SAS Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="b2f2f-164">아티팩트SourceId가 ServiceTopology에서 참조된 경우 TemplateArtifactSourceRelativePath를 사용하여 상대 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="b2f2f-165">-확인</span><span class="sxs-lookup"><span data-stu-id="b2f2f-165">-Confirm</span></span>
<span data-ttu-id="b2f2f-166">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2f2f-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2f2f-167">-WhatIf</span></span>
<span data-ttu-id="b2f2f-168">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2f2f-169">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2f2f-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f2f-170">CommonParameters</span></span>
<span data-ttu-id="b2f2f-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f2f-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f2f-172">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2f2f-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f2f-173">입력</span><span class="sxs-lookup"><span data-stu-id="b2f2f-173">INPUTS</span></span>

### <span data-ttu-id="b2f2f-174">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b2f2f-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b2f2f-175">출력</span><span class="sxs-lookup"><span data-stu-id="b2f2f-175">OUTPUTS</span></span>

### <span data-ttu-id="b2f2f-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="b2f2f-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="b2f2f-177">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b2f2f-177">NOTES</span></span>

## <span data-ttu-id="b2f2f-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2f2f-178">RELATED LINKS</span></span>
