---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 559e23334f9fc98cd51f296aee243152578ba763
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977728"
---
# <span data-ttu-id="03504-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="03504-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="03504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03504-102">SYNOPSIS</span></span>
<span data-ttu-id="03504-103">Managed Instance SQL Azure를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03504-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="03504-104">구문</span><span class="sxs-lookup"><span data-stu-id="03504-104">SYNTAX</span></span>

### <span data-ttu-id="03504-105">CreateNewInstanceDatabaseFromInputParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="03504-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03504-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="03504-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03504-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="03504-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03504-108">설명</span><span class="sxs-lookup"><span data-stu-id="03504-108">DESCRIPTION</span></span>
<span data-ttu-id="03504-109">**New-AzSqlInstanceDatabase** cmdlet은 Azure SQL 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03504-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="03504-110">예제</span><span class="sxs-lookup"><span data-stu-id="03504-110">EXAMPLES</span></span>

### <span data-ttu-id="03504-111">예제 1: 지정된 인스턴스에 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="03504-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/Database01
Name                     : Database01
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="03504-112">이 명령은 instance managedInstance1에서 Database01이라는 인스턴스 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03504-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="03504-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="03504-113">PARAMETERS</span></span>

### <span data-ttu-id="03504-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03504-114">-AsJob</span></span>
<span data-ttu-id="03504-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="03504-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03504-116">-Collation</span><span class="sxs-lookup"><span data-stu-id="03504-116">-Collation</span></span>
<span data-ttu-id="03504-117">사용할 인스턴스 데이터베이스 SQL Azure의 데이터 데이터 통합입니다.</span><span class="sxs-lookup"><span data-stu-id="03504-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

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

### <span data-ttu-id="03504-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03504-118">-DefaultProfile</span></span>
<span data-ttu-id="03504-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03504-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03504-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="03504-120">-InstanceName</span></span>
<span data-ttu-id="03504-121">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03504-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03504-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="03504-122">-InstanceObject</span></span>
<span data-ttu-id="03504-123">인스턴스 개체</span><span class="sxs-lookup"><span data-stu-id="03504-123">The instance object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03504-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="03504-124">-InstanceResourceId</span></span>
<span data-ttu-id="03504-125">인스턴스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="03504-125">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03504-126">-Name</span><span class="sxs-lookup"><span data-stu-id="03504-126">-Name</span></span>
<span data-ttu-id="03504-127">Azure 인스턴스 데이터베이스의 SQL 인스턴스 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03504-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03504-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03504-128">-ResourceGroupName</span></span>
<span data-ttu-id="03504-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03504-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03504-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="03504-130">-Tag</span></span>
<span data-ttu-id="03504-131">Azure Sql Instance Database와 연결되는 태그</span><span class="sxs-lookup"><span data-stu-id="03504-131">The tags to associate with the Azure Sql Instance Database</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03504-132">-확인</span><span class="sxs-lookup"><span data-stu-id="03504-132">-Confirm</span></span>
<span data-ttu-id="03504-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03504-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03504-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03504-134">-WhatIf</span></span>
<span data-ttu-id="03504-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="03504-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03504-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03504-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03504-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03504-137">CommonParameters</span></span>
<span data-ttu-id="03504-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03504-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03504-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03504-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03504-140">입력</span><span class="sxs-lookup"><span data-stu-id="03504-140">INPUTS</span></span>

### <span data-ttu-id="03504-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="03504-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="03504-142">System.String</span><span class="sxs-lookup"><span data-stu-id="03504-142">System.String</span></span>

## <span data-ttu-id="03504-143">출력</span><span class="sxs-lookup"><span data-stu-id="03504-143">OUTPUTS</span></span>

### <span data-ttu-id="03504-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="03504-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="03504-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="03504-145">NOTES</span></span>

## <span data-ttu-id="03504-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03504-146">RELATED LINKS</span></span>
