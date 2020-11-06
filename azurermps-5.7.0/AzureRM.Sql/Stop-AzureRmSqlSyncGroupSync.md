---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 24e61d466ac691f0f6faaa0b87bf819671517809
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529688"
---
# <span data-ttu-id="3bf61-101">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="3bf61-101">Stop-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="3bf61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bf61-102">SYNOPSIS</span></span>
<span data-ttu-id="3bf61-103">동기화 그룹 동기화를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bf61-103">Stops a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bf61-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3bf61-104">SYNTAX</span></span>

```
Stop-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bf61-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3bf61-105">DESCRIPTION</span></span>
<span data-ttu-id="3bf61-106">**AzureRmSqlSyncGroupSync** cmdlet은 동기화 그룹 동기화를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bf61-106">The **Stop-AzureRmSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="3bf61-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3bf61-107">EXAMPLES</span></span>

### <span data-ttu-id="3bf61-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3bf61-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="3bf61-109">이 명령은 동기화 그룹 mysg에 대해 진행 중인 동기화를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bf61-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="3bf61-110">변수</span><span class="sxs-lookup"><span data-stu-id="3bf61-110">PARAMETERS</span></span>

### <span data-ttu-id="3bf61-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3bf61-111">-DatabaseName</span></span>
<span data-ttu-id="3bf61-112">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3bf61-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bf61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bf61-113">-DefaultProfile</span></span>
<span data-ttu-id="3bf61-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3bf61-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf61-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bf61-115">-PassThru</span></span>
<span data-ttu-id="3bf61-116">동기화 그룹을 반환할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bf61-116">Defines Whether return the sync group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf61-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bf61-117">-ResourceGroupName</span></span>
<span data-ttu-id="3bf61-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3bf61-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bf61-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3bf61-119">-ServerName</span></span>
<span data-ttu-id="3bf61-120">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3bf61-120">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bf61-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="3bf61-121">-SyncGroupName</span></span>
<span data-ttu-id="3bf61-122">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3bf61-122">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bf61-123">-확인</span><span class="sxs-lookup"><span data-stu-id="3bf61-123">-Confirm</span></span>
<span data-ttu-id="3bf61-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bf61-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf61-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bf61-125">-WhatIf</span></span>
<span data-ttu-id="3bf61-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3bf61-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bf61-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3bf61-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf61-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bf61-128">CommonParameters</span></span>
<span data-ttu-id="3bf61-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bf61-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bf61-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bf61-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bf61-131">입력</span><span class="sxs-lookup"><span data-stu-id="3bf61-131">INPUTS</span></span>

### <span data-ttu-id="3bf61-132">않아야</span><span class="sxs-lookup"><span data-stu-id="3bf61-132">None</span></span>
<span data-ttu-id="3bf61-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3bf61-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3bf61-134">출력</span><span class="sxs-lookup"><span data-stu-id="3bf61-134">OUTPUTS</span></span>

### <span data-ttu-id="3bf61-135">AzureSqlSyncGroupModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bf61-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="3bf61-136">상속자</span><span class="sxs-lookup"><span data-stu-id="3bf61-136">NOTES</span></span>

## <span data-ttu-id="3bf61-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3bf61-137">RELATED LINKS</span></span>

[<span data-ttu-id="3bf61-138">시작-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="3bf61-138">Start-AzureRmSqlSyncGroupSync</span></span>](./Start-AzureRmSqlSyncGroupSync.md)

