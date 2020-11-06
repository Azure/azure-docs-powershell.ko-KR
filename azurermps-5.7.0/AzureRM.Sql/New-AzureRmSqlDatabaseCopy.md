---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 4e9d33691cfd09681bb115c89d0eaf351ef14f13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524819"
---
# <span data-ttu-id="deb3b-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="deb3b-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="deb3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deb3b-102">SYNOPSIS</span></span>
<span data-ttu-id="deb3b-103">현재 시간에 스냅숏을 사용 하는 SQL 데이터베이스의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="deb3b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="deb3b-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deb3b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="deb3b-105">DESCRIPTION</span></span>
<span data-ttu-id="deb3b-106">**AzureRmSqlDatabaseCopy** cmdlet은 현재 시간에 데이터의 스냅숏을 사용 하는 Azure SQL 데이터베이스의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="deb3b-107">Start-AzureSqlDatabaseCopy cmdlet 대신이 cmdlet을 사용 하 여 일회성 데이터베이스 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="deb3b-108">이 cmdlet은 복사본의 **데이터베이스** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="deb3b-109">참고: New-AzureRmSqlDatabaseSecondary cmdlet을 사용 하 여 데이터베이스에 대 한 지리적 복제를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="deb3b-110">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="deb3b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="deb3b-111">EXAMPLES</span></span>

## <span data-ttu-id="deb3b-112">변수</span><span class="sxs-lookup"><span data-stu-id="deb3b-112">PARAMETERS</span></span>

### <span data-ttu-id="deb3b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="deb3b-113">-AsJob</span></span>
<span data-ttu-id="deb3b-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="deb3b-114">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb3b-115">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="deb3b-115">-CopyDatabaseName</span></span>
<span data-ttu-id="deb3b-116">SQL 데이터베이스 복사본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-116">Specifies the name of the SQL Database copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb3b-117">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deb3b-117">-CopyResourceGroupName</span></span>
<span data-ttu-id="deb3b-118">복사본을 할당할 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-118">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb3b-119">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="deb3b-119">-CopyServerName</span></span>
<span data-ttu-id="deb3b-120">복사본을 호스트 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-120">Specifies the name of the SQL Server which hosts the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb3b-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="deb3b-121">-DatabaseName</span></span>
<span data-ttu-id="deb3b-122">복사할 SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-122">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="deb3b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb3b-123">-DefaultProfile</span></span>
<span data-ttu-id="deb3b-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="deb3b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="deb3b-125">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="deb3b-125">-ElasticPoolName</span></span>
<span data-ttu-id="deb3b-126">복사본을 할당할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-126">Specifies the name of the elastic pool in which to assign the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb3b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deb3b-127">-ResourceGroupName</span></span>
<span data-ttu-id="deb3b-128">복사할 데이터베이스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-128">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="deb3b-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="deb3b-129">-ServerName</span></span>
<span data-ttu-id="deb3b-130">복사할 데이터베이스를 포함 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-130">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="deb3b-131">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="deb3b-131">-ServiceObjectiveName</span></span>
<span data-ttu-id="deb3b-132">복사본에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-132">Specifies the name of the service objective to assign to the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb3b-133">태그</span><span class="sxs-lookup"><span data-stu-id="deb3b-133">-Tags</span></span>
<span data-ttu-id="deb3b-134">Azure SQL 데이터베이스 복사본과 연결할 해시 테이블 형태의 키-값 쌍을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-134">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="deb3b-135">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="deb3b-135">For example:</span></span>

<span data-ttu-id="deb3b-136">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="deb3b-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb3b-137">-확인</span><span class="sxs-lookup"><span data-stu-id="deb3b-137">-Confirm</span></span>
<span data-ttu-id="deb3b-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb3b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deb3b-139">-WhatIf</span></span>
<span data-ttu-id="deb3b-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deb3b-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb3b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb3b-142">CommonParameters</span></span>
<span data-ttu-id="deb3b-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb3b-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deb3b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb3b-145">입력</span><span class="sxs-lookup"><span data-stu-id="deb3b-145">INPUTS</span></span>

### <span data-ttu-id="deb3b-146">않아야</span><span class="sxs-lookup"><span data-stu-id="deb3b-146">None</span></span>
<span data-ttu-id="deb3b-147">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="deb3b-148">출력</span><span class="sxs-lookup"><span data-stu-id="deb3b-148">OUTPUTS</span></span>

### <span data-ttu-id="deb3b-149">AzureSqlDatabaseCopyModel를 통해 서의.</span><span class="sxs-lookup"><span data-stu-id="deb3b-149">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="deb3b-150">이 cmdlet은 복사한 데이터베이스를 나타내는 **database** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb3b-150">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="deb3b-151">상속자</span><span class="sxs-lookup"><span data-stu-id="deb3b-151">NOTES</span></span>

## <span data-ttu-id="deb3b-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="deb3b-152">RELATED LINKS</span></span>

[<span data-ttu-id="deb3b-153">새로운 AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="deb3b-153">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="deb3b-154">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="deb3b-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
