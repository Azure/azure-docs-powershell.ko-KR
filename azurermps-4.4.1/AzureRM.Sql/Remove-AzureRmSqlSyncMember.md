---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
ms.openlocfilehash: d57e73c71e95fe673f9b54d9129714ca22670d31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537808"
---
# <span data-ttu-id="81c1d-101">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="81c1d-101">Remove-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="81c1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="81c1d-103">Azure SQL 데이터베이스 동기화 구성원을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-103">Removes an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81c1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81c1d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81c1d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="81c1d-105">DESCRIPTION</span></span>
<span data-ttu-id="81c1d-106">**AzureRmSqlSyncMember** Cmdlet은 Azure SQL 데이터베이스 동기화 구성원을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-106">The **Remove-AzureRmSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="81c1d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="81c1d-107">EXAMPLES</span></span>

### <span data-ttu-id="81c1d-108">예제 1: 동기화 구성원 제거</span><span class="sxs-lookup"><span data-stu-id="81c1d-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="81c1d-109">이 명령은 syncMember01 이라는 Azure SQL 데이터베이스 동기화 구성원을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="81c1d-110">변수</span><span class="sxs-lookup"><span data-stu-id="81c1d-110">PARAMETERS</span></span>

### <span data-ttu-id="81c1d-111">-확인</span><span class="sxs-lookup"><span data-stu-id="81c1d-111">-Confirm</span></span>
<span data-ttu-id="81c1d-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81c1d-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="81c1d-113">-DatabaseName</span></span>
<span data-ttu-id="81c1d-114">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="81c1d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="81c1d-115">-Force</span></span>
<span data-ttu-id="81c1d-116">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="81c1d-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="81c1d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="81c1d-117">-Name</span></span>
<span data-ttu-id="81c1d-118">동기화 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-118">The sync member name.</span></span>

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

### <span data-ttu-id="81c1d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81c1d-119">-PassThru</span></span>
<span data-ttu-id="81c1d-120">제거 된 동기화 구성원을 반환할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="81c1d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81c1d-121">-ResourceGroupName</span></span>
<span data-ttu-id="81c1d-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="81c1d-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="81c1d-123">-ServerName</span></span>
<span data-ttu-id="81c1d-124">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="81c1d-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="81c1d-125">-SyncGroupName</span></span>
<span data-ttu-id="81c1d-126">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-126">The sync group name.</span></span>

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

### <span data-ttu-id="81c1d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81c1d-127">-WhatIf</span></span>
<span data-ttu-id="81c1d-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81c1d-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81c1d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c1d-130">-DefaultProfile</span></span>
<span data-ttu-id="81c1d-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81c1d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c1d-132">CommonParameters</span></span>
<span data-ttu-id="81c1d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c1d-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81c1d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c1d-135">입력</span><span class="sxs-lookup"><span data-stu-id="81c1d-135">INPUTS</span></span>

## <span data-ttu-id="81c1d-136">출력</span><span class="sxs-lookup"><span data-stu-id="81c1d-136">OUTPUTS</span></span>

### <span data-ttu-id="81c1d-137">AzureSqlSyncMemberModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c1d-137">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="81c1d-138">상속자</span><span class="sxs-lookup"><span data-stu-id="81c1d-138">NOTES</span></span>

## <span data-ttu-id="81c1d-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81c1d-139">RELATED LINKS</span></span>

[<span data-ttu-id="81c1d-140">새로운 AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="81c1d-140">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="81c1d-141">업데이트-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="81c1d-141">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="81c1d-142">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="81c1d-142">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

