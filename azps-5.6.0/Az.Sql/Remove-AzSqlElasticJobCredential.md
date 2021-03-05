---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: d5ee112af595ba88672a26d0f8f64590ea670706
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961339"
---
# <span data-ttu-id="60b14-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="60b14-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="60b14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60b14-102">SYNOPSIS</span></span>
<span data-ttu-id="60b14-103">탄력적 작업 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="60b14-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="60b14-104">구문</span><span class="sxs-lookup"><span data-stu-id="60b14-104">SYNTAX</span></span>

### <span data-ttu-id="60b14-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="60b14-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60b14-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="60b14-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60b14-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="60b14-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60b14-108">설명</span><span class="sxs-lookup"><span data-stu-id="60b14-108">DESCRIPTION</span></span>
<span data-ttu-id="60b14-109">Remove-AzSqlElasticJobCredential cmdlet에서 작업 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="60b14-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="60b14-110">예제</span><span class="sxs-lookup"><span data-stu-id="60b14-110">EXAMPLES</span></span>

### <span data-ttu-id="60b14-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="60b14-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="60b14-112">작업 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="60b14-112">Removes a job credential</span></span>

## <span data-ttu-id="60b14-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="60b14-113">PARAMETERS</span></span>

### <span data-ttu-id="60b14-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="60b14-114">-AgentName</span></span>
<span data-ttu-id="60b14-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="60b14-115">The agent name</span></span>

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

### <span data-ttu-id="60b14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b14-116">-DefaultProfile</span></span>
<span data-ttu-id="60b14-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60b14-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60b14-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60b14-118">-InputObject</span></span>
<span data-ttu-id="60b14-119">작업 자격 증명 개체</span><span class="sxs-lookup"><span data-stu-id="60b14-119">The job credential object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60b14-120">-Name</span><span class="sxs-lookup"><span data-stu-id="60b14-120">-Name</span></span>
<span data-ttu-id="60b14-121">작업 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="60b14-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60b14-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60b14-122">-ResourceGroupName</span></span>
<span data-ttu-id="60b14-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="60b14-123">The resource group name</span></span>

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

### <span data-ttu-id="60b14-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60b14-124">-ResourceId</span></span>
<span data-ttu-id="60b14-125">작업 자격 증명 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="60b14-125">The job credential resource id</span></span>

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

### <span data-ttu-id="60b14-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="60b14-126">-ServerName</span></span>
<span data-ttu-id="60b14-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="60b14-127">The server name</span></span>

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

### <span data-ttu-id="60b14-128">-확인</span><span class="sxs-lookup"><span data-stu-id="60b14-128">-Confirm</span></span>
<span data-ttu-id="60b14-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="60b14-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60b14-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60b14-130">-WhatIf</span></span>
<span data-ttu-id="60b14-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="60b14-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60b14-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60b14-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60b14-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b14-133">CommonParameters</span></span>
<span data-ttu-id="60b14-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="60b14-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b14-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60b14-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b14-136">입력</span><span class="sxs-lookup"><span data-stu-id="60b14-136">INPUTS</span></span>

### <span data-ttu-id="60b14-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="60b14-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="60b14-138">출력</span><span class="sxs-lookup"><span data-stu-id="60b14-138">OUTPUTS</span></span>

### <span data-ttu-id="60b14-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="60b14-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="60b14-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="60b14-140">NOTES</span></span>

## <span data-ttu-id="60b14-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60b14-141">RELATED LINKS</span></span>
