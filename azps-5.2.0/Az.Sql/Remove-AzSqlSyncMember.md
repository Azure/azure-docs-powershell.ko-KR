---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: c508dc9352bfcf70a9d3bad088f2b75de98db43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322678"
---
# <span data-ttu-id="980fc-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="980fc-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="980fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="980fc-102">SYNOPSIS</span></span>
<span data-ttu-id="980fc-103">Azure SQL 데이터베이스 동기화 멤버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="980fc-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="980fc-104">구문</span><span class="sxs-lookup"><span data-stu-id="980fc-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="980fc-105">설명</span><span class="sxs-lookup"><span data-stu-id="980fc-105">DESCRIPTION</span></span>
<span data-ttu-id="980fc-106">**Remove-AzSqlSyncMember** cmdlet은 Azure SQL 데이터베이스 동기화 멤버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="980fc-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="980fc-107">예제</span><span class="sxs-lookup"><span data-stu-id="980fc-107">EXAMPLES</span></span>

### <span data-ttu-id="980fc-108">예제 1: 동기화 멤버 제거</span><span class="sxs-lookup"><span data-stu-id="980fc-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="980fc-109">이 명령은 syncMember01이라는 Azure SQL 데이터베이스 동기화 멤버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="980fc-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="980fc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="980fc-110">PARAMETERS</span></span>

### <span data-ttu-id="980fc-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="980fc-111">-DatabaseName</span></span>
<span data-ttu-id="980fc-112">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="980fc-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="980fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="980fc-113">-DefaultProfile</span></span>
<span data-ttu-id="980fc-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="980fc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="980fc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="980fc-115">-Force</span></span>
<span data-ttu-id="980fc-116">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="980fc-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="980fc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="980fc-117">-Name</span></span>
<span data-ttu-id="980fc-118">동기화 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="980fc-118">The sync member name.</span></span>

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

### <span data-ttu-id="980fc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="980fc-119">-PassThru</span></span>
<span data-ttu-id="980fc-120">제거된 동기화 멤버를 반환할지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="980fc-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="980fc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="980fc-121">-ResourceGroupName</span></span>
<span data-ttu-id="980fc-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="980fc-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="980fc-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="980fc-123">-ServerName</span></span>
<span data-ttu-id="980fc-124">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="980fc-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="980fc-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="980fc-125">-SyncGroupName</span></span>
<span data-ttu-id="980fc-126">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="980fc-126">The sync group name.</span></span>

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

### <span data-ttu-id="980fc-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="980fc-127">-Confirm</span></span>
<span data-ttu-id="980fc-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="980fc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="980fc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="980fc-129">-WhatIf</span></span>
<span data-ttu-id="980fc-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="980fc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="980fc-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="980fc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="980fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="980fc-132">CommonParameters</span></span>
<span data-ttu-id="980fc-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="980fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="980fc-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="980fc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="980fc-135">입력</span><span class="sxs-lookup"><span data-stu-id="980fc-135">INPUTS</span></span>

### <span data-ttu-id="980fc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="980fc-136">System.String</span></span>

## <span data-ttu-id="980fc-137">출력</span><span class="sxs-lookup"><span data-stu-id="980fc-137">OUTPUTS</span></span>

### <span data-ttu-id="980fc-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="980fc-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="980fc-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="980fc-139">NOTES</span></span>

## <span data-ttu-id="980fc-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="980fc-140">RELATED LINKS</span></span>

[<span data-ttu-id="980fc-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="980fc-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="980fc-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="980fc-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="980fc-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="980fc-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

