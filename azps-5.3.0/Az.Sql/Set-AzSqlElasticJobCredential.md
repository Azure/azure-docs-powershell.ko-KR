---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 87ac0ddaa205c2b257a3aadf9ceea5a6ec302eab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492159"
---
# <span data-ttu-id="bd1fd-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="bd1fd-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="bd1fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="bd1fd-103">작업 자격 증명 업데이트</span><span class="sxs-lookup"><span data-stu-id="bd1fd-103">Updates a job credential</span></span>

## <span data-ttu-id="bd1fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd1fd-104">SYNTAX</span></span>

### <span data-ttu-id="bd1fd-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bd1fd-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd1fd-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="bd1fd-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd1fd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bd1fd-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd1fd-108">설명</span><span class="sxs-lookup"><span data-stu-id="bd1fd-108">DESCRIPTION</span></span>
<span data-ttu-id="bd1fd-109">Set-AzSqlElasticJobCredential cmdlet은 작업 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bd1fd-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="bd1fd-110">예제</span><span class="sxs-lookup"><span data-stu-id="bd1fd-110">EXAMPLES</span></span>

### <span data-ttu-id="bd1fd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bd1fd-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="bd1fd-112">작업 자격 증명 업데이트</span><span class="sxs-lookup"><span data-stu-id="bd1fd-112">Updates a job credential</span></span>

## <span data-ttu-id="bd1fd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd1fd-113">PARAMETERS</span></span>

### <span data-ttu-id="bd1fd-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="bd1fd-114">-AgentName</span></span>
<span data-ttu-id="bd1fd-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="bd1fd-115">The agent name</span></span>

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

### <span data-ttu-id="bd1fd-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="bd1fd-116">-Credential</span></span>
<span data-ttu-id="bd1fd-117">자격 증명</span><span class="sxs-lookup"><span data-stu-id="bd1fd-117">The credential</span></span>

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

### <span data-ttu-id="bd1fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd1fd-118">-DefaultProfile</span></span>
<span data-ttu-id="bd1fd-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd1fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd1fd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd1fd-120">-InputObject</span></span>
<span data-ttu-id="bd1fd-121">작업 자격 증명 개체</span><span class="sxs-lookup"><span data-stu-id="bd1fd-121">The job credential object</span></span>

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

### <span data-ttu-id="bd1fd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bd1fd-122">-Name</span></span>
<span data-ttu-id="bd1fd-123">작업 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="bd1fd-123">The job credential name</span></span>

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

### <span data-ttu-id="bd1fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd1fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="bd1fd-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bd1fd-125">The resource group name</span></span>

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

### <span data-ttu-id="bd1fd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd1fd-126">-ResourceId</span></span>
<span data-ttu-id="bd1fd-127">작업 자격 증명 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="bd1fd-127">The job credential resource id</span></span>

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

### <span data-ttu-id="bd1fd-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bd1fd-128">-ServerName</span></span>
<span data-ttu-id="bd1fd-129">서버 이름</span><span class="sxs-lookup"><span data-stu-id="bd1fd-129">The server name</span></span>

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

### <span data-ttu-id="bd1fd-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd1fd-130">-Confirm</span></span>
<span data-ttu-id="bd1fd-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd1fd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd1fd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd1fd-132">-WhatIf</span></span>
<span data-ttu-id="bd1fd-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bd1fd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd1fd-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd1fd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd1fd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd1fd-135">CommonParameters</span></span>
<span data-ttu-id="bd1fd-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd1fd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd1fd-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bd1fd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd1fd-138">입력</span><span class="sxs-lookup"><span data-stu-id="bd1fd-138">INPUTS</span></span>

### <span data-ttu-id="bd1fd-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="bd1fd-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="bd1fd-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="bd1fd-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="bd1fd-141">출력</span><span class="sxs-lookup"><span data-stu-id="bd1fd-141">OUTPUTS</span></span>

### <span data-ttu-id="bd1fd-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="bd1fd-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="bd1fd-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd1fd-143">NOTES</span></span>

## <span data-ttu-id="bd1fd-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd1fd-144">RELATED LINKS</span></span>
