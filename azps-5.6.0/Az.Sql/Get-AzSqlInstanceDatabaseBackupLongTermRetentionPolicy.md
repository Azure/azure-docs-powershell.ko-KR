---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 3b1c2865e6e5084f3108409d9afae0979ae635b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999472"
---
# <span data-ttu-id="451bf-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="451bf-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="451bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="451bf-102">SYNOPSIS</span></span>
<span data-ttu-id="451bf-103">관리되는 데이터베이스의 장기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="451bf-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="451bf-104">구문</span><span class="sxs-lookup"><span data-stu-id="451bf-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="451bf-105">설명</span><span class="sxs-lookup"><span data-stu-id="451bf-105">DESCRIPTION</span></span>
<span data-ttu-id="451bf-106">**Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet은 이 관리되는 데이터베이스에 등록된 장기 보존 정책을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="451bf-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="451bf-107">이 정책은 백업 저장소 정책을 정의하는 데 사용되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="451bf-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="451bf-108">예제</span><span class="sxs-lookup"><span data-stu-id="451bf-108">EXAMPLES</span></span>

### <span data-ttu-id="451bf-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="451bf-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P2W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="451bf-110">데이터베이스에 대한 장기 보존 정책의 현재 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="451bf-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="451bf-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="451bf-111">PARAMETERS</span></span>

### <span data-ttu-id="451bf-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="451bf-112">-DatabaseName</span></span>
<span data-ttu-id="451bf-113">사용할 Azure Managed Database의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="451bf-113">The name of the Azure Managed Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="451bf-114">-DefaultProfile</span></span>
<span data-ttu-id="451bf-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="451bf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="451bf-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="451bf-116">-InstanceName</span></span>
<span data-ttu-id="451bf-117">데이터베이스가 속한 Azure Managed Instance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="451bf-117">The name of the Azure Managed Instance the database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451bf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="451bf-118">-ResourceGroupName</span></span>
<span data-ttu-id="451bf-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="451bf-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451bf-120">-확인</span><span class="sxs-lookup"><span data-stu-id="451bf-120">-Confirm</span></span>
<span data-ttu-id="451bf-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="451bf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="451bf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="451bf-122">-WhatIf</span></span>
<span data-ttu-id="451bf-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="451bf-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="451bf-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="451bf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="451bf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="451bf-125">CommonParameters</span></span>
<span data-ttu-id="451bf-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="451bf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="451bf-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="451bf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="451bf-128">입력</span><span class="sxs-lookup"><span data-stu-id="451bf-128">INPUTS</span></span>

### <span data-ttu-id="451bf-129">System.String</span><span class="sxs-lookup"><span data-stu-id="451bf-129">System.String</span></span>

## <span data-ttu-id="451bf-130">출력</span><span class="sxs-lookup"><span data-stu-id="451bf-130">OUTPUTS</span></span>

### <span data-ttu-id="451bf-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="451bf-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="451bf-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="451bf-132">NOTES</span></span>

## <span data-ttu-id="451bf-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="451bf-133">RELATED LINKS</span></span>

[<span data-ttu-id="451bf-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="451bf-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="451bf-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="451bf-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="451bf-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="451bf-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="451bf-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="451bf-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)