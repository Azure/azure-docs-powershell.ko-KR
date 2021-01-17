---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367186"
---
# <span data-ttu-id="fc509-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="fc509-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="fc509-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc509-102">SYNOPSIS</span></span>
<span data-ttu-id="fc509-103">새 작업 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc509-103">Creates a new job credential</span></span>

## <span data-ttu-id="fc509-104">구문</span><span class="sxs-lookup"><span data-stu-id="fc509-104">SYNTAX</span></span>

### <span data-ttu-id="fc509-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fc509-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc509-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="fc509-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc509-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fc509-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc509-108">설명</span><span class="sxs-lookup"><span data-stu-id="fc509-108">DESCRIPTION</span></span>
<span data-ttu-id="fc509-109">New-AzSqlElasticJobCredential cmdlet에서 새 작업 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc509-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="fc509-110">예제</span><span class="sxs-lookup"><span data-stu-id="fc509-110">EXAMPLES</span></span>

### <span data-ttu-id="fc509-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fc509-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="fc509-112">새 작업 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc509-112">Creates a new job credential</span></span>

## <span data-ttu-id="fc509-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc509-113">PARAMETERS</span></span>

### <span data-ttu-id="fc509-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="fc509-114">-AgentName</span></span>
<span data-ttu-id="fc509-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="fc509-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc509-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="fc509-116">-Credential</span></span>
<span data-ttu-id="fc509-117">자격 증명</span><span class="sxs-lookup"><span data-stu-id="fc509-117">The credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc509-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc509-118">-DefaultProfile</span></span>
<span data-ttu-id="fc509-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc509-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc509-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fc509-120">-Name</span></span>
<span data-ttu-id="fc509-121">작업 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="fc509-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc509-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fc509-122">-ParentObject</span></span>
<span data-ttu-id="fc509-123">에이전트 개체</span><span class="sxs-lookup"><span data-stu-id="fc509-123">The agent object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc509-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fc509-124">-ParentResourceId</span></span>
<span data-ttu-id="fc509-125">에이전트 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="fc509-125">The agent resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc509-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc509-126">-ResourceGroupName</span></span>
<span data-ttu-id="fc509-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fc509-127">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc509-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fc509-128">-ServerName</span></span>
<span data-ttu-id="fc509-129">서버 이름</span><span class="sxs-lookup"><span data-stu-id="fc509-129">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc509-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc509-130">-Confirm</span></span>
<span data-ttu-id="fc509-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc509-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc509-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc509-132">-WhatIf</span></span>
<span data-ttu-id="fc509-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fc509-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc509-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc509-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc509-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc509-135">CommonParameters</span></span>
<span data-ttu-id="fc509-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fc509-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc509-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fc509-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc509-138">입력</span><span class="sxs-lookup"><span data-stu-id="fc509-138">INPUTS</span></span>

### <span data-ttu-id="fc509-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="fc509-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="fc509-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="fc509-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="fc509-141">출력</span><span class="sxs-lookup"><span data-stu-id="fc509-141">OUTPUTS</span></span>

### <span data-ttu-id="fc509-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="fc509-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="fc509-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fc509-143">NOTES</span></span>

## <span data-ttu-id="fc509-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc509-144">RELATED LINKS</span></span>
