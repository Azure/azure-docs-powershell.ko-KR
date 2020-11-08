---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 6c8fdc5b54ca802c8c23df577fc0e0e39de0ba16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048644"
---
# <span data-ttu-id="0a0e5-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0a0e5-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="0a0e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0e5-103">Azure SQL 관리 인스턴스 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="0a0e5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a0e5-104">SYNTAX</span></span>

### <span data-ttu-id="0a0e5-105">CreateNewInstanceDatabaseFromInputParameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="0a0e5-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a0e5-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="0a0e5-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a0e5-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="0a0e5-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a0e5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0a0e5-108">DESCRIPTION</span></span>
<span data-ttu-id="0a0e5-109">**AzSqlInstanceDatabase** Cmdlet은 Azure SQL 관리 인스턴스 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="0a0e5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0a0e5-110">EXAMPLES</span></span>

### <span data-ttu-id="0a0e5-111">예제 1: 지정 된 인스턴스에서 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="0a0e5-111">Example 1: Create a database on a specified instance</span></span>
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

<span data-ttu-id="0a0e5-112">이 명령은 instance managedInstance1에 Database01 이라는 인스턴스 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="0a0e5-113">변수</span><span class="sxs-lookup"><span data-stu-id="0a0e5-113">PARAMETERS</span></span>

### <span data-ttu-id="0a0e5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a0e5-114">-AsJob</span></span>
<span data-ttu-id="0a0e5-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0a0e5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a0e5-116">-데이터 정렬</span><span class="sxs-lookup"><span data-stu-id="0a0e5-116">-Collation</span></span>
<span data-ttu-id="0a0e5-117">사용할 Azure SQL Instance 데이터베이스 데이터 정렬의 데이터 정렬입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

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

### <span data-ttu-id="0a0e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a0e5-118">-DefaultProfile</span></span>
<span data-ttu-id="0a0e5-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a0e5-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0a0e5-120">-InstanceName</span></span>
<span data-ttu-id="0a0e5-121">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-121">The instance name.</span></span>

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

### <span data-ttu-id="0a0e5-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="0a0e5-122">-InstanceObject</span></span>
<span data-ttu-id="0a0e5-123">인스턴스 개체</span><span class="sxs-lookup"><span data-stu-id="0a0e5-123">The instance object</span></span>

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

### <span data-ttu-id="0a0e5-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="0a0e5-124">-InstanceResourceId</span></span>
<span data-ttu-id="0a0e5-125">인스턴스 리소스 id</span><span class="sxs-lookup"><span data-stu-id="0a0e5-125">The instance resource id</span></span>

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

### <span data-ttu-id="0a0e5-126">-이름</span><span class="sxs-lookup"><span data-stu-id="0a0e5-126">-Name</span></span>
<span data-ttu-id="0a0e5-127">만들 Azure SQL 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-127">The name of the Azure SQL Instance Database to create.</span></span>

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

### <span data-ttu-id="0a0e5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a0e5-128">-ResourceGroupName</span></span>
<span data-ttu-id="0a0e5-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="0a0e5-130">태그</span><span class="sxs-lookup"><span data-stu-id="0a0e5-130">-Tag</span></span>
<span data-ttu-id="0a0e5-131">Azure Sql 인스턴스 데이터베이스와 연결할 태그</span><span class="sxs-lookup"><span data-stu-id="0a0e5-131">The tags to associate with the Azure Sql Instance Database</span></span>

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

### <span data-ttu-id="0a0e5-132">-확인</span><span class="sxs-lookup"><span data-stu-id="0a0e5-132">-Confirm</span></span>
<span data-ttu-id="0a0e5-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a0e5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a0e5-134">-WhatIf</span></span>
<span data-ttu-id="0a0e5-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a0e5-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a0e5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0e5-137">CommonParameters</span></span>
<span data-ttu-id="0a0e5-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0e5-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0e5-140">입력</span><span class="sxs-lookup"><span data-stu-id="0a0e5-140">INPUTS</span></span>

### <span data-ttu-id="0a0e5-141">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="0a0e5-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="0a0e5-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0a0e5-142">System.String</span></span>

## <span data-ttu-id="0a0e5-143">출력</span><span class="sxs-lookup"><span data-stu-id="0a0e5-143">OUTPUTS</span></span>

### <span data-ttu-id="0a0e5-144">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="0a0e5-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="0a0e5-145">상속자</span><span class="sxs-lookup"><span data-stu-id="0a0e5-145">NOTES</span></span>

## <span data-ttu-id="0a0e5-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a0e5-146">RELATED LINKS</span></span>
