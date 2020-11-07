---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: d1f1ae44cf1b6d1b6d3afffa3e13ea34c1ffeb51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868457"
---
# <span data-ttu-id="4676d-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="4676d-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="4676d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4676d-102">SYNOPSIS</span></span>
<span data-ttu-id="4676d-103">새 Azure 데이터베이스 마이그레이션 서비스 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="4676d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4676d-104">SYNTAX</span></span>

### <span data-ttu-id="4676d-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4676d-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4676d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4676d-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4676d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4676d-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4676d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4676d-108">DESCRIPTION</span></span>
<span data-ttu-id="4676d-109">New-AzDataMigrationProject cmdlet은 새 Azure 데이터베이스 마이그레이션 서비스 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="4676d-110">이 cmdlet은 Azure Resource 그룹의 이름, 새 프로젝트를 만들 Azure Data 마이그레이션 서비스의 이름, 프로젝트를 만들 지역, 새 프로젝트의 고유 이름, 원본 및 대상 연결 개체, 대상 형식 개체 (마이그레이션할 데이터베이스 목록에 대 한 입력) 등 필요한 모든 매개 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="4676d-111">New-AzDataMigrationConnectionInfo cmdlet을 사용 하 여 원본 및 대상 연결 모두에 대해 새 ConnectionInfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="4676d-112">선택한 데이터베이스에 대 한 DataMigration 정보 목록이 있어야 하는 경우 이 개체는 New-AzDataMigrationDatabaseInfo cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="4676d-113">예제의</span><span class="sxs-lookup"><span data-stu-id="4676d-113">EXAMPLES</span></span>

### <span data-ttu-id="4676d-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="4676d-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="4676d-115">위 예제에서는 MyDMSProject 라는 Azure 데이터베이스 마이그레이션 서비스 인스턴스의 중앙 US 영역에 있는 새 프로젝트를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="4676d-116">변수</span><span class="sxs-lookup"><span data-stu-id="4676d-116">PARAMETERS</span></span>

### <span data-ttu-id="4676d-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="4676d-117">-DatabaseInfo</span></span>
<span data-ttu-id="4676d-118">데이터베이스 Infos.</span><span class="sxs-lookup"><span data-stu-id="4676d-118">Database Infos.</span></span>

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

### <span data-ttu-id="4676d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4676d-119">-DefaultProfile</span></span>
<span data-ttu-id="4676d-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4676d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4676d-121">-InputObject</span></span>
<span data-ttu-id="4676d-122">PSDataMigrationService 개체</span><span class="sxs-lookup"><span data-stu-id="4676d-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="4676d-123">-위치</span><span class="sxs-lookup"><span data-stu-id="4676d-123">-Location</span></span>
<span data-ttu-id="4676d-124">Azure 데이터베이스 마이그레이션 서비스 인스턴스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="4676d-125">-이름</span><span class="sxs-lookup"><span data-stu-id="4676d-125">-Name</span></span>
<span data-ttu-id="4676d-126">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-126">The name of the project.</span></span>

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

### <span data-ttu-id="4676d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4676d-127">-ResourceGroupName</span></span>
<span data-ttu-id="4676d-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="4676d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4676d-129">-ResourceId</span></span>
<span data-ttu-id="4676d-130">DataMigrationService 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="4676d-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4676d-131">-ServiceName</span></span>
<span data-ttu-id="4676d-132">Azure 데이터베이스 마이그레이션 서비스 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-132">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="4676d-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="4676d-133">-SourceConnection</span></span>
<span data-ttu-id="4676d-134">원본 연결 정보</span><span class="sxs-lookup"><span data-stu-id="4676d-134">Source Connection Info.</span></span>

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

### <span data-ttu-id="4676d-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="4676d-135">-SourceType</span></span>
<span data-ttu-id="4676d-136">Project의 원본 플랫폼 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="4676d-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="4676d-137">-TargetConnection</span></span>
<span data-ttu-id="4676d-138">대상 연결 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-138">Target connection information.</span></span>

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

### <span data-ttu-id="4676d-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="4676d-139">-TargetType</span></span>
<span data-ttu-id="4676d-140">Project에 대 한 대상 플랫폼 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="4676d-141">-확인</span><span class="sxs-lookup"><span data-stu-id="4676d-141">-Confirm</span></span>
<span data-ttu-id="4676d-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4676d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4676d-143">-WhatIf</span></span>
<span data-ttu-id="4676d-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4676d-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4676d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4676d-146">CommonParameters</span></span>
<span data-ttu-id="4676d-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4676d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4676d-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4676d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4676d-149">입력</span><span class="sxs-lookup"><span data-stu-id="4676d-149">INPUTS</span></span>

### <span data-ttu-id="4676d-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="4676d-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="4676d-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4676d-151">System.String</span></span>

## <span data-ttu-id="4676d-152">출력</span><span class="sxs-lookup"><span data-stu-id="4676d-152">OUTPUTS</span></span>

### <span data-ttu-id="4676d-153">DataMigration. a i m. PSProject</span><span class="sxs-lookup"><span data-stu-id="4676d-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="4676d-154">상속자</span><span class="sxs-lookup"><span data-stu-id="4676d-154">NOTES</span></span>

## <span data-ttu-id="4676d-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4676d-155">RELATED LINKS</span></span>
