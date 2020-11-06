---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 0e07ce9eb3f3368e17c20a339c65a410b5f1d553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529090"
---
# <span data-ttu-id="8dfd1-101">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8dfd1-101">Get-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="8dfd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dfd1-102">SYNOPSIS</span></span>
<span data-ttu-id="8dfd1-103">Azure SQL 데이터베이스 장애 조치 (Failover) 그룹을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dfd1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8dfd1-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dfd1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8dfd1-105">DESCRIPTION</span></span>
<span data-ttu-id="8dfd1-106">특정 Azure SQL 데이터베이스 장애 조치 그룹을 가져오거나 서버의 장애 조치 (Failover) 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>

<span data-ttu-id="8dfd1-107">장애 조치 (Failover) 그룹의 서버 중 하나를 사용 하 여 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="8dfd1-108">반환 된 값은 장애 조치 그룹과 관련 하 여 지정 된 서버의 상태를 반영 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="8dfd1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8dfd1-109">EXAMPLES</span></span>

### <span data-ttu-id="8dfd1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8dfd1-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="8dfd1-111">서버의 모든 장애 조치 (Failover) 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="8dfd1-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="8dfd1-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="8dfd1-113">특정 장애 조치 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-113">Get a specific Failover Group.</span></span>

## <span data-ttu-id="8dfd1-114">변수</span><span class="sxs-lookup"><span data-stu-id="8dfd1-114">PARAMETERS</span></span>

### <span data-ttu-id="8dfd1-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="8dfd1-115">-FailoverGroupName</span></span>
<span data-ttu-id="8dfd1-116">검색할 Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-116">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dfd1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dfd1-117">-ResourceGroupName</span></span>
<span data-ttu-id="8dfd1-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="8dfd1-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8dfd1-119">-ServerName</span></span>
<span data-ttu-id="8dfd1-120">장애 조치 (Failover) 그룹을 검색할 Azure SQL 데이터베이스 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-120">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="8dfd1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dfd1-121">-DefaultProfile</span></span>
<span data-ttu-id="8dfd1-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dfd1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dfd1-123">CommonParameters</span></span>
<span data-ttu-id="8dfd1-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dfd1-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dfd1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dfd1-126">입력</span><span class="sxs-lookup"><span data-stu-id="8dfd1-126">INPUTS</span></span>

### <span data-ttu-id="8dfd1-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8dfd1-127">System.String</span></span>

## <span data-ttu-id="8dfd1-128">출력</span><span class="sxs-lookup"><span data-stu-id="8dfd1-128">OUTPUTS</span></span>

### <span data-ttu-id="8dfd1-129">System. 개체</span><span class="sxs-lookup"><span data-stu-id="8dfd1-129">System.Object</span></span>

## <span data-ttu-id="8dfd1-130">상속자</span><span class="sxs-lookup"><span data-stu-id="8dfd1-130">NOTES</span></span>

## <span data-ttu-id="8dfd1-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8dfd1-131">RELATED LINKS</span></span>

[<span data-ttu-id="8dfd1-132">새로운 AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8dfd1-132">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8dfd1-133">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8dfd1-133">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8dfd1-134">추가-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8dfd1-134">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="8dfd1-135">제거-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8dfd1-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="8dfd1-136">스위치-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8dfd1-136">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8dfd1-137">제거-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8dfd1-137">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8dfd1-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="8dfd1-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
