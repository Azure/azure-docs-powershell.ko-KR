---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 05f2de37ebeb477d45f96c415759ead3080a9e60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529988"
---
# <span data-ttu-id="b8c0d-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8c0d-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="b8c0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c0d-103">Azure SQL Database 장애 조치 (Failover) 그룹의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c0d-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8c0d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8c0d-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8c0d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b8c0d-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c0d-106">이 명령은 Azure SQL Database 장애 조치 (Failover) 그룹의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c0d-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>

<span data-ttu-id="b8c0d-107">명령 실행을 위해 장애 조치 그룹의 주 서버를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c0d-107">The Failover Group's primary server should be used to execute the command.</span></span>

<span data-ttu-id="b8c0d-108">그룹의 데이터베이스 집합을 제어 하려면 ' AzureRmSqlDatabaseToFailoverGroup ' 및 ' Remove-AzureRmSqlDatabaseFromFailoverGroup '을 대신 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c0d-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>

<span data-ttu-id="b8c0d-109">장애 조치 (Failover) 그룹 기능을 미리 보는 동안에는 '-GracePeriodWithDataLossHours ' 매개 변수에 대해 1 시간 보다 크거나 같은 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8c0d-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="b8c0d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b8c0d-110">EXAMPLES</span></span>

### <span data-ttu-id="b8c0d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8c0d-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="b8c0d-112">장애 조치 그룹의 장애 조치 정책을 ' 자동 '으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c0d-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="b8c0d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b8c0d-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="b8c0d-114">장애 조치 (failover) 그룹의 파이프를 통해 장애 조치 그룹의 장애 조치 정책을 ' 수동 '으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c0d-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="b8c0d-115">변수</span><span class="sxs-lookup"><span data-stu-id="b8c0d-115">PARAMETERS</span></span>

### <span data-ttu-id="b8c0d-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="b8c0d-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="b8c0d-117">보조 서버의 작동 중단이 읽기 전용 끝점의 자동 장애 조치를 트리거해야 하는지 여부</span><span class="sxs-lookup"><span data-stu-id="b8c0d-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="b8c0d-118">이 기능은 아직 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8c0d-118">This feature is not yet supported.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c0d-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c0d-119">-FailoverGroupName</span></span>
<span data-ttu-id="b8c0d-120">Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8c0d-120">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="b8c0d-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="b8c0d-121">-FailoverPolicy</span></span>
<span data-ttu-id="b8c0d-122">Azure SQL Database 장애 조치 (Failover) 그룹의 장애 조치 정책</span><span class="sxs-lookup"><span data-stu-id="b8c0d-122">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c0d-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="b8c0d-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="b8c0d-124">기본 서버에서 작동 중지가 발생 하 고 데이터 손실 없이 장애 조치를 완료할 수 없는 경우 자동 장애 조치가 시작 되기 전의 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="b8c0d-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c0d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c0d-125">-ResourceGroupName</span></span>
<span data-ttu-id="b8c0d-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8c0d-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="b8c0d-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b8c0d-127">-ServerName</span></span>
<span data-ttu-id="b8c0d-128">장애 조치 (Failover) 그룹의 기본 Azure SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8c0d-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="b8c0d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c0d-129">-DefaultProfile</span></span>
<span data-ttu-id="b8c0d-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8c0d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8c0d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c0d-131">CommonParameters</span></span>
<span data-ttu-id="b8c0d-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8c0d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c0d-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c0d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c0d-134">입력</span><span class="sxs-lookup"><span data-stu-id="b8c0d-134">INPUTS</span></span>

### <span data-ttu-id="b8c0d-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b8c0d-135">System.String</span></span>

## <span data-ttu-id="b8c0d-136">출력</span><span class="sxs-lookup"><span data-stu-id="b8c0d-136">OUTPUTS</span></span>

### <span data-ttu-id="b8c0d-137">System. 개체</span><span class="sxs-lookup"><span data-stu-id="b8c0d-137">System.Object</span></span>

## <span data-ttu-id="b8c0d-138">상속자</span><span class="sxs-lookup"><span data-stu-id="b8c0d-138">NOTES</span></span>

## <span data-ttu-id="b8c0d-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8c0d-139">RELATED LINKS</span></span>

[<span data-ttu-id="b8c0d-140">새로운 AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8c0d-140">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b8c0d-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8c0d-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b8c0d-142">추가-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8c0d-142">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="b8c0d-143">제거-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8c0d-143">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="b8c0d-144">스위치-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8c0d-144">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b8c0d-145">제거-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8c0d-145">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b8c0d-146">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b8c0d-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
