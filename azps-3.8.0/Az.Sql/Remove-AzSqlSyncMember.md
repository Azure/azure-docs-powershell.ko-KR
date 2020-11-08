---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: c508dc9352bfcf70a9d3bad088f2b75de98db43d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043162"
---
# <span data-ttu-id="a04d0-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a04d0-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="a04d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a04d0-102">SYNOPSIS</span></span>
<span data-ttu-id="a04d0-103">Azure SQL 데이터베이스 동기화 구성원을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a04d0-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="a04d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a04d0-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a04d0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a04d0-105">DESCRIPTION</span></span>
<span data-ttu-id="a04d0-106">**AzSqlSyncMember** Cmdlet은 Azure SQL 데이터베이스 동기화 구성원을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a04d0-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="a04d0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a04d0-107">EXAMPLES</span></span>

### <span data-ttu-id="a04d0-108">예제 1: 동기화 구성원 제거</span><span class="sxs-lookup"><span data-stu-id="a04d0-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="a04d0-109">이 명령은 syncMember01 이라는 Azure SQL 데이터베이스 동기화 구성원을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a04d0-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="a04d0-110">변수</span><span class="sxs-lookup"><span data-stu-id="a04d0-110">PARAMETERS</span></span>

### <span data-ttu-id="a04d0-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a04d0-111">-DatabaseName</span></span>
<span data-ttu-id="a04d0-112">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a04d0-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a04d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a04d0-113">-DefaultProfile</span></span>
<span data-ttu-id="a04d0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a04d0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a04d0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a04d0-115">-Force</span></span>
<span data-ttu-id="a04d0-116">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="a04d0-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a04d0-117">-이름</span><span class="sxs-lookup"><span data-stu-id="a04d0-117">-Name</span></span>
<span data-ttu-id="a04d0-118">동기화 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a04d0-118">The sync member name.</span></span>

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

### <span data-ttu-id="a04d0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a04d0-119">-PassThru</span></span>
<span data-ttu-id="a04d0-120">제거 된 동기화 구성원을 반환할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="a04d0-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="a04d0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a04d0-121">-ResourceGroupName</span></span>
<span data-ttu-id="a04d0-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a04d0-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a04d0-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a04d0-123">-ServerName</span></span>
<span data-ttu-id="a04d0-124">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a04d0-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a04d0-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a04d0-125">-SyncGroupName</span></span>
<span data-ttu-id="a04d0-126">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a04d0-126">The sync group name.</span></span>

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

### <span data-ttu-id="a04d0-127">-확인</span><span class="sxs-lookup"><span data-stu-id="a04d0-127">-Confirm</span></span>
<span data-ttu-id="a04d0-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a04d0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a04d0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a04d0-129">-WhatIf</span></span>
<span data-ttu-id="a04d0-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a04d0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a04d0-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a04d0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a04d0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a04d0-132">CommonParameters</span></span>
<span data-ttu-id="a04d0-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a04d0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a04d0-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a04d0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a04d0-135">입력</span><span class="sxs-lookup"><span data-stu-id="a04d0-135">INPUTS</span></span>

### <span data-ttu-id="a04d0-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a04d0-136">System.String</span></span>

## <span data-ttu-id="a04d0-137">출력</span><span class="sxs-lookup"><span data-stu-id="a04d0-137">OUTPUTS</span></span>

### <span data-ttu-id="a04d0-138">AzureSqlSyncMemberModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="a04d0-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="a04d0-139">상속자</span><span class="sxs-lookup"><span data-stu-id="a04d0-139">NOTES</span></span>

## <span data-ttu-id="a04d0-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a04d0-140">RELATED LINKS</span></span>

[<span data-ttu-id="a04d0-141">새로운 AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a04d0-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="a04d0-142">업데이트-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a04d0-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="a04d0-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a04d0-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

