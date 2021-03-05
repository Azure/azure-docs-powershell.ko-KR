---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: adc3bc9c8d367da6f031f8847cee7ce48b3f9b43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961387"
---
# <span data-ttu-id="c95aa-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c95aa-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="c95aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c95aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c95aa-103">Azure 데이터베이스 장애 조치 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c95aa-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="c95aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="c95aa-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c95aa-105">설명</span><span class="sxs-lookup"><span data-stu-id="c95aa-105">DESCRIPTION</span></span>
<span data-ttu-id="c95aa-106">이 명령은 지정된 이름으로 장애 조치(Failover) 그룹을 제거하여 모든 데이터베이스 및 복제 관계는 그대로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="c95aa-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="c95aa-107">수신기 엔드포인트는 DNS에서 등록되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c95aa-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="c95aa-108">장애 조치(Failover) 그룹의 기본 서버를 사용하여 명령을 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c95aa-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="c95aa-109">예제</span><span class="sxs-lookup"><span data-stu-id="c95aa-109">EXAMPLES</span></span>

### <span data-ttu-id="c95aa-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c95aa-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="c95aa-111">장애 조치(Failover) 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c95aa-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="c95aa-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c95aa-112">PARAMETERS</span></span>

### <span data-ttu-id="c95aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c95aa-113">-DefaultProfile</span></span>
<span data-ttu-id="c95aa-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c95aa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c95aa-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="c95aa-115">-FailoverGroupName</span></span>
<span data-ttu-id="c95aa-116">제거할 데이터베이스 장애 조치 SQL Azure의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c95aa-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="c95aa-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c95aa-117">-Force</span></span>
<span data-ttu-id="c95aa-118">작업을 수행하기 위한 확인 메시지를 건너뜁합니다.</span><span class="sxs-lookup"><span data-stu-id="c95aa-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="c95aa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c95aa-119">-ResourceGroupName</span></span>
<span data-ttu-id="c95aa-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c95aa-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="c95aa-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c95aa-121">-ServerName</span></span>
<span data-ttu-id="c95aa-122">장애 조치(Failover) 그룹의 기본 Azure SQL 데이터베이스 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c95aa-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="c95aa-123">-확인</span><span class="sxs-lookup"><span data-stu-id="c95aa-123">-Confirm</span></span>
<span data-ttu-id="c95aa-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c95aa-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c95aa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c95aa-125">-WhatIf</span></span>
<span data-ttu-id="c95aa-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c95aa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c95aa-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c95aa-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c95aa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c95aa-128">CommonParameters</span></span>
<span data-ttu-id="c95aa-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c95aa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c95aa-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c95aa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c95aa-131">입력</span><span class="sxs-lookup"><span data-stu-id="c95aa-131">INPUTS</span></span>

### <span data-ttu-id="c95aa-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c95aa-132">System.String</span></span>

## <span data-ttu-id="c95aa-133">출력</span><span class="sxs-lookup"><span data-stu-id="c95aa-133">OUTPUTS</span></span>

### <span data-ttu-id="c95aa-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c95aa-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="c95aa-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c95aa-135">NOTES</span></span>

## <span data-ttu-id="c95aa-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c95aa-136">RELATED LINKS</span></span>

[<span data-ttu-id="c95aa-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c95aa-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c95aa-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c95aa-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c95aa-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c95aa-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c95aa-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c95aa-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="c95aa-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c95aa-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="c95aa-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c95aa-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c95aa-143">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="c95aa-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
