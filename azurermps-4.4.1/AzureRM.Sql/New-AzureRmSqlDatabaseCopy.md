---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: a962ca86c3d65cd11da4169626ed932bb78653b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711475"
---
# <span data-ttu-id="29fb1-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="29fb1-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="29fb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="29fb1-103">현재 시간에 스냅숏을 사용 하는 SQL 데이터베이스의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29fb1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29fb1-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29fb1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="29fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="29fb1-106">**AzureRmSqlDatabaseCopy** cmdlet은 현재 시간에 데이터의 스냅숏을 사용 하는 Azure SQL 데이터베이스의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="29fb1-107">Start-AzureSqlDatabaseCopy cmdlet 대신이 cmdlet을 사용 하 여 일회성 데이터베이스 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="29fb1-108">이 cmdlet은 복사본의 **데이터베이스** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="29fb1-109">참고: New-AzureRmSqlDatabaseSecondary cmdlet을 사용 하 여 데이터베이스에 대 한 지리적 복제를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="29fb1-110">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="29fb1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="29fb1-111">EXAMPLES</span></span>

## <span data-ttu-id="29fb1-112">변수</span><span class="sxs-lookup"><span data-stu-id="29fb1-112">PARAMETERS</span></span>

### <span data-ttu-id="29fb1-113">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="29fb1-113">-CopyDatabaseName</span></span>
<span data-ttu-id="29fb1-114">SQL 데이터베이스 복사본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-114">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="29fb1-115">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29fb1-115">-CopyResourceGroupName</span></span>
<span data-ttu-id="29fb1-116">복사본을 할당할 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-116">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="29fb1-117">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="29fb1-117">-CopyServerName</span></span>
<span data-ttu-id="29fb1-118">복사본을 호스트 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-118">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="29fb1-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29fb1-119">-DatabaseName</span></span>
<span data-ttu-id="29fb1-120">복사할 SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-120">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="29fb1-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="29fb1-121">-ElasticPoolName</span></span>
<span data-ttu-id="29fb1-122">복사본을 할당할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-122">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="29fb1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29fb1-123">-ResourceGroupName</span></span>
<span data-ttu-id="29fb1-124">이 cmdlet이 복사한 데이터베이스를 할당 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-124">Specifies the name of the  Resource Group to which this cmdlet assigns the copied database.</span></span>

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

### <span data-ttu-id="29fb1-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="29fb1-125">-ServerName</span></span>
<span data-ttu-id="29fb1-126">복사할 데이터베이스를 포함 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-126">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="29fb1-127">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="29fb1-127">-ServiceObjectiveName</span></span>
<span data-ttu-id="29fb1-128">복사본에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-128">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="29fb1-129">태그</span><span class="sxs-lookup"><span data-stu-id="29fb1-129">-Tags</span></span>
<span data-ttu-id="29fb1-130">Azure SQL 데이터베이스 복사본과 연결할 해시 테이블 형태의 키-값 쌍을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-130">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="29fb1-131">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="29fb1-131">For example:</span></span>

<span data-ttu-id="29fb1-132">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="29fb1-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fb1-133">-확인</span><span class="sxs-lookup"><span data-stu-id="29fb1-133">-Confirm</span></span>
<span data-ttu-id="29fb1-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29fb1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29fb1-135">-WhatIf</span></span>
<span data-ttu-id="29fb1-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29fb1-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29fb1-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29fb1-138">-DefaultProfile</span></span>
<span data-ttu-id="29fb1-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fb1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29fb1-140">CommonParameters</span></span>
<span data-ttu-id="29fb1-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29fb1-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29fb1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29fb1-143">입력</span><span class="sxs-lookup"><span data-stu-id="29fb1-143">INPUTS</span></span>

## <span data-ttu-id="29fb1-144">출력</span><span class="sxs-lookup"><span data-stu-id="29fb1-144">OUTPUTS</span></span>

### <span data-ttu-id="29fb1-145">AzureSqlDatabaseCopyModel를 통해 서의.</span><span class="sxs-lookup"><span data-stu-id="29fb1-145">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="29fb1-146">이 cmdlet은 복사한 데이터베이스를 나타내는 **database** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fb1-146">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="29fb1-147">상속자</span><span class="sxs-lookup"><span data-stu-id="29fb1-147">NOTES</span></span>

## <span data-ttu-id="29fb1-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29fb1-148">RELATED LINKS</span></span>

[<span data-ttu-id="29fb1-149">새로운 AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="29fb1-149">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="29fb1-150">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="29fb1-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
