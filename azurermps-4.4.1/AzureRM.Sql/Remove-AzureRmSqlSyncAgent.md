---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 481f99baa432c00fc6a619754cee2df83015c047
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702268"
---
# <span data-ttu-id="a8560-101">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a8560-101">Remove-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="a8560-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8560-102">SYNOPSIS</span></span>
<span data-ttu-id="a8560-103">Azure SQL 동기화 에이전트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8560-103">Removes an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8560-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8560-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8560-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a8560-105">DESCRIPTION</span></span>
<span data-ttu-id="a8560-106">**AzureRmSqlSyncAgent** Cmdlet은 Azure SQL 동기화 에이전트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8560-106">The **Remove-AzureRmSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="a8560-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a8560-107">EXAMPLES</span></span>

### <span data-ttu-id="a8560-108">예제 1: 동기화 에이전트 제거</span><span class="sxs-lookup"><span data-stu-id="a8560-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="a8560-109">이 명령은 syncAgent01 이라는 Azure SQL 동기화 에이전트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8560-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="a8560-110">변수</span><span class="sxs-lookup"><span data-stu-id="a8560-110">PARAMETERS</span></span>

### <span data-ttu-id="a8560-111">-확인</span><span class="sxs-lookup"><span data-stu-id="a8560-111">-Confirm</span></span>
<span data-ttu-id="a8560-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8560-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8560-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a8560-113">-Force</span></span>
<span data-ttu-id="a8560-114">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="a8560-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a8560-115">-이름</span><span class="sxs-lookup"><span data-stu-id="a8560-115">-Name</span></span>
<span data-ttu-id="a8560-116">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8560-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8560-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8560-117">-PassThru</span></span>
<span data-ttu-id="a8560-118">제거 된 동기화 에이전트를 반환할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8560-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="a8560-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8560-119">-ResourceGroupName</span></span>
<span data-ttu-id="a8560-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8560-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a8560-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a8560-121">-ServerName</span></span>
<span data-ttu-id="a8560-122">동기화 에이전트가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8560-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="a8560-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8560-123">-WhatIf</span></span>
<span data-ttu-id="a8560-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a8560-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8560-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8560-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8560-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8560-126">-DefaultProfile</span></span>
<span data-ttu-id="a8560-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8560-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8560-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8560-128">CommonParameters</span></span>
<span data-ttu-id="a8560-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8560-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8560-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8560-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8560-131">입력</span><span class="sxs-lookup"><span data-stu-id="a8560-131">INPUTS</span></span>

## <span data-ttu-id="a8560-132">출력</span><span class="sxs-lookup"><span data-stu-id="a8560-132">OUTPUTS</span></span>

### <span data-ttu-id="a8560-133">AzureSqlSyncAgentModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8560-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="a8560-134">상속자</span><span class="sxs-lookup"><span data-stu-id="a8560-134">NOTES</span></span>

## <span data-ttu-id="a8560-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8560-135">RELATED LINKS</span></span>

[<span data-ttu-id="a8560-136">새로운 AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a8560-136">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="a8560-137">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a8560-137">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

