---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 4353a61efd0141947879ad6795c321f5ed43e1d3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215821"
---
# <span data-ttu-id="56e7e-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="56e7e-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="56e7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56e7e-102">SYNOPSIS</span></span>
<span data-ttu-id="56e7e-103">SQL 데이터베이스와 지정 된 보조 데이터베이스 간의 데이터 복제를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e7e-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="56e7e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56e7e-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56e7e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="56e7e-105">DESCRIPTION</span></span>
<span data-ttu-id="56e7e-106">**AzSqlDatabaseSecondary** cmdlet은 지리적 복제 링크를 강제로 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e7e-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="56e7e-107">이 cmdlet은 Stop-AzSqlDatabaseCopy cmdlet을 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e7e-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="56e7e-108">종료 하기 전에 복제 동기화가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="56e7e-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="56e7e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="56e7e-109">EXAMPLES</span></span>

## <span data-ttu-id="56e7e-110">변수</span><span class="sxs-lookup"><span data-stu-id="56e7e-110">PARAMETERS</span></span>

### <span data-ttu-id="56e7e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="56e7e-111">-DatabaseName</span></span>
<span data-ttu-id="56e7e-112">이 cmdlet이 제거 하는 복제 링크가 있는 기본 Azure SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e7e-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="56e7e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e7e-113">-DefaultProfile</span></span>
<span data-ttu-id="56e7e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="56e7e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56e7e-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e7e-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="56e7e-116">파트너 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e7e-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="56e7e-117">-(-)-(서버 이름)</span><span class="sxs-lookup"><span data-stu-id="56e7e-117">-PartnerServerName</span></span>
<span data-ttu-id="56e7e-118">파트너 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e7e-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="56e7e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e7e-119">-ResourceGroupName</span></span>
<span data-ttu-id="56e7e-120">제거할 복제 링크와 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e7e-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="56e7e-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="56e7e-121">-ServerName</span></span>
<span data-ttu-id="56e7e-122">제거할 복제 링크가 있는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e7e-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="56e7e-123">-확인</span><span class="sxs-lookup"><span data-stu-id="56e7e-123">-Confirm</span></span>
<span data-ttu-id="56e7e-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e7e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56e7e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56e7e-125">-WhatIf</span></span>
<span data-ttu-id="56e7e-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56e7e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56e7e-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56e7e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56e7e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e7e-128">CommonParameters</span></span>
<span data-ttu-id="56e7e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e7e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e7e-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="56e7e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e7e-131">입력</span><span class="sxs-lookup"><span data-stu-id="56e7e-131">INPUTS</span></span>

### <span data-ttu-id="56e7e-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="56e7e-132">System.String</span></span>

## <span data-ttu-id="56e7e-133">출력</span><span class="sxs-lookup"><span data-stu-id="56e7e-133">OUTPUTS</span></span>

### <span data-ttu-id="56e7e-134">AzureReplicationLinkModel를 통해 서의.</span><span class="sxs-lookup"><span data-stu-id="56e7e-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="56e7e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="56e7e-135">NOTES</span></span>

## <span data-ttu-id="56e7e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56e7e-136">RELATED LINKS</span></span>

[<span data-ttu-id="56e7e-137">새로운 AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="56e7e-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="56e7e-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="56e7e-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="56e7e-139">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="56e7e-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
