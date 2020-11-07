---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
ms.openlocfilehash: 710ae0ea93c7dc49597210d8890ebef04cc7c367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704097"
---
# <span data-ttu-id="2c082-101">Update-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="2c082-101">Update-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="2c082-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c082-102">SYNOPSIS</span></span>
<span data-ttu-id="2c082-103">동기화 구성원 데이터베이스 또는 동기화 허브 데이터베이스의 동기화 스키마를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="2c082-104">실제 데이터베이스에서 최신 데이터베이스 스키마를 가져온 다음이를 사용 하 여 동기화 메타 데이터 데이터베이스에서 캐시 된 스키마를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="2c082-105">"SyncMemberName"를 지정 하면 구성원 데이터베이스 스키마가 새로 고쳐집니다. 그렇지 않은 경우에는 hub 데이터베이스 스키마를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c082-106">구문과</span><span class="sxs-lookup"><span data-stu-id="2c082-106">SYNTAX</span></span>

```
Update-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c082-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2c082-107">DESCRIPTION</span></span>
<span data-ttu-id="2c082-108">**업데이트 AzureRmSqlSyncSchema** cmdlet은 동기화 구성원 데이터베이스 또는 동기화 허브 데이터베이스에 대 한 동기화 스키마를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-108">The **Update-AzureRmSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="2c082-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2c082-109">EXAMPLES</span></span>

### <span data-ttu-id="2c082-110">예제 1: hub 데이터베이스의 동기화 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="2c082-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="2c082-111">이 명령은 동기화 그룹 syncGroup01의 hub 데이터베이스에 대 한 동기화 스키마를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="2c082-112">예제 2: 구성원 데이터베이스에 대 한 동기화 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="2c082-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="2c082-113">이 명령은 동기화 구성원 syncMember01의 구성원 데이터베이스에 대 한 동기화 스키마를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="2c082-114">변수</span><span class="sxs-lookup"><span data-stu-id="2c082-114">PARAMETERS</span></span>

### <span data-ttu-id="2c082-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2c082-115">-DatabaseName</span></span>
<span data-ttu-id="2c082-116">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="2c082-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c082-117">-DefaultProfile</span></span>
<span data-ttu-id="2c082-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2c082-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c082-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c082-119">-PassThru</span></span>
<span data-ttu-id="2c082-120">이 cmdlet이 작동 하는 동기화 그룹을 반환할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="2c082-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c082-121">-ResourceGroupName</span></span>
<span data-ttu-id="2c082-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="2c082-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2c082-123">-ServerName</span></span>
<span data-ttu-id="2c082-124">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="2c082-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="2c082-125">-SyncGroupName</span></span>
<span data-ttu-id="2c082-126">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-126">The sync group name.</span></span>

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

### <span data-ttu-id="2c082-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="2c082-127">-SyncMemberName</span></span>
<span data-ttu-id="2c082-128">동기화 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-128">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c082-129">-확인</span><span class="sxs-lookup"><span data-stu-id="2c082-129">-Confirm</span></span>
<span data-ttu-id="2c082-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c082-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c082-131">-WhatIf</span></span>
<span data-ttu-id="2c082-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c082-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c082-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c082-134">CommonParameters</span></span>
<span data-ttu-id="2c082-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c082-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c082-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c082-137">입력</span><span class="sxs-lookup"><span data-stu-id="2c082-137">INPUTS</span></span>

### <span data-ttu-id="2c082-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c082-138">System.String</span></span>

## <span data-ttu-id="2c082-139">출력</span><span class="sxs-lookup"><span data-stu-id="2c082-139">OUTPUTS</span></span>

### <span data-ttu-id="2c082-140">AzureSqlSyncGroupModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c082-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="2c082-141">상속자</span><span class="sxs-lookup"><span data-stu-id="2c082-141">NOTES</span></span>

## <span data-ttu-id="2c082-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c082-142">RELATED LINKS</span></span>
