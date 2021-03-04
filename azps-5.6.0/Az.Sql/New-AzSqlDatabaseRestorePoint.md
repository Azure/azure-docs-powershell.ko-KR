---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 8fb320c2caa4993b7880ef719a3d9ea0e0e8c811
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956587"
---
# <span data-ttu-id="765ec-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="765ec-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="765ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="765ec-102">SYNOPSIS</span></span>
<span data-ttu-id="765ec-103">데이터베이스를 복원할 수 있는 SQL 복원 지점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="765ec-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="765ec-104">구문</span><span class="sxs-lookup"><span data-stu-id="765ec-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="765ec-105">설명</span><span class="sxs-lookup"><span data-stu-id="765ec-105">DESCRIPTION</span></span>
<span data-ttu-id="765ec-106">**New-AzSqlDatabaseRestorePoint** cmdlet은 Azure SQL 데이터 웨어하우스에서 복원할 수 있는 새 복원 지점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="765ec-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="765ec-107">이 cmdlet은 현재 Azure SQL 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="765ec-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="765ec-108">예제</span><span class="sxs-lookup"><span data-stu-id="765ec-108">EXAMPLES</span></span>

### <span data-ttu-id="765ec-109">예제 1: 복원 지점 만들기</span><span class="sxs-lookup"><span data-stu-id="765ec-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="765ec-110">이 명령은 Azure SQL 데이터 웨어하우스에 대한 복원 지점을 만들고 복원 지점의 세부 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="765ec-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="765ec-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="765ec-111">PARAMETERS</span></span>

### <span data-ttu-id="765ec-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="765ec-112">-DatabaseName</span></span>
<span data-ttu-id="765ec-113">데이터베이스의 이름을 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="765ec-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="765ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="765ec-114">-DefaultProfile</span></span>
<span data-ttu-id="765ec-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="765ec-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="765ec-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="765ec-116">-ResourceGroupName</span></span>
<span data-ttu-id="765ec-117">데이터베이스가 할당된 리소스 그룹의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="765ec-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="765ec-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="765ec-118">-RestorePointLabel</span></span>
<span data-ttu-id="765ec-119">쉽게 식별할 수 있도록 복원 지점의 레이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="765ec-119">Specifies the label of the restore point for easy identification.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="765ec-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="765ec-120">-ServerName</span></span>
<span data-ttu-id="765ec-121">데이터베이스를 호스트하는 AzureSQL 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="765ec-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="765ec-122">-확인</span><span class="sxs-lookup"><span data-stu-id="765ec-122">-Confirm</span></span>
<span data-ttu-id="765ec-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="765ec-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765ec-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="765ec-124">-WhatIf</span></span>
<span data-ttu-id="765ec-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="765ec-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="765ec-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="765ec-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765ec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="765ec-127">CommonParameters</span></span>
<span data-ttu-id="765ec-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="765ec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="765ec-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="765ec-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="765ec-130">입력</span><span class="sxs-lookup"><span data-stu-id="765ec-130">INPUTS</span></span>

### <span data-ttu-id="765ec-131">System.String</span><span class="sxs-lookup"><span data-stu-id="765ec-131">System.String</span></span>

## <span data-ttu-id="765ec-132">출력</span><span class="sxs-lookup"><span data-stu-id="765ec-132">OUTPUTS</span></span>

### <span data-ttu-id="765ec-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="765ec-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="765ec-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="765ec-134">NOTES</span></span>

## <span data-ttu-id="765ec-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="765ec-135">RELATED LINKS</span></span>
