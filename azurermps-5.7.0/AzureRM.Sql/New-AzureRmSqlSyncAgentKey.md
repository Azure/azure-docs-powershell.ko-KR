---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
ms.openlocfilehash: c6a9c1df9fca93b932ebc65a11c6b126b133465b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531595"
---
# <span data-ttu-id="a2bc9-101">New-AzureRmSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="a2bc9-101">New-AzureRmSqlSyncAgentKey</span></span>

## <span data-ttu-id="a2bc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="a2bc9-103">Azure SQL 동기화 에이전트 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2bc9-103">Creates an Azure SQL Sync Agent Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2bc9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2bc9-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2bc9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a2bc9-105">DESCRIPTION</span></span>
<span data-ttu-id="a2bc9-106">**AzureRmSqlSyncAgentKey** Cmdlet은 Azure SQL 동기화 에이전트 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2bc9-106">The **New-AzureRmSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="a2bc9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a2bc9-107">EXAMPLES</span></span>

### <span data-ttu-id="a2bc9-108">예제 1: Azure SQL 동기화 에이전트에 대 한 동기화 에이전트 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2bc9-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="a2bc9-109">이 명령은 Azure SQL 동기화 에이전트에 대 한 동기화 에이전트 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2bc9-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="a2bc9-110">변수</span><span class="sxs-lookup"><span data-stu-id="a2bc9-110">PARAMETERS</span></span>

### <span data-ttu-id="a2bc9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2bc9-111">-DefaultProfile</span></span>
<span data-ttu-id="a2bc9-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a2bc9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2bc9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2bc9-113">-ResourceGroupName</span></span>
<span data-ttu-id="a2bc9-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2bc9-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="a2bc9-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a2bc9-115">-ServerName</span></span>
<span data-ttu-id="a2bc9-116">동기화 에이전트가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2bc9-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="a2bc9-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="a2bc9-117">-SyncAgentName</span></span>
<span data-ttu-id="a2bc9-118">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2bc9-118">The sync agent name.</span></span>

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

### <span data-ttu-id="a2bc9-119">-확인</span><span class="sxs-lookup"><span data-stu-id="a2bc9-119">-Confirm</span></span>
<span data-ttu-id="a2bc9-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2bc9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2bc9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2bc9-121">-WhatIf</span></span>
<span data-ttu-id="a2bc9-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2bc9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2bc9-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2bc9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2bc9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2bc9-124">CommonParameters</span></span>
<span data-ttu-id="a2bc9-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2bc9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2bc9-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2bc9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2bc9-127">입력</span><span class="sxs-lookup"><span data-stu-id="a2bc9-127">INPUTS</span></span>

### <span data-ttu-id="a2bc9-128">않아야</span><span class="sxs-lookup"><span data-stu-id="a2bc9-128">None</span></span>
<span data-ttu-id="a2bc9-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2bc9-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a2bc9-130">출력</span><span class="sxs-lookup"><span data-stu-id="a2bc9-130">OUTPUTS</span></span>

### <span data-ttu-id="a2bc9-131">AzureSqlSyncAgentKeyModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2bc9-131">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="a2bc9-132">상속자</span><span class="sxs-lookup"><span data-stu-id="a2bc9-132">NOTES</span></span>

## <span data-ttu-id="a2bc9-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2bc9-133">RELATED LINKS</span></span>
