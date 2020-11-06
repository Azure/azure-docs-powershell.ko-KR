---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 8665119abafe928f140f79b2cec8ee2e8fcfeff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528760"
---
# <span data-ttu-id="6f382-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6f382-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="6f382-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f382-102">SYNOPSIS</span></span>
<span data-ttu-id="6f382-103">Azure SQL 데이터베이스 동기화 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f382-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f382-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f382-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f382-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6f382-105">DESCRIPTION</span></span>
<span data-ttu-id="6f382-106">**AzureRmSqlSyncGroup** Cmdlet은 Azure SQL 데이터베이스 동기화 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f382-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="6f382-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6f382-107">EXAMPLES</span></span>

### <span data-ttu-id="6f382-108">예제 1: 동기화 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="6f382-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="6f382-109">이 명령은 syncGroup01 이라는 Azure SQL Database 동기화 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f382-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="6f382-110">변수</span><span class="sxs-lookup"><span data-stu-id="6f382-110">PARAMETERS</span></span>

### <span data-ttu-id="6f382-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6f382-111">-DatabaseName</span></span>
<span data-ttu-id="6f382-112">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f382-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="6f382-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f382-113">-DefaultProfile</span></span>
<span data-ttu-id="6f382-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6f382-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f382-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6f382-115">-Force</span></span>
<span data-ttu-id="6f382-116">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="6f382-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6f382-117">-이름</span><span class="sxs-lookup"><span data-stu-id="6f382-117">-Name</span></span>
<span data-ttu-id="6f382-118">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f382-118">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f382-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f382-119">-PassThru</span></span>
<span data-ttu-id="6f382-120">제거 된 동기화 그룹을 반환할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f382-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="6f382-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f382-121">-ResourceGroupName</span></span>
<span data-ttu-id="6f382-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f382-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="6f382-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6f382-123">-ServerName</span></span>
<span data-ttu-id="6f382-124">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f382-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="6f382-125">-확인</span><span class="sxs-lookup"><span data-stu-id="6f382-125">-Confirm</span></span>
<span data-ttu-id="6f382-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f382-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f382-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f382-127">-WhatIf</span></span>
<span data-ttu-id="6f382-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f382-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f382-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f382-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f382-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f382-130">CommonParameters</span></span>
<span data-ttu-id="6f382-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f382-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f382-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f382-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f382-133">입력</span><span class="sxs-lookup"><span data-stu-id="6f382-133">INPUTS</span></span>

### <span data-ttu-id="6f382-134">않아야</span><span class="sxs-lookup"><span data-stu-id="6f382-134">None</span></span>
<span data-ttu-id="6f382-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f382-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f382-136">출력</span><span class="sxs-lookup"><span data-stu-id="6f382-136">OUTPUTS</span></span>

### <span data-ttu-id="6f382-137">AzureSqlSyncGroupModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f382-137">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="6f382-138">상속자</span><span class="sxs-lookup"><span data-stu-id="6f382-138">NOTES</span></span>

## <span data-ttu-id="6f382-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f382-139">RELATED LINKS</span></span>

[<span data-ttu-id="6f382-140">새로운 AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6f382-140">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="6f382-141">업데이트-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6f382-141">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="6f382-142">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6f382-142">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

