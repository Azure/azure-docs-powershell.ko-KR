---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: 791658e9f4f10fdbb8b1000d6b1bc88d392aaf46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308204"
---
# <span data-ttu-id="a2c43-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="a2c43-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="a2c43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2c43-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c43-103">Azure SQL Server DNS 별칭이 가리키는 서버를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c43-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="a2c43-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2c43-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2c43-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a2c43-105">DESCRIPTION</span></span>
<span data-ttu-id="a2c43-106">이 명령은 별칭이 가리키는 서버를 업데이트 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c43-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="a2c43-107">이 명령은 별칭이 가리키는 새 서버가 있는 경우 구독에 로그인 하는 동안 발행 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c43-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="a2c43-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a2c43-108">EXAMPLES</span></span>

### <span data-ttu-id="a2c43-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="a2c43-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="a2c43-110">이 명령은 이전에 oldServer를 가리키고 있는 별칭을 업데이트 하 여 server newServer를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="a2c43-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="a2c43-111">변수</span><span class="sxs-lookup"><span data-stu-id="a2c43-111">PARAMETERS</span></span>

### <span data-ttu-id="a2c43-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2c43-112">-AsJob</span></span>
<span data-ttu-id="a2c43-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a2c43-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2c43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c43-114">-DefaultProfile</span></span>
<span data-ttu-id="a2c43-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c43-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2c43-116">-이름</span><span class="sxs-lookup"><span data-stu-id="a2c43-116">-Name</span></span>
<span data-ttu-id="a2c43-117">Azure Sql Server Dns 별칭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c43-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c43-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c43-118">-ResourceGroupName</span></span>
<span data-ttu-id="a2c43-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c43-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c43-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="a2c43-120">-SourceServerName</span></span>
<span data-ttu-id="a2c43-121">별칭이 현재 가리키고 있는 Azure Sql Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c43-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c43-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c43-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="a2c43-123">원본 서버의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c43-123">The name of resource group of the source server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c43-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2c43-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="a2c43-125">원본 서버의 구독 id</span><span class="sxs-lookup"><span data-stu-id="a2c43-125">The subscription id of the source server</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c43-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="a2c43-126">-TargetServerName</span></span>
<span data-ttu-id="a2c43-127">별칭이 가리켜야 하는 Azure Sql Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c43-127">The name of Azure Sql Server to which alias should point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c43-128">-확인</span><span class="sxs-lookup"><span data-stu-id="a2c43-128">-Confirm</span></span>
<span data-ttu-id="a2c43-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c43-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2c43-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2c43-130">-WhatIf</span></span>
<span data-ttu-id="a2c43-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2c43-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2c43-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2c43-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2c43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c43-133">CommonParameters</span></span>
<span data-ttu-id="a2c43-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c43-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a2c43-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c43-136">입력</span><span class="sxs-lookup"><span data-stu-id="a2c43-136">INPUTS</span></span>

### <span data-ttu-id="a2c43-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a2c43-137">System.String</span></span>

## <span data-ttu-id="a2c43-138">출력</span><span class="sxs-lookup"><span data-stu-id="a2c43-138">OUTPUTS</span></span>

### <span data-ttu-id="a2c43-139">Microsoft. ServerDnsAlias. AzureSqlServerDnsAliasModel.</span><span class="sxs-lookup"><span data-stu-id="a2c43-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="a2c43-140">상속자</span><span class="sxs-lookup"><span data-stu-id="a2c43-140">NOTES</span></span>

## <span data-ttu-id="a2c43-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2c43-141">RELATED LINKS</span></span>
