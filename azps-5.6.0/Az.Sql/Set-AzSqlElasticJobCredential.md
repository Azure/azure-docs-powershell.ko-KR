---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 9c0d7348a900690a49ebea96bc90c296c2d8e9a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986342"
---
# <span data-ttu-id="16165-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="16165-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="16165-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16165-102">SYNOPSIS</span></span>
<span data-ttu-id="16165-103">작업 자격 증명 업데이트</span><span class="sxs-lookup"><span data-stu-id="16165-103">Updates a job credential</span></span>

## <span data-ttu-id="16165-104">구문</span><span class="sxs-lookup"><span data-stu-id="16165-104">SYNTAX</span></span>

### <span data-ttu-id="16165-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="16165-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16165-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="16165-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16165-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="16165-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16165-108">설명</span><span class="sxs-lookup"><span data-stu-id="16165-108">DESCRIPTION</span></span>
<span data-ttu-id="16165-109">Set-AzSqlElasticJobCredential cmdlet이 작업 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="16165-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="16165-110">예제</span><span class="sxs-lookup"><span data-stu-id="16165-110">EXAMPLES</span></span>

### <span data-ttu-id="16165-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="16165-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="16165-112">작업 자격 증명 업데이트</span><span class="sxs-lookup"><span data-stu-id="16165-112">Updates a job credential</span></span>

## <span data-ttu-id="16165-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="16165-113">PARAMETERS</span></span>

### <span data-ttu-id="16165-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="16165-114">-AgentName</span></span>
<span data-ttu-id="16165-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="16165-115">The agent name</span></span>

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

### <span data-ttu-id="16165-116">-자격 증명</span><span class="sxs-lookup"><span data-stu-id="16165-116">-Credential</span></span>
<span data-ttu-id="16165-117">자격 증명</span><span class="sxs-lookup"><span data-stu-id="16165-117">The credential</span></span>

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

### <span data-ttu-id="16165-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16165-118">-DefaultProfile</span></span>
<span data-ttu-id="16165-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16165-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16165-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16165-120">-InputObject</span></span>
<span data-ttu-id="16165-121">작업 자격 증명 개체</span><span class="sxs-lookup"><span data-stu-id="16165-121">The job credential object</span></span>

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

### <span data-ttu-id="16165-122">-Name</span><span class="sxs-lookup"><span data-stu-id="16165-122">-Name</span></span>
<span data-ttu-id="16165-123">작업 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="16165-123">The job credential name</span></span>

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

### <span data-ttu-id="16165-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16165-124">-ResourceGroupName</span></span>
<span data-ttu-id="16165-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="16165-125">The resource group name</span></span>

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

### <span data-ttu-id="16165-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16165-126">-ResourceId</span></span>
<span data-ttu-id="16165-127">작업 자격 증명 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="16165-127">The job credential resource id</span></span>

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

### <span data-ttu-id="16165-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="16165-128">-ServerName</span></span>
<span data-ttu-id="16165-129">서버 이름</span><span class="sxs-lookup"><span data-stu-id="16165-129">The server name</span></span>

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

### <span data-ttu-id="16165-130">-확인</span><span class="sxs-lookup"><span data-stu-id="16165-130">-Confirm</span></span>
<span data-ttu-id="16165-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16165-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16165-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16165-132">-WhatIf</span></span>
<span data-ttu-id="16165-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="16165-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16165-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16165-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16165-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16165-135">CommonParameters</span></span>
<span data-ttu-id="16165-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16165-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16165-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16165-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16165-138">입력</span><span class="sxs-lookup"><span data-stu-id="16165-138">INPUTS</span></span>

### <span data-ttu-id="16165-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="16165-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="16165-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="16165-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="16165-141">출력</span><span class="sxs-lookup"><span data-stu-id="16165-141">OUTPUTS</span></span>

### <span data-ttu-id="16165-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="16165-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="16165-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16165-143">NOTES</span></span>

## <span data-ttu-id="16165-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16165-144">RELATED LINKS</span></span>
