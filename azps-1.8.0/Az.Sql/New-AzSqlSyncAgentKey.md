---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: 4b04fe3a27178ce5228f8e3fe2a397728a432b6b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698872"
---
# <span data-ttu-id="99fb5-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="99fb5-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="99fb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="99fb5-103">Azure SQL 동기화 에이전트 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99fb5-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="99fb5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99fb5-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99fb5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="99fb5-105">DESCRIPTION</span></span>
<span data-ttu-id="99fb5-106">**AzSqlSyncAgentKey** Cmdlet은 Azure SQL 동기화 에이전트 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99fb5-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="99fb5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="99fb5-107">EXAMPLES</span></span>

### <span data-ttu-id="99fb5-108">예제 1: Azure SQL 동기화 에이전트에 대 한 동기화 에이전트 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99fb5-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="99fb5-109">이 명령은 Azure SQL 동기화 에이전트에 대 한 동기화 에이전트 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99fb5-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="99fb5-110">변수</span><span class="sxs-lookup"><span data-stu-id="99fb5-110">PARAMETERS</span></span>

### <span data-ttu-id="99fb5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99fb5-111">-DefaultProfile</span></span>
<span data-ttu-id="99fb5-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="99fb5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99fb5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99fb5-113">-ResourceGroupName</span></span>
<span data-ttu-id="99fb5-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99fb5-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="99fb5-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="99fb5-115">-ServerName</span></span>
<span data-ttu-id="99fb5-116">동기화 에이전트가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99fb5-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="99fb5-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="99fb5-117">-SyncAgentName</span></span>
<span data-ttu-id="99fb5-118">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99fb5-118">The sync agent name.</span></span>

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

### <span data-ttu-id="99fb5-119">-확인</span><span class="sxs-lookup"><span data-stu-id="99fb5-119">-Confirm</span></span>
<span data-ttu-id="99fb5-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99fb5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99fb5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99fb5-121">-WhatIf</span></span>
<span data-ttu-id="99fb5-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="99fb5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99fb5-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99fb5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99fb5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99fb5-124">CommonParameters</span></span>
<span data-ttu-id="99fb5-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99fb5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99fb5-126">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="99fb5-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99fb5-127">입력</span><span class="sxs-lookup"><span data-stu-id="99fb5-127">INPUTS</span></span>

### <span data-ttu-id="99fb5-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="99fb5-128">System.String</span></span>

## <span data-ttu-id="99fb5-129">출력</span><span class="sxs-lookup"><span data-stu-id="99fb5-129">OUTPUTS</span></span>

### <span data-ttu-id="99fb5-130">AzureSqlSyncAgentKeyModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="99fb5-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="99fb5-131">상속자</span><span class="sxs-lookup"><span data-stu-id="99fb5-131">NOTES</span></span>

## <span data-ttu-id="99fb5-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99fb5-132">RELATED LINKS</span></span>
