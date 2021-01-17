---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353618"
---
# <span data-ttu-id="12bd4-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="12bd4-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="12bd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="12bd4-103">탄력적 작업 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="12bd4-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="12bd4-104">구문</span><span class="sxs-lookup"><span data-stu-id="12bd4-104">SYNTAX</span></span>

### <span data-ttu-id="12bd4-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="12bd4-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12bd4-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="12bd4-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12bd4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="12bd4-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12bd4-108">설명</span><span class="sxs-lookup"><span data-stu-id="12bd4-108">DESCRIPTION</span></span>
<span data-ttu-id="12bd4-109">Remove-AzSqlElasticJobCredential cmdlet은 작업 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="12bd4-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="12bd4-110">예제</span><span class="sxs-lookup"><span data-stu-id="12bd4-110">EXAMPLES</span></span>

### <span data-ttu-id="12bd4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="12bd4-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="12bd4-112">작업 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="12bd4-112">Removes a job credential</span></span>

## <span data-ttu-id="12bd4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12bd4-113">PARAMETERS</span></span>

### <span data-ttu-id="12bd4-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="12bd4-114">-AgentName</span></span>
<span data-ttu-id="12bd4-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="12bd4-115">The agent name</span></span>

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

### <span data-ttu-id="12bd4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12bd4-116">-DefaultProfile</span></span>
<span data-ttu-id="12bd4-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12bd4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12bd4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12bd4-118">-InputObject</span></span>
<span data-ttu-id="12bd4-119">작업 자격 증명 개체</span><span class="sxs-lookup"><span data-stu-id="12bd4-119">The job credential object</span></span>

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

### <span data-ttu-id="12bd4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="12bd4-120">-Name</span></span>
<span data-ttu-id="12bd4-121">작업 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="12bd4-121">The job credential name</span></span>

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

### <span data-ttu-id="12bd4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12bd4-122">-ResourceGroupName</span></span>
<span data-ttu-id="12bd4-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="12bd4-123">The resource group name</span></span>

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

### <span data-ttu-id="12bd4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12bd4-124">-ResourceId</span></span>
<span data-ttu-id="12bd4-125">작업 자격 증명 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="12bd4-125">The job credential resource id</span></span>

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

### <span data-ttu-id="12bd4-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="12bd4-126">-ServerName</span></span>
<span data-ttu-id="12bd4-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="12bd4-127">The server name</span></span>

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

### <span data-ttu-id="12bd4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12bd4-128">-Confirm</span></span>
<span data-ttu-id="12bd4-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="12bd4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12bd4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12bd4-130">-WhatIf</span></span>
<span data-ttu-id="12bd4-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="12bd4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12bd4-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12bd4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12bd4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12bd4-133">CommonParameters</span></span>
<span data-ttu-id="12bd4-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="12bd4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12bd4-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="12bd4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12bd4-136">입력</span><span class="sxs-lookup"><span data-stu-id="12bd4-136">INPUTS</span></span>

### <span data-ttu-id="12bd4-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="12bd4-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="12bd4-138">출력</span><span class="sxs-lookup"><span data-stu-id="12bd4-138">OUTPUTS</span></span>

### <span data-ttu-id="12bd4-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="12bd4-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="12bd4-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="12bd4-140">NOTES</span></span>

## <span data-ttu-id="12bd4-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12bd4-141">RELATED LINKS</span></span>
