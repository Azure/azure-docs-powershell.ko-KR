---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: e35187bf22015f3398a9fd95ce60a1cd597f7c22
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878750"
---
# <span data-ttu-id="a6db9-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="a6db9-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="a6db9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6db9-102">SYNOPSIS</span></span>
<span data-ttu-id="a6db9-103">동기화 그룹 동기화를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6db9-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="a6db9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6db9-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6db9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a6db9-105">DESCRIPTION</span></span>
<span data-ttu-id="a6db9-106">**AzSqlSyncGroupSync** cmdlet은 동기화 그룹 동기화를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6db9-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="a6db9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a6db9-107">EXAMPLES</span></span>

### <span data-ttu-id="a6db9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a6db9-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="a6db9-109">이 명령은 동기화 그룹 mysg에 대 한 동기화를 둥글게 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6db9-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="a6db9-110">변수</span><span class="sxs-lookup"><span data-stu-id="a6db9-110">PARAMETERS</span></span>

### <span data-ttu-id="a6db9-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a6db9-111">-DatabaseName</span></span>
<span data-ttu-id="a6db9-112">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6db9-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a6db9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6db9-113">-DefaultProfile</span></span>
<span data-ttu-id="a6db9-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a6db9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6db9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6db9-115">-PassThru</span></span>
<span data-ttu-id="a6db9-116">동기화 그룹을 반환할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6db9-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="a6db9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6db9-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6db9-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6db9-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="a6db9-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a6db9-119">-ServerName</span></span>
<span data-ttu-id="a6db9-120">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6db9-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a6db9-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a6db9-121">-SyncGroupName</span></span>
<span data-ttu-id="a6db9-122">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6db9-122">The sync group name.</span></span>

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

### <span data-ttu-id="a6db9-123">-확인</span><span class="sxs-lookup"><span data-stu-id="a6db9-123">-Confirm</span></span>
<span data-ttu-id="a6db9-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6db9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6db9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6db9-125">-WhatIf</span></span>
<span data-ttu-id="a6db9-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a6db9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6db9-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6db9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6db9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6db9-128">CommonParameters</span></span>
<span data-ttu-id="a6db9-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6db9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6db9-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a6db9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6db9-131">입력</span><span class="sxs-lookup"><span data-stu-id="a6db9-131">INPUTS</span></span>

### <span data-ttu-id="a6db9-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a6db9-132">System.String</span></span>

## <span data-ttu-id="a6db9-133">출력</span><span class="sxs-lookup"><span data-stu-id="a6db9-133">OUTPUTS</span></span>

### <span data-ttu-id="a6db9-134">AzureSqlSyncGroupModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6db9-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="a6db9-135">상속자</span><span class="sxs-lookup"><span data-stu-id="a6db9-135">NOTES</span></span>

## <span data-ttu-id="a6db9-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6db9-136">RELATED LINKS</span></span>

[<span data-ttu-id="a6db9-137">중지-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="a6db9-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)

