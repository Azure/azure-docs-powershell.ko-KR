---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
ms.openlocfilehash: ebc9386df78af1a730578c57e3957a869bbc299b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176924"
---
# <span data-ttu-id="25ab0-101">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="25ab0-101">Get-AzSqlElasticPool</span></span>

## <span data-ttu-id="25ab0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25ab0-102">SYNOPSIS</span></span>
<span data-ttu-id="25ab0-103">Azure SQL Database에서 탄력적 풀 및 해당 속성 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25ab0-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

## <span data-ttu-id="25ab0-104">구문</span><span class="sxs-lookup"><span data-stu-id="25ab0-104">SYNTAX</span></span>

```
Get-AzSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25ab0-105">설명</span><span class="sxs-lookup"><span data-stu-id="25ab0-105">DESCRIPTION</span></span>
<span data-ttu-id="25ab0-106">**Get-AzSqlElasticPool** cmdlet은 탄력적 풀 및 속성 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25ab0-106">The **Get-AzSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="25ab0-107">기존 탄력적 풀의 이름을 지정하여 해당 풀에 대한 속성 값만 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="25ab0-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="25ab0-108">예제</span><span class="sxs-lookup"><span data-stu-id="25ab0-108">EXAMPLES</span></span>

### <span data-ttu-id="25ab0-109">예제 1: 모든 탄력적 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25ab0-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="25ab0-110">이 명령은 Server01이라는 서버에서 모든 탄력적 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25ab0-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="25ab0-111">예제 2: 특정 탄력적 풀을 얻게</span><span class="sxs-lookup"><span data-stu-id="25ab0-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="25ab0-112">이 명령은 Server01이라는 서버에서 ElasticPool0127이라는 탄력적 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25ab0-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="25ab0-113">예제 3: Azure SQL Elastic Database 풀에 대한 메트릭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25ab0-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-AzMetric -TimeGrain 0:5:0 -MetricName storage_percent
DimensionName  : 
DimensionValue : 
Name           : cpu_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : physical_data_read_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : log_write_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : dtu_consumption_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : storage_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent
```

<span data-ttu-id="25ab0-114">이 명령은 ElasticPool01이라는 탄력적 데이터베이스 SQL Azure에 대한 메트릭을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="25ab0-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

### <span data-ttu-id="25ab0-115">예제 4: 필터링 -ElasticPoolName "ElasticPool\*"을 사용하여 모든 탄력적 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25ab0-115">Example 4: Get all elastic pools using filtering -ElasticPoolName "ElasticPool\*"</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="25ab0-116">이 명령은 "ElasticPool"으로 시작하는 Server01 서버의 모든 탄력적 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25ab0-116">This command gets all of the elastic pools on the server named Server01 that start with "ElasticPool".</span></span>

## <span data-ttu-id="25ab0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25ab0-117">PARAMETERS</span></span>

### <span data-ttu-id="25ab0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25ab0-118">-DefaultProfile</span></span>
<span data-ttu-id="25ab0-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="25ab0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25ab0-120">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="25ab0-120">-ElasticPoolName</span></span>
<span data-ttu-id="25ab0-121">이 cmdlet에서 얻을 탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="25ab0-121">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ab0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25ab0-122">-ResourceGroupName</span></span>
<span data-ttu-id="25ab0-123">이 cmdlet에서 얻을 수 있는 탄력적 풀을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="25ab0-123">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="25ab0-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="25ab0-124">-ServerName</span></span>
<span data-ttu-id="25ab0-125">이 cmdlet에서 얻을 수 있는 탄력적 풀을 포함하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="25ab0-125">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="25ab0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ab0-126">CommonParameters</span></span>
<span data-ttu-id="25ab0-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25ab0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25ab0-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="25ab0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ab0-129">입력</span><span class="sxs-lookup"><span data-stu-id="25ab0-129">INPUTS</span></span>

### <span data-ttu-id="25ab0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="25ab0-130">System.String</span></span>

## <span data-ttu-id="25ab0-131">출력</span><span class="sxs-lookup"><span data-stu-id="25ab0-131">OUTPUTS</span></span>

### <span data-ttu-id="25ab0-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="25ab0-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="25ab0-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25ab0-133">NOTES</span></span>

## <span data-ttu-id="25ab0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25ab0-134">RELATED LINKS</span></span>

[<span data-ttu-id="25ab0-135">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="25ab0-135">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="25ab0-136">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="25ab0-136">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="25ab0-137">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="25ab0-137">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


