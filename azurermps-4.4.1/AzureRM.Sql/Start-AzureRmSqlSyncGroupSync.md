---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: e81667523327c9a83497ce4f586f166fe69d0dc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535399"
---
# <span data-ttu-id="59324-101">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="59324-101">Start-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="59324-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59324-102">SYNOPSIS</span></span>
<span data-ttu-id="59324-103">동기화 그룹 동기화를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="59324-103">Starts a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59324-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59324-104">SYNTAX</span></span>

```
Start-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59324-105">설명은</span><span class="sxs-lookup"><span data-stu-id="59324-105">DESCRIPTION</span></span>
<span data-ttu-id="59324-106">**AzureRmSqlSyncGroupSync** cmdlet은 동기화 그룹 동기화를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="59324-106">The **Start-AzureRmSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="59324-107">예제의</span><span class="sxs-lookup"><span data-stu-id="59324-107">EXAMPLES</span></span>

### <span data-ttu-id="59324-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="59324-108">Example 1</span></span>
```
PS C:\> Start-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="59324-109">이 명령은 동기화 그룹 mysg에 대 한 동기화를 둥글게 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="59324-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="59324-110">변수</span><span class="sxs-lookup"><span data-stu-id="59324-110">PARAMETERS</span></span>

### <span data-ttu-id="59324-111">-확인</span><span class="sxs-lookup"><span data-stu-id="59324-111">-Confirm</span></span>
<span data-ttu-id="59324-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="59324-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59324-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59324-113">-DatabaseName</span></span>
<span data-ttu-id="59324-114">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59324-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="59324-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59324-115">-PassThru</span></span>
<span data-ttu-id="59324-116">동기화 그룹을 반환할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="59324-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="59324-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59324-117">-ResourceGroupName</span></span>
<span data-ttu-id="59324-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59324-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="59324-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="59324-119">-ServerName</span></span>
<span data-ttu-id="59324-120">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59324-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="59324-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="59324-121">-SyncGroupName</span></span>
<span data-ttu-id="59324-122">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59324-122">The sync group name.</span></span>

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

### <span data-ttu-id="59324-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59324-123">-WhatIf</span></span>
<span data-ttu-id="59324-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="59324-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59324-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59324-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59324-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59324-126">-DefaultProfile</span></span>
<span data-ttu-id="59324-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59324-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59324-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59324-128">CommonParameters</span></span>
<span data-ttu-id="59324-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59324-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59324-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59324-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59324-131">입력</span><span class="sxs-lookup"><span data-stu-id="59324-131">INPUTS</span></span>

## <span data-ttu-id="59324-132">출력</span><span class="sxs-lookup"><span data-stu-id="59324-132">OUTPUTS</span></span>

### <span data-ttu-id="59324-133">AzureSqlSyncGroupModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="59324-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="59324-134">상속자</span><span class="sxs-lookup"><span data-stu-id="59324-134">NOTES</span></span>

## <span data-ttu-id="59324-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59324-135">RELATED LINKS</span></span>

[<span data-ttu-id="59324-136">중지-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="59324-136">Stop-AzureRmSqlSyncGroupSync</span></span>](./Stop-AzureRmSqlSyncGroupSync.md)

