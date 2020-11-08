---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048633"
---
# <span data-ttu-id="25ed5-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="25ed5-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="25ed5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="25ed5-103">Azure SQL 데이터베이스 동기화 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ed5-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="25ed5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="25ed5-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25ed5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="25ed5-105">DESCRIPTION</span></span>
<span data-ttu-id="25ed5-106">**AzSqlSyncGroup** Cmdlet은 Azure SQL 데이터베이스 동기화 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ed5-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="25ed5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="25ed5-107">EXAMPLES</span></span>

### <span data-ttu-id="25ed5-108">예제 1: 동기화 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="25ed5-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="25ed5-109">이 명령은 syncGroup01 이라는 Azure SQL Database 동기화 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ed5-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="25ed5-110">변수</span><span class="sxs-lookup"><span data-stu-id="25ed5-110">PARAMETERS</span></span>

### <span data-ttu-id="25ed5-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="25ed5-111">-DatabaseName</span></span>
<span data-ttu-id="25ed5-112">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25ed5-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="25ed5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25ed5-113">-DefaultProfile</span></span>
<span data-ttu-id="25ed5-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="25ed5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25ed5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="25ed5-115">-Force</span></span>
<span data-ttu-id="25ed5-116">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="25ed5-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="25ed5-117">-이름</span><span class="sxs-lookup"><span data-stu-id="25ed5-117">-Name</span></span>
<span data-ttu-id="25ed5-118">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25ed5-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ed5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25ed5-119">-PassThru</span></span>
<span data-ttu-id="25ed5-120">제거 된 동기화 그룹을 반환할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ed5-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="25ed5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25ed5-121">-ResourceGroupName</span></span>
<span data-ttu-id="25ed5-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25ed5-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="25ed5-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="25ed5-123">-ServerName</span></span>
<span data-ttu-id="25ed5-124">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25ed5-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="25ed5-125">-확인</span><span class="sxs-lookup"><span data-stu-id="25ed5-125">-Confirm</span></span>
<span data-ttu-id="25ed5-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ed5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25ed5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25ed5-127">-WhatIf</span></span>
<span data-ttu-id="25ed5-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="25ed5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25ed5-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25ed5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25ed5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ed5-130">CommonParameters</span></span>
<span data-ttu-id="25ed5-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ed5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25ed5-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="25ed5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ed5-133">입력</span><span class="sxs-lookup"><span data-stu-id="25ed5-133">INPUTS</span></span>

### <span data-ttu-id="25ed5-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="25ed5-134">System.String</span></span>

## <span data-ttu-id="25ed5-135">출력</span><span class="sxs-lookup"><span data-stu-id="25ed5-135">OUTPUTS</span></span>

### <span data-ttu-id="25ed5-136">AzureSqlSyncGroupModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ed5-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="25ed5-137">상속자</span><span class="sxs-lookup"><span data-stu-id="25ed5-137">NOTES</span></span>

## <span data-ttu-id="25ed5-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25ed5-138">RELATED LINKS</span></span>

[<span data-ttu-id="25ed5-139">새로운 AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="25ed5-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="25ed5-140">업데이트-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="25ed5-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="25ed5-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="25ed5-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

