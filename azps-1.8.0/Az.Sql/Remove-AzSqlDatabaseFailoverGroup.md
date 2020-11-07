---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 93b20d240e2115fb6522032c13d6d116f3db55aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698860"
---
# <span data-ttu-id="18cd0-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="18cd0-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="18cd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="18cd0-103">Azure SQL Database 장애 조치 (Failover) 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="18cd0-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="18cd0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="18cd0-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18cd0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="18cd0-105">DESCRIPTION</span></span>
<span data-ttu-id="18cd0-106">이 명령은 지정 된 이름의 장애 조치 (Failover) 그룹을 제거 하 고 모든 데이터베이스와 복제 관계는 그대로 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="18cd0-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="18cd0-107">수신기 끝점은 DNS에서 등록 취소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="18cd0-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="18cd0-108">명령 실행을 위해 장애 조치 그룹의 주 서버를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="18cd0-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="18cd0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="18cd0-109">EXAMPLES</span></span>

### <span data-ttu-id="18cd0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="18cd0-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="18cd0-111">장애 조치 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="18cd0-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="18cd0-112">변수</span><span class="sxs-lookup"><span data-stu-id="18cd0-112">PARAMETERS</span></span>

### <span data-ttu-id="18cd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18cd0-113">-DefaultProfile</span></span>
<span data-ttu-id="18cd0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="18cd0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18cd0-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="18cd0-115">-FailoverGroupName</span></span>
<span data-ttu-id="18cd0-116">제거할 Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18cd0-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="18cd0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="18cd0-117">-Force</span></span>
<span data-ttu-id="18cd0-118">작업 수행에 대 한 건너뛰기 확인 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="18cd0-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="18cd0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18cd0-119">-ResourceGroupName</span></span>
<span data-ttu-id="18cd0-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18cd0-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="18cd0-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="18cd0-121">-ServerName</span></span>
<span data-ttu-id="18cd0-122">장애 조치 (Failover) 그룹의 기본 Azure SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18cd0-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="18cd0-123">-확인</span><span class="sxs-lookup"><span data-stu-id="18cd0-123">-Confirm</span></span>
<span data-ttu-id="18cd0-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="18cd0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18cd0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18cd0-125">-WhatIf</span></span>
<span data-ttu-id="18cd0-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="18cd0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18cd0-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18cd0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18cd0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18cd0-128">CommonParameters</span></span>
<span data-ttu-id="18cd0-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="18cd0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18cd0-130">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="18cd0-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18cd0-131">입력</span><span class="sxs-lookup"><span data-stu-id="18cd0-131">INPUTS</span></span>

### <span data-ttu-id="18cd0-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="18cd0-132">System.String</span></span>

## <span data-ttu-id="18cd0-133">출력</span><span class="sxs-lookup"><span data-stu-id="18cd0-133">OUTPUTS</span></span>

### <span data-ttu-id="18cd0-134">AzureSqlFailoverGroupModel (\*. \*.)</span><span class="sxs-lookup"><span data-stu-id="18cd0-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="18cd0-135">상속자</span><span class="sxs-lookup"><span data-stu-id="18cd0-135">NOTES</span></span>

## <span data-ttu-id="18cd0-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18cd0-136">RELATED LINKS</span></span>

[<span data-ttu-id="18cd0-137">새로운 AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="18cd0-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="18cd0-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="18cd0-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="18cd0-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="18cd0-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="18cd0-140">추가-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="18cd0-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="18cd0-141">제거-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="18cd0-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="18cd0-142">스위치-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="18cd0-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="18cd0-143">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="18cd0-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
