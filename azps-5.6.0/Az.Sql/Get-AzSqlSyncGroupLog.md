---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: 40a269ab3d8378ce2f5a2024baee5bca18fe2134
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988801"
---
# <span data-ttu-id="f9039-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="f9039-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="f9039-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9039-102">SYNOPSIS</span></span>
<span data-ttu-id="f9039-103">Azure 데이터베이스 동기화 그룹의 로그를 SQL 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f9039-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="f9039-104">구문</span><span class="sxs-lookup"><span data-stu-id="f9039-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9039-105">설명</span><span class="sxs-lookup"><span data-stu-id="f9039-105">DESCRIPTION</span></span>
<span data-ttu-id="f9039-106">**Get-AzSqlSyncGroupLog** cmdlet은 Azure 데이터베이스 동기화 그룹의 로그를 SQL 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f9039-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="f9039-107">예제</span><span class="sxs-lookup"><span data-stu-id="f9039-107">EXAMPLES</span></span>

### <span data-ttu-id="f9039-108">예제 1: Azure SQL 동기화 그룹의 로그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9039-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="f9039-109">이 명령은 Azure 동기화 그룹의 로그를 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9039-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="f9039-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f9039-110">PARAMETERS</span></span>

### <span data-ttu-id="f9039-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f9039-111">-DatabaseName</span></span>
<span data-ttu-id="f9039-112">Azure 데이터베이스의 SQL 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="f9039-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f9039-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9039-113">-DefaultProfile</span></span>
<span data-ttu-id="f9039-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f9039-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9039-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f9039-115">-EndTime</span></span>
<span data-ttu-id="f9039-116">쿼리할 로그의 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="f9039-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="f9039-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="f9039-117">-LogLevel</span></span>
<span data-ttu-id="f9039-118">쿼리할 로그의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="f9039-118">The type of the logs to query.</span></span>
<span data-ttu-id="f9039-119">유효한 값은 '오류', '경고', '성공' 및 '모두'입니다.</span><span class="sxs-lookup"><span data-stu-id="f9039-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="f9039-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9039-120">-ResourceGroupName</span></span>
<span data-ttu-id="f9039-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9039-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9039-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f9039-122">-ServerName</span></span>
<span data-ttu-id="f9039-123">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f9039-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f9039-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f9039-124">-StartTime</span></span>
<span data-ttu-id="f9039-125">쿼리할 로그의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="f9039-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="f9039-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f9039-126">-SyncGroupName</span></span>
<span data-ttu-id="f9039-127">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9039-127">The sync group name.</span></span>

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

### <span data-ttu-id="f9039-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9039-128">CommonParameters</span></span>
<span data-ttu-id="f9039-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9039-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9039-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9039-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9039-131">입력</span><span class="sxs-lookup"><span data-stu-id="f9039-131">INPUTS</span></span>

### <span data-ttu-id="f9039-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f9039-132">System.String</span></span>

## <span data-ttu-id="f9039-133">출력</span><span class="sxs-lookup"><span data-stu-id="f9039-133">OUTPUTS</span></span>

### <span data-ttu-id="f9039-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="f9039-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="f9039-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f9039-135">NOTES</span></span>

## <span data-ttu-id="f9039-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9039-136">RELATED LINKS</span></span>
