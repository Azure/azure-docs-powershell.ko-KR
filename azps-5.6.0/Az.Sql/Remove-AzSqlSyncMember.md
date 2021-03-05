---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: 58a6ee3d51af355c0824025f856ed1646fa23cf1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995064"
---
# <span data-ttu-id="7fbe2-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7fbe2-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="7fbe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fbe2-102">SYNOPSIS</span></span>
<span data-ttu-id="7fbe2-103">Azure 데이터베이스 동기화 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7fbe2-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="7fbe2-104">구문</span><span class="sxs-lookup"><span data-stu-id="7fbe2-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fbe2-105">설명</span><span class="sxs-lookup"><span data-stu-id="7fbe2-105">DESCRIPTION</span></span>
<span data-ttu-id="7fbe2-106">**Remove-AzSqlSyncMember** cmdlet은 Azure SQL 데이터베이스 동기화 멤버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7fbe2-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="7fbe2-107">예제</span><span class="sxs-lookup"><span data-stu-id="7fbe2-107">EXAMPLES</span></span>

### <span data-ttu-id="7fbe2-108">예제 1: 동기화 멤버 제거</span><span class="sxs-lookup"><span data-stu-id="7fbe2-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="7fbe2-109">이 명령은 syncMember01이라는 azure SQL 데이터베이스 동기화 멤버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7fbe2-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="7fbe2-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7fbe2-110">PARAMETERS</span></span>

### <span data-ttu-id="7fbe2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7fbe2-111">-DatabaseName</span></span>
<span data-ttu-id="7fbe2-112">Azure 데이터베이스의 SQL 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="7fbe2-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="7fbe2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fbe2-113">-DefaultProfile</span></span>
<span data-ttu-id="7fbe2-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7fbe2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fbe2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7fbe2-115">-Force</span></span>
<span data-ttu-id="7fbe2-116">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="7fbe2-116">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbe2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7fbe2-117">-Name</span></span>
<span data-ttu-id="7fbe2-118">동기화 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fbe2-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fbe2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fbe2-119">-PassThru</span></span>
<span data-ttu-id="7fbe2-120">제거된 동기화 멤버를 반환할지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="7fbe2-120">Defines Whether return the removed sync member</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbe2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fbe2-121">-ResourceGroupName</span></span>
<span data-ttu-id="7fbe2-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fbe2-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="7fbe2-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7fbe2-123">-ServerName</span></span>
<span data-ttu-id="7fbe2-124">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7fbe2-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="7fbe2-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="7fbe2-125">-SyncGroupName</span></span>
<span data-ttu-id="7fbe2-126">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fbe2-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fbe2-127">-확인</span><span class="sxs-lookup"><span data-stu-id="7fbe2-127">-Confirm</span></span>
<span data-ttu-id="7fbe2-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fbe2-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbe2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fbe2-129">-WhatIf</span></span>
<span data-ttu-id="7fbe2-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7fbe2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fbe2-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7fbe2-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbe2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fbe2-132">CommonParameters</span></span>
<span data-ttu-id="7fbe2-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7fbe2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fbe2-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fbe2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fbe2-135">입력</span><span class="sxs-lookup"><span data-stu-id="7fbe2-135">INPUTS</span></span>

### <span data-ttu-id="7fbe2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7fbe2-136">System.String</span></span>

## <span data-ttu-id="7fbe2-137">출력</span><span class="sxs-lookup"><span data-stu-id="7fbe2-137">OUTPUTS</span></span>

### <span data-ttu-id="7fbe2-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="7fbe2-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="7fbe2-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7fbe2-139">NOTES</span></span>

## <span data-ttu-id="7fbe2-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fbe2-140">RELATED LINKS</span></span>

[<span data-ttu-id="7fbe2-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7fbe2-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="7fbe2-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7fbe2-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="7fbe2-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7fbe2-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

