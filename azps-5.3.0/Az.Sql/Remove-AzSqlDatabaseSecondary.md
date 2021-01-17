---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 4353a61efd0141947879ad6795c321f5ed43e1d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374578"
---
# <span data-ttu-id="ca277-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ca277-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="ca277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca277-102">SYNOPSIS</span></span>
<span data-ttu-id="ca277-103">SQL 데이터베이스와 지정된 보조 데이터베이스 간의 데이터 복제를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="ca277-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="ca277-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca277-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca277-105">설명</span><span class="sxs-lookup"><span data-stu-id="ca277-105">DESCRIPTION</span></span>
<span data-ttu-id="ca277-106">**Remove-AzSqlDatabaseSecondary** cmdlet은 지역 복제 링크를 강제로 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="ca277-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="ca277-107">이 cmdlet은 Stop-AzSqlDatabaseCopy 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="ca277-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="ca277-108">종료 전에는 복제 동기화가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ca277-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="ca277-109">예제</span><span class="sxs-lookup"><span data-stu-id="ca277-109">EXAMPLES</span></span>

## <span data-ttu-id="ca277-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca277-110">PARAMETERS</span></span>

### <span data-ttu-id="ca277-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ca277-111">-DatabaseName</span></span>
<span data-ttu-id="ca277-112">이 cmdlet이 제거하는 복제 링크가 SQL 기본 Azure SQL 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca277-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ca277-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca277-113">-DefaultProfile</span></span>
<span data-ttu-id="ca277-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ca277-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca277-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca277-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ca277-116">파트너 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca277-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="ca277-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="ca277-117">-PartnerServerName</span></span>
<span data-ttu-id="ca277-118">파트너 이름 지정 SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ca277-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="ca277-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca277-119">-ResourceGroupName</span></span>
<span data-ttu-id="ca277-120">제거할 복제 링크와 연결된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca277-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="ca277-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ca277-121">-ServerName</span></span>
<span data-ttu-id="ca277-122">제거할 복제 링크가 있는 SQL Server 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca277-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="ca277-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca277-123">-Confirm</span></span>
<span data-ttu-id="ca277-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca277-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca277-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca277-125">-WhatIf</span></span>
<span data-ttu-id="ca277-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ca277-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca277-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca277-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca277-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca277-128">CommonParameters</span></span>
<span data-ttu-id="ca277-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca277-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca277-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ca277-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca277-131">입력</span><span class="sxs-lookup"><span data-stu-id="ca277-131">INPUTS</span></span>

### <span data-ttu-id="ca277-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ca277-132">System.String</span></span>

## <span data-ttu-id="ca277-133">출력</span><span class="sxs-lookup"><span data-stu-id="ca277-133">OUTPUTS</span></span>

### <span data-ttu-id="ca277-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="ca277-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="ca277-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca277-135">NOTES</span></span>

## <span data-ttu-id="ca277-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca277-136">RELATED LINKS</span></span>

[<span data-ttu-id="ca277-137">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ca277-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="ca277-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ca277-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="ca277-139">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ca277-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
