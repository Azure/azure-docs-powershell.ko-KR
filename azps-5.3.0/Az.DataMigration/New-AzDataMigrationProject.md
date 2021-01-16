---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: beed4ef06d567250fefa8cef86da133447a9f20c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377679"
---
# <span data-ttu-id="22886-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="22886-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="22886-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22886-102">SYNOPSIS</span></span>
<span data-ttu-id="22886-103">새 Azure Database Migration Service 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22886-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="22886-104">구문</span><span class="sxs-lookup"><span data-stu-id="22886-104">SYNTAX</span></span>

### <span data-ttu-id="22886-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="22886-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22886-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22886-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22886-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22886-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22886-108">설명</span><span class="sxs-lookup"><span data-stu-id="22886-108">DESCRIPTION</span></span>
<span data-ttu-id="22886-109">New-AzDataMigrationProject cmdlet은 새 Azure Database Migration Service 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22886-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="22886-110">이 cmdlet은 Azure 리소스 그룹의 이름, 새 프로젝트를 만들 Azure Data Migration Service의 이름, 프로젝트를 만들 지역, 새 프로젝트의 고유한 이름, 원본 및 대상 연결 개체, 마이그레이션할 데이터베이스 목록에 대한 입력으로 대상 유형 개체와 같은 필요한 모든 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="22886-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="22886-111">New-AzDataMigrationConnectionInfo cmdlet을 사용하여 원본 및 대상 연결 모두에 대한 새 ConnectionInfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22886-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="22886-112">선택한 데이터베이스에 대해 Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo 목록이 필요합니다. 이 개체는 cmdlet을 사용하여 New-AzDataMigrationDatabaseInfo 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22886-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="22886-113">예제</span><span class="sxs-lookup"><span data-stu-id="22886-113">EXAMPLES</span></span>

### <span data-ttu-id="22886-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="22886-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="22886-115">위의 예제에서는 TestService라는 Azure Database Migration Service 인스턴스 아래에서 미국 중부 지역에 있는 MyDMSProject라는 새 프로젝트를 만드는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="22886-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="22886-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22886-116">PARAMETERS</span></span>

### <span data-ttu-id="22886-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="22886-117">-DatabaseInfo</span></span>
<span data-ttu-id="22886-118">데이터베이스 정보.</span><span class="sxs-lookup"><span data-stu-id="22886-118">Database Infos.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22886-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22886-119">-DefaultProfile</span></span>
<span data-ttu-id="22886-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22886-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22886-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22886-121">-InputObject</span></span>
<span data-ttu-id="22886-122">PSDataMigrationService 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="22886-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22886-123">-Location</span><span class="sxs-lookup"><span data-stu-id="22886-123">-Location</span></span>
<span data-ttu-id="22886-124">Azure Database Migration Service 인스턴스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="22886-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="22886-125">-Name</span><span class="sxs-lookup"><span data-stu-id="22886-125">-Name</span></span>
<span data-ttu-id="22886-126">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22886-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22886-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22886-127">-ResourceGroupName</span></span>
<span data-ttu-id="22886-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22886-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22886-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22886-129">-ResourceId</span></span>
<span data-ttu-id="22886-130">DataMigrationService 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="22886-130">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22886-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="22886-131">-ServiceName</span></span>
<span data-ttu-id="22886-132">Azure Database Migration Service 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22886-132">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22886-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="22886-133">-SourceConnection</span></span>
<span data-ttu-id="22886-134">원본 연결 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="22886-134">Source Connection Info.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22886-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="22886-135">-SourceType</span></span>
<span data-ttu-id="22886-136">프로젝트에 대한 원본 플랫폼 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="22886-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="22886-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="22886-137">-TargetConnection</span></span>
<span data-ttu-id="22886-138">대상 연결 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="22886-138">Target connection information.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22886-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="22886-139">-TargetType</span></span>
<span data-ttu-id="22886-140">프로젝트에 대한 대상 플랫폼 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="22886-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="22886-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22886-141">-Confirm</span></span>
<span data-ttu-id="22886-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="22886-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22886-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22886-143">-WhatIf</span></span>
<span data-ttu-id="22886-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="22886-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22886-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22886-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22886-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22886-146">CommonParameters</span></span>
<span data-ttu-id="22886-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="22886-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22886-148">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="22886-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22886-149">입력</span><span class="sxs-lookup"><span data-stu-id="22886-149">INPUTS</span></span>

### <span data-ttu-id="22886-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="22886-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="22886-151">System.String</span><span class="sxs-lookup"><span data-stu-id="22886-151">System.String</span></span>

## <span data-ttu-id="22886-152">출력</span><span class="sxs-lookup"><span data-stu-id="22886-152">OUTPUTS</span></span>

### <span data-ttu-id="22886-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="22886-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="22886-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="22886-154">NOTES</span></span>

## <span data-ttu-id="22886-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22886-155">RELATED LINKS</span></span>
