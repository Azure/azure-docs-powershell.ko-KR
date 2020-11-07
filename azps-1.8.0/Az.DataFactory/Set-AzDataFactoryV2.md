---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 374263c26a3572e8d85e18d1795c27a761866a4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868689"
---
# <span data-ttu-id="91cf3-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="91cf3-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="91cf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="91cf3-103">Data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-103">Creates a data factory.</span></span>

## <span data-ttu-id="91cf3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91cf3-104">SYNTAX</span></span>

### <span data-ttu-id="91cf3-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="91cf3-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91cf3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91cf3-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91cf3-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="91cf3-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91cf3-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="91cf3-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91cf3-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="91cf3-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91cf3-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="91cf3-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91cf3-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="91cf3-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91cf3-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="91cf3-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91cf3-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="91cf3-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91cf3-114">설명은</span><span class="sxs-lookup"><span data-stu-id="91cf3-114">DESCRIPTION</span></span>
<span data-ttu-id="91cf3-115">**AzDataFactoryV2** cmdlet은 지정 된 리소스 그룹 이름 및 위치를 사용 하 여 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="91cf3-116">다음 순서 대로 이러한 작업을 수행 합니다.--data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="91cf3-117">--연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-117">-- Create linked services.</span></span>
<span data-ttu-id="91cf3-118">--데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-118">-- Create datasets.</span></span>
<span data-ttu-id="91cf3-119">--파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="91cf3-120">예제의</span><span class="sxs-lookup"><span data-stu-id="91cf3-120">EXAMPLES</span></span>

### <span data-ttu-id="91cf3-121">예제 1: data factory 만들기</span><span class="sxs-lookup"><span data-stu-id="91cf3-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="91cf3-122">예제 2: 기존 factory 개체를 사용 하 여 repoconfiguration 세부 정보를 사용 하 여 데이터 팩토리 만들기</span><span class="sxs-lookup"><span data-stu-id="91cf3-122">Example 2: Create a data factory with repoconfiguration details using an existing factory object.</span></span>
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

<span data-ttu-id="91cf3-123">이 명령은 WestUS 위치에서 ADF 라는 리소스 그룹에 WikiADF 이라는 data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-123">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="91cf3-124">변수</span><span class="sxs-lookup"><span data-stu-id="91cf3-124">PARAMETERS</span></span>

### <span data-ttu-id="91cf3-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="91cf3-125">-AccountName</span></span>
<span data-ttu-id="91cf3-126">리포지토리 구성의 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-126">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="91cf3-127">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="91cf3-127">-CollaborationBranch</span></span>
<span data-ttu-id="91cf3-128">리포지토리 구성에 대 한 공동 작업 분기입니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-128">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="91cf3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91cf3-129">-DefaultProfile</span></span>
<span data-ttu-id="91cf3-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91cf3-131">-Force</span><span class="sxs-lookup"><span data-stu-id="91cf3-131">-Force</span></span>
<span data-ttu-id="91cf3-132">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-132">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="91cf3-133">-HostName</span><span class="sxs-lookup"><span data-stu-id="91cf3-133">-HostName</span></span>
<span data-ttu-id="91cf3-134">리포지토리 구성의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-134">The host name for repo configuration.</span></span>

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

### <span data-ttu-id="91cf3-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91cf3-135">-InputObject</span></span>
<span data-ttu-id="91cf3-136">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-136">The data factory object.</span></span>

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

### <span data-ttu-id="91cf3-137">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="91cf3-137">-LastCommitId</span></span>
<span data-ttu-id="91cf3-138">리포지토리 구성의 마지막 커밋 id입니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-138">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="91cf3-139">-위치</span><span class="sxs-lookup"><span data-stu-id="91cf3-139">-Location</span></span>
<span data-ttu-id="91cf3-140">이 지역에 데이터 팩터리가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-140">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="91cf3-141">-이름</span><span class="sxs-lookup"><span data-stu-id="91cf3-141">-Name</span></span>
<span data-ttu-id="91cf3-142">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-142">The data factory name.</span></span>

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

### <span data-ttu-id="91cf3-143">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="91cf3-143">-ProjectName</span></span>
<span data-ttu-id="91cf3-144">리포지토리 구성의 프로젝트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-144">The project name for repo configuration.</span></span>

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

### <span data-ttu-id="91cf3-145">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="91cf3-145">-RepositoryName</span></span>
<span data-ttu-id="91cf3-146">리포지토리 구성의 리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-146">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="91cf3-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91cf3-147">-ResourceGroupName</span></span>
<span data-ttu-id="91cf3-148">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-148">The resource group name.</span></span>

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

### <span data-ttu-id="91cf3-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91cf3-149">-ResourceId</span></span>
<span data-ttu-id="91cf3-150">Azure 리소스 팩토리 (V2 data factory)</span><span class="sxs-lookup"><span data-stu-id="91cf3-150">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="91cf3-151">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="91cf3-151">-RootFolder</span></span>
<span data-ttu-id="91cf3-152">리포지토리 구성에 대 한 루트 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-152">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="91cf3-153">태그</span><span class="sxs-lookup"><span data-stu-id="91cf3-153">-Tag</span></span>
<span data-ttu-id="91cf3-154">Data factory의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-154">The tags of the data factory.</span></span>

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

### <span data-ttu-id="91cf3-155">-TenantId</span><span class="sxs-lookup"><span data-stu-id="91cf3-155">-TenantId</span></span>
<span data-ttu-id="91cf3-156">리포지토리 구성의 테 넌 트 id입니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-156">The tenant id for repo configuration.</span></span>

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

### <span data-ttu-id="91cf3-157">-확인</span><span class="sxs-lookup"><span data-stu-id="91cf3-157">-Confirm</span></span>
<span data-ttu-id="91cf3-158">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91cf3-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91cf3-159">-WhatIf</span></span>
<span data-ttu-id="91cf3-160">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-160">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="91cf3-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91cf3-161">CommonParameters</span></span>
<span data-ttu-id="91cf3-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cf3-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91cf3-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91cf3-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91cf3-164">입력</span><span class="sxs-lookup"><span data-stu-id="91cf3-164">INPUTS</span></span>

### <span data-ttu-id="91cf3-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="91cf3-165">System.String</span></span>

### <span data-ttu-id="91cf3-166">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="91cf3-166">System.Collections.Hashtable</span></span>

## <span data-ttu-id="91cf3-167">출력</span><span class="sxs-lookup"><span data-stu-id="91cf3-167">OUTPUTS</span></span>

### <span data-ttu-id="91cf3-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="91cf3-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="91cf3-169">상속자</span><span class="sxs-lookup"><span data-stu-id="91cf3-169">NOTES</span></span>
<span data-ttu-id="91cf3-170">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="91cf3-170">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="91cf3-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91cf3-171">RELATED LINKS</span></span>

[<span data-ttu-id="91cf3-172">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="91cf3-172">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="91cf3-173">제거-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="91cf3-173">Remove-AzDataFactoryV2</span></span>]()
