---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: f2229fa904144b0dd95a054da95db99600963406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529083"
---
# <span data-ttu-id="72eb6-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="72eb6-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="72eb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="72eb6-103">탄력적 풀 및 해당 속성 값의 탄력적 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="72eb6-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72eb6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72eb6-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72eb6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="72eb6-105">DESCRIPTION</span></span>
<span data-ttu-id="72eb6-106">**AzureRmSqlElasticPoolDatabase** cmdlet은 탄력적 풀 및 해당 속성 값의 탄력적 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="72eb6-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="72eb6-107">Azure SQL 데이터베이스에서 탄력적 데이터베이스의 이름을 지정 하 여 해당 데이터베이스에 대 한 속성 값을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72eb6-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="72eb6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="72eb6-108">EXAMPLES</span></span>

### <span data-ttu-id="72eb6-109">예제 1: 탄력적 풀의 모든 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="72eb6-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="72eb6-110">이 명령은 ElasticPool01 이라는 탄력적 풀의 모든 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="72eb6-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="72eb6-111">변수</span><span class="sxs-lookup"><span data-stu-id="72eb6-111">PARAMETERS</span></span>

### <span data-ttu-id="72eb6-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="72eb6-112">-DatabaseName</span></span>
<span data-ttu-id="72eb6-113">이 cmdlet이 가져오는 SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72eb6-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72eb6-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="72eb6-114">-ElasticPoolName</span></span>
<span data-ttu-id="72eb6-115">탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72eb6-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="72eb6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72eb6-116">-ResourceGroupName</span></span>
<span data-ttu-id="72eb6-117">탄력적 풀이 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72eb6-117">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="72eb6-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72eb6-118">-ServerName</span></span>
<span data-ttu-id="72eb6-119">탄력적 풀이 포함 된 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72eb6-119">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="72eb6-120">-확인</span><span class="sxs-lookup"><span data-stu-id="72eb6-120">-Confirm</span></span>
<span data-ttu-id="72eb6-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72eb6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72eb6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72eb6-122">-WhatIf</span></span>
<span data-ttu-id="72eb6-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="72eb6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72eb6-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72eb6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72eb6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72eb6-125">-DefaultProfile</span></span>
<span data-ttu-id="72eb6-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="72eb6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72eb6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72eb6-127">CommonParameters</span></span>
<span data-ttu-id="72eb6-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72eb6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72eb6-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72eb6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72eb6-130">입력</span><span class="sxs-lookup"><span data-stu-id="72eb6-130">INPUTS</span></span>

## <span data-ttu-id="72eb6-131">출력</span><span class="sxs-lookup"><span data-stu-id="72eb6-131">OUTPUTS</span></span>

### <span data-ttu-id="72eb6-132">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="72eb6-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="72eb6-133">상속자</span><span class="sxs-lookup"><span data-stu-id="72eb6-133">NOTES</span></span>

## <span data-ttu-id="72eb6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72eb6-134">RELATED LINKS</span></span>

[<span data-ttu-id="72eb6-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="72eb6-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="72eb6-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="72eb6-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="72eb6-137">새로운 AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="72eb6-137">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="72eb6-138">제거-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="72eb6-138">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="72eb6-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="72eb6-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

