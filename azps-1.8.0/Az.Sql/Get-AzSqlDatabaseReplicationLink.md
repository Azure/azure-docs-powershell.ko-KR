---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
ms.openlocfilehash: 6bb2a3891abe8453ee8460f6879dbc134f6ab29b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699018"
---
# <span data-ttu-id="a0e4a-101">Get-AzSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="a0e4a-101">Get-AzSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="a0e4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e4a-103">Azure SQL 데이터베이스와 리소스 그룹 또는 SQL Server 간의 지역/복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

## <span data-ttu-id="a0e4a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0e4a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0e4a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a0e4a-105">DESCRIPTION</span></span>
<span data-ttu-id="a0e4a-106">**AzSqlDatabaseReplicationLink** Cmdlet은 **AzSqlDatabaseCopy** cmdlet을 대신 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-106">The **Get-AzSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="a0e4a-107">지정 된 Azure SQL 데이터베이스와 리소스 그룹 또는 AzureSQL 서버 간의 모든 지역/복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-107">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="a0e4a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a0e4a-108">EXAMPLES</span></span>

## <span data-ttu-id="a0e4a-109">변수</span><span class="sxs-lookup"><span data-stu-id="a0e4a-109">PARAMETERS</span></span>

### <span data-ttu-id="a0e4a-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0e4a-110">-DatabaseName</span></span>
<span data-ttu-id="a0e4a-111">링크를 검색할 SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-111">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="a0e4a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e4a-112">-DefaultProfile</span></span>
<span data-ttu-id="a0e4a-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a0e4a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0e4a-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e4a-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="a0e4a-115">파트너가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="a0e4a-116">-(-)-(서버 이름)</span><span class="sxs-lookup"><span data-stu-id="a0e4a-116">-PartnerServerName</span></span>
<span data-ttu-id="a0e4a-117">파트너에 대 한 Azure SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a0e4a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e4a-118">-ResourceGroupName</span></span>
<span data-ttu-id="a0e4a-119">링크를 검색할 데이터베이스에 대 한 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="a0e4a-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a0e4a-120">-ServerName</span></span>
<span data-ttu-id="a0e4a-121">연결을 검색할 데이터베이스에 대 한 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="a0e4a-122">-확인</span><span class="sxs-lookup"><span data-stu-id="a0e4a-122">-Confirm</span></span>
<span data-ttu-id="a0e4a-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0e4a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0e4a-124">-WhatIf</span></span>
<span data-ttu-id="a0e4a-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0e4a-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0e4a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e4a-127">CommonParameters</span></span>
<span data-ttu-id="a0e4a-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e4a-129">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e4a-130">입력</span><span class="sxs-lookup"><span data-stu-id="a0e4a-130">INPUTS</span></span>

### <span data-ttu-id="a0e4a-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a0e4a-131">System.String</span></span>

## <span data-ttu-id="a0e4a-132">출력</span><span class="sxs-lookup"><span data-stu-id="a0e4a-132">OUTPUTS</span></span>

### <span data-ttu-id="a0e4a-133">AzureReplicationLinkModel를 통해 서의.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-133">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="a0e4a-134">상속자</span><span class="sxs-lookup"><span data-stu-id="a0e4a-134">NOTES</span></span>

## <span data-ttu-id="a0e4a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0e4a-135">RELATED LINKS</span></span>

[<span data-ttu-id="a0e4a-136">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a0e4a-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
