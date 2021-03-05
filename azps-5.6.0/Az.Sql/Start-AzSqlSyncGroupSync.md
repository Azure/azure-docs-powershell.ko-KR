---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: 13f58f454fb84a4bcd003afd84761197d41c16ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008491"
---
# <span data-ttu-id="aa2a2-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="aa2a2-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="aa2a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="aa2a2-103">동기화 그룹 동기화를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="aa2a2-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="aa2a2-104">구문</span><span class="sxs-lookup"><span data-stu-id="aa2a2-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa2a2-105">설명</span><span class="sxs-lookup"><span data-stu-id="aa2a2-105">DESCRIPTION</span></span>
<span data-ttu-id="aa2a2-106">**Start-AzSqlSyncGroupSync** cmdlet은 동기화 그룹 동기화를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="aa2a2-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="aa2a2-107">예제</span><span class="sxs-lookup"><span data-stu-id="aa2a2-107">EXAMPLES</span></span>

### <span data-ttu-id="aa2a2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="aa2a2-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="aa2a2-109">이 명령은 동기화 그룹 mysg에 대한 동기화 라운드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="aa2a2-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="aa2a2-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aa2a2-110">PARAMETERS</span></span>

### <span data-ttu-id="aa2a2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aa2a2-111">-DatabaseName</span></span>
<span data-ttu-id="aa2a2-112">Azure 데이터베이스의 SQL 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="aa2a2-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="aa2a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa2a2-113">-DefaultProfile</span></span>
<span data-ttu-id="aa2a2-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="aa2a2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa2a2-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa2a2-115">-PassThru</span></span>
<span data-ttu-id="aa2a2-116">동기화 그룹을 반환할지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="aa2a2-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="aa2a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa2a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="aa2a2-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa2a2-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="aa2a2-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aa2a2-119">-ServerName</span></span>
<span data-ttu-id="aa2a2-120">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="aa2a2-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="aa2a2-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="aa2a2-121">-SyncGroupName</span></span>
<span data-ttu-id="aa2a2-122">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa2a2-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa2a2-123">-확인</span><span class="sxs-lookup"><span data-stu-id="aa2a2-123">-Confirm</span></span>
<span data-ttu-id="aa2a2-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa2a2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa2a2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa2a2-125">-WhatIf</span></span>
<span data-ttu-id="aa2a2-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="aa2a2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa2a2-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa2a2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa2a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa2a2-128">CommonParameters</span></span>
<span data-ttu-id="aa2a2-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa2a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa2a2-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa2a2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa2a2-131">입력</span><span class="sxs-lookup"><span data-stu-id="aa2a2-131">INPUTS</span></span>

### <span data-ttu-id="aa2a2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="aa2a2-132">System.String</span></span>

## <span data-ttu-id="aa2a2-133">출력</span><span class="sxs-lookup"><span data-stu-id="aa2a2-133">OUTPUTS</span></span>

### <span data-ttu-id="aa2a2-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="aa2a2-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="aa2a2-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa2a2-135">NOTES</span></span>

## <span data-ttu-id="aa2a2-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa2a2-136">RELATED LINKS</span></span>

[<span data-ttu-id="aa2a2-137">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="aa2a2-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)

