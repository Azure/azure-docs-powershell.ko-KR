---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 5020ddeccc755ef52bf7410d61eb57b637d261bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495609"
---
# <span data-ttu-id="cddb1-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cddb1-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="cddb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cddb1-102">SYNOPSIS</span></span>
<span data-ttu-id="cddb1-103">데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-103">Creates a data factory.</span></span>

## <span data-ttu-id="cddb1-104">구문</span><span class="sxs-lookup"><span data-stu-id="cddb1-104">SYNTAX</span></span>

### <span data-ttu-id="cddb1-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="cddb1-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cddb1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cddb1-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cddb1-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="cddb1-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cddb1-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="cddb1-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cddb1-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="cddb1-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cddb1-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="cddb1-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cddb1-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cddb1-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cddb1-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="cddb1-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cddb1-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="cddb1-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cddb1-114">설명</span><span class="sxs-lookup"><span data-stu-id="cddb1-114">DESCRIPTION</span></span>
<span data-ttu-id="cddb1-115">**Set-AzDataFactoryV2** cmdlet은 지정된 리소스 그룹 이름 및 위치를 사용하여 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="cddb1-116">다음 순서로 이러한 작업을 수행 합니다. -- 데이터 팩터리 만들기.</span><span class="sxs-lookup"><span data-stu-id="cddb1-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="cddb1-117">-- 연결된 서비스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-117">-- Create linked services.</span></span>
<span data-ttu-id="cddb1-118">-- 데이터 세트를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-118">-- Create datasets.</span></span>
<span data-ttu-id="cddb1-119">-- 파이프라인을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="cddb1-120">예제</span><span class="sxs-lookup"><span data-stu-id="cddb1-120">EXAMPLES</span></span>

### <span data-ttu-id="cddb1-121">예제 1: 데이터 팩터리 만들기</span><span class="sxs-lookup"><span data-stu-id="cddb1-121">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration :
```

### <span data-ttu-id="cddb1-122">예제 2: 기존 팩터리 개체를 사용하여 리포지토리 구성 세부 정보가 있는 데이터 팩터리 만들기</span><span class="sxs-lookup"><span data-stu-id="cddb1-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" | Set-AzDataFactoryV2 -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder / -ProjectName "Azure Data Factory"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryVSTSConfiguration
```

<span data-ttu-id="cddb1-123">이 명령은 Azure DevOps 소스 제어 구성을 사용하여 EastUS 위치에 있는 ADF라는 리소스 그룹에 WikiADF라는 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="cddb1-124">예제 3: 새 팩터리 개체를 사용하여 GitHub 리포지토리 구성 세부 정보가 있는 데이터 팩터리 만들기</span><span class="sxs-lookup"><span data-stu-id="cddb1-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
```
PS C:\> New-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location 'EastUS' -HostName 'https://github.com' -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder /

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryGitHubConfiguration
```

<span data-ttu-id="cddb1-125">이 명령은 GitHub 소스 제어 구성을 사용하여 EastUS 위치에 있는 ADF라는 리소스 그룹에 WikiADF라는 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="cddb1-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cddb1-126">PARAMETERS</span></span>

### <span data-ttu-id="cddb1-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cddb1-127">-AccountName</span></span>
<span data-ttu-id="cddb1-128">리포지타이어 구성에 대한 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-128">The account name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="cddb1-129">-CollaborationBranch</span></span>
<span data-ttu-id="cddb1-130">리포지타이지 구성을 위한 공동 작업 분기입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-130">The collaboration branch for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cddb1-131">-DefaultProfile</span></span>
<span data-ttu-id="cddb1-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cddb1-133">-Force</span><span class="sxs-lookup"><span data-stu-id="cddb1-133">-Force</span></span>
<span data-ttu-id="cddb1-134">확인 메시지를 표시하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cddb1-135">-GlobalParameterDefinition</span><span class="sxs-lookup"><span data-stu-id="cddb1-135">-GlobalParameterDefinition</span></span>
<span data-ttu-id="cddb1-136">데이터 팩터리의 전역 매개 변수를 포함하는 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-136">The dictionary containing the global parameters of the data factory.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="cddb1-137">-HostName</span></span>
<span data-ttu-id="cddb1-138">GitHub 리포지터리포지터 구성의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-138">The host name for GitHub repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cddb1-139">-InputObject</span></span>
<span data-ttu-id="cddb1-140">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-140">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-141">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="cddb1-141">-LastCommitId</span></span>
<span data-ttu-id="cddb1-142">리포지토리 구성에 대한 마지막 커밋 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-142">The last commit id for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-143">-Location</span><span class="sxs-lookup"><span data-stu-id="cddb1-143">-Location</span></span>
<span data-ttu-id="cddb1-144">데이터 팩터리가 이 지역에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-144">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-145">-Name</span><span class="sxs-lookup"><span data-stu-id="cddb1-145">-Name</span></span>
<span data-ttu-id="cddb1-146">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-146">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-147">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="cddb1-147">-ProjectName</span></span>
<span data-ttu-id="cddb1-148">프로젝트 이름은 리포지터 구성을 위한 Azure DevOps입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-148">The project name Azure DevOps for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-149">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="cddb1-149">-RepositoryName</span></span>
<span data-ttu-id="cddb1-150">리포지토리 구성에 대한 리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-150">The repository name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cddb1-151">-ResourceGroupName</span></span>
<span data-ttu-id="cddb1-152">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-152">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cddb1-153">-ResourceId</span></span>
<span data-ttu-id="cddb1-154">V2 데이터 팩터리의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-154">The Azure resource ID of V2 data factory.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig
Aliases: Id, DataFactoryId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-155">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="cddb1-155">-RootFolder</span></span>
<span data-ttu-id="cddb1-156">리포지방 구성에 대한 루트 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-156">The root folder for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="cddb1-157">-Tag</span></span>
<span data-ttu-id="cddb1-158">데이터 팩터리의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-158">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-159">-TenantId</span><span class="sxs-lookup"><span data-stu-id="cddb1-159">-TenantId</span></span>
<span data-ttu-id="cddb1-160">Azure DevOps 리포지터 구성에 대한 테넌트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-160">The tenant id for Azure DevOps repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddb1-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cddb1-161">-Confirm</span></span>
<span data-ttu-id="cddb1-162">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cddb1-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cddb1-163">-WhatIf</span></span>
<span data-ttu-id="cddb1-164">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="cddb1-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cddb1-165">CommonParameters</span></span>
<span data-ttu-id="cddb1-166">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cddb1-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cddb1-167">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cddb1-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cddb1-168">입력</span><span class="sxs-lookup"><span data-stu-id="cddb1-168">INPUTS</span></span>

### <span data-ttu-id="cddb1-169">System.String</span><span class="sxs-lookup"><span data-stu-id="cddb1-169">System.String</span></span>

### <span data-ttu-id="cddb1-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cddb1-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="cddb1-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="cddb1-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cddb1-172">출력</span><span class="sxs-lookup"><span data-stu-id="cddb1-172">OUTPUTS</span></span>

### <span data-ttu-id="cddb1-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cddb1-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="cddb1-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cddb1-174">NOTES</span></span>
<span data-ttu-id="cddb1-175">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="cddb1-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cddb1-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cddb1-176">RELATED LINKS</span></span>

[<span data-ttu-id="cddb1-177">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cddb1-177">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="cddb1-178">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cddb1-178">Remove-AzDataFactoryV2</span></span>]()
