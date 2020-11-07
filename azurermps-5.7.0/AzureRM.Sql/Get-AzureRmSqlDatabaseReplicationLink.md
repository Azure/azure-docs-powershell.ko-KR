---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
ms.openlocfilehash: 982a903d702f4143d9eb11e99fa15afc64a040e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702010"
---
# <span data-ttu-id="c645f-101">Get-AzureRmSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="c645f-101">Get-AzureRmSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="c645f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c645f-102">SYNOPSIS</span></span>
<span data-ttu-id="c645f-103">Azure SQL 데이터베이스와 리소스 그룹 또는 SQL Server 간의 지역/복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c645f-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c645f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c645f-104">SYNTAX</span></span>

### <span data-ttu-id="c645f-105">ByDatabaseName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c645f-105">ByDatabaseName (Default)</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c645f-106">ByPartnerServerName</span><span class="sxs-lookup"><span data-stu-id="c645f-106">ByPartnerServerName</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c645f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c645f-107">DESCRIPTION</span></span>
<span data-ttu-id="c645f-108">**AzureRMSqlDatabaseReplicationLink** Cmdlet은 **AzureSqlDatabaseCopy** cmdlet을 대신 합니다.</span><span class="sxs-lookup"><span data-stu-id="c645f-108">The **Get-AzureRMSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="c645f-109">지정 된 Azure SQL 데이터베이스와 리소스 그룹 또는 AzureSQL 서버 간의 모든 지역/복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c645f-109">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="c645f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c645f-110">EXAMPLES</span></span>

## <span data-ttu-id="c645f-111">변수</span><span class="sxs-lookup"><span data-stu-id="c645f-111">PARAMETERS</span></span>

### <span data-ttu-id="c645f-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c645f-112">-DatabaseName</span></span>
<span data-ttu-id="c645f-113">링크를 검색할 SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c645f-113">Specifies the name of the SQL Database for which to retrieve links.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c645f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c645f-114">-DefaultProfile</span></span>
<span data-ttu-id="c645f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c645f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c645f-116">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c645f-116">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c645f-117">파트너가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c645f-117">Specifies the name of the resource group to which the partner is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c645f-118">-(-)-(서버 이름)</span><span class="sxs-lookup"><span data-stu-id="c645f-118">-PartnerServerName</span></span>
<span data-ttu-id="c645f-119">파트너에 대 한 Azure SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c645f-119">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: String
Parameter Sets: ByPartnerServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c645f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c645f-120">-ResourceGroupName</span></span>
<span data-ttu-id="c645f-121">링크를 검색할 데이터베이스에 대 한 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c645f-121">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c645f-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c645f-122">-ServerName</span></span>
<span data-ttu-id="c645f-123">연결을 검색할 데이터베이스에 대 한 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c645f-123">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c645f-124">-확인</span><span class="sxs-lookup"><span data-stu-id="c645f-124">-Confirm</span></span>
<span data-ttu-id="c645f-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c645f-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c645f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c645f-126">-WhatIf</span></span>
<span data-ttu-id="c645f-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c645f-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c645f-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c645f-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c645f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c645f-129">CommonParameters</span></span>
<span data-ttu-id="c645f-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c645f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c645f-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c645f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c645f-132">입력</span><span class="sxs-lookup"><span data-stu-id="c645f-132">INPUTS</span></span>

###  
<span data-ttu-id="c645f-133">이 cmdlet은 주 또는 보조 데이터베이스에 대 한 **ReplicationLink** 또는 **Database** 개체의 인스턴스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c645f-133">This cmdlet accepts instances of the **ReplicationLink** or the **Database** object for the primary or secondary database.</span></span>

## <span data-ttu-id="c645f-134">출력</span><span class="sxs-lookup"><span data-stu-id="c645f-134">OUTPUTS</span></span>

###  
<span data-ttu-id="c645f-135">이 cmdlet은 **ReplicationLink** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c645f-135">This cmdlet returns a **ReplicationLink** object.</span></span>

## <span data-ttu-id="c645f-136">상속자</span><span class="sxs-lookup"><span data-stu-id="c645f-136">NOTES</span></span>

## <span data-ttu-id="c645f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c645f-137">RELATED LINKS</span></span>

[<span data-ttu-id="c645f-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="c645f-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
