---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
ms.openlocfilehash: 924e00578383e103d1451e311d027edd02752496
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527228"
---
# <span data-ttu-id="c919c-101">Get-AzureRmSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="c919c-101">Get-AzureRmSqlSyncGroupLog</span></span>

## <span data-ttu-id="c919c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c919c-102">SYNOPSIS</span></span>
<span data-ttu-id="c919c-103">Azure SQL 데이터베이스 동기화 그룹의 로그를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c919c-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c919c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c919c-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c919c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c919c-105">DESCRIPTION</span></span>
<span data-ttu-id="c919c-106">**AzureRmSqlSyncGroupLog** Cmdlet은 Azure SQL 데이터베이스 동기화 그룹의 로그를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c919c-106">The **Get-AzureRmSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="c919c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c919c-107">EXAMPLES</span></span>

### <span data-ttu-id="c919c-108">예제 1: Azure SQL 동기화 그룹의 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="c919c-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="c919c-109">이 명령은 Azure SQL 동기화 그룹의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c919c-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="c919c-110">변수</span><span class="sxs-lookup"><span data-stu-id="c919c-110">PARAMETERS</span></span>

### <span data-ttu-id="c919c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c919c-111">-DatabaseName</span></span>
<span data-ttu-id="c919c-112">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c919c-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="c919c-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c919c-113">-EndTime</span></span>
<span data-ttu-id="c919c-114">쿼리할 로그의 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="c919c-114">The end time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c919c-115">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="c919c-115">-LogLevel</span></span>
<span data-ttu-id="c919c-116">쿼리할 로그의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c919c-116">The type of the logs to query.</span></span>
<span data-ttu-id="c919c-117">유효한 값은 ' Error ', ' Warning ', ' Success ' 및 ' All '입니다.</span><span class="sxs-lookup"><span data-stu-id="c919c-117">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c919c-118">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c919c-118">-SyncGroupName</span></span>
<span data-ttu-id="c919c-119">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c919c-119">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c919c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c919c-120">-ResourceGroupName</span></span>
<span data-ttu-id="c919c-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c919c-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="c919c-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c919c-122">-ServerName</span></span>
<span data-ttu-id="c919c-123">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c919c-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="c919c-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c919c-124">-StartTime</span></span>
<span data-ttu-id="c919c-125">쿼리할 로그의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="c919c-125">The start time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c919c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c919c-126">-DefaultProfile</span></span>
<span data-ttu-id="c919c-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c919c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c919c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c919c-128">CommonParameters</span></span>
<span data-ttu-id="c919c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c919c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c919c-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c919c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c919c-131">입력</span><span class="sxs-lookup"><span data-stu-id="c919c-131">INPUTS</span></span>

## <span data-ttu-id="c919c-132">출력</span><span class="sxs-lookup"><span data-stu-id="c919c-132">OUTPUTS</span></span>

### <span data-ttu-id="c919c-133">AzureSqlSyncGroupLogModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="c919c-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="c919c-134">상속자</span><span class="sxs-lookup"><span data-stu-id="c919c-134">NOTES</span></span>

## <span data-ttu-id="c919c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c919c-135">RELATED LINKS</span></span>

