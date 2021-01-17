---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: e35187bf22015f3398a9fd95ce60a1cd597f7c22
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492304"
---
# <span data-ttu-id="022df-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="022df-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="022df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="022df-102">SYNOPSIS</span></span>
<span data-ttu-id="022df-103">동기화 그룹 동기화를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="022df-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="022df-104">구문</span><span class="sxs-lookup"><span data-stu-id="022df-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="022df-105">설명</span><span class="sxs-lookup"><span data-stu-id="022df-105">DESCRIPTION</span></span>
<span data-ttu-id="022df-106">**Start-AzSqlSyncGroupSync** cmdlet은 동기화 그룹 동기화를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="022df-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="022df-107">예제</span><span class="sxs-lookup"><span data-stu-id="022df-107">EXAMPLES</span></span>

### <span data-ttu-id="022df-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="022df-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="022df-109">이 명령은 동기화 그룹 mysg에 대한 동기화 라운드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="022df-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="022df-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="022df-110">PARAMETERS</span></span>

### <span data-ttu-id="022df-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="022df-111">-DatabaseName</span></span>
<span data-ttu-id="022df-112">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="022df-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="022df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="022df-113">-DefaultProfile</span></span>
<span data-ttu-id="022df-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="022df-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="022df-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="022df-115">-PassThru</span></span>
<span data-ttu-id="022df-116">동기화 그룹을 반환할지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="022df-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="022df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="022df-117">-ResourceGroupName</span></span>
<span data-ttu-id="022df-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="022df-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="022df-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="022df-119">-ServerName</span></span>
<span data-ttu-id="022df-120">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="022df-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="022df-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="022df-121">-SyncGroupName</span></span>
<span data-ttu-id="022df-122">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="022df-122">The sync group name.</span></span>

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

### <span data-ttu-id="022df-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="022df-123">-Confirm</span></span>
<span data-ttu-id="022df-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="022df-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="022df-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="022df-125">-WhatIf</span></span>
<span data-ttu-id="022df-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="022df-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="022df-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="022df-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="022df-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="022df-128">CommonParameters</span></span>
<span data-ttu-id="022df-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="022df-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="022df-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="022df-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="022df-131">입력</span><span class="sxs-lookup"><span data-stu-id="022df-131">INPUTS</span></span>

### <span data-ttu-id="022df-132">System.String</span><span class="sxs-lookup"><span data-stu-id="022df-132">System.String</span></span>

## <span data-ttu-id="022df-133">출력</span><span class="sxs-lookup"><span data-stu-id="022df-133">OUTPUTS</span></span>

### <span data-ttu-id="022df-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="022df-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="022df-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="022df-135">NOTES</span></span>

## <span data-ttu-id="022df-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="022df-136">RELATED LINKS</span></span>

[<span data-ttu-id="022df-137">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="022df-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)

