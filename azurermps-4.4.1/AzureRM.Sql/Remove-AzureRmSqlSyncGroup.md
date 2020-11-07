---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 99892ee748de030a045bd9d0a022051206236198
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711759"
---
# <span data-ttu-id="0aa6c-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0aa6c-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="0aa6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0aa6c-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa6c-103">Azure SQL 데이터베이스 동기화 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa6c-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aa6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0aa6c-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aa6c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0aa6c-105">DESCRIPTION</span></span>
<span data-ttu-id="0aa6c-106">**AzureRmSqlSyncGroup** Cmdlet은 Azure SQL 데이터베이스 동기화 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa6c-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="0aa6c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0aa6c-107">EXAMPLES</span></span>

### <span data-ttu-id="0aa6c-108">예제 1: 동기화 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="0aa6c-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="0aa6c-109">이 명령은 syncGroup01 이라는 Azure SQL Database 동기화 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa6c-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="0aa6c-110">변수</span><span class="sxs-lookup"><span data-stu-id="0aa6c-110">PARAMETERS</span></span>

### <span data-ttu-id="0aa6c-111">-확인</span><span class="sxs-lookup"><span data-stu-id="0aa6c-111">-Confirm</span></span>
<span data-ttu-id="0aa6c-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa6c-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aa6c-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0aa6c-113">-DatabaseName</span></span>
<span data-ttu-id="0aa6c-114">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0aa6c-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="0aa6c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0aa6c-115">-Force</span></span>
<span data-ttu-id="0aa6c-116">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="0aa6c-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0aa6c-117">-이름</span><span class="sxs-lookup"><span data-stu-id="0aa6c-117">-Name</span></span>
<span data-ttu-id="0aa6c-118">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0aa6c-118">The sync group name.</span></span>

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

### <span data-ttu-id="0aa6c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0aa6c-119">-PassThru</span></span>
<span data-ttu-id="0aa6c-120">제거 된 동기화 그룹을 반환할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa6c-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="0aa6c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aa6c-121">-ResourceGroupName</span></span>
<span data-ttu-id="0aa6c-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0aa6c-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="0aa6c-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0aa6c-123">-ServerName</span></span>
<span data-ttu-id="0aa6c-124">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0aa6c-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="0aa6c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aa6c-125">-WhatIf</span></span>
<span data-ttu-id="0aa6c-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0aa6c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aa6c-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0aa6c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aa6c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa6c-128">-DefaultProfile</span></span>
<span data-ttu-id="0aa6c-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0aa6c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aa6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa6c-130">CommonParameters</span></span>
<span data-ttu-id="0aa6c-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa6c-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aa6c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa6c-133">입력</span><span class="sxs-lookup"><span data-stu-id="0aa6c-133">INPUTS</span></span>

## <span data-ttu-id="0aa6c-134">출력</span><span class="sxs-lookup"><span data-stu-id="0aa6c-134">OUTPUTS</span></span>

### <span data-ttu-id="0aa6c-135">AzureSqlSyncGroupModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa6c-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="0aa6c-136">상속자</span><span class="sxs-lookup"><span data-stu-id="0aa6c-136">NOTES</span></span>

## <span data-ttu-id="0aa6c-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0aa6c-137">RELATED LINKS</span></span>

[<span data-ttu-id="0aa6c-138">새로운 AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0aa6c-138">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="0aa6c-139">업데이트-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0aa6c-139">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="0aa6c-140">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0aa6c-140">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

