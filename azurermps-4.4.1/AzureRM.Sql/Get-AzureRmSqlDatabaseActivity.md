---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: b37ae31c1f0dc6360743a863f0305fd5823cbb3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536159"
---
# <span data-ttu-id="5dc38-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="5dc38-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="5dc38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dc38-102">SYNOPSIS</span></span>
<span data-ttu-id="5dc38-103">탄력적 데이터베이스 이동 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dc38-103">Gets the status of moving elastic databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dc38-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5dc38-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> -ElasticPoolName <String> -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dc38-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5dc38-105">DESCRIPTION</span></span>
<span data-ttu-id="5dc38-106">**AzureRmSqlDatabaseActivity** Cmdlet은 Azure SQL database의 탄력적 데이터베이스 풀로 이동 하거나 외부로 이동한 탄력적 데이터베이스의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dc38-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of elastic databases moving into or out of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="5dc38-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5dc38-107">EXAMPLES</span></span>

### <span data-ttu-id="5dc38-108">예제 1: 모든 SQL 데이터베이스 인스턴스의 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="5dc38-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="5dc38-109">이 명령은 ElasticPool01 이라는 탄력적 풀에 있는 모든 SQL 데이터베이스 인스턴스의 작업 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc38-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="5dc38-110">변수</span><span class="sxs-lookup"><span data-stu-id="5dc38-110">PARAMETERS</span></span>

### <span data-ttu-id="5dc38-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5dc38-111">-DatabaseName</span></span>
<span data-ttu-id="5dc38-112">이 cmdlet이 상태를 가져오는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc38-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="5dc38-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5dc38-113">-ElasticPoolName</span></span>
<span data-ttu-id="5dc38-114">이 cmdlet이 상태를 가져오는 탄력적 데이터베이스 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc38-114">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="5dc38-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5dc38-115">-OperationId</span></span>
<span data-ttu-id="5dc38-116">이 cmdlet이 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc38-116">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dc38-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dc38-117">-ResourceGroupName</span></span>
<span data-ttu-id="5dc38-118">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc38-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5dc38-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5dc38-119">-ServerName</span></span>
<span data-ttu-id="5dc38-120">탄력적 데이터베이스 풀을 호스팅하는 Microsoft SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc38-120">Specifies the name of the Microsoft SQL Server that hosts the elastic database pool.</span></span>

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

### <span data-ttu-id="5dc38-121">-확인</span><span class="sxs-lookup"><span data-stu-id="5dc38-121">-Confirm</span></span>
<span data-ttu-id="5dc38-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc38-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dc38-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dc38-123">-WhatIf</span></span>
<span data-ttu-id="5dc38-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5dc38-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dc38-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5dc38-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dc38-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dc38-126">-DefaultProfile</span></span>
<span data-ttu-id="5dc38-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5dc38-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dc38-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dc38-128">CommonParameters</span></span>
<span data-ttu-id="5dc38-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc38-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dc38-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dc38-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dc38-131">입력</span><span class="sxs-lookup"><span data-stu-id="5dc38-131">INPUTS</span></span>

## <span data-ttu-id="5dc38-132">출력</span><span class="sxs-lookup"><span data-stu-id="5dc38-132">OUTPUTS</span></span>

### <span data-ttu-id="5dc38-133">AzureSqlDatabaseActivityModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="5dc38-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="5dc38-134">상속자</span><span class="sxs-lookup"><span data-stu-id="5dc38-134">NOTES</span></span>

## <span data-ttu-id="5dc38-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5dc38-135">RELATED LINKS</span></span>

