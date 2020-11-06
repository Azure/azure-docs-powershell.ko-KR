---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
ms.openlocfilehash: f06481984ef478a6bf3af51de1796855c265c2c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531617"
---
# <span data-ttu-id="24a96-101">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="24a96-101">Get-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="24a96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24a96-102">SYNOPSIS</span></span>
<span data-ttu-id="24a96-103">Azure SQL 데이터베이스에서 탄력적 풀 및 해당 속성 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24a96-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24a96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24a96-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24a96-105">설명은</span><span class="sxs-lookup"><span data-stu-id="24a96-105">DESCRIPTION</span></span>
<span data-ttu-id="24a96-106">**Get-AzureRmSqlElasticPool** cmdlet은 탄력적 풀 및 해당 속성 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24a96-106">The **Get-AzureRmSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="24a96-107">기존 탄력적 풀의 이름을 지정 하 여 해당 풀에 대 한 속성 값을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a96-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="24a96-108">예제의</span><span class="sxs-lookup"><span data-stu-id="24a96-108">EXAMPLES</span></span>

### <span data-ttu-id="24a96-109">예제 1: 모든 탄력적인 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="24a96-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="24a96-110">이 명령은 Server01 이라는 서버의 모든 탄력적 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24a96-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="24a96-111">예제 2: 특정 탄력적 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="24a96-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
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

<span data-ttu-id="24a96-112">이 명령은 Server01 라는 서버에서 ElasticPool0127 이라는 탄력적 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24a96-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="24a96-113">예제 3: Azure SQL 탄력적 데이터베이스 풀에 대 한 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="24a96-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-Metrics -TimeGrain 0:5:0
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

<span data-ttu-id="24a96-114">이 명령은 ElasticPool01 이라는 Azure SQL 탄력적 데이터베이스 풀에 대 한 메트릭을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a96-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

## <span data-ttu-id="24a96-115">변수</span><span class="sxs-lookup"><span data-stu-id="24a96-115">PARAMETERS</span></span>

### <span data-ttu-id="24a96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a96-116">-DefaultProfile</span></span>
<span data-ttu-id="24a96-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="24a96-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24a96-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="24a96-118">-ElasticPoolName</span></span>
<span data-ttu-id="24a96-119">이 cmdlet이 가져오는 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a96-119">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a96-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a96-120">-ResourceGroupName</span></span>
<span data-ttu-id="24a96-121">이 cmdlet이 가져오는 탄력적인 풀을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a96-121">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="24a96-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="24a96-122">-ServerName</span></span>
<span data-ttu-id="24a96-123">이 cmdlet이 가져오는 탄력적 풀을 포함 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a96-123">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="24a96-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a96-124">CommonParameters</span></span>
<span data-ttu-id="24a96-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a96-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a96-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a96-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a96-127">입력</span><span class="sxs-lookup"><span data-stu-id="24a96-127">INPUTS</span></span>

### <span data-ttu-id="24a96-128">않아야</span><span class="sxs-lookup"><span data-stu-id="24a96-128">None</span></span>
<span data-ttu-id="24a96-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24a96-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24a96-130">출력</span><span class="sxs-lookup"><span data-stu-id="24a96-130">OUTPUTS</span></span>

### <span data-ttu-id="24a96-131">ElasticPool. AzureSqlElasticPoolModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="24a96-131">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="24a96-132">상속자</span><span class="sxs-lookup"><span data-stu-id="24a96-132">NOTES</span></span>

## <span data-ttu-id="24a96-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24a96-133">RELATED LINKS</span></span>

[<span data-ttu-id="24a96-134">새로운 AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="24a96-134">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="24a96-135">제거-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="24a96-135">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="24a96-136">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="24a96-136">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


