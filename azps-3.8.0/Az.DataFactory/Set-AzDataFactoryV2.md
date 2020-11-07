---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 219e5b18a04332d2ee840fb41b92aa9d282a1792
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879393"
---
# <span data-ttu-id="862b7-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="862b7-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="862b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="862b7-102">SYNOPSIS</span></span>
<span data-ttu-id="862b7-103">Data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-103">Creates a data factory.</span></span>

## <span data-ttu-id="862b7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="862b7-104">SYNTAX</span></span>

### <span data-ttu-id="862b7-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="862b7-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862b7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="862b7-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862b7-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="862b7-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862b7-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="862b7-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="862b7-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="862b7-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="862b7-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="862b7-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862b7-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="862b7-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862b7-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="862b7-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862b7-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="862b7-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="862b7-114">설명은</span><span class="sxs-lookup"><span data-stu-id="862b7-114">DESCRIPTION</span></span>
<span data-ttu-id="862b7-115">**AzDataFactoryV2** cmdlet은 지정 된 리소스 그룹 이름 및 위치를 사용 하 여 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="862b7-116">다음 순서 대로 이러한 작업을 수행 합니다.--data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="862b7-117">--연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-117">-- Create linked services.</span></span>
<span data-ttu-id="862b7-118">--데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-118">-- Create datasets.</span></span>
<span data-ttu-id="862b7-119">--파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="862b7-120">예제의</span><span class="sxs-lookup"><span data-stu-id="862b7-120">EXAMPLES</span></span>

### <span data-ttu-id="862b7-121">예제 1: data factory 만들기</span><span class="sxs-lookup"><span data-stu-id="862b7-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="862b7-122">예제 2: 기존 factory 개체를 사용 하 여 리포지토리 구성 세부 정보를 사용 하 여 데이터 팩터리 만들기</span><span class="sxs-lookup"><span data-stu-id="862b7-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
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

<span data-ttu-id="862b7-123">이 명령은 Azure DevOps 원본 컨트롤 구성을 사용 하 여 t e Us 위치에 ADF 라는 리소스 그룹에 WikiADF 라는 data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="862b7-124">예제 3: 새 팩토리 개체를 사용 하 여 GitHub 리포지토리 구성 세부 정보를 사용 하 여 데이터 팩터리 만들기</span><span class="sxs-lookup"><span data-stu-id="862b7-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
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

<span data-ttu-id="862b7-125">이 명령은 GitHub 원본 컨트롤 구성을 사용 하 여 WikiADF 이라는 리소스 그룹에 t e t e 위치에 있는 data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="862b7-126">변수</span><span class="sxs-lookup"><span data-stu-id="862b7-126">PARAMETERS</span></span>

### <span data-ttu-id="862b7-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="862b7-127">-AccountName</span></span>
<span data-ttu-id="862b7-128">리포지토리 구성의 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-128">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="862b7-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="862b7-129">-CollaborationBranch</span></span>
<span data-ttu-id="862b7-130">리포지토리 구성에 대 한 공동 작업 분기입니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-130">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="862b7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="862b7-131">-DefaultProfile</span></span>
<span data-ttu-id="862b7-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="862b7-133">-Force</span><span class="sxs-lookup"><span data-stu-id="862b7-133">-Force</span></span>
<span data-ttu-id="862b7-134">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="862b7-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="862b7-135">-HostName</span></span>
<span data-ttu-id="862b7-136">GitHub 리포지토리 구성의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-136">The host name for GitHub repo configuration.</span></span>

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

### <span data-ttu-id="862b7-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="862b7-137">-InputObject</span></span>
<span data-ttu-id="862b7-138">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-138">The data factory object.</span></span>

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

### <span data-ttu-id="862b7-139">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="862b7-139">-LastCommitId</span></span>
<span data-ttu-id="862b7-140">리포지토리 구성의 마지막 커밋 id입니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-140">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="862b7-141">-위치</span><span class="sxs-lookup"><span data-stu-id="862b7-141">-Location</span></span>
<span data-ttu-id="862b7-142">이 지역에 데이터 팩터리가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-142">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="862b7-143">-이름</span><span class="sxs-lookup"><span data-stu-id="862b7-143">-Name</span></span>
<span data-ttu-id="862b7-144">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-144">The data factory name.</span></span>

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

### <span data-ttu-id="862b7-145">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="862b7-145">-ProjectName</span></span>
<span data-ttu-id="862b7-146">리포지토리 구성에 대 한 project name Azure DevOps입니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-146">The project name Azure DevOps for repo configuration.</span></span>

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

### <span data-ttu-id="862b7-147">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="862b7-147">-RepositoryName</span></span>
<span data-ttu-id="862b7-148">리포지토리 구성의 리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-148">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="862b7-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="862b7-149">-ResourceGroupName</span></span>
<span data-ttu-id="862b7-150">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-150">The resource group name.</span></span>

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

### <span data-ttu-id="862b7-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="862b7-151">-ResourceId</span></span>
<span data-ttu-id="862b7-152">Azure 리소스 팩토리 (V2 data factory)</span><span class="sxs-lookup"><span data-stu-id="862b7-152">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="862b7-153">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="862b7-153">-RootFolder</span></span>
<span data-ttu-id="862b7-154">리포지토리 구성에 대 한 루트 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-154">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="862b7-155">태그</span><span class="sxs-lookup"><span data-stu-id="862b7-155">-Tag</span></span>
<span data-ttu-id="862b7-156">Data factory의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-156">The tags of the data factory.</span></span>

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

### <span data-ttu-id="862b7-157">-TenantId</span><span class="sxs-lookup"><span data-stu-id="862b7-157">-TenantId</span></span>
<span data-ttu-id="862b7-158">Azure DevOps 리포지토리의 구성에 대 한 테 넌 트 id입니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-158">The tenant id for Azure DevOps repo configuration.</span></span>

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

### <span data-ttu-id="862b7-159">-확인</span><span class="sxs-lookup"><span data-stu-id="862b7-159">-Confirm</span></span>
<span data-ttu-id="862b7-160">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="862b7-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="862b7-161">-WhatIf</span></span>
<span data-ttu-id="862b7-162">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-162">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="862b7-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="862b7-163">CommonParameters</span></span>
<span data-ttu-id="862b7-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="862b7-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="862b7-165">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="862b7-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="862b7-166">입력</span><span class="sxs-lookup"><span data-stu-id="862b7-166">INPUTS</span></span>

### <span data-ttu-id="862b7-167">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="862b7-167">System.String</span></span>

### <span data-ttu-id="862b7-168">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="862b7-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="862b7-169">출력</span><span class="sxs-lookup"><span data-stu-id="862b7-169">OUTPUTS</span></span>

### <span data-ttu-id="862b7-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="862b7-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="862b7-171">상속자</span><span class="sxs-lookup"><span data-stu-id="862b7-171">NOTES</span></span>
<span data-ttu-id="862b7-172">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="862b7-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="862b7-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="862b7-173">RELATED LINKS</span></span>

[<span data-ttu-id="862b7-174">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="862b7-174">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="862b7-175">제거-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="862b7-175">Remove-AzDataFactoryV2</span></span>]()
