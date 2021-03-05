---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 8f82162b0f1e5b1f43852880c77d1be1427e3ca1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970256"
---
# <span data-ttu-id="7c894-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="7c894-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="7c894-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c894-102">SYNOPSIS</span></span>
<span data-ttu-id="7c894-103">새 작업 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c894-103">Creates a new job credential</span></span>

## <span data-ttu-id="7c894-104">구문</span><span class="sxs-lookup"><span data-stu-id="7c894-104">SYNTAX</span></span>

### <span data-ttu-id="7c894-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7c894-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c894-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7c894-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c894-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7c894-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c894-108">설명</span><span class="sxs-lookup"><span data-stu-id="7c894-108">DESCRIPTION</span></span>
<span data-ttu-id="7c894-109">New-AzSqlElasticJobCredential cmdlet에서 새 작업 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c894-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="7c894-110">예제</span><span class="sxs-lookup"><span data-stu-id="7c894-110">EXAMPLES</span></span>

### <span data-ttu-id="7c894-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c894-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="7c894-112">새 작업 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c894-112">Creates a new job credential</span></span>

## <span data-ttu-id="7c894-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7c894-113">PARAMETERS</span></span>

### <span data-ttu-id="7c894-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7c894-114">-AgentName</span></span>
<span data-ttu-id="7c894-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="7c894-115">The agent name</span></span>

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

### <span data-ttu-id="7c894-116">-자격 증명</span><span class="sxs-lookup"><span data-stu-id="7c894-116">-Credential</span></span>
<span data-ttu-id="7c894-117">자격 증명</span><span class="sxs-lookup"><span data-stu-id="7c894-117">The credential</span></span>

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

### <span data-ttu-id="7c894-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c894-118">-DefaultProfile</span></span>
<span data-ttu-id="7c894-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c894-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c894-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7c894-120">-Name</span></span>
<span data-ttu-id="7c894-121">작업 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="7c894-121">The job credential name</span></span>

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

### <span data-ttu-id="7c894-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7c894-122">-ParentObject</span></span>
<span data-ttu-id="7c894-123">에이전트 개체</span><span class="sxs-lookup"><span data-stu-id="7c894-123">The agent object</span></span>

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

### <span data-ttu-id="7c894-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7c894-124">-ParentResourceId</span></span>
<span data-ttu-id="7c894-125">에이전트 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="7c894-125">The agent resource id</span></span>

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

### <span data-ttu-id="7c894-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c894-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c894-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7c894-127">The resource group name</span></span>

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

### <span data-ttu-id="7c894-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7c894-128">-ServerName</span></span>
<span data-ttu-id="7c894-129">서버 이름</span><span class="sxs-lookup"><span data-stu-id="7c894-129">The server name</span></span>

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

### <span data-ttu-id="7c894-130">-확인</span><span class="sxs-lookup"><span data-stu-id="7c894-130">-Confirm</span></span>
<span data-ttu-id="7c894-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c894-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c894-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c894-132">-WhatIf</span></span>
<span data-ttu-id="7c894-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c894-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c894-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c894-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c894-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c894-135">CommonParameters</span></span>
<span data-ttu-id="7c894-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7c894-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c894-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c894-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c894-138">입력</span><span class="sxs-lookup"><span data-stu-id="7c894-138">INPUTS</span></span>

### <span data-ttu-id="7c894-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="7c894-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="7c894-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="7c894-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="7c894-141">출력</span><span class="sxs-lookup"><span data-stu-id="7c894-141">OUTPUTS</span></span>

### <span data-ttu-id="7c894-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="7c894-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="7c894-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7c894-143">NOTES</span></span>

## <span data-ttu-id="7c894-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c894-144">RELATED LINKS</span></span>
