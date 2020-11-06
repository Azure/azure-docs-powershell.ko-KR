---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 45be8d0ef10b040fd27a714444bb60bbf6a69951
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535383"
---
# <span data-ttu-id="fabc2-101">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fabc2-101">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="fabc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fabc2-102">SYNOPSIS</span></span>
<span data-ttu-id="fabc2-103">Azure SQL 데이터베이스 장애 조치 그룹의 장애 조치를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fabc2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fabc2-104">SYNTAX</span></span>

```
Switch-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fabc2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fabc2-105">DESCRIPTION</span></span>
<span data-ttu-id="fabc2-106">이 명령은 장애 조치 (Failover) 그룹에 있는 서버의 역할을 전환 하 고 모든 보조 데이터베이스를 주 역할로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="fabc2-107">DNS 클라이언트 캐시를 새로 고치면 모든 새 TDS 세션이 자동으로 보조 서버로 다시 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="fabc2-108">원본 주 서버가 다시 온라인 상태가 되 면 이전의 모든 주 데이터베이스가 보조 역할로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>

<span data-ttu-id="fabc2-109">이 명령을 실행 하려면 장애 조치 그룹의 보조 서버를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="fabc2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fabc2-110">EXAMPLES</span></span>

### <span data-ttu-id="fabc2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fabc2-111">Example 1</span></span>
```
C:\> Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzureRmSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="fabc2-112">장애 조치 (Failover) 그룹의 파이핑에서 데이터 손실을 허용 하는 장애 조치 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="fabc2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="fabc2-113">Example 2</span></span>
```
C:\> Switch-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="fabc2-114">데이터 손실 또는 실패 및 롤백 없이 성공할 수 있는 최상의 장애 조치 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="fabc2-115">변수</span><span class="sxs-lookup"><span data-stu-id="fabc2-115">PARAMETERS</span></span>

### <span data-ttu-id="fabc2-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="fabc2-116">-AllowDataLoss</span></span>
<span data-ttu-id="fabc2-117">장애 조치를 완료 하면 데이터 손실이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="fabc2-118">이렇게 하면 기본 데이터베이스를 사용할 수 없는 경우에도 장애 조치를 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fabc2-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="fabc2-119">-FailoverGroupName</span></span>
<span data-ttu-id="fabc2-120">Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-120">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="fabc2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fabc2-121">-ResourceGroupName</span></span>
<span data-ttu-id="fabc2-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="fabc2-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fabc2-123">-ServerName</span></span>
<span data-ttu-id="fabc2-124">장애 조치 (Failover) 그룹의 보조 Azure SQL 데이터베이스 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-124">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="fabc2-125">-확인</span><span class="sxs-lookup"><span data-stu-id="fabc2-125">-Confirm</span></span>
<span data-ttu-id="fabc2-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fabc2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fabc2-127">-WhatIf</span></span>
<span data-ttu-id="fabc2-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fabc2-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fabc2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fabc2-130">-DefaultProfile</span></span>
<span data-ttu-id="fabc2-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fabc2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fabc2-132">CommonParameters</span></span>
<span data-ttu-id="fabc2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabc2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fabc2-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fabc2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fabc2-135">입력</span><span class="sxs-lookup"><span data-stu-id="fabc2-135">INPUTS</span></span>

### <span data-ttu-id="fabc2-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fabc2-136">System.String</span></span>

## <span data-ttu-id="fabc2-137">출력</span><span class="sxs-lookup"><span data-stu-id="fabc2-137">OUTPUTS</span></span>

### <span data-ttu-id="fabc2-138">System. 개체</span><span class="sxs-lookup"><span data-stu-id="fabc2-138">System.Object</span></span>

## <span data-ttu-id="fabc2-139">상속자</span><span class="sxs-lookup"><span data-stu-id="fabc2-139">NOTES</span></span>

## <span data-ttu-id="fabc2-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fabc2-140">RELATED LINKS</span></span>

[<span data-ttu-id="fabc2-141">새로운 AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fabc2-141">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fabc2-142">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fabc2-142">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fabc2-143">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fabc2-143">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fabc2-144">추가-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fabc2-144">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="fabc2-145">제거-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fabc2-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="fabc2-146">제거-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fabc2-146">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fabc2-147">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="fabc2-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
